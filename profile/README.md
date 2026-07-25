<p align="center">
  <img src="./assets/wordmark.png" alt="Covenant" width="600" />
</p>

Open infrastructure for agent-native computing.

Covenant provides the state, authority, continuity, and accountability layer
for long-running software agents: scoped capabilities, durable memory, runtime
control, append-only audit, commit-scoped provenance, and settlement evidence.

## Projects

| Project                                                           | Purpose                                                                                                    |
| ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| [covenant](https://github.com/open-covenant/covenant)             | Agent-native control plane, daemon, capabilities, memory, runtime, audit, provenance, SDKs, and settlement |
| [covenant-hyre](https://github.com/open-covenant/covenant-hyre)   | Hyre and x402 integration for metered agent services and delivery evidence                                 |
| [covenant-skill](https://github.com/open-covenant/covenant-skill) | Agent skill for using Covenant's verifiable execution and settlement surfaces                              |

## Incubator

[Covenant Timeline](https://github.com/open-covenant/covenant-timeline) is a
pre-alpha temporal-contract format and verifier for long-running agent and
software work. It replays checkpoint decisions from pinned policy and evidence,
then joins effect requests to receipts.

Timeline is being developed as a standalone portable protocol with Covenant as
its first reference adopter. It is not a distributed workflow runtime, a
universal scoring system, or a production authorization service.

```mermaid
flowchart LR
    operator["Human or agent"] --> skill["covenant-skill"]
    skill --> core["Covenant control plane"]
    timeline["Timeline incubator"] -. evidence and decisions .-> core
    core --> runtime["Runtime, memory and capabilities"]
    core --> evidence["Audit and provenance"]
    core --> settlement["Receipts and settlement"]
    core --> hyre["covenant-hyre"]
```

## Current status

Covenant is alpha infrastructure. Its local control plane, capability lifecycle,
memory, audit, provenance, SDK, and several settlement surfaces are implemented
and tested. Production-grade isolation for hostile agent code, networked
multi-peer operation, and the complete daemon-driven economic lifecycle remain
active work.

Covenant Timeline is pre-alpha. Its TypeScript prototype validates temporal
contracts and replays evidence, checkpoint decisions, commands, and receipts.
Canonical byte identity, persistent adapters, a complete CLI, Covenant
integration, and independent interoperability remain active work.

Repository-specific READMEs and security documents define the exact boundary
for each project.

## Participate

- Start with the [Covenant architecture](https://github.com/open-covenant/covenant#architecture).
- Review the [Covenant Timeline program](https://github.com/open-covenant/covenant-timeline/blob/main/PROGRAM.md).
- Open focused issues and proposals in the relevant repository.
- Report vulnerabilities through the affected repository's private
  vulnerability-reporting channel. Do not open public security issues.

Website: [opencovenant.org](https://opencovenant.org)

Documentation: [docs.opencovenant.org](https://docs.opencovenant.org)
