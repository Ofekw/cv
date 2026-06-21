---

name: Ofek Wittenberg
title: Principal Software Engineer
tagline: Xbox · Leading the design and build of the next generation of gaming.
location: Seattle, WA
email: job@ofek.io
linkedin: https://www.linkedin.com/in/ofekw
github: https://github.com/Ofekw

---

## Summary

Over a decade building distributed systems and cloud platforms across gaming, productivity, healthcare, and fintech. My specialty is high-throughput, low-latency backend: services that scale past a million requests per second while holding strong consistency, and the cloud migrations that get them there with zero downtime. I lead and mentor engineers to deliver complex platforms across teams.

## Experience

### Microsoft · 2017 – Present

#### Xbox Platform Services · Senior to Principal Software Engineer · 2023 – Present

- Tech lead for the next-generation Xbox console platform. Architected the ground-up rewrite and cloud migration of the System & Content Update Service, a tier-0 system serving every Xbox client, onto roughly 400 Kubernetes pods across 5 clusters in 3 regions on Cosmos DB.
- Designed a novel in-memory cache that holds strong consistency past a million requests per second, a guarantee rarely attempted at this scale. The auth hot path answers sub-millisecond (0.145 ms at p50); client calls fell from 250 ms to 20 ms, at a 95% cache hit rate.
- Delivered the cutover with zero downtime and no client changes across tens of millions of consoles and PCs, shadowing live traffic and comparing responses to de-risk every step.
- Diagnosed and fixed a memory leak in the Azure Cosmos DB .NET SDK, making a core query path about 100x faster for every Cosmos customer.

#### Xbox Cloud Gaming (xCloud) · Intermediate Software Engineer to Senior · 2020 – 2023

- Joined as one of xCloud's earliest engineers and set its architectural foundation, pioneering the microservices platform, Kubernetes adoption, and a cloud-first design.
- Owned the authentication service, xCloud's highest-throughput service at around 1,000 RPS, and built its game-server routing from scratch across 21 regions: Anycast HTTPS termination, a DNS/ASN map of the internet, and latency-based routing to the closest servers.
- Grew into a technical leader as the platform scaled, mentoring engineers and guiding implementation of core services across the team.

#### Office 365 Systems Engineering · Software Engineer · 2017 – 2020

- A core engineer migrating Office 365 from legacy source control to Git and Azure DevOps, modernizing engineering systems and dev flows for 3,000+ engineers; presented the new processes to audiences of 1,000+.
- Modernized the functional-test infrastructure orchestrating 10,000+ VMs for all Office pull-request gating, one of the most complex workflow engines in the company.

### Centrality.ai · Software Engineer · Contract · 2017

*Auckland, New Zealand*

- Full-stack delivery on a blockchain platform: built a data-migration system and integrated a secure payments and billing pipeline handling sensitive customer data.

### Orion Health · Software Engineer · 2014 – 2016

*Auckland, New Zealand*

- Built enterprise Java web applications powering all hospitals in Australia and New Zealand.

## Ventures & Selected Projects

### TouchPhone · Co-founder & Lead Engineer · 2011 – 2013

*Mobile hardware startup · Oceania*

- Co-founded a hardware and software startup at 17, building proprietary GSM firmware that turned iPod Touches into fully-functional phones. Sold 10,000+ units across Oceania; acquired in 2013 by a European buyer who scaled the product across Europe.

### Smart-Contract Security & DeFi Engineering · Independent

*Security research & DeFi automation*

- Designed and operated an automated suite of DeFi services and a smart-contract auditing and static-analysis toolchain. Used it to uncover exploits in malicious contracts and publicly flag multiple rug-pull projects, helping the community avoid millions in losses.

## Education

### University of Auckland · BE (Hons), Computer Software Engineering · 2013 – 2016

*First Class Honours*

- **Top Engineering Honours Project:** placed 1st overall in the engineering cohort; research published at an ACM conference (*WiSurr*: synchronized, ad-hoc audio broadcast across mobile devices over arbitrary networks).

## Expertise

- **Distributed systems at scale:** hyperscale, high-throughput, low-latency services; distributed caching; distributed and NoSQL databases.
- **Cloud & platform:** Azure, Kubernetes, microservices, cloud-first platform design, zero-downtime migrations.
- **Delivery & reliability:** client and hardware integration, SLA-driven operations, authentication, network routing.
- **Leadership:** technical leadership and mentoring; leading teams of engineers to land complex, cross-team initiatives.