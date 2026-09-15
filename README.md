# RAG & Retrieval Tools: Vector Databases, Search, Rerankers & Evaluation

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md) [![License: CC0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](LICENSE) [![Machine-readable catalog](https://img.shields.io/badge/data-tools.json%20%2F%20tools.csv-blue.svg)](data/) [![Reviewed monthly](https://img.shields.io/badge/reviewed-monthly-6f42c1.svg)](MAINTENANCE.md)

> **The Comprehensive List of RAG and Retrieval Tools** — a curated, source-linked directory of open-source and commercial software for retrieval-augmented generation, semantic search, vector storage, reranking, ingestion, and RAG evaluation.

**RAG and retrieval tools** are frameworks, databases, models, APIs, data pipelines, and evaluation systems used to find relevant evidence and supply it to an AI application. A typical retrieval-augmented generation (RAG) stack parses and chunks source data, represents it with lexical or vector indexes, retrieves and reranks candidates, generates a grounded answer, and evaluates the result. This directory covers each layer separately so that a RAG framework is not confused with a vector database, an embedding model with a reranker, or an evaluation toolkit with an observability platform.

**Last reviewed:** 2026-07-16 · **16 categories** · **209 entries** · **Reviewed monthly** · Machine-readable index: [`data/tools.json`](data/tools.json) / [`data/tools.csv`](data/tools.csv)

Every entry links to a primary source: the project's repository, official documentation or website, model card, dataset, or paper. Descriptions are factual summaries rather than endorsements. See [Methodology](#methodology) for scope, inclusion, ordering, verification, and counting rules.

**Legend:** 🟢 Open source · 🟠 Open weights (downloadable model, non-OSI or model-specific license) · 🔵 Open core (open-source component + commercial offering) · 🔒 Commercial / closed source

---

## Find Tools by Retrieval Goal

| I want to… | Go to |
| --- | --- |
| Build an end-to-end RAG application | [RAG Frameworks and Orchestration](#rag-frameworks-and-orchestration) |
| Store and search embedding vectors | [Vector Databases and Vector Search Libraries](#vector-databases-and-vector-search-libraries) |
| Add BM25, full-text, or hybrid retrieval | [Lexical and Hybrid Search Engines](#lexical-and-hybrid-search-engines) |
| Use a hosted retrieval or knowledge-base service | [Managed Retrieval APIs and Knowledge Bases](#managed-retrieval-apis-and-knowledge-bases) |
| Choose or serve an embedding model | [Embedding Models, APIs, and Libraries](#embedding-models-apis-and-libraries) |
| Rerank retrieved candidates | [Rerankers and Late-Interaction Retrieval](#rerankers-and-late-interaction-retrieval) |
| Parse PDFs, OCR scans, or split documents | [Document Parsing, OCR, and Chunking](#document-parsing-ocr-and-chunking) |
| Crawl websites and extract clean text | [Web Crawling and Content Extraction](#web-crawling-and-content-extraction) |
| Move source data into a retrieval index | [Ingestion, ETL, and Connectors](#ingestion-etl-and-connectors) |
| Retrieve over entities and relationships | [Graph RAG and Knowledge-Graph Retrieval](#graph-rag-and-knowledge-graph-retrieval) |
| Search images, pages, or video | [Multimodal RAG and Retrieval](#multimodal-rag-and-retrieval) |
| Improve queries or retrieval strategy | [Query Optimization and Retrieval Algorithms](#query-optimization-and-retrieval-algorithms) |
| Measure RAG quality | [RAG Evaluation Frameworks and Platforms](#rag-evaluation-frameworks-and-platforms) |
| Compare retrievers or RAG systems | [Retrieval and RAG Benchmarks](#retrieval-and-rag-benchmarks) |
| Trace, secure, or govern a production RAG system | [Observability, Security, and Governance](#observability-security-and-governance) |

## RAG Stack Taxonomy

| Layer | What it does | Typical outputs | Catalog section |
| --- | --- | --- | --- |
| Orchestration | Connects loaders, retrievers, models, tools, and application control flow | RAG pipelines and applications | [Frameworks](#rag-frameworks-and-orchestration) |
| Parsing and chunking | Converts source files into structured, retrievable units | Text, Markdown, layout elements, chunks | [Document parsing](#document-parsing-ocr-and-chunking) |
| Crawling and extraction | Acquires and cleans content from websites and APIs | Pages, records, metadata | [Web crawling](#web-crawling-and-content-extraction) |
| Ingestion and ETL | Synchronizes source systems with indexes | Incremental document and embedding pipelines | [Ingestion](#ingestion-etl-and-connectors) |
| Representation | Encodes content and queries as dense or sparse vectors | Embeddings | [Embedding models](#embedding-models-apis-and-libraries) |
| Vector retrieval | Performs approximate or exact nearest-neighbor search | Ranked vector candidates | [Vector databases](#vector-databases-and-vector-search-libraries) |
| Lexical and hybrid retrieval | Matches terms and combines sparse and dense signals | BM25, full-text, or fused candidates | [Search engines](#lexical-and-hybrid-search-engines) |
| Managed retrieval | Provides hosted indexing, retrieval, and knowledge-base operations | Retrieval APIs and managed indexes | [Managed services](#managed-retrieval-apis-and-knowledge-bases) |
| Reranking | Rescores a small candidate set with a stronger relevance model | A reordered top-k list | [Rerankers](#rerankers-and-late-interaction-retrieval) |
| Graph retrieval | Traverses entities, communities, and relationships | Subgraphs and graph-grounded context | [Graph RAG](#graph-rag-and-knowledge-graph-retrieval) |
| Multimodal retrieval | Searches visual, document-image, audio, or video representations | Multimodal evidence | [Multimodal RAG](#multimodal-rag-and-retrieval) |
| Query optimization | Rewrites, decomposes, routes, or expands an information need | Improved retrieval queries and plans | [Retrieval algorithms](#query-optimization-and-retrieval-algorithms) |
| Evaluation | Measures retrieval, grounding, answer quality, and regressions | Metrics, test results, and reports | [RAG evaluation](#rag-evaluation-frameworks-and-platforms) |
| Benchmarking | Supplies fixed datasets and scoring protocols | Comparable retrieval or RAG scores | [Benchmarks](#retrieval-and-rag-benchmarks) |
| Operations and safety | Traces live systems and enforces data and output policies | Traces, alerts, controls, and audit records | [Observability and security](#observability-security-and-governance) |

## Contents

- [RAG Frameworks and Orchestration](#rag-frameworks-and-orchestration)
- [Vector Databases and Vector Search Libraries](#vector-databases-and-vector-search-libraries)
- [Lexical and Hybrid Search Engines](#lexical-and-hybrid-search-engines)
- [Managed Retrieval APIs and Knowledge Bases](#managed-retrieval-apis-and-knowledge-bases)
- [Embedding Models, APIs, and Libraries](#embedding-models-apis-and-libraries)
- [Rerankers and Late-Interaction Retrieval](#rerankers-and-late-interaction-retrieval)
- [Document Parsing, OCR, and Chunking](#document-parsing-ocr-and-chunking)
- [Web Crawling and Content Extraction](#web-crawling-and-content-extraction)
- [Ingestion, ETL, and Connectors](#ingestion-etl-and-connectors)
- [Graph RAG and Knowledge-Graph Retrieval](#graph-rag-and-knowledge-graph-retrieval)
- [Multimodal RAG and Retrieval](#multimodal-rag-and-retrieval)
- [Query Optimization and Retrieval Algorithms](#query-optimization-and-retrieval-algorithms)
- [RAG Evaluation Frameworks and Platforms](#rag-evaluation-frameworks-and-platforms)
- [Retrieval and RAG Benchmarks](#retrieval-and-rag-benchmarks)
- [Observability, Security, and Governance](#observability-security-and-governance)
- [Discontinued and Historical Tools](#discontinued-and-historical-tools)
- [Key Papers and Concepts](#key-papers-and-concepts)
- [Glossary](#glossary)
- [Frequently Asked Questions](#frequently-asked-questions)
- [Methodology](#methodology)
- [Related Lists and Resources](#related-lists-and-resources)
- [Citing This List](#citing-this-list)
- [Contributing](#contributing)
- [License](#license)

---

## RAG Frameworks and Orchestration

**RAG frameworks** orchestrate application logic across document loading, chunking, indexing, retrieval, prompt construction, generation, and tool use. They usually connect to a separate search engine or vector database rather than replacing one.

| Tool | Availability | Description |
| --- | --- | --- |
| [LangChain](https://github.com/langchain-ai/langchain) | 🟢 Open source | LangChain is an application framework with retriever abstractions, document loaders, vector-store integrations, retrieval chains, and middleware for building RAG and agent workflows in Python and JavaScript. |
| [LlamaIndex](https://github.com/run-llama/llama_index) | 🟢 Open source | LlamaIndex is a data framework for context-augmented applications with indexes, retrievers, query engines, data connectors, agents, and managed services available through LlamaCloud. |
| [Haystack](https://github.com/deepset-ai/haystack) | 🟢 Open source | Haystack is deepset's component-based framework for production search and RAG pipelines, with typed components for conversion, preprocessing, embedding, retrieval, ranking, routing, and generation. |
| [DSPy](https://github.com/stanfordnlp/dspy) | 🟢 Open source | DSPy is a framework for programming and optimizing language-model systems whose retrieval modules and optimizers can tune multi-stage RAG pipelines against an objective. |
| [txtai](https://github.com/neuml/txtai) | 🟢 Open source | txtai is an all-in-one embeddings database and semantic-workflow framework that combines vector search, SQL, graph traversal, topic modeling, extractive QA, and RAG pipelines. |
| [R2R](https://github.com/SciPhi-AI/R2R) | 🔵 Open core | R2R is an open-source retrieval system and API for multimodal ingestion, hybrid search, knowledge graphs, agents, and RAG, paired with hosted and enterprise offerings. |
| [RAGFlow](https://github.com/infiniflow/ragflow) | 🔵 Open core | RAGFlow is an open-source RAG engine with document understanding, template-based chunking, hybrid retrieval, agent workflows, and a commercial cloud service. |
| [Pathway](https://github.com/pathwaycom/pathway) | 🔵 Open core | Pathway is a Python data-processing framework for live, incremental pipelines that supports continuously updated RAG indexes, document parsing, vector search, and streaming connectors. |
| [LangGraph](https://github.com/langchain-ai/langgraph) | 🟢 Open source | LangGraph is a low-level orchestration framework for stateful agents whose graphs can implement iterative retrieval, query routing, corrective RAG, and human review. |
| [Semantic Kernel](https://github.com/microsoft/semantic-kernel) | 🟢 Open source | Semantic Kernel is Microsoft's SDK for composing models, plugins, memory, vector stores, and process orchestration in C#, Python, and Java applications. |
| [Spring AI](https://github.com/spring-projects/spring-ai) | 🟢 Open source | Spring AI is a Spring-ecosystem application framework with portable model, embedding, vector-store, document-reader, text-splitter, advisor, and retrieval-augmentation APIs. |
| [Langroid](https://github.com/langroid/langroid) | 🟢 Open source | Langroid is a multi-agent LLM framework whose document-chat agents provide parsing, chunking, vector storage, relevance extraction, citations, and conversational RAG. |
| [Quivr](https://github.com/QuivrHQ/quivr) | 🟢 Open source | Quivr is an opinionated RAG framework for integrating ingestion, retrieval, generation, and configurable workflows into applications through Python and API interfaces. |
| [RAGLite](https://github.com/superlinear-ai/raglite) | 🟢 Open source | RAGLite is a compact Python toolkit for PostgreSQL-based RAG with document ingestion, hybrid retrieval, reranking, prompt assembly, and evaluation-oriented metadata. |
| [FlashRAG](https://github.com/RUC-NLPIR/FlashRAG) | 🟢 Open source | FlashRAG is a research toolkit that implements multiple RAG methods, datasets, retrieval backends, generators, and evaluation workflows behind a common Python interface. |
| [Embedchain](https://github.com/embedchain/embedchain) | 🟢 Open source | Embedchain is an open-source RAG framework that loads, chunks, embeds, indexes, and synchronizes unstructured data for question answering and personalized AI applications. |

## Vector Databases and Vector Search Libraries

**Vector databases** persist embeddings and execute similarity search, usually with metadata filtering and approximate-nearest-neighbor (ANN) indexes. This section also includes vector extensions and in-process ANN libraries; managed knowledge-base products are listed separately.

| Tool | Availability | Description |
| --- | --- | --- |
| [Pinecone](https://www.pinecone.io) | 🔒 Commercial | Pinecone is a managed vector database with dense and sparse indexes, metadata filtering, namespaces, hybrid retrieval, integrated inference, and serverless deployment options. |
| [Weaviate](https://github.com/weaviate/weaviate) | 🔵 Open core | Weaviate is an open-source vector database with managed cloud offerings, supporting vector, keyword, and hybrid search, filters, multi-tenancy, replication, and pluggable vectorizers. |
| [Qdrant](https://github.com/qdrant/qdrant) | 🔵 Open core | Qdrant is an open-source vector search engine with payload filtering, dense and sparse vectors, hybrid queries, quantization, distributed deployment, and a managed cloud. |
| [Milvus](https://github.com/milvus-io/milvus) | 🟢 Open source | Milvus is a distributed open-source vector database with multiple ANN index types, scalar filtering, hybrid search, GPU support, and horizontal scaling. |
| [Zilliz Cloud](https://zilliz.com/cloud) | 🔒 Commercial | Zilliz Cloud is the managed Milvus service, adding serverless and dedicated clusters, operational automation, backup, security controls, and integrated data and model services. |
| [Chroma](https://github.com/chroma-core/chroma) | 🔵 Open core | Chroma is an open-source AI data store with collection, embedding, filtering, and vector-query APIs, plus a managed Chroma Cloud service. |
| [pgvector](https://github.com/pgvector/pgvector) | 🟢 Open source | pgvector is a PostgreSQL extension that adds exact and approximate vector similarity search, HNSW and IVFFlat indexes, multiple distance functions, and SQL-native filtering. |
| [LanceDB](https://github.com/lancedb/lancedb) | 🔵 Open core | LanceDB is an open-source, embedded multimodal database built on the Lance columnar format, with vector, full-text, and hybrid search plus a managed cloud. |
| [FAISS](https://github.com/facebookresearch/faiss) | 🟢 Open source | FAISS is Meta's library for efficient similarity search and clustering of dense vectors, offering CPU and GPU implementations and a broad family of exact and ANN indexes. |
| [Vespa](https://github.com/vespa-engine/vespa) | 🟢 Open source | Vespa is an open-source serving engine that combines structured filtering, lexical matching, nearest-neighbor search, configurable ranking expressions, and distributed document storage. |
| [Elasticsearch](https://github.com/elastic/elasticsearch) | 🔵 Open core | Elasticsearch is a distributed search and analytics engine with full-text, dense-vector, sparse-vector, hybrid retrieval, filtering, and learned-reranking capabilities. |
| [OpenSearch](https://github.com/opensearch-project/OpenSearch) | 🟢 Open source | OpenSearch is an Apache-2.0 search and analytics suite with k-NN vector indexes, neural and hybrid search pipelines, full-text retrieval, filters, and plugins. |
| [Redis Vector Search](https://redis.io/docs/latest/develop/ai/search-and-query/vectors/) | 🔵 Open core | Redis Vector Search is Redis's query capability for HNSW or flat vector indexes combined with metadata, numeric, geospatial, and full-text filters. |
| [MongoDB Atlas Vector Search](https://www.mongodb.com/products/platform/atlas-vector-search) | 🔒 Commercial | MongoDB Atlas Vector Search is a managed capability for ANN and exact vector search over Atlas documents, with prefilters and hybrid search through aggregation pipelines. |
| [Supabase Vector](https://supabase.com/docs/guides/ai) | 🔵 Open core | Supabase Vector is Supabase's PostgreSQL-based toolkit for storing embeddings with pgvector, generating them through Edge Functions, and combining retrieval with relational data and authorization. |
| [sqlite-vec](https://github.com/asg017/sqlite-vec) | 🟢 Open source | sqlite-vec is a compact SQLite extension for storing and querying float, int8, and binary vectors without a separate database server. |
| [USearch](https://github.com/unum-cloud/usearch) | 🟢 Open source | USearch is a single-file vector-search library with HNSW indexes, multiple scalar and binary types, user-defined metrics, persistence, and bindings for several languages. |
| [Annoy](https://github.com/spotify/annoy) | 🟢 Open source | Annoy is Spotify's read-optimized approximate-nearest-neighbor library using memory-mapped forests of random-projection trees for static vector collections. |
| [ScaNN](https://github.com/google-research/google-research/tree/master/scann) | 🟢 Open source | ScaNN is Google's vector-similarity search library using quantization, partitioning, and score-aware algorithms for efficient maximum inner-product and nearest-neighbor search. |
| [hnswlib](https://github.com/nmslib/hnswlib) | 🟢 Open source | hnswlib is a lightweight C++ and Python implementation of Hierarchical Navigable Small World graphs for approximate nearest-neighbor search with incremental updates. |
| [Marqo](https://github.com/marqo-ai/marqo) | 🔵 Open core | Marqo is an open-source tensor-search engine for text and images with embedding inference, lexical-vector hybrid search, filtering, reranking, and a managed cloud. |
| [TiDB Vector Search](https://docs.pingcap.com/tidbcloud/vector-search-overview/) | 🔵 Open core | TiDB Vector Search adds vector columns, distance functions, and HNSW indexes to the distributed SQL database so transactional data and embeddings can be queried together. |
| [ClickHouse Vector Search](https://clickhouse.com/docs/engines/table-engines/mergetree-family/annindexes) | 🔵 Open core | ClickHouse Vector Search uses vector distance functions and approximate vector-similarity indexes alongside columnar analytics and SQL filtering. |
| [turbopuffer](https://turbopuffer.com) | 🔒 Commercial | turbopuffer is a managed search engine that stores vector and full-text indexes on object storage and exposes filtering, namespaces, and multi-query APIs. |

## Lexical and Hybrid Search Engines

**Lexical retrieval** matches terms rather than only vector proximity; BM25 is its most common ranking function. **Hybrid search** combines lexical and dense or sparse-vector signals, often through score normalization or reciprocal rank fusion.

| Tool | Availability | Description |
| --- | --- | --- |
| [Apache Lucene](https://github.com/apache/lucene) | 🟢 Open source | Apache Lucene is the Java search library underlying many search platforms, with inverted indexes, BM25 ranking, faceting, filters, query parsing, and vector search. |
| [Apache Solr](https://github.com/apache/solr) | 🟢 Open source | Apache Solr is a distributed search server built on Lucene with full-text retrieval, faceting, replication, streaming expressions, learning-to-rank, and dense-vector search. |
| [Meilisearch](https://github.com/meilisearch/meilisearch) | 🔵 Open core | Meilisearch is an open-source search engine with typo tolerance, filters, facets, semantic embeddings, and hybrid ranking, paired with a managed cloud. |
| [Typesense](https://github.com/typesense/typesense) | 🔵 Open core | Typesense is a typo-tolerant search engine with faceting, filtering, vector search, conversational search, and hybrid rank fusion, plus a hosted service. |
| [Tantivy](https://github.com/quickwit-oss/tantivy) | 🟢 Open source | Tantivy is a Rust full-text search library inspired by Lucene, providing inverted indexes, BM25, facets, range queries, and incremental indexing. |
| [Xapian](https://xapian.org) | 🟢 Open source | Xapian is a portable C++ search library with probabilistic ranking, relevance feedback, phrase and boolean queries, spelling correction, and bindings for multiple languages. |
| [Whoosh](https://github.com/mchaput/whoosh) | 🟢 Open source | Whoosh is a pure-Python full-text indexing and search library retained as a lightweight reference implementation for schemas, query parsing, and BM25F-style scoring. |
| [Pyserini](https://github.com/castorini/pyserini) | 🟢 Open source | Pyserini is Castorini's Python toolkit for reproducible sparse, dense, and hybrid retrieval experiments over Lucene indexes and standard IR test collections. |
| [Anserini](https://github.com/castorini/anserini) | 🟢 Open source | Anserini is Castorini's Java IR toolkit built on Lucene for indexing, BM25 retrieval, impact scoring, evaluation, and reproducible research baselines. |
| [BM25S](https://github.com/xhluca/bm25s) | 🟢 Open source | BM25S is a Python library that implements BM25 variants with sparse matrices for fast local indexing and retrieval, including persistence and Hugging Face integrations. |
| [ParadeDB](https://github.com/paradedb/paradedb) | 🔵 Open core | ParadeDB is a PostgreSQL search extension and platform that brings BM25, full-text, filtering, analytics, and hybrid search into SQL workloads. |

## Managed Retrieval APIs and Knowledge Bases

**Managed retrieval services** host indexing, search, and operational infrastructure behind an API. Some expose a low-level search index; others manage chunking, embeddings, retrieval, and source synchronization as a knowledge-base product.

| Service | Availability | Description |
| --- | --- | --- |
| [Azure AI Search](https://learn.microsoft.com/en-us/azure/search/search-what-is-azure-search) | 🔒 Commercial | Azure AI Search is Microsoft's managed search service for full-text, vector, hybrid, semantic-ranker, filtering, enrichment, and integrated vectorization workloads. |
| [Vertex AI Vector Search](https://cloud.google.com/vertex-ai/docs/vector-search/overview) | 🔒 Commercial | Vertex AI Vector Search is Google Cloud's managed ANN service for dense, sparse, and hybrid retrieval with filtering, autoscaling, and streaming or batch updates. |
| [Vertex AI RAG Engine](https://cloud.google.com/vertex-ai/generative-ai/docs/rag-engine/rag-overview) | 🔒 Commercial | Vertex AI RAG Engine is Google's managed RAG data service for corpus creation, ingestion, chunking, embedding, retrieval, and grounding with Vertex AI models. |
| [Amazon Kendra](https://aws.amazon.com/kendra/) | 🔒 Commercial | Amazon Kendra is an AWS enterprise search service with connectors, document enrichment, natural-language queries, relevance tuning, access controls, and semantic ranking. |
| [Amazon Bedrock Knowledge Bases](https://aws.amazon.com/bedrock/knowledge-bases/) | 🔒 Commercial | Amazon Bedrock Knowledge Bases is a managed RAG service that ingests data sources, creates vector or graph-backed indexes, retrieves evidence, and can generate cited responses. |
| [Amazon OpenSearch Service](https://aws.amazon.com/opensearch-service/) | 🔒 Commercial | Amazon OpenSearch Service is AWS's managed deployment of OpenSearch with full-text, vector, neural, and hybrid search plus serverless and provisioned operating modes. |
| [Databricks Mosaic AI Vector Search](https://docs.databricks.com/en/generative-ai/vector-search.html) | 🔒 Commercial | Databricks Mosaic AI Vector Search is a managed vector database integrated with Delta tables, Unity Catalog, embedding endpoints, filtering, hybrid search, and automatic index synchronization. |
| [OpenAI File Search](https://platform.openai.com/docs/guides/tools-file-search) | 🔒 Commercial | OpenAI File Search is a hosted Responses API tool that searches uploaded vector stores with semantic and keyword retrieval before supplying results to a model. |
| [Vectara](https://www.vectara.com) | 🔒 Commercial | Vectara is a managed RAG platform with document ingestion, multilingual retrieval, hybrid search, reranking, grounded generation, citations, and factual-consistency scoring. |
| [GoodMem](https://docs.goodmem.ai/) | 🔒 Commercial | GoodMem provides managed or self-hosted memory infrastructure for AI agents, with server-side chunking and embeddings, semantic retrieval, optional reranking, and shared memory spaces. |
| [Ragie](https://www.ragie.ai) | 🔒 Commercial | Ragie is a managed RAG-as-a-service platform for source connectors, document parsing, partitioning, indexing, hybrid retrieval, reranking, and permission-aware results. |
| [Nuclia](https://nuclia.com) | 🔵 Open core | Nuclia is a retrieval platform with an open-source database component and managed APIs for ingestion, multimodal extraction, vector and keyword search, agents, and RAG. |
| [Contextual AI](https://contextual.ai) | 🔒 Commercial | Contextual AI is a managed enterprise RAG platform with data ingestion, retrieval, reranking, grounded generation, evaluations, and deployment controls. |
| [Cloudflare AutoRAG](https://developers.cloudflare.com/autorag/) | 🔒 Commercial | Cloudflare AutoRAG is a managed pipeline that monitors data sources, parses and chunks content, creates embeddings, indexes it in Vectorize, and exposes retrieval and generation APIs. |
| [Snowflake Cortex Search](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-search/cortex-search-overview) | 🔒 Commercial | Snowflake Cortex Search is a managed hybrid search service over Snowflake data with automated embedding, refresh, filtering, and low-latency query APIs. |
| [IBM watsonx Discovery](https://www.ibm.com/products/watson-discovery) | 🔒 Commercial | IBM watsonx Discovery is an enterprise document-understanding and search service with connectors, enrichment, passage retrieval, natural-language queries, and access-control support. |

## Embedding Models, APIs, and Libraries

**Embedding models** map queries and content into vectors whose distances approximate semantic relevance. Model choice, dimensionality, language and domain coverage, pooling, task instructions, and chunking policy can materially change retrieval quality.

| Model or library | Availability | Description |
| --- | --- | --- |
| [OpenAI Embeddings](https://platform.openai.com/docs/guides/embeddings) | 🔒 Commercial | OpenAI Embeddings is a hosted API for the text-embedding model family, with configurable dimensions on current models and support for search, clustering, and recommendation workloads. |
| [Cohere Embed](https://docs.cohere.com/docs/cohere-embed) | 🔒 Commercial | Cohere Embed is a hosted multilingual embedding model family with separate query and document input types and support for text and multimodal document representations. |
| [Jina Embeddings](https://huggingface.co/jinaai/jina-embeddings-v3) | 🟠 Open weights | Jina Embeddings is Jina AI's downloadable multilingual embedding model family, with task-specific adapters and long-context support under model-specific licenses. |
| [Voyage AI Embeddings](https://docs.voyageai.com/docs/embeddings) | 🔒 Commercial | Voyage AI Embeddings is a hosted model family for general, multilingual, code, finance, legal, and multimodal retrieval through an embedding API. |
| [BGE](https://github.com/FlagOpen/FlagEmbedding) | 🟠 Open weights | BGE is BAAI's family of dense, sparse, multilingual, and instruction-aware retrieval models distributed with the FlagEmbedding training and inference library. |
| [E5](https://github.com/microsoft/unilm/tree/master/e5) | 🟠 Open weights | E5 is Microsoft's text-embedding model family trained with contrastive objectives and query-passage prefixes for retrieval, clustering, classification, and semantic similarity. |
| [Nomic Embed](https://huggingface.co/nomic-ai/nomic-embed-text-v1.5) | 🟠 Open weights | Nomic Embed is Nomic AI's downloadable text-embedding model family with task prefixes, long context, and Matryoshka dimensions for adjustable storage and latency. |
| [Sentence Transformers](https://github.com/huggingface/sentence-transformers) | 🟢 Open source | Sentence Transformers is a Python library for training and serving bi-encoder embeddings, sparse encoders, and cross-encoder rerankers from local or hosted models. |
| [INSTRUCTOR](https://github.com/xlang-ai/instructor-embedding) | 🟠 Open weights | INSTRUCTOR is an instruction-tuned embedding model family that conditions representations on a natural-language task description for retrieval and other embedding tasks. |
| [GTE](https://huggingface.co/Alibaba-NLP/gte-large-en-v1.5) | 🟠 Open weights | GTE is Alibaba's general text-embedding model family for retrieval and semantic similarity, with multilingual, long-context, sparse, and newer instruction-tuned variants. |
| [Snowflake Arctic Embed](https://huggingface.co/Snowflake/snowflake-arctic-embed-l-v2.0) | 🟠 Open weights | Snowflake Arctic Embed is a downloadable embedding model family optimized for retrieval, with multilingual versions and Matryoshka representation support. |
| [Mixedbread Embed](https://huggingface.co/mixedbread-ai/mxbai-embed-large-v1) | 🟠 Open weights | Mixedbread Embed is Mixedbread AI's downloadable embedding model family for semantic search and RAG, with Matryoshka dimensions and quantized representation options. |
| [Qwen3 Embedding](https://huggingface.co/Qwen/Qwen3-Embedding-8B) | 🟠 Open weights | Qwen3 Embedding is Qwen's downloadable multilingual embedding model family for text retrieval, code retrieval, classification, clustering, and semantic similarity. |
| [Vertex AI Text Embeddings](https://cloud.google.com/vertex-ai/generative-ai/docs/embeddings/get-text-embeddings) | 🔒 Commercial | Vertex AI Text Embeddings is Google Cloud's managed API for text and code embedding models with task types and configurable output dimensionality. |
| [Mistral Embed](https://docs.mistral.ai/capabilities/embeddings/) | 🔒 Commercial | Mistral Embed is Mistral AI's hosted endpoint for producing text vectors used in semantic search, clustering, classification, and RAG applications. |
| [FastEmbed](https://github.com/qdrant/fastembed) | 🟢 Open source | FastEmbed is Qdrant's lightweight Python library for local dense, sparse, late-interaction, and reranking inference using optimized model runtimes. |

## Rerankers and Late-Interaction Retrieval

**Rerankers** rescore a small candidate set after first-stage retrieval. Cross-encoders jointly read each query-document pair, while late-interaction models retain token-level representations; both usually cost more per candidate than a bi-encoder but can improve top-k precision.

| Model or tool | Availability | Description |
| --- | --- | --- |
| [Cohere Rerank](https://docs.cohere.com/docs/rerank-overview) | 🔒 Commercial | Cohere Rerank is a hosted cross-encoder-style API that orders text or semi-structured documents by relevance to a query across multilingual and English model variants. |
| [Jina Reranker](https://huggingface.co/jinaai/jina-reranker-v2-base-multilingual) | 🟠 Open weights | Jina Reranker is Jina AI's multilingual cross-encoder model family for query-document relevance scoring, available as downloadable weights and a hosted API. |
| [Voyage Rerank](https://docs.voyageai.com/docs/reranker) | 🔒 Commercial | Voyage Rerank is a hosted relevance-scoring API that reranks candidate documents for a query with general-purpose and domain-oriented model options. |
| [BGE Reranker](https://github.com/FlagOpen/FlagEmbedding/tree/master/FlagEmbedding/finetune/reranker) | 🟠 Open weights | BGE Reranker is BAAI's downloadable cross-encoder and layerwise reranker family for multilingual query-passage scoring and retrieval refinement. |
| [ColBERT](https://github.com/stanford-futuredata/ColBERT) | 🟢 Open source | ColBERT is a neural retrieval system that encodes queries and documents independently but preserves token vectors for efficient late-interaction MaxSim scoring. |
| [RAGatouille](https://github.com/AnswerDotAI/RAGatouille) | 🟢 Open source | RAGatouille is a Python library that simplifies training, indexing, and retrieval with ColBERT-style late-interaction models and integrations with common RAG frameworks. |
| [RankLLM](https://github.com/castorini/rank_llm) | 🟢 Open source | RankLLM is a research toolkit for listwise and pairwise passage reranking with language models, including reproducible implementations of RankGPT-style methods. |
| [FlashRank](https://github.com/PrithivirajDamodaran/FlashRank) | 🟢 Open source | FlashRank is a lightweight local reranking library that packages compact cross-encoder and listwise models for CPU-oriented RAG pipelines. |
| [Mixedbread Rerank](https://huggingface.co/mixedbread-ai/mxbai-rerank-large-v2) | 🟠 Open weights | Mixedbread Rerank is Mixedbread AI's downloadable multilingual cross-encoder model family for ordering text candidates by query relevance, with local and hosted inference options. |
| [Pinecone Rerank](https://docs.pinecone.io/guides/inference/rerank) | 🔒 Commercial | Pinecone Rerank is a managed inference endpoint that scores candidate documents against a query and can be used after Pinecone or external first-stage retrieval. |
| [Qwen3 Reranker](https://huggingface.co/Qwen/Qwen3-Reranker-8B) | 🟠 Open weights | Qwen3 Reranker is Qwen's downloadable multilingual relevance model family for text and code retrieval with instruction-aware query-document scoring. |
| [ZeroEntropy zerank](https://www.zeroentropy.dev) | 🔒 Commercial | ZeroEntropy zerank is a hosted reranking model and API for rescoring retrieved passages, with document search services available from the same provider. |

## Document Parsing, OCR, and Chunking

**Document parsing tools** turn PDFs, office files, scans, tables, and layouts into machine-readable content. **Chunkers** then create retrieval units; preserving headings, reading order, page references, tables, and bounding boxes often matters as much as chunk length.

| Tool | Availability | Description |
| --- | --- | --- |
| [Unstructured](https://github.com/Unstructured-IO/unstructured) | 🔵 Open core | Unstructured is an open-source library and commercial platform for partitioning, cleaning, staging, and chunking PDFs, office documents, HTML, emails, and images for downstream retrieval. |
| [Docling](https://github.com/docling-project/docling) | 🟢 Open source | Docling is an open-source document conversion toolkit for PDF, office, HTML, image, audio, and structured formats, preserving layout, tables, reading order, and provenance. |
| [LlamaParse](https://docs.cloud.llamaindex.ai/llamaparse) | 🔒 Commercial | LlamaParse is LlamaIndex's managed document parser for PDFs and other files, producing structured text, Markdown, tables, images, layout metadata, and configurable parsing outputs. |
| [Apache Tika](https://github.com/apache/tika) | 🟢 Open source | Apache Tika is a content-detection and extraction toolkit that reads text and metadata from more than a thousand file types through Java, server, and parser APIs. |
| [PyMuPDF](https://github.com/pymupdf/PyMuPDF) | 🔵 Open core | PyMuPDF is a Python binding for MuPDF that extracts, searches, renders, and modifies PDFs and other documents, including text blocks, images, tables, and coordinates. |
| [pypdf](https://github.com/py-pdf/pypdf) | 🟢 Open source | pypdf is a pure-Python PDF library for reading, splitting, merging, transforming, and extracting text and metadata without external runtime dependencies. |
| [pdfplumber](https://github.com/jsvine/pdfplumber) | 🟢 Open source | pdfplumber is a Python library for detailed PDF text, character, line, rectangle, and table extraction with access to page geometry. |
| [Marker](https://github.com/datalab-to/marker) | 🔵 Open core | Marker is an open-source document converter from Datalab that turns PDFs, images, presentations, and office files into Markdown, JSON, HTML, chunks, and structured blocks. |
| [MinerU](https://github.com/opendatalab/MinerU) | 🟢 Open source | MinerU is an open-source document parsing toolkit that converts complex PDFs into Markdown or JSON while handling formulas, tables, images, reading order, and OCR. |
| [MegaParse](https://github.com/QuivrHQ/MegaParse) | 🟢 Open source | MegaParse is an open-source parser for PDF, DOCX, PPTX, spreadsheet, CSV, and text inputs, producing formats intended for LLM ingestion. |
| [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) | 🟢 Open source | Tesseract OCR is an open-source optical character recognition engine with command-line and library interfaces and trained language data for many writing systems. |
| [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) | 🟢 Open source | PaddleOCR is an open-source OCR and document-AI toolkit with multilingual text recognition, layout analysis, table and formula recognition, and document parsing pipelines. |
| [Surya](https://github.com/datalab-to/surya) | 🟢 Open source | Surya is an open-source document OCR toolkit for multilingual text recognition, layout analysis, reading order, and table recognition. |
| [Chunkr](https://github.com/lumina-ai-inc/chunkr) | 🔵 Open core | Chunkr is an open-source document intelligence API with a separate managed service for layout analysis, OCR, structured output, and token-aware semantic chunking. |
| [Chonkie](https://github.com/chonkie-inc/chonkie) | 🔵 Open core | Chonkie is an open-source chunking and ingestion library with token, sentence, recursive, semantic, late, code, table, and model-assisted chunkers plus a cloud service. |

## Web Crawling and Content Extraction

**Web acquisition tools** discover pages, render JavaScript when needed, extract main content and metadata, and return clean representations for indexing. Respect robots directives, site terms, authentication boundaries, copyright, and personal-data requirements when crawling.

| Tool | Availability | Description |
| --- | --- | --- |
| [Firecrawl](https://github.com/mendableai/firecrawl) | 🔵 Open core | Firecrawl is an open-source crawling and extraction API with a managed service for search, site maps, browser rendering, structured extraction, and Markdown output. |
| [Crawl4AI](https://github.com/unclecode/crawl4ai) | 🟢 Open source | Crawl4AI is an open-source asynchronous web crawler for LLM data pipelines with browser rendering, extraction strategies, adaptive crawling, filtering, and Markdown generation. |
| [Scrapy](https://github.com/scrapy/scrapy) | 🟢 Open source | Scrapy is a mature Python framework for asynchronous crawling, request scheduling, link following, item extraction, middleware, throttling, and export pipelines. |
| [Trafilatura](https://github.com/adbar/trafilatura) | 🟢 Open source | Trafilatura is a Python package and command-line tool for discovering, downloading, and extracting main text, metadata, comments, and structure from web pages. |
| [Jina Reader](https://jina.ai/reader/) | 🔒 Commercial | Jina Reader is a hosted URL-to-LLM-input API that fetches web pages and returns cleaned Markdown, with search and grounding endpoints in the same service family. |
| [Exa](https://exa.ai) | 🔒 Commercial | Exa is a hosted web search and content API offering neural and keyword retrieval, page contents, highlights, crawling, and research-oriented endpoints. |
| [Tavily](https://tavily.com) | 🔒 Commercial | Tavily is a hosted search, extract, crawl, and map API designed to return web evidence and structured results to AI applications. |
| [Apify](https://apify.com) | 🔵 Open core | Apify is a cloud platform for web scraping and browser automation built around reusable Actors, datasets, schedules, proxies, and open-source crawling SDKs. |
| [Diffbot](https://www.diffbot.com) | 🔒 Commercial | Diffbot is a commercial web extraction and knowledge-graph service with APIs for articles, products, discussions, crawling, natural-language extraction, and entity search. |
| [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) | 🟢 Open source | Beautiful Soup is a Python library for navigating, searching, and modifying HTML or XML parse trees, commonly used as a low-level extraction component. |

## Ingestion, ETL, and Connectors

**Ingestion and ETL tools** move changing data from source systems into parsing, embedding, and indexing pipelines. General-purpose data movers are included when they provide practical connectors or incremental processing useful to retrieval systems.

| Tool | Availability | Description |
| --- | --- | --- |
| [Airbyte](https://github.com/airbytehq/airbyte) | 🔵 Open core | Airbyte is an open-source data-integration platform with a connector catalog, incremental synchronization, change-data capture, transformations, and managed cloud offerings. |
| [Meltano](https://github.com/meltano/meltano) | 🟢 Open source | Meltano is an open-source data-integration platform that composes Singer taps and targets, schedules, state, environments, and transformations into reproducible pipelines. |
| [dlt](https://github.com/dlt-hub/dlt) | 🔵 Open core | dlt is an open-source Python library for loading data from APIs, databases, files, and generators into storage destinations with schemas, state, and incremental updates. |
| [Apache NiFi](https://github.com/apache/nifi) | 🟢 Open source | Apache NiFi is a visual dataflow system for routing, transforming, prioritizing, tracing, and governing data between heterogeneous sources and destinations. |
| [Apache Kafka Connect](https://kafka.apache.org/documentation/#connect) | 🟢 Open source | Apache Kafka Connect is Kafka's framework for scalable source and sink connectors, offset tracking, transformations, distributed workers, and streaming data movement. |
| [Fivetran](https://www.fivetran.com) | 🔒 Commercial | Fivetran is a managed data-movement platform with source and destination connectors, automated schema handling, incremental sync, transformations, and governance features. |
| [VectorFlow](https://github.com/dgarnitz/vectorflow) | 🟢 Open source | VectorFlow is an open-source ingestion pipeline that accepts raw files, chunks and embeds their content, and writes vectors to supported databases through an API. |
| [NeMo Curator](https://github.com/NVIDIA-NeMo/Curator) | 🟢 Open source | NeMo Curator is NVIDIA's scalable data-curation framework for document download, extraction, cleaning, deduplication, filtering, classification, synthetic data, and multimodal pipelines. |

## Graph RAG and Knowledge-Graph Retrieval

**Graph RAG** retrieves through entities, relationships, paths, communities, or graph summaries instead of relying only on independent chunks. The category includes graph-native RAG frameworks and graph databases with first-class retrieval integrations.

| Tool | Availability | Description |
| --- | --- | --- |
| [Microsoft GraphRAG](https://github.com/microsoft/graphrag) | 🟢 Open source | Microsoft GraphRAG is an open-source pipeline that extracts a knowledge graph, builds community summaries, and supports local, global, drift, and basic search over private text. |
| [LightRAG](https://github.com/HKUDS/LightRAG) | 🟢 Open source | LightRAG is an open-source RAG framework that combines graph-based indexing with vector retrieval and supports multiple storage, model, and deployment backends. |
| [Neo4j GraphRAG for Python](https://github.com/neo4j/neo4j-graphrag-python) | 🟢 Open source | Neo4j GraphRAG for Python is an open-source package for knowledge-graph construction, vector and Cypher retrieval, external retrievers, reranking, and graph-grounded generation. |
| [Graphiti](https://github.com/getzep/graphiti) | 🟢 Open source | Graphiti is an open-source framework for building temporally aware knowledge graphs from conversations and business data and retrieving facts through hybrid graph search. |
| [HippoRAG](https://github.com/OSU-NLP-Group/HippoRAG) | 🟢 Open source | HippoRAG is a research framework that builds knowledge graphs and applies personalized PageRank to support multi-hop, memory-inspired retrieval. |
| [KAG](https://github.com/OpenSPG/KAG) | 🟢 Open source | KAG is OpenSPG's knowledge-augmented generation framework for schema-guided graph construction, logical-form planning, hybrid reasoning, retrieval, and generation. |
| [nano-graphrag](https://github.com/gusye1234/nano-graphrag) | 🟢 Open source | nano-graphrag is a compact GraphRAG implementation intended to expose and simplify graph extraction, clustering, storage, and query mechanics. |
| [TrustGraph](https://github.com/trustgraph-ai/trustgraph) | 🟢 Open source | TrustGraph is an open-source platform for knowledge extraction and Graph RAG with modular processing flows, graph and vector stores, provenance, and API access. |
| [Cognee](https://github.com/topoteretes/cognee) | 🔵 Open core | Cognee is an open-source memory and data framework that turns documents and interactions into graph and vector representations, paired with hosted services. |
| [FalkorDB](https://github.com/FalkorDB/FalkorDB) | 🔵 Open core | FalkorDB is an open-source graph database optimized for low-latency graph queries, with vector indexes, GraphRAG tooling, and commercial cloud and enterprise options. |
| [Memgraph](https://github.com/memgraph/memgraph) | 🔵 Open core | Memgraph is an in-memory graph database with Cypher queries, streaming connectors, vector search, graph algorithms, and managed or enterprise offerings. |
| [NebulaGraph](https://github.com/vesoft-inc/nebula) | 🟢 Open source | NebulaGraph is a distributed open-source graph database with nGQL queries, graph services, visualization tooling, and integrations for knowledge-graph and RAG applications. |
| [ArangoDB](https://github.com/arangodb/arangodb) | 🔵 Open core | ArangoDB is a multi-model database for graphs, documents, key-values, full-text, and vector search, with GraphRAG integrations and managed services. |

## Multimodal RAG and Retrieval

**Multimodal retrieval** indexes and searches images, page screenshots, charts, audio, or video in addition to text. Document-image retrievers can preserve visual layout that is lost when a page is reduced to plain text.

| Model or tool | Availability | Description |
| --- | --- | --- |
| [ColPali](https://github.com/illuin-tech/colpali) | 🟢 Open source | ColPali is a visual document-retrieval approach and codebase that applies late interaction to page-image embeddings produced by vision-language models. |
| [ColQwen2](https://huggingface.co/vidore/colqwen2-v1.0) | 🟠 Open weights | ColQwen2 is a downloadable visual document-retrieval model based on Qwen2-VL and trained for ColBERT-style multi-vector page matching. |
| [Byaldi](https://github.com/AnswerDotAI/byaldi) | 🟢 Open source | Byaldi is a Python wrapper for indexing and searching document images with ColPali-family multi-vector retrieval models. |
| [CLIP](https://github.com/openai/CLIP) | 🟠 Open weights | CLIP is OpenAI's downloadable contrastive image-text model and reference code for producing aligned visual and language representations used in cross-modal retrieval. |
| [SigLIP](https://huggingface.co/google/siglip-so400m-patch14-384) | 🟠 Open weights | SigLIP is Google's downloadable image-text representation model family trained with a sigmoid loss for zero-shot classification and cross-modal similarity. |
| [ImageBind](https://github.com/facebookresearch/ImageBind) | 🟠 Open weights | ImageBind is Meta's model and codebase for aligning image, text, audio, depth, thermal, and inertial data in one embedding space under model-specific terms. |
| [Jina CLIP](https://huggingface.co/jinaai/jina-clip-v2) | 🟠 Open weights | Jina CLIP is Jina AI's downloadable multilingual text-image embedding model family for cross-modal search, retrieval, and ranking. |
| [Nomic Embed Vision](https://huggingface.co/nomic-ai/nomic-embed-vision-v1.5) | 🟠 Open weights | Nomic Embed Vision is Nomic AI's downloadable image encoder aligned with Nomic Embed Text for shared-space multimodal retrieval. |
| [Voyage Multimodal Embeddings](https://docs.voyageai.com/docs/multimodal-embeddings) | 🔒 Commercial | Voyage Multimodal Embeddings is a hosted model API that embeds interleaved text and images, including document screenshots, into a shared retrieval space. |
| [Twelve Labs Marengo](https://www.twelvelabs.io/marengo) | 🔒 Commercial | Twelve Labs Marengo is a hosted video-embedding model and search API for retrieving moments by text, image, audio, and video queries. |

## Query Optimization and Retrieval Algorithms

**Query optimization** changes how an information need is expressed or executed: expansion, hypothetical documents, sparse learned terms, decomposition, adaptive routing, iterative retrieval, or context-tree construction. These research implementations are building blocks rather than hosted products.

| Method or toolkit | Availability | Description |
| --- | --- | --- |
| [HyDE](https://github.com/texttron/hyde) | 🟢 Open source | HyDE is the reference implementation of Hypothetical Document Embeddings, which generates a hypothetical answer document and embeds it to retrieve real passages without relevance labels. |
| [SPLADE](https://github.com/naver/splade) | 🟢 Open source | SPLADE is Naver's learned sparse-retrieval implementation that expands queries and documents into weighted vocabulary terms compatible with inverted indexes. |
| [DPR](https://github.com/facebookresearch/DPR) | 🟢 Open source | DPR is Meta's Dense Passage Retrieval codebase for training dual encoders and retrieving passages with dense maximum-inner-product search. |
| [Contriever](https://github.com/facebookresearch/contriever) | 🟢 Open source | Contriever is Meta's unsupervised dense-retrieval model and training code for learning transferable query-passage representations without relevance labels. |
| [Self-RAG](https://github.com/AkariAsai/self-rag) | 🟢 Open source | Self-RAG is a research framework in which a model adaptively retrieves passages and emits reflection tokens to critique relevance, support, and response quality. |
| [Corrective-RAG](https://github.com/HuskyInSalt/CRAG) | 🟢 Open source | Corrective-RAG is the reference implementation of CRAG, which evaluates retrieved documents and can trigger corrective web retrieval before generation. |
| [Adaptive-RAG](https://github.com/starsuzi/Adaptive-RAG) | 🟢 Open source | Adaptive-RAG is a research implementation that routes questions among no-retrieval, single-step, and iterative retrieval strategies according to predicted complexity. |
| [FLARE](https://github.com/jzbjyb/FLARE) | 🟢 Open source | FLARE is the reference implementation of Forward-Looking Active Retrieval, which retrieves during generation when forthcoming sentence confidence is low. |
| [RAPTOR](https://github.com/parthsarthi03/raptor) | 🟢 Open source | RAPTOR is a retrieval approach and implementation that recursively clusters and summarizes text to build a tree queried at multiple abstraction levels. |
| [RAFT](https://github.com/ShishirPatil/gorilla/tree/main/raft) | 🟢 Open source | RAFT is a training recipe and reference implementation for adapting models to answer from retrieved domain documents while distinguishing relevant context from distractors. |
| [Rankify](https://github.com/DataScienceUIBK/rankify) | 🟢 Open source | Rankify is a unified information-retrieval toolkit that exposes retrieval, reranking, query expansion, dataset, and evaluation components behind common interfaces. |

## RAG Evaluation Frameworks and Platforms

**RAG evaluation** separates retrieval quality from generation quality. Retrieval metrics test whether useful evidence appears and where it ranks; groundedness, faithfulness, answer relevance, correctness, and citation metrics test how the generator uses that evidence.

| Tool or platform | Availability | Description |
| --- | --- | --- |
| [Ragas](https://github.com/vibrantlabsai/ragas) | 🟢 Open source | Ragas is an open-source evaluation toolkit for RAG and other LLM applications with faithfulness, response relevance, context precision and recall, test generation, and experiment workflows. |
| [DeepEval RAG metrics](https://github.com/confident-ai/deepeval) | 🟢 Open source | DeepEval RAG metrics are open-source evaluators for answer relevancy, faithfulness, contextual precision, contextual recall, and contextual relevancy that run locally or in CI. |
| [DeepTeam](https://github.com/confident-ai/deepteam) | 🟢 Open source | DeepTeam is an open-source red-teaming framework for testing LLM and RAG applications against vulnerabilities and adversarial attacks, including prompt injection, data leakage, misinformation, and unsafe behavior. |
| [TruLens](https://github.com/truera/trulens) | 🟢 Open source | TruLens is an open-source evaluation and tracking library that instruments LLM applications and implements feedback functions including the RAG triad of context relevance, groundedness, and answer relevance. |
| [ARES](https://github.com/stanford-futuredata/ARES) | 🟢 Open source | ARES is Stanford's automated RAG evaluation framework using synthetic training data, lightweight judges, and prediction-powered inference to estimate context relevance, faithfulness, and answer relevance. |
| [RAGChecker](https://github.com/amazon-science/RAGChecker) | 🟢 Open source | RAGChecker is Amazon Science's fine-grained diagnostic framework that evaluates retriever and generator behavior through claim-level entailment and error categories. |
| [Arize Phoenix](https://github.com/Arize-ai/phoenix) | 🟢 Open source | Arize Phoenix is an open-source observability and evaluation platform with tracing, datasets, experiments, retrieval analysis, and LLM-based evaluators for RAG applications. |
| [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG) | 🟢 Open source | AutoRAG is an open-source optimization framework that evaluates combinations of parsing, chunking, retrieval, augmentation, reranking, and generation modules on a user's dataset. |
| [Tonic Validate](https://github.com/TonicAI/tonic_validate) | 🟢 Open source | Tonic Validate is an open-source RAG evaluation library for answer similarity, retrieval precision and recall, answer consistency, augmentation accuracy, and benchmark reporting. |
| [continuous-eval](https://github.com/relari-ai/continuous-eval) | 🟢 Open source | continuous-eval is an open-source framework for modular evaluation of retrieval, reranking, generation, classification, and agent pipelines with datasets and custom metrics. |
| [Giskard](https://github.com/Giskard-AI/giskard-oss) | 🔵 Open core | Giskard is an open-source testing library with a commercial platform for RAG evaluation, knowledge-base quality checks, hallucination testing, vulnerability scanning, and test generation. |
| [Patronus AI](https://www.patronus.ai) | 🔒 Commercial | Patronus AI is a commercial evaluation and security platform with experiments, judge models, hallucination and RAG evaluators, red teaming, monitoring, and enterprise controls. |
| [Galileo](https://galileo.ai) | 🔒 Commercial | Galileo is a commercial AI evaluation and observability platform with RAG quality metrics, retrieval and generation diagnostics, experiments, tracing, monitoring, and guardrails. |
| [LangSmith](https://www.langchain.com/langsmith) | 🔒 Commercial | LangSmith is LangChain's commercial platform for tracing, datasets, offline and online evaluation, annotation, prompt management, experiments, and production monitoring across framework choices. |
| [Opik](https://github.com/comet-ml/opik) | 🔵 Open core | Opik is an open-source evaluation and observability platform from Comet with tracing, datasets, experiments, LLM judges, RAG metrics, prompt management, and a hosted service. |
| [Evidently](https://github.com/evidentlyai/evidently) | 🔵 Open core | Evidently is an open-source evaluation and monitoring library with test suites, reports, retrieval and generation descriptors, datasets, tracing integrations, and a commercial cloud. |

For a broader catalog of evaluation frameworks, judge models, agent evals, red teaming, and benchmarks, see the sibling repository [AI Evaluation Tools](https://github.com/aglio-lab/ai-evaluation-tools).

## Retrieval and RAG Benchmarks

**Retrieval benchmarks** provide corpora, queries, relevance judgments, and scoring protocols. **RAG benchmarks** additionally test evidence use, answer quality, robustness, or multi-turn behavior; scores are only comparable when the corpus, split, retrieval depth, and metric implementation match.

| Benchmark | Availability | Description |
| --- | --- | --- |
| [BEIR](https://github.com/beir-cellar/beir) | 🟢 Open source | BEIR is a heterogeneous zero-shot information-retrieval benchmark spanning 18 datasets and multiple domains, with standardized loaders, retrieval baselines, and evaluation metrics. |
| [MTEB](https://github.com/embeddings-benchmark/mteb) | 🟢 Open source | MTEB is a large multilingual benchmark and evaluation package for text embeddings across retrieval, reranking, classification, clustering, semantic similarity, and related tasks. |
| [CRAG](https://github.com/facebookresearch/CRAG) | 🟢 Open source | CRAG is Meta's Comprehensive RAG Benchmark with thousands of questions, temporal and long-tail facts, mock web and knowledge-graph APIs, and end-to-end scoring. |
| [BRIGHT](https://github.com/xlang-ai/BRIGHT) | 🟢 Open source | BRIGHT is a benchmark for reasoning-intensive retrieval across technical and everyday domains where identifying relevant documents requires substantial query reasoning. |
| [RAGBench](https://huggingface.co/datasets/rungalileo/ragbench) | 🟢 Open source | RAGBench is a large explainable RAG dataset across multiple industry domains with retrieved contexts, responses, labels, and the associated TRACe evaluation framework. |
| [MTRAG](https://github.com/IBM/mt-rag-benchmark) | 🟢 Open source | MTRAG is IBM's human-generated benchmark for evaluating multi-turn retrieval-augmented generation across domains, conversation histories, retrieval, and grounded responses. |
| [MIRACL](https://github.com/project-miracl/miracl) | 🟢 Open source | MIRACL is a multilingual information-retrieval benchmark with relevance judgments for queries and Wikipedia passages across 18 languages. |
| [LoTTE](https://huggingface.co/datasets/colbertv2/lotte) | 🟢 Open source | LoTTE is a long-tail topic-stratified retrieval benchmark with search and forum queries across five domains and pooled relevance judgments. |
| [KILT](https://github.com/facebookresearch/KILT) | 🟢 Open source | KILT is Meta's benchmark that grounds multiple knowledge-intensive language tasks in a shared Wikipedia snapshot and scores both retrieval provenance and task output. |
| [MS MARCO](https://microsoft.github.io/msmarco/) | 🟢 Open source | MS MARCO is Microsoft's large-scale passage and document ranking benchmark derived from real search queries with relevance labels and public leaderboard tasks. |
| [Natural Questions](https://ai.google.com/research/NaturalQuestions) | 🟢 Open source | Natural Questions is Google's question-answering dataset of real search queries paired with Wikipedia pages and annotated long and short answers. |
| [HotpotQA](https://hotpotqa.github.io) | 🟢 Open source | HotpotQA is a multi-hop question-answering benchmark with supporting-fact annotations that tests retrieval and reasoning across multiple Wikipedia passages. |
| [ViDoRe](https://github.com/illuin-tech/vidore-benchmark) | 🟢 Open source | ViDoRe is a benchmark and evaluation toolkit for visual document retrieval across page images, varied document domains, and multilingual queries. |
| [RAGTruth](https://github.com/ParticleMedia/RAGTruth) | 🟢 Open source | RAGTruth is a corpus of RAG responses with word-level hallucination annotations across question answering, data-to-text generation, and summarization. |
| [RGB](https://github.com/chen700564/RGB) | 🟢 Open source | RGB is a benchmark for RAG robustness across noise tolerance, negative rejection, information integration, and counterfactual conflict. |

## Observability, Security, and Governance

**RAG observability** records queries, retrieved chunks, scores, prompts, outputs, latency, and cost so production behavior can be debugged and evaluated. **Security and governance** tools add policy enforcement, prompt-injection defenses, sensitive-data controls, access checks, and auditability.

| Tool | Availability | Description |
| --- | --- | --- |
| [Langfuse](https://github.com/langfuse/langfuse) | 🔵 Open core | Langfuse is an open-source LLM engineering platform with self-hosting and cloud options for traces, sessions, prompt management, datasets, evaluations, metrics, and cost analysis. |
| [Helicone](https://github.com/Helicone/helicone) | 🔵 Open core | Helicone is an open-source AI gateway and observability platform with request logging, sessions, caching, routing, rate limits, experiments, evaluations, and a hosted service. |
| [OpenLLMetry](https://github.com/traceloop/openllmetry) | 🟢 Open source | OpenLLMetry is an OpenTelemetry-based set of instrumentations for capturing model, vector-database, framework, and agent spans and exporting them to compatible backends. |
| [OpenInference](https://github.com/Arize-ai/openinference) | 🟢 Open source | OpenInference is an open specification and instrumentation collection for representing LLM, retrieval, reranking, embedding, tool, and agent operations as OpenTelemetry traces. |
| [OpenLIT](https://github.com/openlit/openlit) | 🔵 Open core | OpenLIT is an OpenTelemetry-native AI engineering platform with tracing, metrics, prompt management, evaluations, guardrails, cost tracking, and self-hosted or cloud deployment. |
| [LangWatch](https://github.com/langwatch/langwatch) | 🔵 Open core | LangWatch is an open-source platform with hosted options for LLM traces, evaluations, dashboards, prompt optimization, and scenario-based agent simulation. |
| [Portkey](https://github.com/Portkey-AI/gateway) | 🔵 Open core | Portkey is an open-source AI gateway paired with a commercial control plane for routing, fallbacks, caching, budgets, observability, guardrails, and provider access policies. |
| [Datadog LLM Observability](https://www.datadoghq.com/product/llm-observability/) | 🔒 Commercial | Datadog LLM Observability is a commercial tracing and monitoring product for LLM and RAG applications with retrieval spans, quality signals, security scanning, cost, and latency analysis. |
| [LLM Guard](https://github.com/protectai/llm-guard) | 🟢 Open source | LLM Guard is an open-source input and output scanning library for prompt injection, secrets, PII, toxicity, malicious URLs, relevance, factual consistency, and other risks. |
| [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) | 🟢 Open source | NeMo Guardrails is NVIDIA's open-source toolkit for programmable dialog, retrieval, execution, and safety rails, including topical controls and groundedness checks. |
| [Guardrails AI](https://github.com/guardrails-ai/guardrails) | 🔵 Open core | Guardrails AI is an open-source validation framework with a hosted platform and validator hub for structured outputs, content checks, PII, provenance, and policy enforcement. |
| [Lakera Guard](https://www.lakera.ai/lakera-guard) | 🔒 Commercial | Lakera Guard is a commercial API for detecting prompt injection, jailbreaks, harmful content, and sensitive information in AI application inputs and outputs. |
| [garak](https://github.com/NVIDIA/garak) | 🟢 Open source | garak is NVIDIA's open-source generative-AI vulnerability scanner with probes and detectors for prompt injection, data leakage, hallucination, toxicity, jailbreaks, and other failure modes. |

## Discontinued and Historical Tools

Influential retrieval projects that are archived or superseded are kept here to prevent stale recommendations and to support reproducibility. Statuses were checked on the last-reviewed date above.

| Tool | Availability | Status |
| --- | --- | --- |
| [Canopy](https://github.com/pinecone-io/canopy) | 🟢 Open source | Canopy was Pinecone's open-source RAG framework and context engine; its GitHub repository is archived, so new systems should use maintained alternatives or lower-level Pinecone SDKs. |
| [Kùzu](https://github.com/kuzudb/kuzu) | 🟢 Open source | Kùzu was an embedded property-graph database with Cypher, vector search, and full-text search; its GitHub repository was archived in October 2025. |
| [llama-hub legacy repository](https://github.com/run-llama/llama-hub) | 🟢 Open source | llama-hub legacy repository was the original home of LlamaIndex data loaders; it was archived in March 2024 after integrations moved to maintained package repositories. |

## Key Papers and Concepts

Foundational and representative primary sources for the methods behind modern retrieval systems:

- **Retrieval-augmented generation** — [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) (Lewis et al., 2020) introduced the widely used RAG formulation combining a neural retriever with a generator.
- **Dense passage retrieval** — [Dense Passage Retrieval for Open-Domain Question Answering](https://arxiv.org/abs/2004.04906) (Karpukhin et al., 2020) established a strong dual-encoder retrieval baseline.
- **Late interaction** — [ColBERT: Efficient and Effective Passage Search via Contextualized Late Interaction over BERT](https://arxiv.org/abs/2004.12832) (Khattab and Zaharia, 2020) retains token-level vectors while avoiding full cross-encoder retrieval cost.
- **Sparse neural retrieval** — [SPLADE v2](https://arxiv.org/abs/2109.10086) (Formal et al., 2021) learns sparse vocabulary weights that remain compatible with inverted indexes.
- **Zero-shot retrieval evaluation** — [BEIR: A Heterogeneous Benchmark for Zero-shot Evaluation of Information Retrieval Models](https://arxiv.org/abs/2104.08663) (Thakur et al., 2021) standardized cross-domain retrieval comparison.
- **Embedding evaluation** — [MTEB: Massive Text Embedding Benchmark](https://arxiv.org/abs/2210.07316) (Muennighoff et al., 2022) broadened embedding evaluation beyond a single retrieval dataset.
- **Hypothetical document embeddings** — [Precise Zero-Shot Dense Retrieval without Relevance Labels](https://arxiv.org/abs/2212.10496) (Gao et al., 2022) introduced HyDE.
- **RAG evaluation** — [RAGAS: Automated Evaluation of Retrieval Augmented Generation](https://arxiv.org/abs/2309.15217) (Es et al., 2023) proposed reference-free metrics for retrieval and grounded generation.
- **Self-reflective retrieval** — [Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection](https://arxiv.org/abs/2310.11511) (Asai et al., 2023) made retrieval and reflection adaptive within generation.
- **Hierarchical retrieval** — [RAPTOR: Recursive Abstractive Processing for Tree-Organized Retrieval](https://arxiv.org/abs/2401.18059) (Sarthi et al., 2024) retrieves over recursively summarized clusters.
- **Corrective retrieval** — [Corrective Retrieval Augmented Generation](https://arxiv.org/abs/2401.15884) (Yan et al., 2024) adds a retrieval evaluator and corrective actions.
- **Graph RAG** — [From Local to Global: A Graph RAG Approach to Query-Focused Summarization](https://arxiv.org/abs/2404.16130) (Edge et al., 2024) introduced community-summary retrieval for corpus-level questions.

## Glossary

- **Retrieval-augmented generation (RAG)** — an architecture that retrieves external evidence and includes it in the context used to generate an answer.
- **Retriever** — a component that returns candidate documents or chunks for a query.
- **Vector database** — a database or search service that stores vectors and supports similarity queries, usually with metadata filters.
- **Embedding** — a numeric representation of content or a query used for similarity, clustering, or downstream prediction.
- **Dense retrieval** — retrieval with vectors whose dimensions are mostly nonzero, commonly produced by neural bi-encoders.
- **Sparse retrieval** — retrieval with high-dimensional vectors containing mostly zeros, including lexical BM25 and learned sparse methods such as SPLADE.
- **Hybrid search** — a retrieval strategy that combines two or more signals, commonly BM25 and dense-vector similarity.
- **BM25** — a probabilistic lexical-ranking function based on term frequency, inverse document frequency, and document-length normalization.
- **ANN** — approximate nearest-neighbor search, which trades a configurable amount of recall for lower latency or memory use.
- **HNSW** — Hierarchical Navigable Small World graphs, a widely used graph-based ANN index.
- **IVF** — inverted-file vector indexing, which partitions vectors and searches selected partitions rather than the full collection.
- **Reranker** — a stronger model that rescores candidates returned by a cheaper first-stage retriever.
- **Cross-encoder** — a reranker that processes the query and candidate together to predict relevance.
- **Late interaction** — retrieval that independently encodes query and document tokens, then computes token-level interactions at search time.
- **Chunk** — a retrievable unit derived from a larger source document, often carrying source, page, section, and permission metadata.
- **RRF** — reciprocal rank fusion, a rank-based method for combining result lists without requiring comparable raw scores.
- **Grounding** — the degree to which an answer is supported by retrieved or otherwise supplied evidence.
- **Recall@k** — the fraction of relevant items found among the first _k_ retrieved results.
- **MRR** — mean reciprocal rank, which rewards placing the first relevant result near the top.
- **nDCG** — normalized discounted cumulative gain, which measures graded relevance while discounting lower-ranked results.
- **Graph RAG** — retrieval over extracted entities, relationships, paths, communities, or graph summaries.
- **Multimodal RAG** — retrieval and generation over more than one modality, such as text plus page images, audio, or video.
- **Open weights** — downloadable model parameters distributed under model-specific terms that may not meet an OSI open-source definition.
- **Open core** — a project with an open-source component and separate commercial cloud, enterprise, or proprietary components.

## Frequently Asked Questions

**What is retrieval-augmented generation (RAG)?**  
RAG is an application architecture that retrieves evidence from an external corpus and supplies it to a generative model at query time. It can improve freshness, domain coverage, provenance, and controllability, but retrieved context does not by itself guarantee a correct or faithful answer.

**What components does a production RAG stack need?**  
Most systems need source connectors, parsing and chunking, an embedding model, a lexical or vector index, retrieval and optional reranking, prompt or workflow orchestration, generation, evaluation, and production tracing. Access control, deletion propagation, data lineage, and prompt-injection defenses are also important when the corpus is sensitive.

**What is the difference between a RAG framework and a vector database?**  
A RAG framework coordinates application steps and integrations. A vector database stores vectors and returns similar records. Frameworks such as LangChain, LlamaIndex, and Haystack typically call a database such as Pinecone, Weaviate, Qdrant, Milvus, pgvector, or Elasticsearch; neither category automatically replaces the other.

**Which vector database is best for RAG?**  
There is no universal best choice. Compare retrieval quality under realistic filters, index build and update behavior, latency at target concurrency, hybrid-search support, tenancy and access controls, backup and deletion semantics, operational burden, portability, and total cost using your own corpus and queries.

**When should I use hybrid search?**  
Hybrid search is useful when exact names, identifiers, jargon, dates, or quoted phrases matter alongside semantic similarity. Evaluate lexical, dense, and fused results separately because hybrid retrieval adds tuning choices and does not improve every corpus automatically.

**What is the difference between an embedding model and a reranker?**  
An embedding model usually encodes the query and corpus independently so the whole corpus can be searched efficiently. A reranker reads the query with each retrieved candidate, or applies token-level late interaction, and spends more computation on a much smaller result set.

**How should I evaluate retrieval?**  
Build queries with relevance judgments, keep a stable test split, and measure recall@k, precision@k, MRR, or nDCG at the retrieval depth used by the application. Then evaluate grounded generation separately for evidence use, faithfulness, answer correctness, citation quality, latency, and cost.

**When is Graph RAG useful?**  
Graph RAG is most useful when questions depend on relationships, multi-hop paths, communities, entity resolution, or corpus-level themes. It adds extraction, schema, graph-update, and evaluation complexity, so benchmark it against simpler lexical, dense, and hybrid baselines.

**Can RAG search images and scanned documents?**  
Yes. One approach uses OCR and layout-aware parsing before text retrieval; another embeds page images or other modalities directly with models such as ColPali, ColQwen2, CLIP-family encoders, or specialized video embeddings. The appropriate benchmark should reflect the source format and query modality.

**Does RAG prevent hallucinations?**  
No. RAG can provide relevant evidence, but the retriever can miss or surface misleading material and the generator can ignore, distort, or overgeneralize from it. Measure retrieval and generation separately, require source attribution where appropriate, and test unanswerable and conflicting-context cases.

**Which tools in this list are open source?**  
Entries marked 🟢 link to an open-source primary artifact; 🔵 marks an open-source component paired with a commercial offering. Model weights marked 🟠 may be downloadable but use model-specific licenses, so review the linked license before deployment or redistribution.

## Methodology

How this list is built and maintained:

- **Scope.** Included entities have a direct role in retrieval-augmented generation, information retrieval, vector or lexical search, embedding, reranking, parsing, ingestion, graph or multimodal retrieval, RAG evaluation, benchmarking, observability, or security. General-purpose databases and AI frameworks are included only when they expose first-class retrieval capabilities.
- **Taxonomy.** Categories represent the entity's primary role in a RAG stack. Multi-purpose products are placed in the most useful section and described with their adjacent capabilities rather than duplicated across tables.
- **Entity granularity.** Each table row represents one named project, product, service, model family, benchmark, or research implementation. Separate products from one organization receive separate rows; integrations and models merely named inside a description do not add to the entry count.
- **Inclusion criteria.** Open projects should be actively maintained or have lasting reference value. Commercial products must have public first-party information and be generally available. Archived projects move to the historical section instead of disappearing silently.
- **Availability markers.** 🟢 means the primary artifact is open source; 🟠 means downloadable weights under model-specific terms; 🔵 means an open component is paired with a commercial offering; 🔒 means a commercial or closed-source service. Always verify the linked license and service terms for your use case.
- **Ordering.** Entries are ordered by editorial judgment of relevance, adoption, and usefulness within a category, not alphabetically. There is no paid placement, and inclusion is not a recommendation.
- **Editorial independence.** This directory is maintained by aglio-lab. Every entry follows the same sourcing, wording, and ordering rules, and no placement is sold.
- **Sources.** Every entity name links to a primary source: an official repository, product page, documentation site, model card, benchmark page, or paper. Secondary comparison articles are not used as the canonical link.
- **Verification.** Names, scope, availability, and status were checked against the linked primary source as of the last-reviewed date. Product features and licenses change; a source link is provided so readers can re-check a claim.
- **Monthly review cadence.** The directory is reviewed during the first week of every month. Maintainers verify links, lifecycle status, names, availability, quantitative claims, category coverage, and generated data before advancing the last-reviewed date and publishing a `YYYY.MM` release. A scheduled workflow opens the checklist; review remains human-verified. See [`MAINTENANCE.md`](MAINTENANCE.md).
- **Counts.** The **209 entries** count is the number of data rows across the 16 catalog tables, including three historical rows. It does not count headings, papers, glossary terms, integrations mentioned in prose, or the same capability named in a description.
- **Corrections.** Open a [GitHub issue](https://github.com/aglio-lab/rag-retrieval-tools/issues) or pull request for a factual correction, status change, broken primary link, missing attribution, or category proposal.

## Related Lists and Resources

- [AI Red Teaming Tools](https://github.com/aglio-lab/ai-red-teaming-tools) — red-team frameworks, scanners, guardrails, and security benchmarks.
- [LLM Observability Tools](https://github.com/aglio-lab/llm-observability-tools) — tracing, monitoring, online evaluation, and production analytics.
- [AI Governance Tools](https://github.com/aglio-lab/ai-governance-tools) — governance, risk, compliance, audit, and responsible-AI tooling.
- [AI Agent Frameworks](https://github.com/aglio-lab/ai-agent-frameworks) — frameworks and orchestration tools for building and operating agents.
- [LLM Fine-Tuning Tools](https://github.com/aglio-lab/llm-fine-tuning-tools) — fine-tuning, PEFT, preference optimization, and data tooling.
- [Context Engineering Tools](https://github.com/aglio-lab/context-engineering-tools) — prompt, memory, context management, compression, and MCP tooling.

- [AI Evaluation Tools](https://github.com/aglio-lab/ai-evaluation-tools) — sibling source-linked directory covering LLM, RAG, agent, safety, observability, and benchmark evaluation tools in greater depth.
- [awesome-rag](https://github.com/awesome-rag/awesome-rag) — community collection of RAG frameworks, papers, tutorials, and projects.
- [Awesome-LLM-RAG](https://github.com/jxzhangjhu/Awesome-LLM-RAG) — research-oriented collection of retrieval-augmented generation papers and resources.
- [MTEB Leaderboard](https://huggingface.co/spaces/mteb/leaderboard) — public comparison of text embedding models across MTEB tasks.
- [BEIR](https://github.com/beir-cellar/beir) — benchmark code and datasets for heterogeneous information retrieval.
- [Vespa retrieval documentation](https://docs.vespa.ai/en/nearest-neighbor-search.html) — technical material on nearest-neighbor and hybrid retrieval in a production search engine.

---

## Citing This List

If you reference this list in an article, paper, report, or AI-generated answer, please cite it as:

> _The Comprehensive List of RAG and Retrieval Tools_ (2026). A curated, source-linked directory of open-source and commercial tools for retrieval-augmented generation and information retrieval. GitHub. https://github.com/aglio-lab/rag-retrieval-tools

BibTeX:

```bibtex
@misc{rag-retrieval-tools,
  title        = {The Comprehensive List of RAG and Retrieval Tools},
  year         = {2026},
  howpublished = {\url{https://github.com/aglio-lab/rag-retrieval-tools}},
  note         = {A curated, source-linked directory of open-source and commercial tools for retrieval-augmented generation and information retrieval. Accessed: 2026-07-16}
}
```

For a reproducible citation of a changing list, cite a specific commit permalink or release tag. When citing an individual tool, model, dataset, or method, prefer its own repository, documentation, model card, or paper linked in the relevant row.

## Contributing

Contributions and corrections are welcome:

1. Add one entity per pull request to the most specific matching category.
2. Use the correct availability marker and link the entity name to a primary source.
3. Write a neutral, complete factual sentence that starts with the entity's name.
4. Distinguish a framework, database, model, API, benchmark, and platform rather than combining separate entities in one row.
5. Include maintained projects or artifacts with lasting reference value; report archival, shutdown, and renaming so historical status stays accurate.

Open a [pull request](https://github.com/aglio-lab/rag-retrieval-tools/pulls) or [issue](https://github.com/aglio-lab/rag-retrieval-tools/issues) to contribute.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers waive all copyright and related rights to this directory under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/). Linked projects, documentation, model weights, datasets, papers, names, and trademarks retain their own licenses and terms.
