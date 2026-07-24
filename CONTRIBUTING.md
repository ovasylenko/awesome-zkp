# Contributing to Awesome ZKP

Thank you for helping keep this list useful. Awesome ZKP is curated rather than exhaustive: an entry should save readers time, expose an important trade-off, or provide a clearly better source than what is already listed.

Participation is governed by the repository's [Code of Conduct](CODE_OF_CONDUCT.md).

## Before You Submit

1. Search the README for the resource, project, and canonical URL.
2. Read the most specific existing section and explain what the addition contributes that is not already covered.
3. Prefer an official specification, documentation site, standards body, paper, or source repository over a secondary article.
4. Confirm that the link is active and that the description matches the linked source today.
5. Check the project's license, latest meaningful release or update, security policy, audits, and current network or product status.

Do not submit affiliate links, referral links, press-release rewrites, token promotion, generic company homepages when technical documentation exists, or abandoned projects without enduring historical value.

## Entry Format

Use one concise sentence that explains why the resource is useful:

```markdown
- [Resource Name](https://example.com/) - What it provides and the reader or problem it serves.
```

Descriptions should end with a period. Avoid unsupported superlatives such as “fastest,” “first,” “production-grade,” or “10x” unless the primary source defines the comparison and methodology.

## Lifecycle Labels

Use a label only when an official source states it:

- **Research:** paper, prototype, or experimental implementation.
- **Alpha:** incomplete or explicitly not production-ready.
- **Beta:** public testing with possible breaking changes.
- **Production:** officially supported for production use; this is not an independent security endorsement.
- **LTS:** maintenance and security support without active feature development.
- **Historical:** sunset, archived, or retained for lasting technical significance.

If the official status is unclear, leave the entry unlabeled and state the uncertainty in the pull request. Never infer production readiness from mainnet deployment, GitHub activity, funding, or marketing language.

## Required Pull Request Evidence

GitHub loads the repository's pull request template automatically. Complete every field rather than deleting sections that do not apply; use “Not applicable” with a short reason. The template records source provenance, lifecycle and audit evidence, the resource's distinct value, its zero-knowledge mode, and the contributor's verification checks.

## Reviewing Technical Claims

For proof systems and libraries, identify the arithmetization, commitment scheme, setup model, supported fields or curves, security assumptions, and zero-knowledge mode where relevant.

For benchmarks, require the exact version or commit, security parameters, workload, proof mode, hardware, thread count, accelerators, peak memory, proof size, verifier environment, and whether setup or compilation time is included. Results without enough information to reproduce or compare should not be summarized as rankings.

For applications and infrastructure, verify supported networks, verification-key management, trusted setup provenance, audit status, upgrade authority, data availability, and whether guarantees are cryptographic, crypto-economic, or operational.

## Pull Request Scope

Keep each pull request focused. A single resource or one coherent category is easier to verify than a large mixed batch. Update documentation in the same pull request as any taxonomy or policy change.

All contributions are made available under the repository's [CC0 1.0 Universal dedication](LICENSE).
