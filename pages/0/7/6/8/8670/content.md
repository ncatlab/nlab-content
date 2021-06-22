
#Contents#
* table of contents
{:toc}

## Idea

In the preprints listed at _[[inter-universal Teichmüller theory]]_, [[Shinichi Mochizuki]] has claimed, in particular, a proof of the _[[abc conjecture]]_. Over the years, the proposed proof has been met with a fair amount of scepticism from various authors, some of which is referenced below.

## Reactions

### Dimitrov's commentary
  
> The following is verbatim quoted from [Dimitrov 2012](#Dimitrov12).

***

**Completely rewritten. (9/26)**

It seems indeed that nothing like Theorem 1.10 from Mochizuki's IUTT-IV could hold. 

Here is an infinite set of counterexamples, assuming for convenience two standard conjectures (the first being in fact a consequence of ABC), that contradict Thm. 1.10 *very* badly. 

*Assumptions:* 

- A (Consequence of ABC) *For all but finitely many elliptic curves over $\mathbb{Q}$, the conductor $N$ and the minimal discriminant $\Delta$ satisfy $\log{|\Delta|} \lt (\log{N})^2$.*

- B (Uniform Serre Open Image conjecture) *For each* $d \in \mathbb{N}$, *there is a constant* $c(d) \lt \infty$ *such that for every number field* $F/\mathbb{Q}$ with $[F:\mathbb{Q}] \leq d$, *and every
     non-CM elliptic curve* $E$ *over* $F$, *and every prime* $\ell \geq c(d)$, *the Galois representation of* $G_F$ *on* $E[\ell]$ *has full image* $\mathrm{GL}_2(\mathbb{Z}/{\ell})$. (In fact, it is sufficient to take the weaker version in which $F$ is held fixed. )

Further, as far as I can tell from the proof of Theorem 1.10 of IUTTIV, the only reason for taking $F \coloneqq F_{\mathrm{tpd}}\big( \sqrt{-1}, E_{F_{\mathrm{tpd}}}[3\cdot 5]
 \big)$ --- rather than simply $F \coloneqq F_{\mathrm{tpd}}(\sqrt{-1})$ --- was to ensure that $E$ has semistable reduction over $F$. *Since I will only work in what follows with semistable elliptic curves over* $\mathbb{Q}$, *I will assume, for a mild technical convenience in the examples below, that for elliptic curves already semistable over* $F_{\mathrm{tpd}}$, *we may actually take* $F \coloneqq F_{\mathrm{tpd}}(\sqrt{-1})$ *in Theorem 1.10.*


*The infinite set of counterexamples.* They come from Masser's paper *Masser: Note on a conjecture of Szpiro, *Asterisque* 1990*, as follows. Masser has produced an infinite set of Frey-Hellougarch (i.e., semistable and with rational 2-torsion) elliptic curves over $\mathbb{Q}$ whose conductor $N$ and minimal discriminant $\Delta$ satisfy
\[
\label{eqone}
\frac{1}{6}\log{|\Delta|} \geq \log{N} + \frac{\sqrt{\log{N}}}{\log{\log{N}}}.
\]
(Thus, $N$ in these examples may be taken arbitrarily large. ) By (A) above, taking $N$ big enough will ensure that
\[
\label{eqtwo}
\log{|\Delta|} \lt (\log{N})^2.
\]
Next, the sum of the logarithms of the primes in the interval $\big( (\log{N})^2, 3(\log{N})^2 \big)$ is $2(\log{N})^2 + o((\log{N})^2)$, so it is certainly $\gt (\log{N})^2$ for $N \gg 0$ big enough.  Thus, by \eqref{eqtwo}, it is easy to see that the interval $\big( (\log{N})^2, 3(\log{N})^2 \big)$ contains a prime $\ell$ which divides neither $|\Delta|$ nor any of the exponents $\alpha = \mathrm{ord}_p(\Delta)$ in the prime factorization $|\Delta| = \prod p^{\alpha}$ of $|\Delta|$.

Consider now the pair $(E,\ell)$: it has $F_{\mathrm{mod}} = \mathbb{Q}$, and since $E$ has rational $2$-torsion, $F_{\mathrm{tpd}} = \mathbb{Q}$ as well. Let $F \coloneqq \mathbb{Q} \big(
\sqrt{-1}\big)$. I claim that, upon taking $N$ big enough, the pair $(E_F,\ell)$ arises from an **initial $\Theta$-datum** as  in IUTT-I, Definition 3.1. Indeed:

- Certainly (a), (e), (f) of IUTT-I, Def. 3.1 are satisfied (with appropriate $\underline{\mathbb{V}}, \, \underline{\epsilon}$);
- (b) of IUTT-I, Def. 3.1 is satisfied since by construction $E$ is semistable over $\mathbb{Q}$;
- (c) of IUTT-I, Def. 3.1 is satisfied, in view of (B) above and the choice of $\ell$, as soon as $N \gg 0$ is big enough (recall that $\ell \gt (\log{N})^2$ by construction!), and by the observation that, for $v$ a place of $F = \mathbb{Q}(\sqrt{-1})$, the order of the $v$-adic $q$-parameter of $E$ equals $\mathrm{ord}_v (\Delta)$, which equals $\mathrm{ord}_p(\Delta)$ for $v \mid p \gt 2$, and $2\cdot\mathrm{ord}_2(\Delta)$ for $v \mid 2$; 

while $\mathbb{V}_{\mathrm{mod}}^{\mathrm{bad}}$ consists of the primes dividing $\Delta$;

- Finally, (d) of IUTT-I, Def. 3.1 is satisfied upon excluding at most four of Masser's examples $E$. (See page 37 of IUTT-IV).


**Now**, take $\epsilon \coloneqq \big( \log{N} \big)^{-2}$ in Theorem 1.10 of IUTT-IV; this is certainly permissible for $N \gg 0$ large enough. *I claim that the conclusion of Theorem 1.10 contradicts \eqref{eqone} as soon as $N \gg 0$ is large enough.*

For note that Mochizuki's quantity $\log(\mathfrak{q})$ is precisely $\log{|\Delta|}$ (reference: see e.g. Szpiro's article in the Grothendieck Festschrift, vol. 3); his $\log{(\mathfrak{d}^{\mathrm{tpd}})}$ is zero; his $d_{\mathrm{mod}}$ is $1$; and his $\log{(\mathfrak{f}^{\mathrm{tpd}})}$ is our $\log{N}$. By construction, our choice $\epsilon \coloneqq \big( \log{N} \big)^{-2}$ then makes $1/\ell \lt \epsilon$ and $\ell \lt 3/\epsilon$, whence the finaly display of Theorem 1.10 would yield
$$
\frac{1}{6} \log{|\Delta|} \leq (1+29\epsilon) \cdot \log{N} + 2\log{(3\epsilon^{-8})}
\lt \log{N} + 16\log{\log{N}} + 32,
$$
where we have used $\epsilon \log{N} = (\log{N})^{-1} \lt 1$ for $N \gt 3$, and $2\log{3} \lt 3$.



*The last display contradicts \eqref{eqone} as soon as $N \gg 0$ is big enough.*



Thus Masser's examples yield infinitely many counterexamples to Theorem 1.10 of IUTT-IV (as presently written).




**Added on 10/15.** Mochizuki has commented on the apparent contradiction between Masser's examples and Theorem 1.10: 

&lt;http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20IV%20(comments).pdf>

(Point (4.) in those Comments was subsequently modified twice. ) He writes that he will revise portions of IUTT-III and IUTT-IV, and will make them available in the near future. Taking into account the latest version of point (4.) from Mochizuki's Comments, here is the anticipated revised version of Theorem 1.10 (after taking $\epsilon \sim 1/\ell$ - which is essentially optimal - and not worrying about the best constants or the most general version):

Take the pair $(E,\ell)$, where $E/\mathbb{Q}$ is a semistable elliptic curve with (say, for the sake of simplifying) rational $2$-torsion (i.e., a Frey-Hellegouarch curve) of minimal discriminant $\Delta$ and conductor $N$ (square-free). Assume that:

- $\ell$ divides neither $N$ nor the any of the exponents in the prime factorization of $\Delta$;
- The Galois representation of $G_{\mathbb{Q}(\sqrt{-1})}$ on $E[\ell]$ has full image $\mathrm{GL}_2(\mathbb{Z}/\ell)$. (*Conjecturally, this condition should only exclude a finite list of values of $\ell$, independent of $E$. Therefore, it does not appear to be an essential condition here.*)
- The $2$-adic valuation of $\Delta$ is bounded. (*Assume this for simplicity in the statement below. It is not truly an essential condition either*).
- $\ell = O(\log{N})$ (Such a choice, compliant with the three previous conditions, can be ensured; see Section 2 in IUTT-IV, or the paper [GenEll]).

Let $M \coloneqq \prod_{p \mid N,  p \lt \ell} p$. *Then*, with the corrections outlined by Mochizuki, the revised Theorem 1.10 should essentially read (and certainly *imply*):
$$
\frac{1}{6} \log{\Delta} \lt \Big( 1 + \frac{200}{\ell} \Big) \log{N}  + \omega(M) \cdot \log{\log{N}} - \log{M} + O\big( \log{\log{N}} \big),
$$
where $\omega(\cdot)$ denotes "number of prime factors." If we take $\ell \sim \log{N}$ and $\omega(M)$ bounded (i.e., restrict to conductors $N$ which are only divisible by a bounded number of primes $\lt \log{N}$), then this consequence would yield $(1/6) \log{\Delta} \lt \log{N} + O(\log{\log{N}})$. (*Must this be true for $N$ a large enough square-free integer such that the number of primes $\lt \log{N}$ dividing $N$ is bounded*? A reminder: in terms of the $abc$-triple, $\Delta$ is *essentially* $(abc)^2$, and $N = \mathrm{rad}(abc)$).

A side remark: note that the inverse $1/\ell$ of the prime level from the de Rham-Etale correspondence $(E^{\dagger}, \lt \ell) \leftrightarrow E[\ell]$ in Mochizuki's "Hodge-Arakelov theory" ultimately figures as the $\epsilon$ in the ABC conjecture. 


*(I have deleted the remainder of the 10/15 Addendum, since it is now obsolete after Mochizuki's revised comments.)*

**Added on 3-13-13.** Mochizuki has posted revisions of his second and third papers on Inter-Universal Teichmuller Theory. They can be found at the bottom of his webpage [here](http://www.kurims.kyoto-u.ac.jp/~motizuki/papers-english.html).

***

> end of verbatim quote from [Dimitrov 2012](#Dimitrov12).


### Scholze & Stix's comment

See [Scholze & Stix 2018](#ScholzeStix18).


## Related entries

* [[abc conjecture]]

* [[Mochizuki's corollary 3.12]]

## References

For [[Shinichi Mochizuki]]'s proposed proof see the references at *[[inter-universal Teichmüller theory]]*.

Commentary on this proof by other authors:

* {#Dimitrov12} Vesselin Dimitrov, MO comment 2012 ([MO:a/107279](https://mathoverflow.net/a/107279/381))

* {#ScholzeStix18} [[Peter Scholze]], [[Jakob Stix]], _Why abc is still a conjecture_, 2018 ([pdf](https://ncatlab.org/nlab/files/why_abc_is_still_a_conjecture.pdf))

