# RideShare — Intelligent Route-Based Carpooling

**Cloud pilot live:** https://rideshare-carpooling-eight.vercel.app

RideShare is a driver-first carpooling app. Drivers share seats on trips they already plan to take; passengers choose pickup/drop GPS points, see a fare estimate, and request a compatible seat. Matching prioritizes forward-direction on-route stops, then nearby detours.

## Connected cloud services
- **Frontend**: React + Vite, deployed on Vercel under RASNA
- **GitHub**: https://github.com/nitishkulkarni07/rideshare
- **Database/Auth**: dedicated Supabase PostgreSQL project `ebnkhhnjrsgryezlxvjz`
- **Map/routing**: Leaflet/OpenStreetMap; OSRM demo routing with an estimated-distance fallback
- **Security**: Supabase Auth and RLS on six ride-related tables; server-validated booking/acceptance RPCs

## Run locally
```bash
cd frontend
npm install
npm run dev
```

## Current cloud features
Passenger / driver sign-up and login, interactive GPS map, distance and estimated fare, payment preference (demo only), driver journey publishing, on-route-first/nearby-second matching, driver acceptance, ride status, GPS updates while browser is active, manual completion with a reason, rating/feedback and ride audit download.

## Scope and limitations
This repository currently contains the **cloud-adapted pilot frontend**, **not the full original Windows C++/SQLite source**. The earlier Windows code remains in the RideShare ZIP shared in ChatGPT. This cloud pilot does not yet have:
- Verified automatic completion based on repeated destination GPS readings
- Road-polyline matching (current match server checks a straight-line corridor)
- Multiple simultaneous accepted passengers in one vehicle
- Real UPI, net banking or wallet payments
- Guaranteed GPS in the background or live-traffic optimized navigation
- Full end-to-end two-device verification

Build and static HTTP checks passed. Perform two-device authentication, trip, and persistence testing before accepting real customers.

## Deployment
Vercel project: https://vercel.com/rasna3/rideshare-carpooling
Project Root Directory: `frontend`; Build Command: `npm run build`; Output Directory: `dist`.
A production build was created from GitHub commit `b584e49`. A permanent Git integration for automatic deployments was not independently confirmed.
Do not put Supabase secret/service_role keys in frontend code.
