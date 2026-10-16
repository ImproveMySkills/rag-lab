# Agents Instructions

## Objectif

Construire une plateforme RAG maintenable et exploitable.

## Règles

### Architecture

Utiliser une architecture hexagonale.

packages :

com.improvemyskills.rag

    api
    application
    domain
    infrastructure

### Spring

- Constructor Injection uniquement
- Aucun field injection
- Aucun @Autowired

### Qualité

- Java 21
- Checkstyle
- PMD
- SpotBugs
- Sonar Friendly

### Tests

- JUnit 5
- Mockito
- Testcontainers

Couverture minimale :

80 %

### Documentation

Tout endpoint REST doit être documenté.

### Code

Préférer :

- records
- Optional
- streams lorsque pertinent

Éviter :

- code dupliqué
- méthodes > 30 lignes

### LLM

Tous les prompts doivent être externalisés.

### Configuration

Aucune valeur en dur.