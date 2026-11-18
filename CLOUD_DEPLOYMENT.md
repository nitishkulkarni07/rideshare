# RideShare Cloud Pilot

This frontend is a React/Vite adaptation of RideShare, using Supabase PostgreSQL and Auth instead of the existing local Windows C++ server. It is a pilot, not an exact copy of the Windows interface.

Features: customer/driver sign-up, route map and GPS, OSRM estimated routes, fare estimates, passenger requests, on-route priority matching (simple geographic corridor), accept/start/complete rides, cash confirmation, rating and audit history. Online payments are demonstrations only. Automatic GPS-based completion and full curved-road matching are not implemented in this pilot.

Existing local C++/SQLite code remains separately available in the previously provided project ZIP. See README for project overview.
