# Post 5 — What is Graph RAG?

**Visual asset:** `post-5-preview.png` (source: `post-5-graphic.html`)

---

## PT

O que é Graph RAG? Diferente do RAG tradicional, quase ninguém fala sobre isso ainda — porque a maioria dos projetos "de grafo" na prática ainda é RAG com um verniz de grafo por cima.

Graph RAG = Graph Retrieval-Augmented Generation. A resposta do LLM é ancorada em um grafo de conhecimento estruturado — entidades e relações reais — em vez de texto recuperado solto. Letra por letra:

G — Graph (Grafo)
Um grafo estruturado de entidades e relações reais — equipamentos, componentes, sintomas, causas e ações — extraído dos manuais. Não é uma pilha de trechos de texto, é conhecimento organizado.

R — Retrieval (Recuperação)
Em vez de buscar texto parecido, um algoritmo determinístico (não o LLM!) percorre as arestas reais do grafo — a recuperação é uma travessia, não uma busca por similaridade.

A — Augmented (Aumentada)
O prompt do modelo é enriquecido com o caminho exato encontrado nesse grafo — a cadeia específica de arestas que conecta o sintoma relatado a uma causa e uma solução.

G — Generation (Geração)
O modelo escreve a resposta usando somente esse caminho, citando a cadeia exata de relações percorrida e o manual de origem.

A analogia que uso: um chat de IA comum é um técnico trabalhando de memória — confiante, mas às vezes errado. Um Graph RAG funciona como alguém seguindo o diagrama elétrico real da planta: antes de responder, traça o caminho real de sintoma até causa e ação corretiva.

Toda resposta é um percurso por essa cadeia — Equipamento → Componente → Sintoma → Causa → Ação — nunca um atalho por cima dela.

#GraphRAG #KnowledgeGraph #IA #LLM #GenerativeAI #EngenhariaDeIA

---

## EN

What is Graph RAG? Unlike traditional RAG, almost nobody talks about this yet — because most "graph" projects in practice are still RAG with a graph-shaped coat of paint.

Graph RAG = Graph Retrieval-Augmented Generation. The LLM's answer is grounded in a structured knowledge graph — real entities and relationships — instead of loose retrieved text. Letter by letter:

G — Graph
A structured graph of real entities and relationships — equipment, components, symptoms, causes and actions — extracted from the manuals. Not a pile of text passages, actual organized knowledge.

R — Retrieval
Instead of searching for similar-sounding text, a deterministic algorithm (not the LLM!) walks the graph's real edges — retrieval is a traversal, not a similarity search.

A — Augmented
The model's prompt is enriched with the exact path found in that graph — the specific chain of edges connecting the reported symptom to a cause and a fix.

G — Generation
The model writes the answer using only that path, citing the exact chain of relationships followed and the manual it came from.

The analogy I use: a regular AI chat is a technician working from memory — confident, but occasionally wrong. A Graph RAG works like someone following the plant's actual wiring diagram: before answering, it traces the real path from symptom to cause to corrective action.

Every answer is a walk along that chain — Equipment → Component → Symptom → Cause → Action — never a shortcut across it.

#GraphRAG #KnowledgeGraph #AI #LLM #GenerativeAI #AIEngineering
