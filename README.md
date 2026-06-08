# Fan Engagement — Azure Cloud & AI Reference Simulator

An **architectural "art of the possible" prototype**: a **Major League Sports fan-engagement**
platform — showcased here with the NBA — rendered as an **Xcode-style device simulator**. Pick a device (iPhone / iPad / Apple
Watch / Web), navigate the fan app in the center, and watch the **Microsoft Azure reference
architecture light up 360° around it** — every screen "activates the brain," pulsing the exact
Azure services that power it and explaining *why*.

> ⚠️ **Prototype to showcase Microsoft Azure Cloud & AI reference architecture.**
> Not affiliated with, endorsed by, or sponsored by the NBA or any of its teams or players.
> Team names and player names are used illustratively for an educational architecture demo.

## The idea

Two lenses at once:

- **Front of house** — a companion fan app. *At home* it's a second screen to the big TV;
  *at the venue* it's a pre/during/post-game concierge.
- **Under the hood** — as you tap through modules, the surrounding architecture animates to
  show which Azure tiers and services are engaged, with a live "brain panel" rationale.

## Use cases modeled

Onboarding (team + favorite player → Fan 360) · For-You feed · **Live game with Favorite-Player
POV** · live stats & win-probability · trivia & team history (RAG) · AI auto-highlights · where-to-watch
concierge (Peacock/Prime/League Pass) · merch & digital memorabilia · tickets & smart-venue wayfinding ·
responsible sports betting · social watch parties · athlete local events · **Memory Lane** (games you
attended).

## Architecture tiers (from the reference)

| Tier | Services |
|------|----------|
| 0 · Fan Clients | Web / iOS / Android, Web PubSub + SignalR |
| 1 · Edge & Identity | Front Door + WAF, DDoS, Entra External ID, API Management |
| 2–3 · App & Channels | App Service / AKS, Azure CDN, media-partner encode, Dynamics 365 Commerce, Azure Maps |
| 4 · AI Office Core | Azure OpenAI / AI Foundry, Azure AI Search, Azure ML, AI Video Indexer |
| 5 · Data & Analytics | Microsoft Fabric (Fan 360), Event Hubs, Stream Analytics, Cosmos DB / Azure SQL, Data Lake |
| Cross-cutting | Defender for Cloud, Sentinel, Purview, Key Vault |

**Currency notes:** Azure Media Services is retired (live encode runs via a media partner on Azure;
AI Video Indexer does the video AI). Azure Personalizer is retiring — recommendations run on Azure ML.

## Run

It's a single self-contained `index.html` — open it, or visit the GitHub Pages site. No build step.

---
Built as a Technical-PM upskilling sandbox for applied Cloud & AI.
