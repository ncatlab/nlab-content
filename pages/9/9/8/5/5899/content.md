
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[monad]] $(T,\mu,\eta)$ is left (resp. right) [[adjoint functor|adjoint]] to a [[comonad]] $(G,\delta,\epsilon)$, if its underlying endofunctor $T$ is _[[left adjoint]]_ (resp. _[[right adjoint]]_) to the underlying [[1-morphism]] $G$ of the comonad, and $\delta$ and $\epsilon$ are conjugate/adjoint/[[mate]] 2-cells to $\mu$ and $\eta$ in the sense explained below.


## Construction

In fact given a [[monad]] $\mathbf{T} = (T,\mu^T,\eta^T)$ which has a _[[right adjoint]]_ $G$, automatically $G$ is a part of a comonad $\mathbf{G} = (G,\delta^G,\epsilon^G)$ where $\delta^G$ and $\epsilon^G$ are in some sense dual to $\mu^T$ and $\eta^T$.

Thus there is a bijective correspondence between monads having a right adjoint and comonads having a left adjoint (and "2-dually" between comonads having a right adjoint and monads having a left adjoint, as explained below). This is little more than a consequence of two general facts: 

1. If $T\dashv G$ then $T^k \dashv G^k$ for every [[natural number]] $k$. 

2. Given two [[adjunctions]] $S\dashv T$ and $S'\dashv T'$ where $S,S': B\to A$, then there is a [[bijection]] between the [[natural transformations]] $\phi:S'\Rightarrow S$ and natural transformations $\psi:T\Rightarrow T'$ such that 

$$
\array{
  A (S,-) &\to& B(-,T)
  \\
  {}^{\mathllap{A(\phi,-)}}\downarrow &&\downarrow {}^{\mathrlap{B(-,\psi)}}
  \\
  A(S',-)&\to & B(-,T')
}
$$

where the horizontal arrows are the natural bijections given by the adjunctions. [Eilenberg & Moore 1965](#EilenbergMoore65) would write $\phi\dashv\psi$ and talk about "adjointness for morphisms" (of functors), which is of course relative to the given adjunctions among functors. MacLane calls the correspondence *conjugation* (p 99-102 in *[[Categories for Working Mathematician]]*).  It is a special case, of a general construction of [[mates]]. 

If $\eta,\eta'$ and $\epsilon,\epsilon'$ are their 
[[unit of an adjunction|unit]] and counit of course the upper arrow is $(S M\stackrel{f}\to N)\mapsto T f\circ \eta_M$ and the lower arrow $(S'M\stackrel{g}\to N)\mapsto T'g\circ\eta'_M$. Thus the condition renders as 

$$T'(f\circ\phi_M)\circ\eta'_M = \psi_N\circ T f\circ\eta_M$$ 

or $T'f\circ T'\phi_M\circ\eta'_M = T'f\circ \psi_{SM}\circ\eta_M$. Given $\phi$, the uniqueness of $B(-,\psi)$ is clear from the above [[diagram]], as the horizontal arrows are [[isomorphism|invertible]]. $B(-,\psi)$ determines $\psi$, namely $\psi_N = B(-,\psi)(id_N)$. For the existence of $\psi$ (given $\phi$) satisfying the above equation, one proposes that $\psi$ is the composition
$\psi  = T'\epsilon \circ T'\phi T \circ \eta'T$, i.e.

$$
T\stackrel{\eta' T}\longrightarrow T'S' T\stackrel{T'\phi T}\longrightarrow T' S T \stackrel{T'\epsilon}\longrightarrow T'
$$
and checks that it works. The inverse is similarly given by the composition
$$
S'\stackrel{S'\eta}\longrightarrow S' T S\stackrel{S'\psi S}\longrightarrow S'T'S\stackrel{\epsilon' S}\longrightarrow S
$$

This correspondence now enables in our special case to dualize $\mu^T$ to $\delta^G$, and similarly unit to the counit. 

## Duality

The construction above easily dualises to a bijection between *comonads* on $\mathcal{C}$ having a *right* adjoint and *monads* having a *left* adjoint. However, 1-categorical duality is not enough to analyse this: in the [[opposite category]] $\mathcal{C}^{op}$, monads and comonads are swapped and so are left and right adjoints (see [[opposite adjunction]]); thus we still get a correspondence between comonads having a left adjoint and monads having a right adjoint.

Instead, as explained in [math.SE:a/3564754](https://math.stackexchange.com/a/3564754), one can generalise the construction above to [[monads]] and [[adjunctions]] in any [[2-category]]; the special case under consideration here being **[[Cat]]**. The dual construction then follows by instantiating the construction in $\mathbf{Cat}^{op}$, the [[1-cell dual]] of $\mathbf{Cat}$: this swaps left and right adjoints but leaves monads and comonads unchanged.

## Examples


\begin{example}\label{AdjointMonadsInducedFromAdjointTriples}
**(adjoint monads induced from adjoint triples of adjoint functors)**
\linebreak
Every [[adjoint triple]] (of [[adjoint functors]]) $F^*\dashv F_* \dashv F^!$ [induces](monad#RelationBetweenAdjunctionsAndMonads) an [[adjoint pair]] $F_* F^*\dashv F_* F^!$. The endofunctor $F_* F^*$ is underlying a monad induced by the adjunction $F^*\dashv F_*$ and $F_* F^!$ is underlying a comonad induced by the adjuntion $F_*\dashv F^!$. This pair of a monad and a comonad are adjoint. 
\end{example}

(See also at *[[adjoint modality]]*.)

## Properties

### General

\begin{proposition}
\label{IsomorphismOfEMCategories}
 Given an [[adjoint functor|adjoint pair]] of a [[monad]] and comonad

$$
  \lozenge \,\dashv\, \Box
$$

on some category $\mathcal{C}$, then there is an [[equivalence of categories|equivalence]] between their [[Eilenberg-Moore categories]] of [[algebra over a monad|algebras]] over $\lozenge$ and [[coalgebra over a comonad|coalgebras]] over $\Box$, compatible with their [[forgetful functors]] to $\mathcal{C}$:

\begin{tikzcd}[column sep=-1pt]
  \mathrm{EM}(\lozenge)
  \ar[dr, "{ U }"{swap}]
  \ar[rr, "{\sim}"]
  &&
  \mathrm{EM}(\Box)
  \ar[dl, "{ U }"]  
  \\
  &
  \mathcal{C}
\end{tikzcd}
\end{proposition}
This is due to [Eilenberg & Moore 1965](#EilenbergMoore65), where it is implied by the last part of Prop. 3.3. In the more explicit form above the statement may be found in [MacLane & Moerdijk 1992, Thm. 2 on p. 249](#MacLaneMoerdijk92),


### General adjoint (co)algebras $End(A)$

Given a [[small category]] $A$, the [[endofunctor category]] $End(A)$ (of [[endofunctors]] and [[natural transformations]] between them, with [[vertical composition]] as [[composition]]) is [[monoidal category|monoidal]] with respect to the composition as the tensor product of objects (endofunctor) and Godement product ([[horizontal composition]]) as the [[tensor product]] of morphisms (natural transformations). Hence we can consider [[operads]] and [[algebras over operads]], as well as, dually, coalgebras over cooperads; or some other framework for general algebras and coalgebras (or even props). 

In any case, given an adjunction $T\dashv G$, operations $T^n\to T$ dualize to cooperations $G\to G^n$, and more generally multioperations $T^k\to T^l$ dualize to the multioperations $G^l\to G^k$. We would like to sketch the proof that the identities for operations on $T$, correspond to the identities on cooperations on $G$ (and more generally there is a duality among the identities for multioperations). This is essentially the consequence of 

__Lemma.__ ([[Zoran Škoda|Zoran]]) Given the adjunction $T\dashv G$ with unit $\eta$ and counit $\epsilon$, and the sequence

$$
T^k \stackrel{\alpha}\longrightarrow T^l\stackrel\beta\longrightarrow T^s
$$

the composition $\alpha^*\circ\beta^*$ of the dual (in the above sense) sequence

$$
G^k \stackrel{\alpha^*}\longleftarrow G^l\stackrel{\beta^*}\longleftarrow G^s
$$

equal to the dual $(\beta\circ\alpha)^*$ of $\beta\circ\alpha$,

*Proof*. [[Mike Shulman]] notices that this is a special case of known contravariant functoriality of [[mate]]s, but here is a direct proof.

We need to prove that the composition

$$
G^s\stackrel{\eta_l G^s}\to G^l T^l G^s\stackrel{G^l\beta G^s}\to G^l T^s G^s\stackrel{G^l \epsilon_s}\to G^l\stackrel{\eta_k G^l}\to G^k T^k G^l\stackrel{G^k\alpha G^l}\to G^k T^l G^l\stackrel{G^k\epsilon_l}\to G^k 
$$

equals the composition

$$
G^s\stackrel{\eta_k G^l}\to G^k T^k G^s\stackrel{G^k\alpha G^l}\to G^k T^l G^s\stackrel{G^k\beta G^s}\to G^k T^s G^s\stackrel{G^k\epsilon_s}\to G^k.
$$

Note that in the two compositions there is an opposite order between the expressions involving $\alpha$ and those involving $\beta$. But anyway, their equality reduces to a naturality calculation (which in particular exchanges the order of $\alpha$ and $\beta$ in effect): 

$$\array{
G^s &\stackrel{\eta_l G^s}\to & G^l T^l G^s &\stackrel{G^l\beta G^s}\to & G^l T^s G^s&\stackrel{G^l \epsilon_s}\longrightarrow& G^l\\
\eta^k G^s\downarrow &&\downarrow \eta_k G^l T^l G^s&&\downarrow \eta_k G^l T^s G^s&& \downarrow \eta_k G^l \\
G^k T^k G^s &\stackrel{G^k T^k\eta_l G^s}\longrightarrow &G^k T^k G^l T^l G^s &\stackrel{G^k T^k G^l \beta G^s}\longrightarrow & G^k T^k G^l T^s G^s &\stackrel{G^k T^k G^l \epsilon_s}\longrightarrow & G^k T^k G^l\\
G^k \alpha G^s \downarrow && \downarrow G^k \alpha G^l T^l G^s&&\downarrow G^k \alpha G^k T^s G^s&&\downarrow G^k \alpha G^l\\
G^k T^l G^s &\stackrel{G^k T^l\eta_l G^s}\longrightarrow & G^k T^l G^l T^l G^s &\stackrel{G^k T^l G^l \beta G^s}\longrightarrow & G^k T^l G^l T^s G^s &\stackrel{G^k T^l G^l\epsilon_s}\longrightarrow & G^k T^l G^l\\
G^k\beta G^s \downarrow &&\downarrow{\rho} &&\downarrow G^k \epsilon_l T^s G^s &&\downarrow G^k\epsilon_l \\
G^k T^s G^s &=&G^k T^s G^l &=&G^k T^s G^s&\stackrel{G^k \epsilon_s}\longrightarrow& G^k
}$$

where $\rho := G^k \beta G^s \circ G^k \epsilon_l G^s = G^k\epsilon_l T^s G^s\circ G^k T^l G^l \beta G^s$. The commutativity of all small squares in the diagram is evident, except the lower left corner. This one follows by one of the triangle identities for the adjunction $T^l\dashv G^l$. Namely,

$$
G^k \beta G^s = G^k \beta G^s \circ (G^k \epsilon_l T^l G^s\circ G^k T^l \eta_l G^s) = \rho \circ G^k T^l \eta_l G^s
$$

## Examples

### Adjoint modalities

An [[adjoint modality]] is an example of a pair of adjoint monads.

## References

Discussion of adjoint monads originates with

* {#EilenbergMoore65} [[Samuel Eilenberg]], [[John Moore]], Section 3 in: _Adjoint functors and triples_, Illinois J. Math. **9** 3 (1965) 381-398 &lbrack;[doi:10.1215/ijm/1256068141](https://doi.org/10.1215/ijm/1256068141)&rbrack;
 
(there called "adjoint triples", sticking with the old term "triple" for "monad", a terminology that now clashes with the modern use of *[[adjoint triples]]* of [[adjoint functors]]).

Textbook account:


* {#MacLaneMoerdijk92} [[Saunders Mac Lane]], [[Ieke Moerdijk]], pp. 248 in: _[[Sheaves in Geometry and Logic|Sheaves in Geometry and Logic --- A First Introduction to Topos Theory]]_, Springer (1992) &lbrack;[doi:10.1007/978-1-4612-0927-0](https://dx.doi.org/10.1007/978-1-4612-0927-0)&rbrack;



Discussion in the context of [[ambidextrous adjunctions]] and [[Frobenius monads]]:

* {#Street04} [[Ross Street]], *Frobenius monads and pseudomonoids*, J. Math. Phys. **45** 3930 (2004) &lbrack;[doi:10.1063/1.1788852](https://doi.org/10.1063/1.1788852)&rbrack;

* {#Lauda05} [[Aaron Lauda]], *Frobenius algebras and ambidextrous adjunctions*, Theory and Applications of Categories **16** 4 (2006) 84-122 &lbrack;[arXiv:math/0502550](http://arxiv.org/abs/math/0502550), [tac:16-04](http://www.tac.mta.ca/tac/volumes/16/4/16-04abs.html)&rbrack;

[[!redirects adjoint monads]]
[[!redirects adjoint comonad]]
[[!redirects adjoint comonads]]