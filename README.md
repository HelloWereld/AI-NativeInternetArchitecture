Network Working Group                                         A. Moolman
Internet-Draft                                           Independent
Intended status: Informational                            16 May 2025
Expires: 16 November 2025

              AI-Native Internet Architecture
               draft-arnomoolman-ienet-ai-stack-00

Abstract

   This document specifies an AI-natively optimized Internet architecture,
   introducing new protocols and extensions across the transport, session,
   presentation, and application layers to enable seamless discovery,
   routing, compute offload, and secure model invocation. It defines the
   TIP container format, ModelRPC handshake, Tensor-QUIC (T-QUIC)
   transport extension, and associated discovery and trust mechanisms.

Status of This Memo

   This Internet-Draft is submitted in full conformance with the
   provisions of BCP 78 and BCP 79.

   Internet-Drafts are working documents of the Internet Engineering
   Task Force (IETF). Note that other groups may also distribute
   working documents as Internet-Drafts. The list of current Internet-
   Drafts is at https://datatracker.ietf.org/drafts/current/.

   Internet-Drafts are draft documents valid for a maximum of six months
   and may be updated, replaced, or obsoleted by other documents at any
   time. It is inappropriate to use Internet-Drafts as reference
   material or to cite them other than as "work in progress."

   This Internet-Draft will expire on 16 November 2025.

Copyright Notice

   Copyright (c) 2025 IETF Trust and the persons identified as the
   document authors. All rights reserved.

   This document is subject to BCP 78 and the IETF Trust's Legal
   Provisions Relating to IETF Documents
   (https://trustee.ietf.org/license-info) in effect on the date of
   publication of this document. Please review these documents
   carefully, as they describe your rights and restrictions with respect
   to this document.

1.  Introduction

   The increasing integration of artificial intelligence into online
   services demands a native adaptation of the Internet architecture.
   This document introduces core design principles and protocol
   extensions tailored for AI-native communication and computation.

2.  TIP Container Format

   TIP (Tensor Internet Package) is a structured container optimized for
   the transport of AI workloads. It encapsulates model inputs,
   execution contexts, priority metadata, and result expectations in a
   compact format, designed to be compatible with streaming and caching
   mechanisms.

3.  ModelRPC Handshake

   ModelRPC is a new session-layer protocol enabling clients to discover,
   negotiate, and invoke remote AI models. It incorporates trust
   assertions, model version negotiation, privacy guarantees, and
   resource quotas into a structured handshake mechanism.

4.  Tensor-QUIC (T-QUIC)

   T-QUIC is a transport-layer extension of QUIC with optimizations for
   tensor transmission. Enhancements include stream-level priority
   weights, model-centric congestion control, and GPU-aware forwarding
   hints to minimize latency and maximize compute locality.

5.  Discovery and Trust

   This architecture introduces a model discovery service built atop DNS
   extensions and a decentralized registry. Trust is managed via signed
   model manifests and audit trails ensuring reproducibility and
   transparency of model behaviors and weights.

6.  Security Considerations

   Special care is required for execution integrity, model poisoning
   mitigation, and federated trust anchors. TIP and ModelRPC include
   cryptographic signature enforcement and privacy-preserving model
   selection mechanisms.

7.  IANA Considerations

   This document requests the allocation of protocol numbers for TIP,
   ModelRPC, and T-QUIC from the appropriate IANA registries.

8.  Acknowledgments

   The author thanks the open research and developer communities advancing
   AI infrastructure and trust on the Internet.

Author's Address

   Arno Moolman
   Independent
   South Africa
   Email: arnomoolman@msn.com
