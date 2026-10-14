# Besoin

Développer une application RAG (Retrieval Augmented Generation) permettant d'interroger un corpus documentaire métier constitué principalement de fichiers PDF.

## Objectifs

L'utilisateur pose une question.

Le système :

1. Recherche les passages les plus pertinents dans les documents.
2. Construit un contexte.
3. Interroge un LLM exécuté localement via Ollama.
4. Retourne une réponse fondée uniquement sur les données du corpus.

## Fonctionnalités

### Import documentaire

- Import manuel de PDF
- Import automatique depuis un répertoire
- Réindexation complète
- Réindexation incrémentale

### Vectorisation

- Découpage des documents (chunking)
- Génération des embeddings
- Stockage dans ChromaDB

### Recherche

- Recherche sémantique
- Top K configurable

### Génération

- Utilisation d'Ollama
- Réponse contextualisée
- Limitation des hallucinations

### REST API

POST /api/rag/ask

POST /api/rag/index

GET /api/rag/documents

GET /api/rag/health

### Observabilité

- Spring Actuator
- Micrometer
- Logs structurés

### Sécurité

- Pas d'exécution distante
- RAG strictement basé sur les documents