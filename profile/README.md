# LiventCord

LiventCord is an open-source, self-hosted real-time communication platform designed around a distributed system architecture. It provides messaging, guilds, media handling, and voice/video communication while keeping full control of infrastructure, data, and deployment in the hands of the operator.

The project is built as a multi-service system rather than a single monolithic application. Different components are responsible for API handling, realtime communication, media processing, edge services, and client interaction.

---

## System Overview

LiventCord is composed of several independent services that communicate through HTTP, WebSockets, Redis streams, and event-based messaging.

Core runtime components:

* **.NET Core API** – main application layer (auth, users, guilds, channels, permissions, messaging, persistence)
* **Go services** – realtime WebSocket gateway, media services, telemetry
* **Redis** – event streaming, pub/sub, caching, realtime propagation
* **Cloudflare Workers** – edge services, lightweight APIs, media and GIF services
* **Docker** – deployment and service orchestration

Supporting tooling:

* Python services and scripts for bots, crawlers, and automation
* Node/TypeScript for frontend tooling, workers, and build pipelines

---

## Functional Capabilities

* Real-time messaging (guilds, channels, DMs)
* Distributed event broadcasting via WebSockets and Redis
* Friend system and invitations
* Media upload, processing, preview, and proxying
* File storage and retrieval
* Voice and video signaling (WebRTC integration)
* Multi-client synchronization
* Edge-based APIs for media and auxiliary services

---

## Backend Architecture

### API Layer

* **.NET Core 8**

  * Authentication and identity
  * Guild, channel, and permission systems
  * Messaging and metadata
  * File and media endpoints
  * Database abstraction via EF Core

### Realtime Layer

* **Go WebSocket API**

  * Connection management
  * Room/channel session handling
  * Presence, typing, and status events
  * Redis-backed event propagation

### Media Services

* **Go media services**

  * Media scraping
  * Metadata extraction
  * Thumbnail generation
  * Storage handling

### Edge Services

* **Cloudflare Workers**

  * Media APIs
  * GIF service
  * Hit logging
  * Lightweight edge endpoints

---

## Frontend

The client is a full real-time application, It handles:

* WebSocket communication
* realtime event processing
* client-side state management
* optimistic updates
* media rendering
* voice/video integration

Tech stack:

* Vue + Vite + TypeScript
* WebRTC
* WebSocket-based event model
* Modular state and UI architecture

---

## Data Layer

Entity Framework Core is used for persistence, with support for multiple databases:

* PostgreSQL
* MySQL
* MariaDB
* SQL Server
* SQLite
* Oracle
* Firebird

---

## Deployment Model

* Containerized services (Docker)
* Multi-service orchestration
* Independent scaling of API, realtime, and media layers
* Edge services deployed separately via Cloudflare Workers

---

## Design Principles

* Service separation instead of monolith design
* Event-driven realtime architecture
* Infrastructure ownership
* Self-hosted by default
* No dependency on third-party platforms for core functionality

---

## Contributing

Contributions are welcome.

---

## License

GNU General Public License v3.0
