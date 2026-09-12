# Erdős–Straus Cross-Shift Structure: Proven Results, Complete Affine Classification, and the Remaining Termination Problem

Consolidation date: 12 September 2026. Research records: 10–11 September 2026.

## Abstract

This note consolidates fixed-shift divisor criteria, a Type-II completion theorem and its defect version, the exceptional negative-character branch at shift 31, and a classification of uniform affine Type-II factor exits at shift 67. On the progression $p=2041+26040m$, for an actual prime with a fixed-67 miss, the classified family provides an exit precisely when $C_{67}$ contains one of the seven prime factors $11,13,41,43,433,1933,4933$. The classification includes arbitrary composite trigger divisors. Its proof combines an algebraic reduction with a reproducible exhaustive finite calculation. Rationally varying certificate divisors do not enlarge this family when the shift remains nonconstant affine and validity is required throughout the progression. An explicit prime terminal lies outside the family but has a certificate at shift 3. The universal termination problem remains unresolved. An independent totient-sum asymptotic is retained in Appendix C.

## 1. Scope and claim boundary

The equation is

$$\frac4p=\frac1x+\frac1y+\frac1z,\qquad x,y,z\in\mathbb Z_{>0}.$$

Unless another domain is stated, $p$ is prime, $p\equiv1\pmod4$, and a shift $k$ is a positive integer with $k\equiv3\pmod4$ and $\gcd(p,k)=1$. Write $C_k=(p+k)/4$. A **fixed-$k$ miss** means that both exact targets in Section 2 fail. It says nothing about another shift.

The working Mordell classes are $a_0\in\{1,121,169,289,361,529\}\pmod{840}$. Their historical role is background; the proofs below use the stated congruences directly. Base-character and routed-root assumptions used in a historical finite graph are separate inputs, listed in Appendix A. They are not inferred merely from membership in a Mordell class.

We use $\ell$ for an actual prime factor, $h,D$ for actual positive divisors, $Q=4u-1$ for an affine modulus, $e$ for a fixed Type-II divisor, and $\mathcal Q_k$ for the nonzero quadratic residues modulo a prime $k$. This separates three different historical uses of the letter $q$. The variable $R$ denotes an unprocessed factor, not a new prime input. “Uniform” means validity for **every sufficiently large integer parameter**, including composite progression members. It does not mean validity only at sampled primes.

Statements marked **computer-assisted** have a proved finite reduction and an exhaustive exact enumeration. Statements marked **finite regression** assert only the specified finite facts. Neither type is a proof of global termination. Independent human verification of the internal derivations is not documented in the supplied record. No claim of global literature priority is made. Erdős–Straus remains open.

## 2. Fixed-shift divisor-square framework

**Theorem 1 (exact fixed-shift targets).** Under the standing assumptions, a decomposition with $x=C_k$ exists if and only if at least one of the following holds:

$$\text{Type I: }d\mid C_k^2,\quad4d\equiv-1\pmod k;$$
$$\text{Type II: }d\mid C_k^2,\quad d\equiv-C_k\pmod k.$$

**Proof.** Put $C=C_k$ and $N=pC$. The remaining equation is $k/N=1/y+1/z$, equivalently

$$(ky-N)(kz-N)=N^2.$$

Both factors on the left are positive. Thus the equation is equivalent to $A\mid N^2$ and $A\equiv-N\pmod k$, with

$$y=(N+A)/k,\qquad z=(N+N^2/A)/k.$$

Here $\gcd(N,k)=1$, so the second numerator is divisible by $k$ whenever the first is. Also $\gcd(p,C)=1$. The exponent of $p$ in $A$ is 0, 1, or 2; replacing $A$ by $N^2/A$ interchanges 0 and 2. We may therefore write $A=p^2d$ or $A=pd$, where $d\mid C^2$. Using $p\equiv4C\pmod k$ gives precisely the two targets. All constructed denominators are positive integers. This is the classical divisor-square reduction, not a novelty claim. $\square$

For later use, if $B\mid C$, write $C=BR$. A Type-I divisor $d_0\mid B^2$ remains valid for $C$. A Type-II divisor $d_0\mid B^2$ with $d_0\equiv-B\pmod k$ lifts to $d=d_0R\mid C^2$ with $d\equiv-C\pmod k$. This block-lifting rule also holds at composite shifts.

## 3. Type-II completion theorem

Here and in Section 4, $k$ is prime and $k\equiv3\pmod4$. Let $G\mid C_k$, and assume **every prime factor of $G$ lies in $\mathcal Q_k$**. In particular $G$ is a unit modulo $k$. Define

$$D_G=\{d\bmod k:d\mid G^2\},\qquad T_G(x)=\frac{G}{4x}\pmod k.$$

The map $T_G$ is an involution of $\mathcal Q_k$. Ordinary QR saturation means $D_G=\mathcal Q_k$; completion saturation means $D_G\cup T_G(D_G)=\mathcal Q_k$.

**Theorem 2 (completion saturation).** Under these hypotheses, if $D_G\cup T_G(D_G)=\mathcal Q_k$, then fixed-$k$ miss is equivalent to every prime factor of $C_k$ being a quadratic residue modulo $k$.

**Proof.** If all factors are QR, every divisor of $C_k^2$ is QR, whereas $-1/4$ and $-C_k$ are NQR; both targets fail. Conversely let an NQR prime $\ell\mid C_k$ occur. It does not divide $G$, so $C_k=G\ell R$. Put $x=-1/(4\ell)\in\mathcal Q_k$. If $x\in D_G$, choose $e\mid G^2$ with $e\equiv x$; then $e\ell$ is a Type-I divisor. Otherwise $x\in T_G(D_G)$ and the involution gives $T_G(x)=-G\ell\in D_G$. Choose $e\mid G^2$ in that residue; then $eR\mid C_k^2$ and $eR\equiv-C_k$, a Type-II divisor. $\square$

This extends the ordinary QR-saturation lemma of the audited public framework [3]. It makes certain rigid cases elementary once their seed divisibility is known; it does not import the full finite-state closure as a hypothesis. Novelty beyond that comparison is not established.

## 4. Defect prime-support theorem

**Theorem 3 (defect restriction).** With the hypotheses preceding Theorem 2, set

$$E_{k,G}=\mathcal Q_k\setminus(D_G\cup T_G(D_G)).$$

In a fixed-$k$ miss, each NQR prime factor $\ell$ of $C_k$ satisfies

$$\ell\bmod k\in\{-1/(4x):x\in E_{k,G}\}.$$

**Proof.** The two certificates in the proof of Theorem 2 exclude every $x=-1/(4\ell)$ outside $E_{k,G}$. This is a necessary support restriction, not its converse. $\square$

The following small sets are obtained by listing divisors of $G^2$; the completion verifier reproduces them exactly.

| $k$ | $G$ | $|\mathcal Q_k|$ | $|D_G|$ | $\mathcal Q_k\setminus D_G$ | $E_{k,G}$ |
|---:|---:|---:|---:|:---|:---|
|31|10|15|9|8,9,14,16,18,28|empty|
|47|42|23|21|27,34|empty|
|59|105|29|25|12,19,26,36|empty|
|31|14|15|9|8,9,16,19,20,25|9|
|71|30|35|25|27,32,37,40,43,49,54,57,58,64|40,49|

The allowed NQR residues are respectively $\{6\}$ at $(31,14)$ and $\{46,67\}$ at $(71,30)$.

**Corollary 4 (unique negative source).** If $G=14\mid C_{31}$ and there is a fixed-31 miss with $(C_{31}/31)=-1$, exactly one NQR prime occurs, with exponent one and residue 6. If $G=30\mid C_{71}$ and there is a fixed-71 miss with $(C_{71}/71)=-1$, exactly one NQR prime occurs, with exponent one and residue 46 or 67.

**Proof.** Count prime occurrences with multiplicity. At 31, three occurrences of residue 6 give a block $B=14\ell_1\ell_2\ell_3$ and Type-II divisor 14, since $6^3=-1\pmod{31}$. At 71 the following blocks give certificates; repeated primes are allowed when the requisite multiplicities occur:

| NQR residues in the block after the seed 30 | divisor | type |
|:---|:---|:---|
|67,67|$180\ell_1\ell_2^2$|I|
|46,46,46|$6(\ell_1\ell_2\ell_3)^2$|II|
|46,46,67|$2\ell_1\ell_2^2\ell_3^2$|I|

The Type-I residue is $53=-1/4\pmod{71}$; for the middle row $46^3=66$ and $6\cdot66^2=-30\cdot66=8$. Each divisor divides the block square and lifts. Thus a miss has at most two NQR occurrences. Negative character requires an odd number, hence exactly one. $\square$

For the six class seeds $G=\gcd(210,(a_0+k)/4)$, completion can occur only for $k\le325$: $(k-1)/2\le2\tau(G^2)\le162$. Exhaustion gives 22 pairs, 17 ordinarily saturated and five additional completion pairs. The latter are $(a_0,k,G)=(169,31,10),(289,31,10),(121,47,42),(289,47,42),(361,59,105)$. This census is complete for these prescribed seeds, not for all seeds.

## 5. The $a_0=361$, $k=31$ exceptional branch

**Theorem 5 (factor-level description).** Let $p\equiv361\pmod{840}$ be prime and suppose $(C_{31}/31)=-1$. There is a fixed-31 miss if and only if

$$C_{31}=14\ell S,$$

where $\ell$ is prime, $\ell\equiv6\pmod{31}$, $v_\ell(C_{31})=1$, and every prime factor $r$ of $S$ satisfies $r\equiv1\pmod{31}$.

**Proof.** The progression forces $14\mid C_{31}$ and $2,7$ are QR modulo 31. Corollary 4 leaves exactly one NQR occurrence $\ell$. To exclude every extra nonidentity QR residue, use the following complete table. For an extra actual prime $r$, the block is $B=14\ell r$ and the divisor is $e\ell^a r^b$.

| $r\bmod31$ | $e$ | $a$ | $b$ | type |
|---:|---:|---:|---:|:---|
|2|49|0|0|II|
|4|1|2|0|II|
|5|14|0|0|II|
|7|1|0|0|II|
|8|1|2|2|II|
|9|1|0|2|II|
|10|7|2|2|II|
|14|2|0|0|II|
|16|49|0|2|II|
|18|7|0|0|II|
|19|7|0|2|II|
|20|2|0|2|II|
|25|14|0|2|II|
|28|1|1|2|I|

In each row $e\mid14^2$, $a,b\le2$, and direct reduction gives $-B$ or $-1/4$. This includes extra occurrences of 2 and 7 beyond the seed. Block lifting proves necessity. Conversely, all divisors of $C_{31}^2$ have residues $e6^a$ with $e\mid14^2$ and $0\le a\le2$. This finite set omits both $23=-1/4$ and $9=-14\cdot6$. Hence both targets fail. $\square$

## 6. Reduction to $p\equiv2041\pmod{26040}$

**Corollary 6 (necessary progression and exact residual identities).** Under Theorem 5's miss hypotheses, put $N=C_{31}/14$. Then

$$N\equiv37\pmod{465},\qquad p=2041+26040m\quad(m\ge0).$$

**Proof.** From $p\equiv361\pmod{840}$ and $p=56N-31$ we get $N\equiv7\pmod{15}$. The factor description gives $N\equiv6\pmod{31}$. CRT gives $N\equiv37\pmod{465}$ and substitution gives the assertion. This is a necessary reduction, not a sufficient characterization of all members. $\square$

On this progression the following identities are exact:

| shift | companion decomposition |
|---:|:---|
|31|$14(37+465m)=14N$|
|59|$105(5+62m)=105M$|
|67|$31(17+210m)=31T$|
|191|$186(3+35m)=186U$|
|479|$210(3+31m)=210V$|
|439|$310(2+21m)$|
|563|$651(1+10m)$|
|3167|$1302(1+5m)$|
|10979|$3255(1+2m)$|
|23999|$6510(m+1)$|
|50039|$6510(m+2)$|
|76079|$6510(m+3)$|

Also $15M-2N=1$, $31T-14N=9$, $31T-105M=2$. These imply pairwise coprimality of $N,M,T$: use $N\equiv1\pmod3$ and oddness of $M,T$ for the last two possible common factors. The shifts 23999 and 50039 are composite, which is allowed for the exact divisor criterion. These formulas are an arithmetic descent skeleton. **Numerical size descent is not Erdős–Straus infinite descent.** They do not supply a transition preserving survivor hypotheses or a solution-lifting induction.

**Lemma 7 (reciprocity and retained sources).** Let $p\equiv1\pmod4$ be prime, let $k\ne p$ be prime with $k\equiv3\pmod4$, and let $\ell$ be an odd prime dividing $C_k$. Then

$$\left(\frac\ell p\right)=\left(\frac p\ell\right)=\left(\frac{-k}\ell\right)=\left(\frac\ell k\right).$$

If the same $\ell$ divides $C_K$ at another prime shift $K\equiv3\pmod4$, $K\ne p$, its sign is unchanged.

**Proof.** The first equality uses $p\equiv1\pmod4$; the second uses $p\equiv-k\pmod\ell$. Quadratic reciprocity for $k\equiv3\pmod4$ gives $(k/\ell)=(\ell/k)(-1/\ell)$, canceling the sign in $(-k/\ell)$. All symbols are nonzero under the hypotheses. Applying the same calculation at $K$ proves the final assertion. $\square$

In particular, $(C_k/k)=(p/k)=(k/p)$ for such prime shifts. This does not justify a Legendre symbol at a composite shift. Retaining a unique bad source at a later unique-source miss retains that same prime, rather than automatically producing a smaller one.

## 7. The $k=67$ terminal framework

For a positive integer $B$ coprime to $k$, define its signed divisor set

$$A_k(B)=\left\{\prod_{\ell^f\parallel B}\ell^{j_\ell}\bmod k:-f\le j_\ell\le f\right\}.$$

For a fully factored companion, the divisor residues of $C_k^2$ are $C_k A_k(C_k)$. The two exclusions for a miss are therefore

$$-1\notin A_k(C_k),\qquad -(4C_k)^{-1}\notin A_k(C_k).$$

**Lemma 8 (local monotonicity and its termination boundary).** Let $k\equiv3\pmod4$ be prime. While processing actual occurrences in $C_k=BR$, adding a prime residue $r$ changes $A=A_k(B)$ to $A'=A\cup rA\cup r^{-1}A$. If $H(A)=\{r:rA=A\}$, then $H(A)$ is a subgroup, $H(A)\subseteq H(A')$, and a transition is neutral precisely when $r\in H(A)$. If $-1\notin A'$, each nonneutral transition increases $|A|$ by at least two. Every NQR transition is nonneutral.

**Proof.** The set $A$ contains 1 and is closed under inverses. Its stabilizer is a subgroup contained in $A$; stabilization of $A$ stabilizes its three translates, proving monotonicity. Equality $A'=A$ is equivalent to $rA=A$. New elements occur in inverse pairs; the only self-inverse units are $\pm1$, neither of which can be new in a surviving transition. If $-1\notin A$, $H(A)$ has odd order, hence is contained in $\mathcal Q_k$. An NQR residue is therefore not neutral. $\square$

For a surviving block put $\rho=(k-2-|A|)/2$. The lexicographic pair $(\rho,R)$ decreases when an actual prime occurrence is processed: either the rank drops or $R$ drops at equal rank. This terminates **factor processing**. It can terminate at $R=1$ with a miss and is not an ES termination theorem.

**Corollary 9 (bounded core at 67).** For a fixed-67 miss with $C_{67}=31T$, there is $B\mid C_{67}$ with $31\mid B$ such that

$$A_{67}(B)=A_{67}(C_{67}),\quad\Omega(B)\le(|A_{67}(C_{67})|-1)/2\le32.$$

Every prime factor of $C_{67}/B$ lies in the final stabilizer. The number of NQR prime occurrences in $T$ is at most 31.

**Proof.** The seed 31 has $A_0=\{1,13,31\}$ and rank 31. Retain the seed and every subsequent nonneutral occurrence, omitting neutral ones. Omissions do not change the set, and stabilizer monotonicity puts all omitted factors in the final stabilizer. Each retained additional occurrence costs at least two elements. NQR occurrences cannot be omitted. $\square$

This bounds a number of occurrences, not their sizes or the number of neutral factors. The bound 31 is sharp for the abstract residue process: starting with 31, append nine residues 13 and then twenty-two residues 31. All transitions survive and the sizes run from 3 to 65. The verifier checks the entire path; it makes no claim that a prime in the branch realizes it.

**Finite result 10 (abstract state census; computer-assisted).** For the fixed-67 residue automaton starting at $(A,c)=(\{1,13,31\},31)$, with transitions $(A,c)\mapsto(A\cup rA\cup r^{-1}A,cr)$ and the two block-miss exclusions, there are 3,373 signed sets, 10,545 raw states and 10,415 strongly connected components (SCCs). The SCCs are exactly $(A,cH(A))$: a cycle cannot strictly increase $A$, so every edge in it is neutral, and multiplication by $H(A)$ connects its phase coset. The quotient is acyclic under strict set growth.

| $|H(A)|$ | raw states | SCCs | sink SCCs |
|---:|---:|---:|---:|
|1|10,358|10,358|92|
|3|165|55|2|
|11|22|2|1|
|total|10,545|10,415|95|

The only possible stabilizer sizes are 1,3,11: order must divide 33, while order 33 would force its QR coset and the coset containing 31 into $A$, including $-1$. The transition verifier exhausts all 66 residues at each reached state and checks closure. An actual factorization may finish at **any** reached state; it need not reach a sink of the unrestricted abstract graph. For a partial block the label $4B\pmod{67}$ is not the original input residue $p\equiv4BR$. Cross-shift rules on $p$ cannot be applied to that partial label without further arithmetic information.

An additional structural identity in the source record is the **abstract normalization edge**. At a block-miss state $(A,c)$ take $r=(4c)^{-1}$. The exclusions $-1\notin A$ and $-(4c)^{-1}\notin A$, together with inverse closure, imply $-1\notin A\cup rA\cup r^{-1}A$. The new phase is $c'=1/4$, so its other target is also $-1$; the edge survives. It is strict precisely when $4c\notin H(A)$. Hence every sink has $4c\in H(A)$. The exact sink-phase union at 67 is $\{1,9,14,15,22,24,25,29,37,40,59,62,64\}$. This edge is an operation on residues: there need not be an actual prime of that residue dividing the remaining $R$.

If $T\equiv1\pmod{67}$, then $m\equiv28\pmod{67}$ and, writing $m=28+67n$, we have $C_{479}=14070(13+31n)$. Since $5628\mid14070^2$ and $4\cdot5628+1=479\cdot47$, shift 479 supplies a Type-I exit. Thus a simultaneous 67/479 miss cannot leave $A=A_0$: every neutral factor at the seed has residue 1. It has $|A|\ge5$ and $\rho\le30$. This rank bound alone does not strengthen the bound on NQR occurrences.

There is a separate conditional bound of 29 if $T$ contains a QR prime with residue $r\ne1$. Insert that occurrence first. The QR part of $A_0\cup rA_0\cup r^{-1}A_0$ contains the three distinct elements $1,r,r^{-1}$. If its NQR part contained only $31,13$, multiplication by the odd-order element $r$ would permute those two elements, hence fix both, forcing $r=1$. Thus the NQR part has at least four elements, the set has at least seven, and this QR occurrence consumes at least two rank units before any NQR occurrence is inserted. At most 29 NQR occurrences can follow. This argument requires the extra QR-factor hypothesis.

## 8. Affine Type-II identity

**Theorem 11 (classical affine certificate).** Let $p>0$, $p\equiv1\pmod4$, and let $u,e$ be positive integers with $Q=4u-1>0$, $e\mid u^2$, and $Q\mid p+4e$. Set $K=(p+4e)/Q$ and $v=u^2/e$. Then $K$ is a positive integer congruent to 3 modulo 4, $C_K=uK-e$, and

$$\boxed{\frac4p=\frac1{uK-e}+\frac1{pu}+\frac1{p(vK-u)}}.$$

**Proof.** The defining equation gives $p=QK-4e$ and $p+K=4(uK-e)$. Reduction modulo 4 gives $K\equiv3$. Also $C_K=(p+K)/4>0$, $e\mid C_K^2$ and $C_K+e=uK$. The last denominator is $p(vK-u)=puC_K/e>0$, an integer since $v$ is an integer. The last two reciprocals sum to $K/(pC_K)$, and $p+K=4C_K$ proves the identity. $\square$

This is within the classical congruence family $p\equiv-a/c\pmod{4acd-1}$ discussed by Bloom–Elsholtz [1]. To see the parameter match, write $e=a^2d$ with $d$ squarefree; $e\mid u^2$ implies $ad\mid u$, so $u=acd$. Multiplication by $c$ shows $p\equiv-4e\pmod Q$ is equivalent to $cp\equiv-a\pmod Q$. This underlying identity is not claimed as a new discovery.

**Lemma 12 (uniform affine reduction).** Let $p_n=P+Ln$ with $P,L>0$, $\gcd(P,L)=1$, $P\equiv1\pmod4$ and $4\mid L$. Suppose $K_n$ is nonconstant affine, positive for sufficiently large integers $n$, and for all such $n$ it is an integer congruent to 3 modulo 4. Put $C_n=(p_n+K_n)/4$. A fixed positive integer $e$ satisfies $e\mid C_n^2$ and $K_n\mid C_n+e$ throughout that tail if and only if

$$Q=4u-1\mid L,\quad e\mid u^2,\quad Q\mid P+4e,\quad K_n=(p_n+4e)/Q$$

for a positive integer $u$.

**Proof.** Write $K_n=\alpha n+\beta$. Eventual integer values force integer slope and intercept; positivity and nonconstancy give $\alpha>0$. The positive integer sequence $(C_n+e)/K_n$ converges, hence is eventually a constant $u$. Polynomial equality gives $L=(4u-1)\alpha$ and $P+4e=(4u-1)\beta$. Since $QC_n=up_n+e$, the divisibility $e\mid C_n^2$ implies $e\mid u^2p_n^2$. For each prime $\ell\mid e$, primitivity gives arbitrarily large $n$ with $\ell\nmid p_n$, yielding $v_\ell(e)\le2v_\ell(u)$. The converse is Theorem 11. $\square$

## 9. Actual-factor trigger theorem

**Theorem 13 (actual-factor trigger, including composite factors).** Let $p\equiv1\pmod4$ be positive and suppose $h\mid C_{67}$. If positive integers $s,u,e$ satisfy

$$sh=4u-1,\quad\gcd(s,h)=1,\quad e\mid u^2,$$
$$4e\equiv67\pmod h,\qquad p+4e\equiv0\pmod s,$$

then $K=(p+4e)/(sh)$ gives the certificate of Theorem 11. No primality of $h$ is required. If $p$ is prime and $0<K<p$, this is an admissible shift in Theorem 1.

**Proof.** Since $p\equiv-67\pmod h$, both coprime factors $h,s$ divide $p+4e$. Thus their product does, and Theorem 11 applies. The final claim is immediate from primality and the strict size inequality. $\square$

## 10. Seven-factor classification theorem

Fix an actual prime $p=2041+26040m$, $m\ge0$, with a fixed-67 miss, and put $C=C_{67}$. For **any** divisor $D\mid C$, let $\mathcal P_D$ denote the full progression defined by

$$p'\equiv2041\pmod{26040},\qquad D\mid(p'+67)/4.$$

It has step $L_D=\operatorname{lcm}(26040,4D)$. It is primitive: it contains $p$, and $p$ is coprime to $26040D$. The latter follows from the branch and $p\ne67$. Also $D$ is odd and $\gcd(D,105\cdot67)=1$, because $C=527+6510m$ is coprime to 105 and to 67. A **uniform affine factor exit** means one nonconstant affine $K$ and one fixed positive $e$ satisfying Lemma 12 on all sufficiently large integer members of $\mathcal P_D$. There is no independent extra residue restriction in this definition.

**Lemma 14 (arbitrary-divisor normalization).** Every such exit has parameters

$$Q=sh=4u-1,\quad h\mid D,\quad s\mid3255,\quad\gcd(s,h)=1,$$
$$e\mid u^2,\qquad h\mid4e-67,\qquad s\mid2041+4e.\tag{N}$$

It therefore already works on $\mathcal P_h$.

**Proof.** Lemma 12 gives odd $Q\mid L_D$, hence $Q\mid\operatorname{lcm}(3255,D)$, with $3255=3\cdot5\cdot7\cdot31$. Assign the factors 3,5,7 of $Q$ to $s$; their exponents are at most one. If $v_{31}(Q)=1$, assign 31 to $s$; if $v_{31}(Q)\ge2$, assign its **entire power** to $h$. Assign all other prime powers to $h$. Then $h\mid D$, $s\mid3255$ and $\gcd(s,h)=1$. Reduction of $Q\mid P_D+4e$ modulo $h$ and $s$ gives (N). Conversely, (N) implies $Q\mid p'+4e$ on $\mathcal P_h$. Simply setting $s=\gcd(Q,3255)$ would not correctly handle higher powers of 31. $\square$

**Lemma 15 (finite square-divisor reduction).** Suppose $k$ is an admissible shift for an actual prime, fixed-$k$ miss holds, $h>k$, $h\mid C_k$, $Q=sh=4u-1$, $e\mid u^2$ and $Q\mid p+4e$. Define

$$v=u^2/e,\quad a=(4e-k)/h,\quad b=(4kv-1)/h.$$

Then $a,b$ are positive integers, $\Delta=ks^2-ab>0$, and

$$\Delta h=a+kb-2ks>0,$$
$$\boxed{\Delta(ah+k)=(a-ks)^2},\qquad
\boxed{\Delta(bh+1)=k(b-s)^2}.\tag{S}$$

Exactly one of $1\le a<ks,\ b>s$ or $1\le b<s,\ a>ks$ holds.

**Proof.** Modulo $h$, $4e\equiv k$ and $4u\equiv1$. From $ev=u^2$ we obtain $4kv\equiv1$. Thus $a,b$ are integers. Since $h>k$ and $4e-k>-h$, $a\ge0$, and $a=0$ is impossible for $k\equiv3\pmod4$; also $b>0$. Expanding $(ah+k)(bh+1)=16kev=k(sh+1)^2$ gives

$$(ab-ks^2)h=2ks-a-kb.$$

If $ab>ks^2$, AM–GM gives $a+kb\ge2\sqrt{kab}>2ks$, a contradiction. If equality holds, $a=ks,b=s$, so $e=ku$ and $k\mid u$. Then $Q\equiv-1\pmod k$ and $Q\mid p+4e=p+k+kQ$, hence $Q\mid C_k$ because $Q$ is odd. The divisor $C_kQ\mid C_k^2$ supplies the original Type-II target, contradicting the miss. Therefore $\Delta>0$. Substitution proves both identities (S). Both variables below their thresholds contradict $a+kb>2ks$; both above contradict $ab<ks^2$. Equality at one threshold is also impossible by (S). $\square$

This proves an exhaustive finite procedure for each fixed $k,s$:

1. Handle $1\le h\le k$ directly, enumerating $e\mid((sh+1)/4)^2$ when $sh\equiv3\pmod4$.
2. For $1\le a<ks$, enumerate $\Delta\mid(a-ks)^2$, recover $b=(ks^2-\Delta)/a$ and $h=((a-ks)^2/\Delta-k)/a$.
3. For $1\le b<s$, enumerate $\Delta\mid k(b-s)^2$, recover $a=(ks^2-\Delta)/b$ and $h=(k(b-s)^2/\Delta-1)/b$.
4. Retain only positive integers, $h>k$ in the last two loops, the stated inequalities, and all original conditions (N).

There is no chosen upper cutoff on $h$. A useful derived bound is $h\le(ks-1)^2-k$: since $(a-1)(kb-1)\ge0$, we have $a+kb\le kab+1$; use $ab\le ks^2-1$ and $\Delta\ge1$ in $\Delta h=a+kb-2ks$.

**Finite classification 16 (computer-assisted exhaustive table).** Applying this procedure at $k=67$ for all 16 divisors $s\mid3255$, imposing odd $h$, $\gcd(h,105\cdot67)=1$ and (N), gives precisely the following nine rows in the nondegenerate domain of Lemma 15 and the direct small-$h$ domain.

| $h$ | $s$ | $Q=sh$ | $u$ | $e$ | $v=u^2/e$ |
|---:|---:|---:|---:|---:|---:|
|11|1|11|3|3|3|
|13|3|39|10|20|5|
|41|7|287|72|27|192|
|43|5|215|54|6|486|
|319|1|319|80|256|25|
|433|3|1299|325|125|845|
|937|15|14055|3514|251|49196|
|1933|3|5799|1450|500|4205|
|4933|3|14799|3700|1250|10952|

**Verification of the finite component.** The function `square_classification` in the preserved classification verifier implements exactly the four steps above. Its sieve factors integers no larger than $67\cdot3255=218085$; it forms their complete square-divisor lists, reconstructs $a,b,h,e$, and rechecks (N). The full loops derive the rows before comparing with the table. The bounds in Lemma 15 establish coverage of all eligible $h$, including composite $h$ and repeated prime powers. A separately implemented direct enumeration for $h\le10000$ confirms all eight surviving rows, but that bounded check is not the completeness argument. The full run and per-$s$ loop counts are retained in `verification-runs/factor-trigger-classification.txt`. $\square$

**Theorem 17 (seven-factor classification; computer-assisted).** For the actual prime and fixed-67 miss specified at the start of this section, a uniform affine factor exit exists using some divisor $D\mid C$ if and only if

$$\gcd\big(C,11\cdot13\cdot41\cdot43\cdot433\cdot1933\cdot4933\big)>1.$$

**Proof.** Lemmas 12, 14 and 15 reduce necessity to Classification 16. The row $h=937$ is impossible at a miss: $937\equiv-1\pmod{67}$, so $C\cdot937$ would be a Type-II divisor. The composite row $319=11\cdot29$ implies the factor-11 condition. All other rows are the seven displayed prime factors. Conversely, any of those factors supplies the corresponding row, and Theorem 13 gives a uniform certificate. In all seven rows $e\le1250$, $Q\ge11$, and $p\ge2041$, so $4e<(Q-1)p$, proving $0<K<p$ and admissibility at the actual prime. $\square$

## 11. Composite-divisor completeness

**Corollary 18 (no further coverage by composite triggers).** Under Theorem 17's hypotheses and its definition of uniformity, allowing arbitrary composite $D\mid C$, including $D=C$, or any finite collection of actual restrictions $D_i\mid C$, adds no coverage beyond the seven prime factors.

**Proof.** Combine the restrictions into $D=\operatorname{lcm}(D_i)\mid C$. Lemma 14 includes its full prime-power information. Classification 16 leaves only the additional surviving composite trigger 319, which is subsumed by 11. $\square$

This is a completeness statement for the specified family, not an extrapolation from a scan of small composite factors. An extra progression restriction independent of actual divisibility by $C_{67}$ changes the universe and is not excluded here.

## 12. Variable-divisor affine limitation theorem

**Lemma 19 (eventually integer-valued rational functions).** If $f\in\mathbb Q(n)$ is integer-valued at every sufficiently large integer $n$, then $f\in\mathbb Q[n]$.

**Proof.** Divide to write $f=A+R/B$, with $\deg R<\deg B$. Choose a positive integer $M$ clearing the coefficients of $A$. The integer $M(f(n)-A(n))$ tends to zero and is eventually zero. The polynomial $R$ has infinitely many zeros and is identically zero. $\square$

**Theorem 20 (rational-divisor rigidity).** Let $p_n=P+Ln$ satisfy Lemma 12's primitive progression hypotheses. Let $K_n$ be nonconstant affine, eventually positive, integral and congruent to 3 modulo 4, and put $C_n=(p_n+K_n)/4$. Suppose a rational function $\delta(n)\in\mathbb Q(n)$ is a positive integer satisfying

$$\delta(n)\mid C_n^2,\qquad K_n\mid C_n+\delta(n)$$

for every sufficiently large integer $n$. Assume also that $K$ is coprime to $p$ at a prime member where this formula is proposed as an admissible exit. Then, as rational-function identities,

$$\delta(n)=e\quad\hbox{or}\quad\delta(n)=C_n^2/e$$

for a fixed positive integer $e$. In both cases $e\mid C_n^2$ and $K_n\mid C_n+e$ throughout the tail.

**Proof.** Apply Lemma 19 to $\delta$ and $E=C^2/\delta$. They are polynomials whose product is the square of the nonconstant linear polynomial $C$. Thus their degrees are $(0,2),(1,1)$ or $(2,0)$, with each nonconstant factor proportional to a power of $C$. Any constant factor is a positive integer.

The first case is the conclusion. In the middle case, $\delta=rC$, $r>0$ rational, and the convergent integer sequence $(1+r)C/K$ is constant. Thus $K$ is proportional to $C$, hence to $p=4C-K$. Write $K=jp$. Integrality and $\gcd(P,L)=1$ force the rational number $j$ to be an integer: its reduced denominator divides every sufficiently large $p_n$, whose greatest common divisor is 1. Positivity gives $j\ge1$, contradicting admissibility at the specified prime member.

In the last case $E=e$ is constant. By Lemma 19, $C(C+e)/(eK)$ is a polynomial, so the linear polynomial $K$ divides $C(C+e)$ over $\mathbb Q$. It is proportional either to $C$, excluded as above, or to $C+e$. Write $C+e=(A/B)K$ in lowest positive terms. The original quotient is $AC/(Be)$ and is integer-valued, so $B\mid C_n$. Also $B(C_n+e)=AK_n$ gives $B\mid K_n$. Consequently $B\mid p_n$ throughout the tail; primitivity gives $B=1$. Hence $K_n\mid C_n+e$, and $e\mid C_n^2$ follows from integrality of $\delta=C^2/e$. $\square$

**Corollary 21.** Allowing a rationally varying divisor in Theorem 17, with the same nonconstant affine shift, whole-progression quantifier, and admissibility, gives exactly the same seven-factor coverage. The case $\delta=C_K^2/e$ merely exchanges the two denominators

$$\frac{p(C_K+e)}K,\qquad\frac{p(C_K+C_K^2/e)}K.$$

**Proof.** Theorem 20 reduces to Lemma 12 and Theorem 17. The displayed pair is the Type-II construction of Theorem 1, so complementation interchanges it without changing $K$. $\square$

This theorem exhausts the stated uniform affine Type-II family. It does not exhaust pointwise, piecewise, non-affine, Type-I, or mixed cross-shift certificates.

## 13. Explicit factor-43 and factor-4933 exits

For factor 43, $(s,Q,u,e,v)=(5,215,54,6,486)$ and

$$K=(p+24)/215.$$

The base branch gives $p\equiv1\pmod5$; $43\mid C_{67}$ gives $p\equiv19\pmod{43}$. CRT supplies integrality. One verified prime is $p=536374041272521$, with

$$C_{67}=31\cdot43\cdot197\cdot510635947.$$

Its exit is

$$\frac4p=\frac1{134717201063796}
+\frac1{28964198228716134}
+\frac1{650329286071599231036684747444}.$$

The second preserved factor-43 prime is $27012366369467161$, with residual prime $25716168607$ in place of $510635947$. Its three denominators are $6784501320703380$, $1458667783951226694$, and $1649388917780761677822974985337620$. Both examples have the same saturated fixed-67 signature used below. They are finite certificates, not existence claims for infinitely many primes in their family.

For factor 4933, the verified parameters are

$$(s,Q,u,e,v)=(3,14799,3700,1250,10952),\qquad K=(p+5000)/14799.$$

Indeed $4e-67=4933$ and $2041+4e=7041$ is divisible by 3. The actual prime $p=353857093321$ has

$$C_{67}=31\cdot4933\cdot578489,\quad N=6318876667,$$
$$M=842516889=3\cdot17\cdot383\cdot43133.$$

Here $N$ is prime and $N\equiv6\pmod{31}$; every prime factor of the **composite** $M$ is QR modulo 59. Exact checks give misses at 31,59,67 and

$$\frac4{353857093321}=\frac1{88470251050}
+\frac1{1309271245287700}
+\frac1{92665244610519158781668}.$$

## 14. Same-signature / different-factor obstruction

**Proposition 22 (explicit arithmetic terminal and family obstruction).** The prime

$$p_*=4742209557133801$$

has

$$C_*=(p_*+67)/4=1185552389283467=31\cdot197\cdot311\cdot624212471.$$

It lies on the branch, misses at 31,59,67, and satisfies

$$A_{67}(C_*)=\{1,2,\ldots,65\},\qquad C_*\equiv17\pmod{67}.$$

It is therefore a fully processed $R=1$, rank-zero terminal. None of the seven classified primes divides $C_*$, so no divisor of $C_*$ supplies a uniform affine factor exit in Theorem 17, even with the rational extension of Corollary 21.

**Proof and finite evidence.** The preserved verifier proves primality by exhaustive trial division, checks the full factorization and signed set, and verifies both target failures. Its exact earlier-branch data are $N=84682313520247$ and $M=11290975136033$, both prime; $N\equiv6\pmod{31}$ and $M$ is QR modulo 59. Seven divisions check absence of the trigger factors. The exclusion then follows from Theorem 17, not from a bounded search over possible exits. A separate actual-divisor regression checks all 16 divisors of $C_*$, 45 eligible normalized moduli after the proved bound, and 1,531 divisor candidates, finding no classified exit. $\square$

In increasing factor order the residues modulo 67 are $(31,63,43,3)$. Replacing the actual factor 43 of the examples in Section 13 by the actual factor 311 preserves residue 43; their entire $(A,c)$ signatures agree. However $43\nmid C_*$ and $215\nmid p_*+24$. Equality of signatures therefore does not transfer the factor-43 formula. This is a failure of that signature-only inference, not a theorem against every conceivable residue-based argument.

The same prime has a **Type-I certificate at shift 3**, with $d=252148139$ and

$$\frac4{4742209557133801}
=\frac1{1185552389283451}
+\frac1{1890148803686908273902706895169340443930}
+\frac1{1874045958839011567761385163370}.$$

The exact rational identity, positivity, divisibility and target congruence are independently recomputed. Thus this is not an ES counterexample. It proves that the classified uniform affine Type-II strategy is incomplete as a global termination mechanism; it does not prove that cross-shift methods fail or that no certificate exists.

## 15. Exhausted proof mechanisms

The following are distinctions between a false universal proposal, an exhausted specified family, and an obligation not established by existing identities.

| Route | Exact obstruction or boundary | What remains possible |
|:---|:---|:---|
|Same signature transfers an actual-factor exit|Section 14: identical $(A,c)$, but $215\nmid p_*+24$.|Other formulas or finer arithmetic data.|
|Next repeated bad-prime route automatically hits|The finite regression below has misses at both the immediate route and first prime route.|Different routes; pointwise certificates.|
|Every next-route miss produces a smaller bad prime|Lemma 7 preserves the sign of the retained actual prime; the recorded next prime routes still miss. No survivor-preserving smaller-source rule is proved.|A different descent with a proved invariant and lifting step.|
|More composite trigger factors complete the affine family|Corollary 18 and $p_*$: only 319 adds a row, already covered by 11.|Independent progression refinements or other certificate families.|
|Rationally varying the divisor expands uniform affine exits|Theorem 20: constant divisor or its complement only.|Non-rational arithmetic choices, non-affine shifts, other quantifiers.|
|Tiny fixed-depth survivor density implies emptiness|A density estimate permits an infinite sparse set; no step from density to emptiness is supplied.|A separate covering or termination theorem.|
|Finite factor processing terminates ES|Lemma 8 ends at $R=1$; Proposition 22 is an actual local miss there.|Cross-shift exit for every arithmetic terminal.|

The repeated-route regression uses $K_j=31+4j\ell$:

| $p$ | retained bad prime $\ell$ | immediate $K_1$ (miss) | first prime $K_j$ (miss) |
|---:|---:|---:|---:|
|54121|967|3899|27107|
|1408201|25147|100619|402383|
|1824841|32587|130379|130379|

The descent verifier checks prime inputs, prime sources, full companion factorizations and misses; its prime-route character checks use Lemma 7's direction. Composite immediate shifts are tested by the divisor criterion, not Legendre symbols.

**Finite classification 23 (constant seed shells; computer-assisted).** On the entire original progression, neither a Type-I witness supported on the forced seed $G(k)=\gcd(6510,(2041+k)/4)$ nor a centered Type-II block witness $e\mid G^2$, $G\mid G(k)$, $k\mid e+G$ exists.

**Proof of finite reduction and calculation.** For Type I, $e\mid6510^2$ and $k\mid4e+1$. Enumerating all 243 choices of $e$ gives 168 distinct admissible-parity candidate shifts (largest 3,139,267), none with $e\mid G(k)^2$. For centered Type II, enumerate all $G\mid6510$, all $e\mid G^2$, and all $k\mid e+G$; 1,024 $(G,e)$ pairs give 488 distinct candidate shifts (largest 10,601,535), none with $G\mid G(k)$. These are complete finite divisor lists, recomputed in the descent verifier; no shift cutoff is assumed. $\square$

This excludes those two seed-shell constructions only. The source-67 refinement and affine refinements in Appendix B survive this exclusion because they use additional information.

## 16. Remaining termination obligation

The missing implication is to **produce a cross-shift exit for every admissible arithmetic terminal realization**, or to prove another genuinely well-founded termination mechanism whose hypotheses persist and whose solution lifts to the original input. A finite abstract graph, a bound on nonneutral factors, affine residual identities, and a finite-depth density bound do not supply that implication.

The classified uniform affine phase has reached its stated boundary. The record leaves open pointwise certificates depending on actual factorization; refined or piecewise progressions; non-affine $K(p)$; Type-I exits; mixed Type-I/Type-II mechanisms; and recursive arithmetic descent with a proved well-founded invariant. None is designated a successful route here. No new investigation of these directions is part of this consolidation.

## 17. Verification and provenance

The proof dependencies are: Theorem 1 → completion/defect → exceptional branch → progression; Theorem 1 → signed-state structure; classical Theorem 11 → Lemma 12 → normalization and square reduction → exact finite table → Theorem 17; Lemma 19 → Theorem 20 → Corollary 21. The totient theorem below is independent. The conditional public graph in Appendix A is not a premise of the seven-factor classification.

See [RESEARCH_STATUS.md](RESEARCH_STATUS.md) for claim-by-claim scope, [VERIFICATION.md](VERIFICATION.md) for verifier roles, and [PROVENANCE.md](PROVENANCE.md) for attribution. All original records are preserved; the `sources/workspace/` tree contains byte-identical research-text snapshots. `audit/original-files.json` records their hashes and the original historical ZIP member hashes. The fresh logs record a rerun rather than merely repeating old PASS messages.

## Appendix A. Conditional closure and finite arithmetic records

The public recursive graph uses source arity at most two, at least one derived source on each new route, exact compatible residue restrictions, and seed $\operatorname{lcm}(G,\text{routed sources})$. At prime destinations it uses QR saturation or its completion extension; at composite destinations the retained rule is saturation of the **positive Jacobi kernel**, not the QR subgroup. Promotion extracts a single unknown odd-exponent prime factor only when the other character factors are fixed positive by the class. Its canonical key retains class, exact residues and derived sources; one proof ancestry with required misses is retained. State counts are not counts of disjoint prime classes.

The base positive sources are:

For application to an actual prime, all source and destination character symbols must be nonzero. Restricting $p$ above the finite destination bound is sufficient for the two recorded runs, whose base and root sources are below that bound. Minimality of one/two-source routes is part of the graph rule; adding unrestricted source combinations would define a different finite graph.

| $a_0$ | base sources |
|---:|:---|
|1|7,23|
|121|7,19,23,47|
|169|7,11,23,31|
|289|7,11,23,31,47|
|361|7,23,59|
|529|7,11,23,31|

The eight conditional root extractions are:

| $a_0$ | parent miss | exact routed residues | extracted positive source |
|---:|---:|:---|---:|
|121|39|$p\bmod47=8$|13|
|169|51|$p\bmod11=4,\ p\bmod23=18$|17|
|169|111|$p\bmod23=4$|37|
|289|39|$p\bmod11=5,\ p\bmod47=8$|13|
|289|51|$p\bmod11=4,\ p\bmod23=18$|17|
|289|215|$p\bmod11=5,\ p\bmod31=2$|43|
|529|51|$p\bmod11=4,\ p\bmod23=18$|17|
|529|171|$p\bmod11=5,\ p\bmod23=13$|19|

These are inherited conditional inputs [3,4], not re-proved global facts in this note. The historical and self-contained verifiers agree on the following finite graph results:

| predicate and destination bound | states | edges | new source/class pairs | maximum depth |
|:---|---:|---:|---:|---:|
|ordinary saturation, $k\le1000$|70|66|13|5|
|completion, $k\le1000$|2324|2564|48|10|
|completion, $k\le2000$|2324|2564|48|10|

There are 35 additional conditional pairs and no lost baseline pair. Their exact residues and proof paths are in the fresh JSON report. Equality of the last two finite runs is not closure for arbitrary destination bounds.

The separate prime census records 745 primes and 274 misses for $(a_0,k)=(361,59)$ below $2\cdot10^6$, all with QR support. Below $10^7$, the $(169,71),(289,71),(529,71)$ rows respectively have $(3400,1090,12)$, $(3454,1052,10)$, $(3411,1083,11)$ for (primes, misses, negative misses), with zero violations of the defect and unique-source restrictions. These are finite checks of theorems, not their proofs.

## Appendix B. Earlier cross-shift coverage and negative coupling tests

**Finite classification 24 (preserved refined families; computer-assisted).** Let $p=2041+26040m$ be prime, $m\ge0$. The following two tables retain the earlier whole-progression sufficient certificates on the stated refinements, with their separate universes. Both describe only their specified libraries, not every fixed-shift or affine exit.

First, refining by $p\equiv-k\pmod{67}$ forces $S=67G\mid C_k$ when $G\mid\gcd(6510,(2041+k)/4)$. For Type I use $d=e$; for centered Type II use $d=eC_k/S$.

| $p\bmod67$ | $k$ | $S$ | $e$ | type |
|---:|---:|---:|---:|:---|
|2|199|4690|328300|I|
|7|17279|14070|82075|I|
|8|59|7035|2345|I|
|10|191|12462|4154|I|
|13|255|938|6566|I|
|32|35|201|201|I|
|44|23|402|201|I|
|52|15|134|1|II|
|57|479|14070|5628|I|
|58|143|2814|19698|I|
|59|11599|20770|13915900|I|
|62|4159|20770|25|II|
|66|135|134|1|II|

This table exhausts its specified source-67 seed-shell family: list $e\mid(6510\cdot67)^2$, $k\mid4e+1$ (729 $e$ choices), and $G\mid6510$, $e\mid(67G)^2$, $k\mid e+67G$ (3,072 $(G,e)$ choices), then test forced divisibility and coprimality. All entries are directly proved sufficient by Theorem 1 and block lifting. There remain 23 NQR and 30 QR residues outside this family, so it does not force a character sign at 67.

Second, apply Lemma 12 separately on the primitive refinements modulo 67, whose step is 1,744,680. Enumerating $Q\mid L$, $Q\equiv3\pmod4$, $e\mid((Q+1)/4)^2$ gives 264 pairs. The covered residues are $3,14,20,32,43,44,45,50,53,57,60,63,66$. Four overlap the preceding table and residue 63 already has a fixed-67 Type-II hit ($C_{67}\equiv-1$). The eight additional rows are:

| $p\bmod67$ | $Q$ | $u$ | $e$ | $K$ |
|---:|---:|---:|---:|:---|
|3|335|84|16|$(p+64)/335$|
|14|6231|1558|164|$(p+656)/6231$|
|20|335|84|196|$(p+784)/335$|
|43|335|84|6|$(p+24)/335$|
|45|335|84|441|$(p+1764)/335$|
|50|67|17|289|$(p+1156)/67$|
|53|335|84|1176|$(p+4704)/335$|
|60|6231|1558|722|$(p+2888)/6231$|

The terminal verifier supplies a prime realization and an exact identity for every row. These formulas use an independent residue refinement and thus are not subsumed by Theorem 17's definition of $\mathcal P_D$. Within the abstract raw-state census, the old family covers 2,041 phase labels and these rows add 1,245, totaling 3,286 and leaving 7,259. These are abstract-label counts, not counts of primes or survivor densities. Factor-specific exits cannot be subtracted as whole phase labels. $\square$

Additional complete affine exclusions from Lemma 12 are retained: the phase-one progression $p'=1173841+1744680n$ has zero hits among 264 pairs; adding actual factors 43 and 197 yields progression $7885382761+14779184280n$ and exactly $(Q,e)=(215,6)$ among 2,044 pairs; replacing 43 by 311 yields $83499813961+106891309560n$ and zero hits among 2,304 pairs. The witness $p_*$ occurs at parameter 44,364 of the last progression. These exclusions require whole-progression validity as defined; they do not forbid pointwise exits.

Negative coupling regressions are also preserved. At $m=1234$, $p=32135401$ misses at 31,59,67 with $T=259157\equiv1\pmod{67}$ prime, so no additional NQR source or signed-set growth is forced; it exits at 479. At $m=222$, $p=5782921$ misses at 31,59,191 although $U=3\cdot2591$ has only QR factors modulo 191. At $m=25354$, $p=660220201$ misses at 31,59,67 and at shifts $191,439,563,3167,10979,76079,23999,50039$, but has the prescribed 479 exit. Its exact denominators there are $165055170$, $5121715887414699762$, $227510643359055$. These refute the respective automatic coupling proposals, not ES.

Exploratory bounded searches and their stopping rules remain in `sources/workspace/work/`. In particular, the old prime-factor scan through 2000 found six surviving triggers among 297 tested primes; that is historical finite evidence and is superseded, as a coverage list, by the seven-factor theorem. No unbounded conclusion is imported from search scripts that stopped after the first examples.

## Appendix C. Independent coprime totient-sum result

**Theorem 25 (two-parameter totient asymptotic).** For real $J\to\infty$,

$$W(J)=\sum_{\substack{1\le u,a\le J\\(u,a)=1}}\frac1{\varphi(4ua)}
\sim\frac9{2\pi^2}(\log J)^2.$$

**Proof.** For $\Re s,\Re t>0$ the two-variable Dirichlet series has an absolutely convergent Euler product. Set $x=\ell^{-1-s},y=\ell^{-1-t}$. At an odd prime its local factor is

$$1+\frac\ell{\ell-1}\left(\frac x{1-x}+\frac y{1-y}\right),$$

since coprimality allows positive exponent on at most one variable. At 2 it is $\tfrac12(1+x/(1-x)+y/(1-y))$. Factoring out $\zeta(1+s)\zeta(1+t)$ gives a regular product $H(s,t)$ with

$$H_\ell=1+\frac{x+y}{\ell-1}-\frac{\ell+1}{\ell-1}xy\quad(\ell>2),
\qquad H_2=\frac12-\frac18\,2^{-s-t}.$$

Write $H(s,t)=\sum h(d,e)d^{-s}e^{-t}$. For any fixed $0<\eta<1/2$ its absolute coefficient sum with weights $d^\eta e^\eta$ is finite: each odd local contribution is $1+O(\ell^{-2+\eta}+\ell^{-2+2\eta})$. Coefficient convolution therefore gives

$$W(J)=\sum_{d,e\le J}h(d,e)\,\mathsf H_{\lfloor J/d\rfloor}\mathsf H_{\lfloor J/e\rfloor},$$

where $\mathsf H_n$ is a harmonic number. For each fixed $d,e$ the product divided by $(\log J)^2$ tends to 1. Extend the summand by zero outside $d,e\le J$; for $J\ge3$ each normalized harmonic factor is at most 2. Absolute summability permits dominated convergence, giving limit $H(0,0)$. Finally

$$H(0,0)=\frac38\prod_{\ell>2}(1+\ell^{-2})
=\frac38\frac{12}{\pi^2}=\frac9{2\pi^2},$$

using $\prod_\ell(1+\ell^{-2})=\zeta(2)/\zeta(4)$. $\square$

The constant is $0.45594532639052\ldots>0.45$, so $W(J)\ge0.45(\log J)^2$ eventually, without an explicit threshold here. Dahan [2, Lemma 4.22 and Section 7] records the lower coefficient $3/(2\pi^2)$ and asks for a coefficient at least 0.45. This comparison concerns that preprint; it is not a global priority claim or an audit of its other results. The theorem is independent of the terminal-state argument. Finite checks include the exact value $W(25)=13932881/1900800$ and the four historical normalized values near $0.62795,0.59503,0.57114,0.55559$ at $J=100,300,1000,3000$; convergence is proved above, not inferred from those values.

## References

1. Thomas F. Bloom and Christian Elsholtz, *Egyptian fractions*, Nieuw Archief voor Wiskunde, 5/23(4), 2022, pp. 237–245, especially Theorem 1 and the classical congruence families. [Author-hosted article](https://www.math.tugraz.at/~elsholtz/WWW/papers/bloom-elsholtz-naw5-2022-23-4-237.pdf).
2. Benjamin Dahan, *Sieve dimension and search depth for the Erdős–Straus conjecture, $n\equiv1\pmod{24}$*, arXiv:2608.24035v1, 25 August 2026. [Versioned text](https://arxiv.org/html/2608.24035v1).
3. CENTL public research record, *QR-saturating seeds and routed rigidity upgrades*. [Public source](https://github.com/chasebryan/centl/blob/main/research/erdos-straus/QR-SATURATING-ROUTED-SEEDS.md). Mutable repository reference; the internal extension is compared with the audited framework, without a global novelty claim.
4. CENTL public research record, *Recursive character promotion*. [Public source](https://github.com/chasebryan/centl/blob/main/research/erdos-straus/RECURSIVE-CHARACTER-PROMOTION.md). The preserved local classifier snapshot is `sources/workspace/work/public_recursive.py`; no upstream commit identity is inferred from that copy.

The uniform affine Type-II phase is now classified and exhausted on the stated $k=67$ branch, but a universal exit from every admissible arithmetic terminal state is still unproved; the Erdős–Straus conjecture remains open.
