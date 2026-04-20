# bantrwrld 🌱

> I built bantrwrld to create an experience that allows people worldwide to go out and experience shared interests and activities — not just scroll through them.

## What is bantrwrld?

bantrwrld is a real-world social networking platform built around one idea: the best connections happen offline. It's a hyper-local, event-driven app that works like a real-life LFG system — instantly matching you with people who share your lifestyle, so you can stop doom-scrolling and start actually doing things.

No follower counts. No infinite feeds. No FOMO content. Just real people, real places, real events.

### The Problem

- Moved to a new city and don't know anyone? **We got you.**
- Tired of superficial connections that never leave the app? **Same.**
- Want to find your people but don't know where to look? **We'll help.**
- Sick of planning hangouts that never actually happen? **We make it easy.**

### What Makes Us Different

- **No infinite scroll** — your time is yours
- **Hyper-local focus** — events in your actual area, not the internet
- **Real-life LFG** — instantly connect with people who match your lifestyle
- **Quality over quantity** — meaningful connections, not follower counts
- **Gets you offline** — the app's goal is to close the app

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js 15, React 19, TypeScript, Tailwind CSS 4 |
| Backend | Node.js, Express 4, TypeScript |
| ORM | TypeORM 0.3 + PostgreSQL + PostGIS |
| Auth | Custom JWT + bcryptjs + refresh tokens |
| Realtime | Socket.IO 4.8 |
| Payments | Stripe |
| Email | Resend |
| Maps | MapLibre GL |
| Storage | AWS S3 / MinIO |
| Cache | Redis |
| Infrastructure | Docker, Railway, Vercel |

## Getting Started

### Prerequisites

- Node.js 20+
- Docker
- Git

### Quick Setup

```bash
# Clone the repo
git clone https://github.com/7onyx7/bantrwrld.git
cd bantrwrld

# Start local services (PostgreSQL, Redis, MinIO, Mailhog)
docker-compose up -d

# Install dependencies
cd frontend && npm install
cd ../backend && npm install

# Configure environment
cp backend/.env.example backend/.env
# Set NEXT_PUBLIC_API_URL in your frontend environment

# Run database migrations
cd backend && npm run db:migrate

# Start dev servers
npm run dev:all
```

**Local service URLs:**
- Frontend: http://localhost:3000
- Backend API: http://localhost:3001
- MinIO console: http://localhost:9001
- Mailhog UI: http://localhost:8025

## Project Status

**Currently in active development** — web MVP nearing launch readiness.

### What's Working
- [x] User registration & login with JWT auth
- [x] Group creation with geo-pinning
- [x] Event management (create, update, RSVP)
- [x] Interactive map (geocoding + MapLibre)
- [x] Real-time updates via Socket.IO
- [x] File uploads (S3/MinIO)
- [x] Security hardening
- [ ] Mobile app (planned)
- [ ] AI-powered event suggestions (planned)

## Architecture Philosophy

**Start Simple, Scale Smart**

As a solo founder, I'm not building Netflix on day one. This is designed to:
- Ship features fast without microservices complexity
- Debug easily when things break (they will)
- Scale when we actually have users
- Migrate to distributed systems when we have a team

It's a modular monolith — clean service boundaries, but one codebase. Much easier to reason about at 2 AM.

## Documentation

See [docs/](./docs/) for technical guides, security documentation, and project planning.

## License

MIT License — see [LICENSE](./LICENSE) for details.

## Contact

Built by [7onyx7](https://github.com/7onyx7)

- 📧 [bantrwrld@gmail.com](mailto:bantrwrld@gmail.com)

---

*The best app is the one you close to go hang out with friends IRL.* 🌱
