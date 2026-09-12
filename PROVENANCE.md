# Provenance and Attribution

## Dates and scope

The supplied workspace records an AI-assisted investigation beginning on 10 September 2026, followed by the completion, descent, transition, terminal-exit, core-factor and factor-classification notes dated 11 September 2026. This consolidation was prepared on 12 September 2026. These are the dates recorded in the materials and the consolidation session; they are not independently certified public priority timestamps.

The purpose of this archive is preservation, mathematical audit, reproducibility and a precise account of the unresolved frontier. It does not claim to prove the Erdős–Straus conjecture. No claim of global literature priority is made.

## AI assistance

The internal derivations, searches, verification programs and editorial consolidation were developed with AI assistance using ChatGPT/Codex. Statements are supported by explicit arguments and reproducible calculations rather than by the identity or confidence of an AI system. Independent human verification of the internal results is not documented in the supplied record. Independent verification is welcome; contacting an author or researcher is not a prerequisite for this archive, and no such contact was made as part of this task.

## Classical and external dependencies

- The divisor-square transformation and the underlying affine congruence family are classical. The relevant congruence parametrization is discussed in Thomas F. Bloom and Christian Elsholtz, *Egyptian fractions* (2022), particularly Theorem 1. [Author-hosted article](https://www.math.tugraz.at/~elsholtz/WWW/papers/bloom-elsholtz-naw5-2022-23-4-237.pdf). The consolidated note re-derives the identities and does not claim novelty for them.
- The comparison with ordinary QR saturation and the conditional source graph uses the CENTL public research notes [QR-saturating seeds](https://github.com/chasebryan/centl/blob/main/research/erdos-straus/QR-SATURATING-ROUTED-SEEDS.md) and [recursive character promotion](https://github.com/chasebryan/centl/blob/main/research/erdos-straus/RECURSIVE-CHARACTER-PROMOTION.md). The local classifier is preserved as a historical source snapshot. Its hash certifies the local content, not an inferred upstream commit. The `main` references are mutable. Imported graph premises are explicitly kept conditional.
- The totient-sum comparison is with Benjamin Dahan, arXiv:2608.24035v1, Lemma 4.22 and Section 7. [Versioned preprint](https://arxiv.org/html/2608.24035v1). The analytic proof in the archive is independent; no conclusion about the remainder of that preprint is required here.

Primary references were checked during consolidation for these limited attribution points. This is not an exhaustive prior-art review. A legacy reference to `SQUARE-COMPLETION-PRIOR-ART.md` in the public repository could not be retrieved in this session; no theorem in the consolidated archive relies on its unavailable contents. The working six residue classes are specified directly, so no scanned-PDF transcription of that list is used as a proof premise.

## Internal derivations and their status

The completion/defect argument, exceptional factor restriction, signed-state analysis, arithmetic regressions, normalized seven-factor classification and rational-divisor limitation are internal derivations in the supplied archive. Their proof and computation dependencies are enumerated in [RESEARCH_STATUS.md](RESEARCH_STATUS.md). They may be described as structural strengthenings relative to the audited public framework where that comparison is explicitly made. No broader novelty or priority assertion is warranted by this consolidation.

The finite graph censuses and bounded searches remain finite results. The seven-factor theorem is computation-assisted and range-free only within its proved universe. The rational-divisor theorem is supported by an algebraic argument; the complement samples are checks of the construction, not proof of rigidity. The totient asymptotic is proved using absolute convergence and dominated convergence, not numerical fitting.

## Preservation and version resolution

All 77 files present before consolidation were inventoried by relative path, size and SHA-256. Every original remains in place, including older ZIP archives and generated caches. All 69 research text, code and data files have byte-identical snapshots under `sources/workspace/`; no old README, proof, verifier or log was overwritten. The historical Chinese translation baseline is retained in its original language as provenance; the new mathematical exposition is English.

The six-factor stage remains a historical finite scan. The current account uses the later proof and verifier establishing seven factors, including 4933. Earlier factor-43 examples remain in the record, with their later affine exits added in the consolidated account. The replacement terminal is distinguished from them by its actual factors. Detailed resolutions appear in [INTEGRATION_LOG.md](INTEGRATION_LOG.md).

No new mathematical search was initiated during consolidation. The task was to read, audit, reconcile, verify and delimit the existing record. No claim that an AI proved the conjecture is made.
