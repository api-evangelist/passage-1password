---
title: "Scaling security reviews at 1Password: Solving the context and nondeterminism problems"
url: "https://1password.com/blog/scaling-security-reviews-solving-context-and-nondeterminism"
date: "2026-07-30"
author: "info@1password.com (Megan Barker)"
feed_url: "https://1password.com/blog/index.xml"
---
In our last post , we shared how we began to scale our security code review process with SAGE. We discussed how we gathered historical Product Security (ProdSec) review records to create a 1Password-specific ruleset, the three-stage Finder/Critic/Judge pipeline, and the limitations of our v1 implementation. Above all, human ProdSec reviewers still had to bring full context to the findings: where the trust boundaries lie, which directories are sensitive, and whether mitigations exist elsewhere in the codebase.
