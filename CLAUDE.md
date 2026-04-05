# Emily Summer Trip Dashboard

## Overview
Interactive travel dashboard for Emily's 22-day European summer trip (Jun 3-25, 2026). Password-protected, hosted on GitHub Pages. Midnight Aurora dark theme matching the Melissa summer-trip dashboard style.

## Repository
- **Path**: `/Users/aaxis/Documents/GitHub/emily-summer`
- **Remote**: `https://github.com/djctwo/emily-summer` (public, branch: main)
- **Live URL**: `https://djctwo.github.io/emily-summer/`
- **Password**: SHA-256 hashed (`emilysummer123!@#`), sessionStorage persistence
- **Launcher**: `~/Applications/Dashboards/Emily Summer.app`

## Traveler
- **Emily Elizabeth Cleary**, 15 years old, from Las Vegas
- **Dad (Doug)** lives in Kaiserslautern, Germany — works weekdays, free weekends
- **Interests**: museums, shopping, beach, city, food tours, adventure, riding trains

## Trip Structure
- **Jun 3**: Travel LAS→BOS→FRA (JetBlue B6478 + Condor DE2039, booking 15635316-02)
- **Jun 4-5**: Arrival & KL settling in
- **Jun 6-7**: Weekend 1 — Paris by TGV (suggested)
- **Jun 8-13**: Explorer week (KL solo activities + Rhine Valley day trip Sat)
- **Jun 14-18**: Athens, Greece (SKY express, confirmation FX4K8A, Acropolis Muses apartment booking 5392664665)
- **Jun 19**: Recovery day
- **Jun 20-22**: Düsseldorf (Japantown, Spanish restaurants, sightseeing; Bad Bunny concert Sun night NOT shown)
- **Jun 23-24**: Final KL days
- **Jun 25**: Departure FRA→LAS direct (Condor DE2062, seat 20A)

## Dashboard Structure
- **File**: `index.html` — single-file HTML, ~2940 lines
- **Theme**: Midnight Aurora with warm amber tints (blue/purple/cyan gradients + gold accents, frosted glass panels, backdrop blur) — matches summer-trip dashboard
- **Tabs**: Itinerary, Athens, Düsseldorf, Weekend Trips, KL Solo Guide, Travel Info
- **Mobile nav**: Fixed bottom tab bar (Itinerary, Athens, Düsseldorf, Info) on screens < 768px, desktop tab bar hidden
- **Stats**: Compact stats strip (22 Days / 3 Countries / 6 Flights / 4 Cities / 1 Island Cruise)
- **Map**: Leaflet.js with dark tiles, custom emoji divIcon markers for all destinations + day trip ideas
- **Countdown timer**: Gradient pill badge with border
- **Collapsible sections**: Weather & Destinations on itinerary tab; Travel Info tab has 4 collapsible groups (Flights & Accommodation, Prep & Packing, Emergency & Language, Restaurants & Photo Spots)
- **Interactive features**: Packing checklist (30 items, localStorage), booking progress tracker (12 items, localStorage), share/copy itinerary button
- **PWA**: apple-mobile-web-app meta tags, inline base64 manifest, SVG emoji favicon

## Features Added (from summer-trip parity)
- Trip timeline bar (color-coded day segments with hover expand)
- Weather cards (4 cities: KL, Paris, Athens, Düsseldorf)
- Destination cards (5 destinations with emoji heroes)
- Visual flight cards (airport codes + arrow + times)
- Overnights row (KL x14, Paris x1, Athens x4, Düsseldorf x2, In-flight x1)
- Day tags (drive, train, flight, food, landmark, beach, chill, boat, shopping, country)
- Overnight badges on key day cards
- Emergency grid (numbers, addresses, embassies across 3 columns)
- Language cheat sheet (Greek + German side-by-side)
- Booking progress panel (12 items with priority badges: Booked/Urgent/Soon/Later)
- Quick Book links (Booking.com, Skyscanner, GetYourGuide, DB, Rome2Rio, Google Maps)
- Restaurant wishlist (6 cards: Kostas, A for Athens, Lukumades, Takumi, Bakery My Heart, Ladurée)
- Photo spots (6 cards with best times: Areopagus, Lycabettus, Anafiotika, Trocadéro, Sacré-Cœur, MedienHafen)
- Print styles (white background, hide map/timeline, expand all collapsibles)

## Design Critique History
- **Initial score**: 23/40 (Acceptable) — scored 2025-04-05
- **Issues fixed**: Travel Info overload (collapsible sections), itinerary top-heaviness (compact strip + collapsible weather/destinations), no mobile nav (bottom tab bar added), text contrast (bumped to WCAG AA), cold aesthetic (warm amber tints), checkbox affordance (visible backgrounds + hover), copy deduplication (Explorer Week solo days)
- **Rollback tag**: `pre-critique-fixes` — tag before batch design changes

## Key Design Decisions
- No prices shown anywhere (user requirement)
- Bad Bunny concert (Jun 21 Sun night in Düsseldorf) NOT mentioned (Emily not attending)
- Solo weekdays: KL-only activities (no solo day trips outside KL — she's 15)
- Athens tab: 20 Wikimedia Commons images + Google Images links on all 27 attraction names
- Weekend Trips tab: 10 train-accessible destinations from KL (Paris, Amsterdam, Heidelberg, Cologne, Strasbourg, Rhine Valley, Luxembourg, Bruges, Black Forest, Swiss Alps)
- Password gate: SHA-256 via Web Crypto API, sessionStorage persistence
- Midnight Aurora theme kept intentionally to match summer-trip sibling dashboard

## Conventions
- Update CLAUDE.md and Session_History continuously throughout sessions
- All session notes in `Session_History/`
- No prices in any content
