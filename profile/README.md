## Welcome!

This collection of repositories is owned by [Joseph Melberg](https://github.com/Joseph-Melberg) for the purpose of ongoing practice in software architecting and development.

## Plane Domain

```mermaid
graph TD;
    Data==>Inter.PlaneWrangler;
    Inter.Metronome --> | Each second | Inter.PlaneWrangler;
    Inter.Metronome --> | Each minute | Inter.PlaneIndexer;
    Inter.PlaneWrangler--> |Position Data| Inter.Proxy;
    Inter.PlaneIndexer --> |History Data| Inter.Proxy; 
    Inter.PlaneWrangler==> |Position Data| Inter.PlaneIndexer;
```

More information on each service is available in their respective repository, linked below.

|Service Name| Description |
|-|-|
|[Inter.Metronome](https://github.com/InterMW/Inter.Metronome)| A service for triggering other services.|
|[Inter.PlaneWrangler](https://github.com/InterMW/Inter.PlaneWrangler)| A service for combining incoming data and providing current position data for consumption.|
|[Inter.PlaneIndexer](https://github.com/InterMW/Inter.PlaneIndexer) | A service providing past position data for consumption.|
|[Inter.Proxy](https://github.com/InterMW/Inter.Proxy)| A service that provides external access to the web api's of the other services.|

# Planned Domains
## Device Domain

```mermaid
graph TD;
    Data ==> Inter.Usage;
    Data ==> Inter.Thermometer;
```

## Utility Domain

```mermaid
graph TD;
    Source ==> |Some message | Service;
    Service ==> |Some message| Destination;
    Service --> |The time it took to perform the prompted action| Inter.Timer;

```
