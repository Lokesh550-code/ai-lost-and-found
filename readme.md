# Campus Lost & Found

An AI-assisted lost-and-found platform for a college campus.

Students can report lost/found items, search existing reports, receive potential matches, and submit claims. Admins manage reports and verify claims.

## MVP

- Student authentication
- Create **Lost / Found** reports
- Upload item images
- Browse, search & filter reports
- AI-assisted matching between lost and found items
- Potential match scoring
- Submit and review claims
- Admin dashboard for reports, users & claims
- Mark items as resolved/returned

**AI suggests matches; humans make the final decision.**

## User Types

### Student

- Create and manage reports
- Search lost/found items
- View potential matches
- Submit claims

### Admin

- Manage users and reports
- Review claims
- Resolve cases

## Tech Stack

**Web**

- React + Vite
- Tailwind CSS
- React Router

**API**

- Python
- FastAPI
- MongoDB driver / ODM
- JWT authentication

**AI**

- Python
- FastAPI
- Text & image embedding models
- Custom matching/scoring logic

**Infrastructure**

- MongoDB Atlas
- ImageKit
- Vercel / Render

## Architecture

```text
        ┌─────────────┐
        │     Web     │
        │ React+vite  │
        └──────┬──────┘
               │
               ▼
        ┌─────────────┐
        │     API     │
        │   FastAPI   │
        └───┬─────┬───┘
            │     │
            ▼     ▼
       MongoDB    AI
                  Service
```

The project is a **monorepo** with three applications:

```text
apps/
├── web/       # React frontend
├── api/       # FastAPI backend
└── ai/        # AI matching service
```

The API owns application state and database access. The AI service only performs matching/analysis.

## Scope

The MVP focuses on one college campus. Advanced features such as mobile apps, real-time chat, push notifications, advanced fraud detection, and complex infrastructure are outside the initial scope.
