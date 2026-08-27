# Post 3 — How RAG works (the pipeline)

**Visual asset:** `post-3-preview.png` (source: `post-3-graphic.html`)

---

## PT

Por trás de qualquer RAG "de verdade" tem uma pipeline de 3 etapas que a maioria dos frameworks esconde debaixo do capô. Construí a minha do zero em Python puro para entender cada uma:

1️⃣ Indexação
O documento é dividido em pedaços pequenos ("chunks"), cortando por seção e depois por parágrafo — nunca no meio de uma tabela, ou você separa rótulo do valor. Cada pedaço vira um vetor de números (embedding) que representa seu significado.

2️⃣ Retrieval
A pergunta também vira um vetor. O sistema busca, por similaridade de cosseno, os pedaços cujo significado está mais próximo da pergunta. Sem FAISS, sem Chroma — numa escala pequena, uma multiplicação de matriz em NumPy puro já resolve.

3️⃣ Generation
Os pedaços recuperados vão para o LLM com regras rígidas: responder só com esse contexto, nunca estimar um número que não está escrito ali, e citar a fonte (documento, página, seção).

O detalhe que faz a diferença: se nenhum pedaço passar do limiar mínimo de similaridade, o sistema conclui que a resposta não está no documento. Um "não sei" honesto vale mais que um número inventado.

#RAG #Python #EngenhariaDeIA #LLM #NLP

---

## EN

Behind any "real" RAG system there's a 3-step pipeline most frameworks hide under the hood. I built mine from scratch in plain Python to understand each one:

1️⃣ Indexing
The document is split into small pieces ("chunks"), cutting by section first, then by paragraph — never mid-table, or you separate a label from its value. Each chunk becomes a vector of numbers (an embedding) capturing its meaning.

2️⃣ Retrieval
The question also becomes a vector. The system finds, via cosine similarity, the chunks whose meaning is closest to the question. No FAISS, no Chroma — at a small scale, one matrix multiplication in plain NumPy is instant.

3️⃣ Generation
The retrieved chunks go to the LLM under strict rules: answer only from that context, never estimate a number that isn't literally written there, and cite the source (document, page, section).

The detail that matters most: if no chunk passes the minimum similarity threshold, the system concludes the answer isn't in the document. An honest "I don't know" beats an invented number.

#RAG #Python #AIEngineering #LLM #NLP
