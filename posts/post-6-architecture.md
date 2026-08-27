# Post 6 — Architecture: how the project actually works (Graph RAG Agent Mining)

**Visual asset:** `post-6-preview.png` (source: `post-6-graphic.html`)

---

## PT

Por dentro do Graph RAG Agent Mining: 7 módulos Python pequenos e legíveis, sem nenhum framework de graph-RAG pronto no meio do caminho. Assim funciona, do manual de manutenção à resposta ancorada:

1️⃣ Manuais de origem (`data/raw/`) — 4 manuais de manutenção sintéticos, um por tipo de ativo de mineração.

2️⃣ Extração (`src/extraction.py`) — um LLM lê cada manual e extrai triplas estruturadas, usando só 4 relações permitidas. O que não se encaixa no esquema é descartado.

3️⃣ Construção do grafo (`src/graph_builder.py`) — as triplas viram um único grafo direcionado (NetworkX). A mesma entidade citada em manuais diferentes vira um nó compartilhado.

4️⃣ Identificação da entidade + checagem de especificidade (`src/graph_query.py`) — um LLM mapeia a pergunta para um nó real; uma checagem determinística pede mais detalhe se a pergunta for ambígua.

5️⃣ Travessia determinística (`src/graph_query.py`) — um algoritmo simples, não o LLM, percorre até 3 saltos seguindo a cadeia causal real.

6️⃣ Resposta ancorada (`src/answer_builder.py`) — o LLM escreve a resposta só a partir do caminho percorrido, citando a cadeia exata e o manual de origem.

7️⃣ Interface (`app.py`, Streamlit) — chat com conversas separadas e uma animação ao vivo rastreando os nós do grafo enquanto a resposta é preparada.

Código aberto, dados sintéticos, zero frameworks de graph-RAG prontos. Link nos comentários.

#GraphRAG #Python #EngenhariaDeIA #KnowledgeGraph #LLM #Portfolio

---

## EN

Inside Graph RAG Agent Mining: 7 small, readable Python modules, with no pre-built graph-RAG framework anywhere in between. Here's how it works, from maintenance manual to grounded answer:

1️⃣ Source manuals (`data/raw/`) — 4 synthetic maintenance manuals, one per mining asset type.

2️⃣ Extraction (`src/extraction.py`) — an LLM reads each manual and extracts structured triples, using only 4 allowed relations. Anything that doesn't fit the schema is discarded.

3️⃣ Graph construction (`src/graph_builder.py`) — the triples become one directed graph (NetworkX). The same entity mentioned in different manuals becomes a shared node.

4️⃣ Entity linking & specificity check (`src/graph_query.py`) — an LLM maps the question to a real node; a deterministic check asks for more detail if the question is ambiguous.

5️⃣ Deterministic traversal (`src/graph_query.py`) — a plain algorithm, not the LLM, walks up to 3 hops following the real causal chain.

6️⃣ Grounded answer (`src/answer_builder.py`) — the LLM writes the answer only from the traced path, citing the exact chain and the source manual.

7️⃣ Interface (`app.py`, Streamlit) — chat with separate conversations and a live animation tracing the graph nodes while the answer is prepared.

Open source, synthetic data, zero pre-built graph-RAG frameworks. Link in the comments.

#GraphRAG #Python #AIEngineering #KnowledgeGraph #LLM #Portfolio
