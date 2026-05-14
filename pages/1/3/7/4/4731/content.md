

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


\tableofcontents

## Idea

The notion of _connection on a 2-bundle_ generalizes the notion of [[connection on a bundle]] from [[principal bundle]]s to [[principal 2-bundle]]s / [[gerbe]]s.

It comes with a notion of [[higher parallel transport|2-dimensional parallel transport]].

For an exposition of the concepts here see also at _[[infinity-Chern-Weil theory introduction]]_ the section _[Connections on principal 2-bundles](http://ncatlab.org/nlab/show/infinity-Chern-Weil%20theory%20introduction#ConnectionOn2Bundle)_ .

## Definition

For $G$ a [[Lie 2-group]], a _connection_ on a $G$-[[principal 2-bundle]] coming from a [[cocycle]] $g : X \to \mathbf{B}G$ is a lift of the cocycle to the  [[2-groupoid of Lie 2-algebra valued forms]] $\mathbf{B}G_{conn}$

$$
  \array{
     && \mathbf{B}G_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow & \downarrow
     \\
     X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

## Properties

### On trivial 2-bundles

When the underlying [[principal 2-bundle]] over a [[smooth manifold]] $X$ is topologically trivial, then the connections on it are identified with [[Lie 2-algebra valued differential forms]] on $X$.

Recall from the discussion there what such form data looks like.

Let $\mathfrak{g}$ be some [[Lie 2-algebra]]. For instance for discussion of connections on $G$-[[gerbe]]s ($G$ a [[Lie group]]) this would be the [[automorphism 2-group|derivation Lie 2-algebra]] of the [[Lie algebra]] of $G$.

Let $\mathfrak{g}_0$ and $\mathfrak{g}_1$ be the two vector spaces involved and let

$$
  \{t^a\} \,, \;\;\; \{b^i\}
$$

be a dual basis, respectively. The structure of a Lie 2-algebra is conveniently determined by writing out the most general [[Chevalley-Eilenberg algebra]] 

$$
  CE(\mathfrak{g}) \in cdgAlg_\mathbb{R}
$$

with these generators.

We thus have

$$
  d_{CE(\mathfrak{g})} t^a = - \frac{1}{2}C^a{}_{b c} t^b \wedge t^c - r^a{}_i b^i
$$

$$
  d_{CE(\mathfrak{g})} b^i = -\alpha^i_{a j} t^a \wedge b^j  
    - 
    r^i{}_{a b c} t^a \wedge t^b \wedge t^c
  \,,
$$

for collections of structure constants $\{C^a{}_{b c}\}$ (the bracket on $\mathfrak{g}_0$) and $\{r^i_a\}$ (the differential $\mathfrak{g}_1 \to \mathfrak{g}_0$) and $\{\alpha^i{}_{a j}\}$ (the [[action]] of $\mathfrak{g}_0$ on $\mathfrak{g}_1$) and $\{r_{a b c}\}$ (the "Jacobiator" for the bracket on $\mathfrak{g}_0$).

These constants are subject to constraints (the weak [[Jacobi identity]] and its higher [[coherence law]]s) which are precisely equivalent to the condition

$$
  (d_{CE(\mathfrak{g})})^2 = 0
  \,.
$$

Over a test space $U$ a $\mathfrak{g}$-valued form datum is a morphism

$$
  \Omega^\bullet(U) \leftarrow W(\mathfrak{g}) 
   : 
  (A,B)
$$

from the [[Weil algebra]] $W(\mathfrak{g})$.

This is given by a 1-form

$$
  A \in \Omega^1(U, \mathfrak{g}_0)
$$

and a 2-form

$$
  B \in \Omega^2(U, \mathfrak{g}_1)
  \,.
$$

The [[curvature]] of this is $(\beta, H)$, where the 2-form component ("fake curvature") is

$$
  \beta^a = d_{dR} A^a + \frac{1}{2}C^a{}_{b c} A^b \wedge A^c
  + r^{a}_{i} B^i
$$

and whose 3-form component is 

$$
  H^i
     = 
   d_{dR} B^i
   +
   \alpha^i{}_{a j} A^a \wedge B^j
   +
   r^i{}_{a b c} A^a \wedge A^b \wedge A^c
  \,.
$$


### Differential &#268;ech cocycle data

We spell out the data of a connection on a 2-bundle over a [[smooth manifold]] $X$ with respect to a given [[open cover]] $\{U_i \to X\}$, following 
([FSS](#FSS), [SchreiberCohesive](#SchreiberCohesive))

(...)

## Examples

* A [[differential string structure]] (untwisted) is a 2-connection with coefficients in the [[string 2-group]] / [[string Lie 2-algebra]].

* The [[worldvolume]] theory of the [[fivebrane]] is expected to be a [[6d (2,0)-supersymmetric QFT]] containing a [[self-dual higher gauge theory]] whose fields are 2-connections (see _[Self-dual 2-connections](http://ncatlab.org/nlab/show/NS5-brane#SelfDual2Connections)_ there).

* A connection on a [[twisted vector bundle]] is naturally a 2-connection.

## Related concepts

* [[connection on a bundle]]

* **connection on a 2-bundle** / [[connection on a gerbe]] / [[connection on a bundle gerbe]]

  * [[2-groupoid of Lie 2-algebra valued forms]]

* [[connection on a 3-bundle]] / [[connection on a bundle 2-gerbe]]

* [[connection on an ∞-bundle]]

* [[parallel transport]], [[higher parallel transport]]

* [[holonomy]]


## References

### General

Connections on 2-bundles with vanishing 2-form curvature and arbitrary 3-form curvature are defined in terms of their [[higher parallel transport]] are discussed in

* [[Urs Schreiber]],  [[Konrad Waldorf]]: _Smooth Functors vs. Differential Forms_, Homology, Homotopy Appl. **13** 1 (2011) 143--203 &lbrack;[doi:10.4310/HHA.2011.v13.n1.a7](https://dx.doi.org/10.4310/HHA.2011.v13.n1.a7), [arXiv:0802.0663 math.DG](http://arxiv.org/abs/0802.0663)&rbrack;

* [[Urs Schreiber]],  [[Konrad Waldorf]]: *Connections on non-abelian gerbes and their holonomy*, Theory and Applications of Categories **28** 17 (2013) 476--540 &lbrack;[tac:28-17](http://www.tac.mta.ca/tac/volumes/28/17/28-17abs.html), [arXiv:0808.1923 math.DG](http://arxiv.org/abs/0808.1923), <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">web</a>&rbrack;

expanding on:

* [[John Baez]], [[Urs Schreiber]]: *Higher Gauge Theory*, in: *Categories in Algebra, Geometry and Mathematical Physics*, Contemporary Mathematics **431**, AMS (2007) 7-30 &lbrack;[arXiv:math/0511710 math.DG](http://arxiv.org/abs/math/0511710), [doi:10.1090/conm/431](https://doi.org/10.1090/conm/431) [ams:conm-431](https://bookstore.ams.org/conm-431)&rbrack;

Further discussion and illustration and relation to [[tensor networks]]:

* {#Parzygnat18} [[Arthur Parzygnat]]: _Two-dimensional algebra in lattice gauge theory_, Journal of Mathematical Physics **60** 043506 (2019) &lbrack;[arXiv:1802.01139](https://arxiv.org/abs/1802.01139), [doi:10.1063/1.5078532](https://doi.org/10.1063/1.5078532)&rbrack;



Examples of 2-connections with vanishing 2-form curvature obtained from [[geometric quantization]] are discusssed in

* Olivier Brahic, _On the infinitesimal Gauge Symmetries of closed forms_ ([arXiv](http://arxiv.org/abs/1010.2189))

The [[cocycle]] data for 2-connections with coeffcients in [[automorphism 2-group]]s but without restrictions on the 2-form curvature  have been proposed in 

* [[Lawrence Breen]], [[William Messing]], _Differential Geometry of Gerbes _ Advances in Mathematics, Volume 198, Issue 2, 20 (2005) ([arXiv:math/0106083](http://arxiv.org/abs/math/0106083))

* [[Lawrence Breen]], _Differential Geometry of Gerbes and Differential Forms_ ([arXiv:0802.1833](http://arxiv.org/abs/0802.1833))

and 

* [[Paolo Aschieri]], Luigi Cantini, [[Branislav Jurco]], _Nonabelian Bundle Gerbes, their Differential Geometry and Gauge Theory_ , Communications in Mathematical Physics Volume 254, Number 2 (2005) 367-400,([arXiv:hep-th/0312154](http://arxiv.org/abs/hep-th/0312154)).


A discussion of general (non fake-flat, now called "[[adjusted Weil algebra|adjusted]]") local 2-connections:

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:L-infinity algebra connections|$L_\infty$-connections and applications to String- and Chern-Simons $n$-transport]]_, in *Quantum Field Theory*, Birh&auml;user (2009) 303--424 &lbrack;[doi:10.1007/978-3-7643-8736-5_17](https://doi.org/10.1007/978-3-7643-8736-5_17), [arXiv:0801.3480](http://arxiv.org/abs/0801.3480)&rbrack;

and their globalization:

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech cocycles for differential characteristic classes]]_, Advances in Theoretical and Mathematical Physics, **16** 1 (2012) 149--250 &lbrack;[doi:10.4310/ATMP.2012.v16.n1.a5](https://dx.doi.org/10.4310/ATMP.2012.v16.n1.a5), [arXiv:1011.4735 math.AT](https://arxiv.org/abs/1011.4735)&rbrack;

* {#SchreiberCohesive} [[Urs Schreiber]]: *[[schreiber:differential cohomology in a cohesive topos]]*
  (cf. [[connection on an infinity-bundle]] for more general discussion)

Discussion of the [[adjusted Weil algebra|adjusted]] version (see there for more) in terms of [[crossed modules]]:

* {#KimSaemann20} [[Hyungrok Kim]], [[Christian Saemann]], *Adjusted Parallel Transport for Higher Gauge Theories*, J. Phys. A **52** (2020) 445206 &lbrack;[arXiv:1911.06390](https://arxiv.org/abs/1911.06390), [doi:10.1088/1751-8121/ab8ef2](https://doi.org/10.1088/1751-8121/ab8ef2)&rbrack;

* [[Dominik Rist]], [[Christian Saemann]], [[Martin Wolf]]: *Explicit Non-Abelian Gerbes with Connections*, J. Phys. A **59** (2026) 035201 &lbrack;[doi:10.1088/1751-8121/ae2e60](https://doi.org/10.1088/1751-8121/ae2e60), [arXiv:2203.00092 math.AT](https://arxiv.org/abs/2203.00092)&rbrack;

* [[Konrad Waldorf]]: *Adjusted connections on non-abelian bundle gerbes* \[<a href="https://arxiv.org/abs/2604.24513">arXiv:2604.24513 math.DG</a>\]


### Applications to physics

Nonabelian 2-connections appear for instance as [[orientifold]] [[B-fields]] in [[type II string theory]], as [[differential string structure]] in [[heterotic string theory]], and as fields in non-abelian [[7-dimensional Chern-Simons theory]]. See at these pages for references.

An appearance in 4-dimensional [[Yang-Mills theory]] and [[4d TQFT]] is reported in 

* [[Sergei Gukov]], [[Anton Kapustin]], _[[Topological Quantum Field Theory, Nonlocal Operators, and Gapped Phases of Gauge Theories]]_ ([arXiv:1307.4793](http://arxiv.org/abs/1307.4793))
 {#GukovKapustin13}


[[!redirects connections on a 2-bundle]]
[[!redirects connections on 2-bundles]]

[[!redirects 2-connection]]
[[!redirects 2-connections]]

[[!redirects principal 2-connection]]
[[!redirects principal 2-connections]]


[[!redirects connection on a principal 2-bundle]]

[[!redirects principal 2-bundle with connection]]
[[!redirects principal 2-bundles with connection]]

