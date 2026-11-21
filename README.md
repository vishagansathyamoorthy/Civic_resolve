# CivicResolve: AI-Powered Civic Issue Platform

**Live demo:** https://vishagansathyamoorthy.github.io/Civic_resolve/

CivicResolve lets citizens report local problems (potholes, overflowing garbage, water pipe bursts, broken streetlights, sewage overflow) with a photo and GPS location. AI classifies each issue, sets its priority and routes it to the right department. Municipal admins track deadlines, view analytics, dispatch crews and verify fixes with after-photos.

## Features

- **Easy reporting:** title, description, photo upload, and automatic location through browser GPS or a draggable pin on a live map (Leaflet + OpenStreetMap). No API key is needed for location.
- **Multilingual input:** write in a regional language and see a live English translation.
- **AI triage:** Google Gemini classifies the category, assigns the department, scores public-safety risk and checks that the photo matches the description. A built-in local engine does the same offline, so the app works without a key.
- **Smart duplicate merging:** repeat reports of the same nearby issue are merged and show how many citizens are affected.
- **Priority and SLA:** Critical, High, Medium and Low priorities with target hours, overdue flags and automatic escalation.
- **Admin mode (PIN protected):** analytics by category, SLA performance chart, hotspot map, and AI strategic suggestions.
- **Dispatch tools:** send work orders to the nodal officer by WhatsApp, email or a simulated call, and print official work orders.
- **Fix verification:** upload an after-photo and Gemini Vision checks that the problem is really resolved.
- **Data export:** export complaints as a spreadsheet file.

## Tech stack

HTML, CSS and JavaScript in a single file, Leaflet and OpenStreetMap for maps, Google Gemini API (optional), browser Geolocation API.

## Setup

1. Clone the repo: git clone https://github.com/vishagansathyamoorthy/Civic_resolve.git
2. Open the folder and run a local server (browser location needs localhost or https): python -m http.server 8000
3. Open http://localhost:8000
4. Optional: open "Google Gemini API Key Settings" on the report page and paste a key from Google AI Studio (https://aistudio.google.com/apikey). The key stays in your browser and is never saved or committed. Without it, the local AI engine is used.
5. Admin mode: use the role toggle at the top and enter the demo PIN 1234.

## Notes

- Complaints are stored in the browser for this demo.
- The Gemini key is entered by the user at runtime, so no secrets are in this repository.
