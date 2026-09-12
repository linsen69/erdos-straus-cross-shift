# Erdős–Straus Cross-Shift Research Archive

**Status: 12 September 2026. Erdős–Straus remains open.**

This archive consolidates the research records of 10–11 September 2026. It contains proved structural statements, a computation-assisted classification of a precisely defined affine family, explicit arithmetic certificates, and the remaining termination obligation. No claim of global literature priority is made.

## Problem

For prime $p$, seek positive integers $x,y,z$ satisfying

$$\frac4p=\frac1x+\frac1y+\frac1z.$$

At a shift $k\equiv3\pmod4$ with $\gcd(p,k)=1$, put $C_k=(p+k)/4$. The exact fixed-shift targets are

$$d\mid C_k^2,\quad4d\equiv-1\pmod k\quad\text{(Type I)},$$
$$d\mid C_k^2,\quad d\equiv-C_k\pmod k\quad\text{(Type II)}.$$

## What is proved

- **Completion and defect theory.** For a QR-supported seed $G\mid C_k$ at a prime shift, the involution $T_G(x)=G/(4x)$ extends ordinary QR saturation. Full completion makes a fixed-shift miss equivalent to QR-only prime support; its defect restricts possible NQR factors.
- **Exceptional branch.** On $p\equiv361\pmod{840}$, a negative-character miss at 31 has exactly $C_{31}=14\ell S$, where $\ell\equiv6\pmod{31}$ occurs once and every prime factor of $S$ is $1\pmod{31}$. Necessarily $p=2041+26040m$.
- **Local state structure.** Signed divisor sets grow monotonically; nonneutral transitions decrease a finite rank. The resulting core bound controls factor occurrences, and the finite graph is classified. Factor processing may still end at a miss with no factors left.
- **Complete affine factor classification.** The seven-factor theorem includes arbitrary composite trigger divisors. Rationally varying divisors add only divisor complements when the shift remains nonconstant affine and validity is uniform.
- **Separate analytic result.** The coprime totient sum has leading constant $9/(2\pi^2)$. This result does not settle termination.

Full hypotheses and proofs appear in [MASTER_PROOF.md](MASTER_PROOF.md); statement numbers run consecutively from 1 to 25. Exact finite enumerations are marked as computational components, separately from finite regressions.

## The seven-factor classification

Let $p=2041+26040m$ be an actual prime with a fixed-67 miss and $C=C_{67}=31(17+210m)$. Choose any divisor $D\mid C$, including a composite divisor. Consider a nonconstant affine shift and a fixed Type-II divisor valid for every sufficiently large integer member of the progression defined by

$$p'\equiv2041\pmod{26040},\qquad D\mid(p'+67)/4.$$

Such an exit exists for some $D$ **if and only if** one of these seven prime factors divides $C$:

$$11,\quad13,\quad41,\quad43,\quad433,\quad1933,\quad4933.$$

| actual factor $h$ | $s$ | $Q=sh$ | $u$ | $e$ | $v=u^2/e$ |
|---:|---:|---:|---:|---:|---:|
|11|1|11|3|3|3|
|13|3|39|10|20|5|
|41|7|287|72|27|192|
|43|5|215|54|6|486|
|433|3|1299|325|125|845|
|1933|3|5799|1450|500|4205|
|4933|3|14799|3700|1250|10952|

Each row gives $K=(p+4e)/Q$ and

$$\frac4p=\frac1{uK-e}+\frac1{pu}+\frac1{p(vK-u)}.$$

The underlying congruence identity is classical; see [Bloom–Elsholtz](https://www.math.tugraz.at/~elsholtz/WWW/papers/bloom-elsholtz-naw5-2022-23-4-237.pdf). The internal classification reduces all eligible divisors to an exact finite square-divisor enumeration. Its only additional surviving composite row is $319=11\cdot29$, already covered by 11. No independent extra congruence refinement is included in this universe.

## Most important obstruction

The actual prime

$$p_*=4742209557133801,\qquad C_{67}=31\cdot197\cdot311\cdot624212471$$

is a fully processed rank-zero fixed-67 miss. It contains none of the seven factors. Therefore **none of its divisors supplies an exit in the classified family**. Its signed local state agrees with earlier examples containing factor 43, but it does not contain 43; their factor-43 formula cannot be transferred from the signature alone.

This is **not** an Erdős–Straus counterexample. It has an explicit Type-I certificate at shift 3, retained with all three denominators in Section 14 of the master proof and verified by exact rational arithmetic.

## What the method does not prove

The classification is not a classification of all ES exits. It does not exhaust pointwise, piecewise, non-affine, Type-I, or mixed certificates. A smaller residual integer is not an infinite-descent proof; finite-depth density contraction does not imply emptiness; finishing a local factorization does not guarantee an exit.

The main open obligation is a cross-shift exit for **every admissible arithmetic terminal realization**, or another survivor-preserving mechanism with a proved well-founded invariant and a solution-lifting step. No such mechanism is proved here.

## Verification

Python 3.10 or later; standard library only; no network required. From this archive directory:

```sh
python -B verify_master.py
```

To rerun the latest classification alone:

```sh
python -B verify_master.py --stage factor-trigger-classification
```

The orchestrator checks source hashes and runs the six preserved stage verifiers plus the independent totient regression. It creates fresh logs in `verification-runs/`. It does not replace the proofs. Use normal Python, without `-O`; the historical totient script uses assertions. See [VERIFICATION.md](VERIFICATION.md) for exact roles and limits.

## File map

| file | purpose |
|:---|:---|
|[MASTER_PROOF.md](MASTER_PROOF.md)|Formal consolidated mathematics and preserved side results.|
|[RESEARCH_STATUS.md](RESEARCH_STATUS.md)|Ledger of proofs, finite evidence, exhausted routes and obligations.|
|[PROVENANCE.md](PROVENANCE.md)|Dates, attribution and AI assistance.|
|[VERIFICATION.md](VERIFICATION.md)|Reproduction instructions and computational boundaries.|
|[INTEGRATION_LOG.md](INTEGRATION_LOG.md)|Version conflicts, corrections and consolidation decisions.|
|[audit/SOURCE_AUDIT.md](audit/SOURCE_AUDIT.md)|Complete original-file coverage and preservation record.|
|[audit/original-files.json](audit/original-files.json)|Original file hashes, parsed-data census and historical ZIP member hashes.|
|[verification-runs/run-summary.json](verification-runs/run-summary.json)|Fresh verifier outcomes.|
|`sources/workspace/`|Unmodified snapshots of all original research text, code and data.|

## Provenance and AI assistance

The internal derivations and consolidation were developed with AI assistance using ChatGPT/Codex. Classical identities and inherited public-framework inputs are attributed separately. No independent human verification of the internal results is documented in this record; independent verification is welcome and is not a prerequisite for retaining the archive. The original records have not been removed or overwritten. Historical snapshots may retain superseded wording or their original language; the consolidated documents control the current claim scope.

The uniform affine Type-II phase is now classified and exhausted on the stated $k=67$ branch, but a universal exit from every admissible arithmetic terminal state is still unproved; the Erdős–Straus conjecture remains open.
