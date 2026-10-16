# AI Story Recommender

A practical AI application demonstrating recommendation architecture, personalization, API design, and production-minded engineering.

## Goal

Build a recommendation service that can evolve from an explainable baseline to semantic embeddings and learned ranking without rewriting the application architecture.

## Architecture

```text
Web / Mobile Client
        |
        v
     REST API
        |
        v
Recommendation Engine
   |            |
   v            v
Similarity    Ranking
   |            |
   +------> Results
```

## Current MVP

- FastAPI REST API
- Explainable recommendation scoring
- User-interest matching
- Deterministic ranking
- Pydantic validation
- Unit tests
- Docker configuration

### Example

```text
POST /recommend

{
  "user_id": "demo-user",
  "interests": ["mystery", "adventure"]
}
```

The response ranks stories according to matched interests and exposes the matching signals.

## Design principle

The application is separated from the recommendation strategy:

```text
Application
    |
Recommendation Interface
    |
Ranking Strategy
    +-- Rule-based baseline
    +-- Embedding similarity
    +-- ML ranking (future)
```

This makes the system easier to test and allows the model layer to evolve independently.

## Roadmap

- [x] Basic story/content model
- [x] User preference input
- [x] REST API
- [x] Deterministic recommendation engine
- [x] Unit tests
- [x] Dockerfile
- [ ] Semantic embeddings
- [ ] Similarity search
- [ ] PostgreSQL persistence
- [ ] Recommendation evaluation
- [ ] Learned ranking
- [ ] Lightweight web client
- [ ] CI pipeline

## Why this project matters

Modern AI products need more than a model call. They need reliable application architecture around models, data, ranking, APIs, persistence, evaluation, and iteration.

This project is a focused demonstration of that engineering approach.

It complements my professional experience in AI-integrated applications, computer vision, C/C++, Qt, mobile development, real-time systems, enterprise software, system architecture, and technical project leadership.

## Author

**Jinge H.**

**Senior Software Engineer | AI & Software Solutions Architect | Technical Project Lead**
