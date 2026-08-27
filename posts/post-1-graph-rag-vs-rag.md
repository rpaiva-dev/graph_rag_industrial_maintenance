# Post 1 — Graph RAG vs RAG

**Visual assets:** `post-1-preview.png` (static image) · `post-1-graph-rag-vs-rag-animation.html` (open in a browser and screen-record ~8-10s for a native LinkedIn video/GIF — LinkedIn doesn't support embedded HTML).

---

## PT

A maioria dos sistemas de IA que "conversam com seus documentos" hoje é RAG.

Eu construí os dois — RAG e Graph RAG — do zero (sem LangChain, sem framework de grafo), e a diferença entre eles não é sutil.

🔶 RAG (Retrieval-Augmented Generation)
Divide os documentos em pedaços, busca os mais parecidos com a pergunta, e o LLM responde com base neles. Ótimo para perguntas abertas sobre documentos — contratos, relatórios, manuais.

🔷 Graph RAG (Graph Retrieval-Augmented Generation)
Em vez de texto, um LLM extrai um grafo de conhecimento real — entidades e relações. A pergunta é mapeada para um nó, e um algoritmo determinístico (não o LLM!) percorre o caminho causal real. O LLM só escreve a resposta a partir desse caminho.

A diferença na prática:
→ RAG advinha como os fatos se conectam.
→ Graph RAG prova o caminho — ou pede mais detalhes quando a pergunta é ambígua.

Construí um Graph RAG aplicado a diagnóstico de manutenção com dados sintéticos: você descreve o sintoma, o agente percorre o grafo e responde com a causa provável e a ação corretiva, citando o caminho exato.

Código aberto, sem frameworks de graph-RAG prontos. Link nos comentários. 👇

#IA #RAG #KnowledgeGraph #LLM #GenerativeAI #MachineLearning #Portfolio

---

## EN

Most "chat with your documents" AI systems today are RAG.

I built both — RAG and Graph RAG — from scratch (no LangChain, no graph framework), and the difference between them isn't subtle.

🔶 RAG (Retrieval-Augmented Generation)
Splits documents into chunks, retrieves the ones closest to the question, and the LLM answers from them. Great for open-ended questions over documents — contracts, reports, manuals.

🔷 Graph RAG (Graph Retrieval-Augmented Generation)
Instead of text, an LLM extracts a real knowledge graph — entities and relationships. The question is mapped to a node, and a deterministic algorithm (not the LLM!) walks the real causal path. The LLM only writes the answer from that path.

The difference in practice:
→ RAG guesses how facts connect.
→ Graph RAG proves the path — or asks for more detail when the question is ambiguous.

I built a Graph RAG for mining-asset maintenance diagnostics all synthetic data: describe the symptom, the agent walks the graph, and answers with the probable cause and corrective action, citing the exact path.

Open source, zero pre-built graph-RAG frameworks. Link in the comments. 👇

#AI #RAG #KnowledgeGraph #LLM #GenerativeAI #MachineLearning #Portfolio
