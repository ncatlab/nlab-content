
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[Dold-Kan correspondence]] relates [[simplicial abelian groups]] to [[connective chain complexes]]. The _Eilenberg-Zilber theorem_ says how in this context [[double complexes]] and their [[total complexes]] relate to [[bisimplicial sets|bisimplicial groups]] and their [[diagonal of a bisimplicial set|diagonals]]/[[total simplicial sets]].

Analogously there is also a version of the theorem for bi-cosimplicial abelian groups.

## Statement

### A version for simplicial abelian groups:

Let $A \colon \Delta^{op} \times \Delta^{op} \to Ab$ be a [[bisimplicial object|bisimplicial]] [[abelian group]]. Write 

* $C_\bullet diag A$ for the [[Moore complex]] of its [[diagonal of a bisimplicial set|diagonal]] [[simplicial group]] $diag A \colon \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{A}{\to} Ab$;

* $Tot (C A)$ for the [[total complex]] of the [[double complex]] obtained by applying the [[Moore complex]] functor on both arguments of $A$.

+-- {: .num_theorem }
###### Theorem
**(Dold-Puppe generalization of Eilenberg-Zilber)**

There is a [[quasi-isomorphism]] (even a chain-[[homotopy equivalence]])

$$
  R : C_\bullet diag (A) \stackrel{\simeq}{\to} Tot C (A)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


Notice (see the discussion at [[bisimplicial set]]) that the diagonal simplicial set is isomorphic to the [[nerve and realization|realization]] given by the [[coend]]

$$
  diag F_{\bullet,\bullet} 
  \simeq 
   \int^{[n] \in \Delta} \Delta^n \times F_{n,\bullet}
  \,.
$$

=--


### Cosimplicial version


Let $A : \Delta \times \Delta \to Ab$ be a bi-cosimplicial abelian group. And let $C : Ab^\Delta \to Ch^\bullet$ the Moore cochain complex functor. Write $C(A)$ for the [[double complex]] obtained by applying $C$ to each of the two cosimplicial directions. Then we have [[natural isomorphisms]] in [[cochain cohomology]].

+-- {: .num_theorem }
###### Theorem

There is a [[natural isomorphism]]

$$
  H^\bullet C^\bullet diag(A)
  \simeq
  H^\bullet Tot C^\bullet(A)
$$ 

=--


###Crossed complex version

A version for [[crossed complexes]] is given by [[Andy Tonks]]. We give a summary:

First note that there is a tensor product for crossed complexes developed by Brown and Higgins.  Letting $K$ and $L$ be simplicial sets.

*  There is an Alexander-Whitney diagonal approximation defined as a natural transformation

$$a_{K,L}: \pi(K\times L)\to \pi K \otimes \pi L.$$

* Using [[shuffles]], one defines an Eilenberg - Zilber map

$$b_{K,L}:\pi K \otimes \pi L \to\pi(K\times L), $$

in a somewhat similar way to chain complexes.

*  The composite 

$$\pi(K\times L)\to \pi K \otimes \pi L\to\pi(K\times L), $$

is homotopic to the identity on $\pi(K\times L)$,  whilst the other composite is the identity on $\pi K \otimes \pi L$, thus this is a strong deformation retract  of $\pi(K\times L)$.


###The Eilenberg - Zilber theorem for simplicial sets

Cegarra and Remedios have proved a version of the Eilenberg -  Zilber theorem for simplicial sets.  This is discussed under the entry on [[bisimplicial set]]s.

## Applications 

### Eilenberg-Zilber/Alexaner-Whitney deformation retraction

\begin{proposition}\label{EZAWDeformationRetract}
**([[Eilenberg-Zilber/Alexander-Whitney deformation retraction]])** \linebreak

Let 

* $A, B \,\in\, sAb = $ [[SimplicialAbelianGroups]]

and denote 

* by $N(A), N(B) \,\in\, Ch^+_\bullet = $ [[ConnectiveChainComplexes]] their [[normalized chain complexes]], 

* by $A \otimes B \,\in\, sAb$ the degreewise [[tensor product of abelian groups]],

* by $N(A) \otimes N(B)$ the [[tensor product of chain complexes]].

Then there is a [[deformation retraction]]

\begin{tikzcd}
  N(A) \otimes N(B)
  \ar[
    rr,
    bend right=20,
    "\mathrm{id}"{below},
    "\ "{above, name=t}
  ]
  \ar[
    rr,
    phantom,
    "\ "{name=s, yshift=-6pt}
  ]
  \ar[
    r,
    "\nabla_{A,B}"
  ]
  &
  N( A \otimes B )
  \ar[
    r,
    "\Delta_{A,B}"
  ]
  &
  N(A) \otimes N(B)
  \ar[
    from=s,
    to=t,
    -,
   shift left=1pt
  ]
  \ar[
    from=s,
    to=t,
    -,
   shift right=1pt
  ]
\end{tikzcd}

\begin{tikzcd}
  N( A \otimes B )
  \ar[
    rr,
    bend right=20,
    "\mathrm{id}"{below},
    "\ "{above, name=t}
  ]
  \ar[
    rr,
    phantom,
    "\ "{name=s, yshift=-6pt}
  ]
  \ar[
    r,
    "\Delta_{A,B}"
  ]
  &
  N(A) \otimes N(B)
  \ar[
    r,
    "\nabla_{A,B}"
  ]
  &
  N( A \otimes B )
  \ar[
    from=s,
    to=t,
    Rightarrow
  ]
\end{tikzcd}

where 

* $\nabla_{A,B}$ is the [[Eilenberg-Zilber map]];

* $\Delta_{A,B}$ is the [[Alexander-Whitney map]].

\end{proposition}

For unnormalized chain complexes, where we have a [[homotopy equivalence]], this is the original [[Eilenberg-Zilber theorem]] ([Eilenberg & Zilber 1953](EZAW+deformation+retraction#EilenbergZilber53), [Eilenberg & MacLane 1954, Thm. 2.1](EZAW+deformation+retraction#EilenbergMacLane54)). The above [[deformation retraction]] for normalized chain complexes is [Eilenberg & MacLane 1954, Thm. 2.1a](EZAW+deformation+retraction#EilenbergMacLane54). Both are reviewed in [May 1967, Cor. 29.10](EZAW+deformation+retraction#May67). Explicit description of the [[homotopy operator]] is given in [Gonzalez-Diaz & Real 1999](EZAW+deformation+retraction#GonzalezDiazReal99).


### Homology of products of topological spaces 
 {#ProdTopSp}

The following is the special case of the [[Eilenberg-Zilber/Alexander-Whitney deformation retraction]] (Prop. \ref{EZAWDeformationRetract}) for [[singular simplicial sets]], observing that forming [[free simplicial abelian groups]] preserves monoidal products.
This is the original motivating application in [Eilenberg &Zilber 1953](#EilenbergZilber53)

Let $X$ and $Y$ be two [[topological spaces]]. Their [[singular homology]] [[chain complexes]] $C_\bullet(X)$ and $C_\bullet(Y)$ are the [[Moore complexes]] of the [[simplicial abelian groups]] $\mathbb{Z}[Sing X]$ and $\mathbb{Z}[Sing Y]$ [[free abelian group]] on their [[singular simplicial complexes]]. 

So from the Dold-Puppe [[quasi-isomorphism]] $R$ from above we have a [[quasi-isomorphism]] of [[chain complexes]] of their [[product topological space]]:

$$
  \begin{aligned}
    C_\bullet(X \times Y)
    & \coloneqq
    C_\bullet( \mathbb{Z}[Sing X \times Sing Y] )
    \\
    &=
    C_\bullet( diag \mathbb{Z}[Sing X_\bullet] 
      \otimes \mathbb{Z}[Sing Y_\bullet] )
    \\
    & 
    \underoverset{\;\simeq\;}{R}{\longrightarrow}
      Tot 
      C_\bullet(\mathbb{Z}[Sing X]) \otimes C_\bullet(\mathbb{Z}[Sing Y])
    \\
    & 
    = 
    Tot C_\bullet(X) \otimes C_\bullet(Y) 
  \end{aligned}
$$

and hence in particular an isomorphism in [[singular cohomology]].

By following through these maps one can obtain an explicit description of the quasi isomorphism if need be.

### Transgression in group cohomology

See at *[[transgression in group cohomology]]*.

## References

Original references:

* {#EilenbergZilber53} [[Samuel Eilenberg]], [[Joseph Zilber]], _On Products of Complexes_, Amer. Jour. Math. 75 (1): 200&#8211;204, (1953) ([jstor:2372629](https://www.jstor.org/stable/2372629))

* {#EilenbergMacLane54} [[Samuel Eilenberg]], [[Saunders MacLane]], Section 2 of: *On the Groups $H(\Pi,n)$, II: Methods of Computation*, Annals of Mathematics, Second Series, Vol. 60, No. 1 (Jul., 1954), pp. 49-139 ([jstor:1969702](https://www.jstor.org/stable/1969702), [doi:10.2307/2372629](https://doi.org/10.2307/2372629))

using the definition of the [[Eilenberg-Zilber map]] in:

* {#EilenbergMacLane53} [[Samuel Eilenberg]], [[Saunders MacLane]], (5.3) of: *On the groups $H(\Pi,n)$*, I*, Ann. of Math. (2) 58, (1953), 55&#8211;106. ([jstor:1969820](https://www.jstor.org/stable/1969820))

Review in:


* {#Dold95} [[Albrecht Dold]], Section VI 12.1 in *Lectures on Algebraic Topology*, Springer 1995 ([doi:10.1007/978-3-642-67821-9](https://www.springer.com/gp/book/9783540586609), [pdf](https://link.springer.com/content/pdf/bfm%3A978-3-642-67821-9%2F1.pdf))


A weak version of the simplicial statement: 

* [[Charles Weibel]], Theorem 8.1.5 in: _An introduction to homological algebra_

The stronger version as stated above: 

* [[Albrecht Dold]], [[Dieter Puppe]], Chapter 2 of: _Homologie nicht-additiver Funktoren. Anwendungen_, Ann. Inst. Fourier **11** (1961) pp. 201-312. ([numdam:AIF_1961__11__201_0](http://archive.numdam.org/item/AIF_1961__11__201_0), [pdf](http://archive.numdam.org/article/AIF_1961__11__201_0.pdf))

where is is ascribed to [[Pierre Cartier]].  This result is discussed in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* [[Paul Goerss]], [[J. F. Jardine]], _[[Simplicial homotopy theory]]_ 
([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

The cosimplicial version of the theorem appears as:

* L. Grunenfelder and M. Mastnak, Theorem A.3 in: _Cohomology of abelian matched pairs and the Kac sequence_ ([arXiv:math/0212124](http://arxiv.org/abs/math/0212124))

The crossed complex version is given in 

* [[Andy Tonks|A.P. Tonks]], _On the Eilenberg-Zilber Theorem for crossed complexes_. J. Pure Appl. Algebra, 179~(1-2) (2003) 199--220,

  (for more detail see Tonks' [thesis](https://groupoids.org.uk/pdffiles/tonksthesis.pdf)),

and on page 360 of *[[Nonabelian Algebraic Topology]]*.


