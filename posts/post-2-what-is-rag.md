# Post 2 — What is RAG? (definition)

**Visual asset:** `post-2-preview.png` (source: `post-2-graphic.html`)

---

## PT

O que é RAG, de verdade? Não é mágica — é uma técnica de 3 letras que resolve um problema bem específico: LLMs não sabem o que está nos SEUS documentos.

R — Retrieval (Recuperação)
Antes de responder qualquer coisa, o sistema busca nos seus documentos os trechos mais relacionados à pergunta. Como um bibliotecário puxando as páginas certas da estante.

A — Augmented (Aumentada)
O prompt do LLM é enriquecido com esses trechos recuperados. Em vez de depender só da memória do treinamento, o modelo recebe o material relevante junto com a pergunta.

G — Generation (Geração)
O modelo escreve a resposta usando SOMENTE o que recebeu, citando a fonte.

A analogia que mais uso: um chat de IA comum é um aluno fazendo prova de memória — quando não sabe, chuta com convicção. RAG transforma isso em prova com consulta: antes de responder, busca as páginas certas e ordena "responda só com isso, e diga de onde tirou".

Nos próximos posts vou destrinchar como essa pipeline funciona por dentro (sem framework, só Python puro) e por que isso importa na prática.

#RAG #IA #LLM #EngenhariaDeIA #GenerativeAI

---

## EN

What is RAG, really? It's not magic — it's a 3-letter technique that solves one specific problem: LLMs don't know what's inside YOUR documents.

R — Retrieval
Before answering anything, the system searches your documents for the passages most related to the question. Like a librarian pulling the right pages off the shelf.

A — Augmented
The LLM's prompt is enriched with those retrieved passages. Instead of relying only on training memory, the model gets the relevant material attached to the question.

G — Generation
The model writes the answer using ONLY what it received, citing the source.

The analogy I use most: a regular AI chat is a student taking a closed-book exam — when it doesn't know, it guesses confidently. RAG turns it into an open-book exam: before answering, it fetches the right pages and says "answer using only this, and cite where it came from."

Next posts will break down how this pipeline actually works under the hood (no framework, plain Python) and why it matters in practice.

#RAG #AI #LLM #AIEngineering #GenerativeAI
