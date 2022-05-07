
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

The [[Dold-Kan correspondence]] relates [[simplicial groups]] to [[chain complexes]]. The _Eilenberg-Zilber theorem_ says how in this context [[double complexes]] and their [[total complexes]] relate to [[bisimplicial sets|bisimplicial groups]] and their [[diagonal of a bisimplicial set|diagonals]]/[[total simplicial sets]].

Analogously there is also a version of the theorem for bi-cosimplicial abelian groups.

## Statement

###A  version for simplicial abelian groups:

Let $A : \Delta^{op} \times \Delta^{op} \to Ab$ be a [[bisimplicial object|bisimplicial abelian group]]. Write 

* $C_\bullet diag A$ for the [[Moore complex]] of its diagonal simplicial group $diag A : \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{A}{\to} Ab$;

* $Tot (C A)$ for the [[total complex]] of the [[double complex]] obtained by applying the [[Moore complex]] functor on both arguments of $A$.

+-- {: .un_theorem }
###### Theorem
**(Dold-Puppe generalization of Eilenberg-Zilber)**

There is a [[quasi-isomorphism]] (even a chain-[[homotopy equivalence]])

$$
  R : C_\bullet diag (A) \stackrel{\simeq}{\to} Tot C (A)
  \,.
$$

=--

+-- {: .un_remark}
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


Let $A : \Delta \times \Delta \to Ab$ be a bi-cosimplicial abelian group. And let $C : Ab^\Delta \to Ch^\bullet$ the Moore cochain complex functor. Write $C(A)$ for the [[double complex]] obtained by applying $C$ to each of the two cosimplicial directions. Then we have natural isomorphisms in cohomology

+-- {: .un_theorem }
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

### Homology groups of products of topological spaces {#ProdTopSp}

This is the original motivating application.

Let $X$ and $Y$ be two [[topological spaces]]. Their [[chain homology]] complexes $C_\bullet(X)$ and $C_\bullet(Y)$ are the [[Moore complex]]es of the simplicial abelian groups $\mathbb{Z}[Sing X]$ and $\mathbb{Z}[Sing Y]$. So from the Dold-Puppe [[quasi-isomorphism]] $R$ from above we have a [[quasi-isomorphism]] from the [[singular cohomology]] of their [[product topological space]]

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
    & \underoverset{\simeq}{R}{\longrightarrow}
      Tot C_\bullet(\mathbb{Z}[Sing X]) \otimes C_\bullet(\mathbb{Z}[Sing Y])
    \\
    & = Tot C_\bullet(X) \otimes C_\bullet(Y) 
  \end{aligned}
$$

and hence in particular an isomorphism in cohomology.

By following through these maps one can obtain an explicit description of the quasi isomorphism if needs be.


## References

The original reference is

* [[Samuel Eilenberg]], [[Joseph Zilber]], _On Products of Complexes_, Amer. Jour. Math. 75 (1): 200&#8211;204, (1953) ([jstor:2372629](https://www.jstor.org/stable/2372629))

A weak version of the simplicial statement is in theorem 8.1.5 in 

* [[Charles Weibel]], _An introduction to homological algebra_

The stronger version as stated above, published by Dold and Puppe,  in chapter 2 of 

* [[Albrecht Dold]], [[Dieter Puppe]], _Homologie nicht-additiver Funktoren. Anwendungen_, Ann. Inst. Fourier **11** (1961) pp. 201-312. ([numdam:AIF_1961__11__201_0](http://archive.numdam.org/item/AIF_1961__11__201_0), [pdf](http://archive.numdam.org/article/AIF_1961__11__201_0.pdf))

where is is ascribed to [[Pierre Cartier]].  This result is discussed in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

The cosimplicial version of the theorem appears as theorem A.3 in

* L. Grunenfelder and M. Mastnak, _Cohomology of abelian matched pairs and the Kac sequence_ ([arXiv:math/0212124](http://arxiv.org/abs/math/0212124))


The crossed complex  version is given in 

* [[Andy Tonks|A.P. Tonks]], _On the Eilenberg-Zilber Theorem for crossed complexes_. J. Pure Appl. Algebra, 179~(1-2) (2003) 199--220,

(for more detail see Tonks' [thesis](https://groupoids.org.uk/pdffiles/tonksthesis.pdf)),

and on page 360 of [[Nonabelian Algebraic Topology]].