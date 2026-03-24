# Proof of Concept - Savings Goal Visualizer

## Scope
- App category: Logistics & Operations
- Entity model: Savings Goal Operation
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Location: `location` (text)
- Capacity: `capacity` (number)
- Execution Notes: `execution_notes` (textarea)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"active","payload":{"location":"Demo value","capacity":12,"execution_notes":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 76
- Generated UTC: 2026-03-24T15:52:22.336871+00:00
- Status: Phase-2 complete
