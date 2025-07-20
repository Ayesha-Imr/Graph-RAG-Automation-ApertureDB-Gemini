# Automating Knowledge Graph Creation & Enabling Efficient Graph RAG with ApertureDB and Gemini

This repo contains notebooks, in parts, showing how to automatically create knowledge graphs from your data and perform graph RAG. 

## Part 1: Automating Knowledge Graph Creation with ApertureDB and Gemini
### Part 1.1:
Use an LLM (Gemini 2.5 in this case) to intelligently extract entities from your data source, and ingest them into ApertureDB.
- [Blog Post](https://www.aperturedata.io/resources/automating-knowledge-graph-creation-with-gemini-and-aperturedb-p1)

### Part 1.2:
Use an LLM (Gemini 2.5 in this case) to intelligently extract relationships between entities and ingest them into ApertureDB, creating a complete knowledge graph.
- [Blog Post](https://www.aperturedata.io/resources/automating-knowledge-graph-creation-with-gemini-and-aperturedb-p2)

### Notebook (contains parts 1.1 and 1.2 both):
- [Cloud Version](Notebooks/ApertureDB_Knowledge_Graph_with_Gemini.ipynb)
- [Local (udocker version)](Notebooks/LOCAL_ApertureDB_Knowledge_Graph_with_Gemini.ipynb)

## Part 2: Graph RAG with ApertureDB and Gemini
### Part 2.1: Building the Semantic Layer
Creating Descriptors (embeddings) of knowledge graph entities using Gemini embeddngs, ingesting them into a DescriptorSet (vector index), and connecting them with the knowledge graph in ApertureDB.
#### Notebook:
- [Cloud Version](Notebooks/GraphRAG_with_ApertureDB_Part_1.ipynb)
- [Local (udocker version)](Notebooks/LOCAL_GraphRAG_with_ApertureDB_Part_1.ipynb)

### Part 2.2: Implementing and Evaluating Graph RAG
Implement graph RAG using our knowledge graph and compare it with vanilla RAG, using numerical + LLM-as-a-Judge evals through Gemini.
#### Notebook:
- [Cloud Version](Notebooks/GraphRAG_with_ApertureDB_Part_2.ipynb)
- [Local (udocker version)](Notebooks/LOCAL_GraphRAG_with_ApertureDB_Part_2.ipynb)

