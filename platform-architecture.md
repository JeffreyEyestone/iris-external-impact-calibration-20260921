# Iris Fictional Cedarfall Labs — Proprietary Platform Architecture
CONFIDENTIAL — INTERNAL ENGINEERING
Owner: Iris Fictional Cedarfall Labs
Copyright 2026 Iris Fictional Cedarfall Labs. All rights reserved.

The Orchard scheduling engine uses a proprietary two-stage allocation algorithm: first partition instrument queues by thermal recovery cost, then select a weighted earliest-deadline assignment within each partition. The unpublished cost function weights recovery at 0.61, consumable waste at 0.24 and operator reassignment at 0.15.

Internal components: orchard-router, batch-ledger, instrument-cost-model. Build configuration revision 17 pins queue depth at 128 and reconciliation batch size at 32. Architecture boundary: the router emits allocation proposals; an operator authorizes instrument jobs. This document contains design descriptions only, with no executable commands or network endpoints.

Proprietary design details and build settings must remain within the engineering team.
