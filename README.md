# Automating Knowledge Graph Creation & Enabling Efficient Graph RAG with ApertureDB and Gemini

This repo contains notebooks, in parts, showing how to automatically create knowledge graphs from your data and perform graph RAG. 

- The Cloud version notebooks involve signing up to [ApertureDB](https://www.aperturedata.io/) Cloud and creating a managed DB instance there to which you can remotely connect.
- The local version notebooks involve using [udocker](https://indigo-dc.github.io/udocker/) (a library which allows running Docker images in constrained environments like Colab notebooks) to create DB instances locally which you can persist in Google Drive if you want - mitigating the need to sign up to ApertureD Cloud.

Besides the initial DB setup and connection, the notebooks - and thereby the core functionality - are exactly the same.

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
- [Blog Post](https://www.aperturedata.io/resources/automating-knowledge-graph-creation-with-gemini-and-aperturedb-p3)

### Part 2.2: Implementing and Evaluating Graph RAG
Implement graph RAG using our knowledge graph and compare it with vanilla RAG, using numerical + LLM-as-a-Judge evals through Gemini.
#### Notebook:
- [Cloud Version](Notebooks/GraphRAG_with_ApertureDB_Part_2.ipynb)
- [Local (udocker version)](Notebooks/LOCAL_GraphRAG_with_ApertureDB_Part_2.ipynb)
- [Blog Post](https://www.aperturedata.io/resources/automating-knowledge-graph-creation-with-gemini-and-aperturedb-p4)


## Sample Data
In case you don't have any sample PDF lying around, or do not want to use your own, you can use one the sample data PDFs from the repo to test out the notebooks.
- [Cloud Computing Lecture Notes](https://github.com/Ayesha-Imr/Graph-RAG-Automation-ApertureDB-Gemini/blob/main/Sample%20Data/Cloud%20Computing%20Copy%20Lecture%20Notes.pdf): My Cloud Computing course lecture notes PDF consisting of 42 pages - this is the data I have used to create these notebooks.
- [Attention is All You Need Research Paper](https://github.com/Ayesha-Imr/Graph-RAG-Automation-ApertureDB-Gemini/blob/main/Sample%20Data/Attention%20Is%20All%20You%20Need.pdf): A legendary research paper.
- [Harry Potter Book 1 Chapter 1](https://github.com/Ayesha-Imr/Graph-RAG-Automation-ApertureDB-Gemini/blob/main/Sample%20Data/Harry-Potter-1-Chapter-1.pdf): Chapter 1 PDF of my favourite book series' first book - Harry Potter & The Philosopher's Stone.


