### Business Models and RecSys Topology
* Example of architecture by use case:
    - A streaming media platform, by contrast, serves a relatively static catalog of items to millions of largely independent users. This shifts the engineering focus entirely toward read-heavy memory cache designs, globally distributed edge-caching replicas, and ultra-fast item-retrieval layers where data updates can occur asynchronously.

* Summary
    - A platform's business model dictates its recommendation architecture:
        - Professional Networks: Require dense, write-heavy, bidirectional graph traversals.
        - Streaming Services: Need read-heavy, globally distributed edge caching for static catalogs.
        - Enterprise SaaS: Demand strict multi-tenant data isolation to prevent leaks.

### Analyzing Platform Constraints 
* Man this is a boring section. I don't care about designing SaaS B2B system

* Across all models there is still a consistent, multi-stage rec system pipeline 
    - the data substrates and latency/ isolation constraints where those pipeline steps operate changes 

### Mapping Domain Specific Caching and Graph Topologies
* 

