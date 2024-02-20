## Welcome!

This organization is an ongoing practice in software architecting and development.

```mermaid
graph TD;
    Data==>Inter.PlaneWrangler;
    Inter.Metronome --> | Each second | Inter.PlaneWrangler;
    Inter.Metronome --> | Each minute | Inter.PlaneIndexer;
    Inter.PlaneWrangler--> |Position Data| PlaneViewer;
    Inter.PlaneIndexer --> |History Data| PlaneViewer;
    Inter.PlaneWrangler==> |Position Data| Inter.PlaneIndexer;
```
