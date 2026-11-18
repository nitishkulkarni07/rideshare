# RideShare — Route-Based Carpooling

RideShare is a driver-first carpooling application with GPS-based matching, fare estimates, ride tracking, and RideTrust audit features.

## Deployment status

- Supabase project: `ebnkhhnjrsgryezlxvjz` — database tables created and RLS enabled.
- Vercel project: `rasna3/rideshare-carpooling` — created, not deployed.
- Application source must be uploaded before deployment.
- The existing C++/SQLite backend **has not yet been migrated** to the Supabase PostgreSQL database. A frontend-only deployment cannot provide working login or booking.

## Repository layout after source upload

- `frontend/`: React/Vite web application
- `backend/`: current Windows C++ backend, for migration
- `supabase/`: PostgreSQL schema / migrations
- `tests/`: integration tests

Do not commit `.env`, database passwords, API secrets, or local SQLite files. Online payment flows are demos, not actual payment gateway transactions.
