---

name: Ofek Wittenberg
title: Principal Software Engineer
tagline: Principal Software Engineer @ Xbox · Leading, designing and building the next generation of gaming.
location: Seattle, WA
email: job@ofek.io
linkedin: https://www.linkedin.com/in/ofekw
github: https://github.com/Ofekw

---

## Summary

Principal Software Engineer with over a decade building distributed systems and cloud platforms across gaming, productivity, healthcare, and fintech. My specialty is high-throughput, low-latency backend: services that run at hundreds of thousands to millions of requests per second at single-digit-millisecond latency, the caching and consistency models that keep them correct under load, and the cloud migrations that get them there with zero downtime. I lead and mentor engineers and deliver complex platforms across many partner teams.

## Experience

### Microsoft

*2017 - Present · Seattle, WA · Remote*

#### Xbox Platform Services · Senior to Principal Software Engineer · 2023 - Present

- Tech lead driving the design and implementation of the foundational platform services powering the next generation of Xbox console, owning the architecture and guiding a team of engineers through delivery.
- Architected the ground-up rewrite and on-prem to cloud migration of the System & Content Update Service, one of the most foundational services powering all of Xbox across PC, console, Cloud Gaming, and internal systems (including Xbox authentication), re-platforming from on-prem hosts to distributed Kubernetes pods backed by a distributed datastore.
- Designed a novel in-memory caching layer that preserves strong consistency at \~80K RPS with headroom beyond 1M RPS, a guarantee rarely held at this scale; auth-sensitive APIs respond in under 5 ms and client calls average under 50 ms.
- Delivered the migration with zero downtime and no required client changes, coordinating execution across many partner teams.

#### Xbox Cloud Gaming (xCloud) · Intermediate Software Engineer to Senior · 2020 - 2023

- Joined as one of xCloud's earliest engineers and set its architectural foundation, pioneering the microservices platform, Kubernetes adoption, and a cloud-first design.
- Owned the authentication service (one of xCloud's highest-throughput services) and designed its global game-server routing from scratch: Anycast HTTPS termination, a DNS/ASN map of the internet, and performance-based routing so players reach the closest, best-quality servers.
- Grew into a technical leader as the platform scaled, mentoring engineers and guiding implementation of core services across the team.

#### Office 365 Systems Engineering · Software Engineer · 2017 - 2020 · Vancouver, BC

- A core engineer migrating Office 365 from legacy source control to Git and Azure DevOps, modernizing engineering systems and dev flows for 3,000+ engineers; presented the new processes to audiences of 1,000+.
- Modernized the functional-test infrastructure orchestrating 10,000+ VMs for all Office pull-request gating, one of the most complex workflow engines in the company.

### Centrality.AI · Software Engineer (Contract)

*Auckland, New Zealand · 2017*

- Full-stack delivery on a blockchain platform: built a data-migration system and integrated a secure payments and billing pipeline handling sensitive customer data.

### Orion Health · Software Engineer

*Auckland, New Zealand · 2014 - 2016*

- Built enterprise Java web applications powering all hospitals in Australia and New Zealand.

## Ventures & Selected Projects

### TouchPhone · Co-founder & Lead Engineer · 2011 - 2013

- Co-founded a hardware and software startup at 17, building proprietary GSM firmware that turned iPod Touches into fully-functional phones. Sold 10,000+ units across Oceania; acquired in 2013 by a European buyer who scaled the product across Europe.

### Smart-Contract Security & DeFi Engineering · Independent

- Designed and operated an automated suite of DeFi services and a smart-contract auditing and static-analysis toolchain. Used it to uncover exploits in malicious contracts and publicly flag multiple rug-pull projects, helping the community avoid millions in losses.

## Education

### University of Auckland · BE (Hons), Computer Software Engineering

*First Class Honours · 2013 - 2016*

- **Top Engineering Honours Project:** placed 1st overall in the engineering cohort; research published at an ACM conference (*WiSurr*: synchronized, ad-hoc audio broadcast across mobile devices over arbitrary networks).

## Expertise

- **Distributed systems at scale:** hyperscale, high-throughput, low-latency services; distributed caching; distributed and NoSQL databases.
- **Cloud & platform:** Azure, Kubernetes, microservices, cloud-first platform design, zero-downtime migrations.
- **Delivery & reliability:** client and hardware integration, SLA-driven operations, authentication, network routing.
- **Leadership:** technical leadership and mentoring; leading teams of engineers to land complex, cross-team initiatives.