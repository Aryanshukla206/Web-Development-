# Web-Development-Projects
Welcome to my web development journey! 🚀 This repository showcases a collection of my projects .
<hr>
<h1>Project 1 : Country Flags with Hover Effect</h1>
<br>
<h2>Description</h2>
A simple HTML and CSS project that displays flags of different countries with a stylish hover effect. Perfect for showcasing CSS skills and attention to detail.
<br>
<h2>Technologies Used</h2>
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>
<br>
<h2>Features</h2>
<ul>
  <li>Flags of various countries</li>
  <li>Smooth hover effects to highlight each flag</li>
</ul>
<br>
<h2>How to View</h2>
<br>
  Simply open the <a href="https://github.com/Aryanshukla206/Web-Development-/blob/main/index.html">index.html</a> file in your browser to see the flags in action.
<hr>

```mermaid
flowchart LR
  subgraph Clients
    A[Web Client]
    B[Mobile Client]
  end

  subgraph Infra
    PM[Process Manager / Orchestration<br/>(PM2 / Kubernetes)]
    LB[Load Balancer]
  end

  subgraph Server["API Server (app)"]
    HTTP[HTTP Server<br/>(createServer(app))]
    Socket[SocketService<br/>(WebSocket / Socket.IO)]
    Routes[API Routes<br/>(initializeApiRoutes)]
  end

  subgraph Services["Application Services"]
    DB[MongoDBService<br/>(MongoDB)]
    Entity[EntitySportsService<br/>(provider worker)]
    Updater[CricketDataUpdaterService<br/>(update mode)]
    Shorts[ShortsServices<br/>(YouTube shorts sync)]
    Logger[Logger / Error Reporting<br/>(Sentry / Datadog)]
  end

  subgraph External["External Systems"]
    CricketAPIs[Cricket Data Providers / RSS / APIs]
    YouTube[YouTube Data APIs]
    ThirdPartyAuth[Auth / OAuth / Payment (optional)]
  end

  %% Client -> LB -> HTTP
  A -->|HTTPS| LB
  B -->|HTTPS| LB
  LB --> HTTP

  %% HTTP internals
  HTTP --> Routes
  HTTP --> Socket
  Routes --> DB
  Socket --> DB
  Socket --> A
  Socket --> B

  %% Services interactions
  Entity -->|writes/updates| DB
  Updater -->|writes/updates| DB
  Shorts -->|writes/updates| DB
  Updater -->|fetches from| CricketAPIs
  Entity -->|ingests from| CricketAPIs
  Shorts -->|fetches from| YouTube

  %% Logging & monitoring
  HTTP --> Logger
  Entity --> Logger
  Updater --> Logger

  %% Orchestration
  PM --> LB
  PM --> Entity
  PM --> Updater
  PM --> HTTP

  %% Legend (optional)
  classDef infra fill:#f8f9fa,stroke:#bbb;
  class Infra,Server,Services,External infra;


```
