
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--



\tableofcontents


## Idea

An $n$-fold [[iterated loop space]] $\Omega^n X$ canonically carries the structure of an [[En-algebra|$E_n$-algebra]] (an [[algebra over an operad|algebra over]] the [[little n-disk operad]] $\mathcal{C}_n$) with [[symmetric group|$Sym(k)$]]-[[equivariant map|equivariant]] structure maps

$$
  \mathcal{C}_n(k)
  \times_{Sym(k)}
  \big(
    \Omega^n X
  \big)^k
  \overset{\mu_k}{\longrightarrow}
  \Omega^n X
  \,.
$$

Passing to [[ordinary homology|ordinary]] [[homology of loop spaces|homology of the loop space]] with [[coefficients]] in a [[finite field]], $H_\bullet\big( \Omega^n X; \mathbb{F}_p \big)$, the *Dyer-Lashof operations* are essentially the pushforward/images in homology under the binary operation $\mu_2$

$$
  H_\bullet\big(
    \mathcal{C}_n(2)
    \times_{Sym(2)} 
    (\Omega^n X)^2
    ;
    \mathbb{F}_p
  \big)
  \overset
    { (\mu_2)_\ast }
    {\longrightarrow}
  H_\bullet\big(
    \Omega^n X;
    \mathbb{F}_p
  \big)
  \mathrlap{\,.}
$$

or rather, this map precomposed with 

$$
  \begin{array}{ccc}
    H_i\big(
     \mathcal{C}_n(2)/Sym(2)
     ;
     \mathbb{F}_p
    \big)
    \times
    H_q\big(
      \Omega^n X
     ;
     \mathbb{F}_p
    \big)
    &
    \overset
      {\phantom{-} \boxtimes \phantom{-}}
      {\longrightarrow}
    &
    H_{i + 2 q}\big(
      \mathcal{C}_n(2)
      \times_{Sym(2)} 
      (\Omega^n X)^2
      ;
      \mathbb{F}_p
    \big)
    \\
    (e_i, x) 
    &\mapsto&
    e_i \boxtimes (x \otimes x)
    \mathrlap{\,.}
  \end{array}
$$

Mote concretely:

$$
  \begin{aligned}
    \mathcal{C}_n(2) 
    & \simeq Conf_2\big(\mathbb{R}^n\big)
    \\
    & \simeq S^{n-1}
  \end{aligned}
$$ 

is [[weak homotopy equivalence|equivalently]] the [[configuration space of points|configuration space of 2 points]] in $\mathbb{R}^n$, which in turn is [[weak homotopy equivalence|equivalently]] the [[n-sphere|$(n-1)$-sphere]] of [[direction of a vector|directions]] between these two points. Therefore

$$
  \mathcal{C}_n(2) \big/ Sym(2)
  \simeq
  \mathbb{R}P^{n-1}
$$

is [[weak homotopy equivalence|equivalently]] the [[real projective space]].

For $p=2$, the [[ordinary homology]] of this space is (cf. [there](real+projective+space#HomologyAndCohomology) and use the [[universal coefficient theorem]]):

$$
  H_i\big(
    \mathbb{R}P^{n-1};
    \mathbb{F}_2
  \big)
  \simeq
  \left\{
  \begin{array}{ll}
    \mathbb{F}_2 & \;\text{for}\; 0 \leq i \leq n-1 
    \\
    0 & \text{otherwise.}
  \end{array}
  \right.
$$ 

Therefore there is a unique homology generator $e_i$ in each degree up to $n-1$. 

Finally, the Dyer-Lashof operations $Q_i$ at the even prime are the above homology maps indexed by these generators:
$$
  \begin{array}{ccc}
    H_q\big(
      \Omega^n X
      ;
      \mathbb{F}_2
    \big)
    &\overset{\phantom{-}Q_i\phantom{-}}{\longrightarrow}&
    H_{i + 2q}\big(
      \Omega^n X
      ;
      \mathbb{F}_2
    \big)
    \\
    x
    &\mapsto&
    (\mu_2)_\ast\big(
      e_i 
        \boxtimes 
      (x \otimes x)
    \big)
    \mathrlap{\,.}
  \end{array}
$$


## Related entries 

* [[power operation]]

* [[homology of loop space|homology of]] [[iterated loop spaces]]


## References

The original articles:

* [[Tatsuji Kudo]], [[Shôrô Araki]]: *Topology of $H_n$-Spaces and $H$-Squaring Operations*, Memoirs of the Faculty of Science, Kyushu University. Series A, Mathematics **10** 2 (1956) 85--120 \[<a href="https://doi.org/10.2206/kyushumfs.10.85">doi:10.2206/kyushumfs.10.85</a>\] 

* [[William Browder]]: *Homology operations and loop spaces*, Illinois J. Math. **4**  3 (1960) 347--357 \[<a href="doi.org/10.1215/ijm/1255456051">http://doi:10.1215/ijm/1255456051</a>\]

* [[Eldon Dyer]], [[Richard Lashof]]: _Homology of Iterated Loop Spaces_,  American Journal of Mathematics **84** 1 (1962) 35--88 \[<a href="https://doi.org/10.2307/2372804">doi:10.2307/2372804</a>, [jstor:2372804](https://www.jstor.org/stable/2372804)\]

Further early discussion:

* [[Goro Nishida]]: *Cohomology operations in iterated loop spaces*, Proc. Japan Acad. **44** 3 (1968) 104--109 \[<a href="doi.org/10.3792/pja/1195521291">doi:10.3792/pja/1195521291</a>\]

The modern reformulation via [[operads]] is hinted at in

* {#May72} [[Peter May]]; §5 in: *The geometry of iterated loop spaces*, Lecture Notes in Mathematics **271**, Springer (1972) &lbrack;[doi:10.1007/BFb0067491](https://link.springer.com/book/10.1007/BFb0067491), scan: [pdf](https://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf), retyped: [pdf](https://www.math.uchicago.edu/~may/BOOKS/gils.pdf)&rbrack;

and expanded on in:

* [[Frederick R. Cohen]], [[Thomas J. Lada]], [[J. Peter May]]:  *The Homology of Iterated Loop Spaces*, Lecture Notes in Mathematics **533**, Springer (1976) \[<a href="https://doi.org/10.1007/BFb0080464">doi:10.1007/BFb0080464</a>\] 

Review:

* [[Guozhen Wang]]: *Dyer-Lashof Operations*, talk slides (2018) &lbrack;[pdf](https://pouiyter.github.io/dyer-lashof.pdf)&rbrack;

* [[Tyler Lawson]]: *$E_n$-ring spectra and Dyer-Lashof operations* \[<a href="https://arxiv.org/abs/2002.03889">arXiv:2002.03889</a>\]

[[!redirects Dyer-Lashof operations]]

[[!redirects Kudo-Araki-Dyer-Lashof operation]]
[[!redirects Kudo-Araki-Dyer-Lashof operations]]

