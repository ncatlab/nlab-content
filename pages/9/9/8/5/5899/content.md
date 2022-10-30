
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

A [[monad]] $(T,\mu,\eta)$ is adjoint to a [[comonad]] $(G,\delta,\epsilon)$, if its underlying endofunctor $T$ is _[[left adjoint]]_ to the underlying 1-cell $G$ of the comonad, and $\delta$ and $\epsilon$ are conjugate/adjoint 2-cells to $\mu$ and $\eta$ in the sense explained below.


## Construction

In fact given a [[monad]] $\mathbf{T} = (T,\mu^T,\eta^T)$ which has a _[[right adjoint]]_ $G$, automatically $G$ is a part of a comonad $\mathbf{G} = (G,\delta^G,\epsilon^G)$ where $\delta^G$ and $\epsilon^G$ are in some sense dual to $\mu^T$ and $\eta^T$. 

Thus there is a bijective correspondence between monads having right adjoint and comonads having left adjoint (what [[Alexander Rosenberg]] calls **duality**). I am not sure that the terminology is optimal. In any case, it is a little more than a consequence of two general facts. 

1. If $T\dashv G$ then $T^k \dashv G^k$ for every [[natural number]] $k$. 

2. Given two [[adjunction]]s $S\dashv T$ and $S'\dashv T'$ where $S,S': B\to A$, then there is a [[bijection]] between the [[natural transformation]]s $\phi:S'\Rightarrow S$ and natural transformations $\psi:T\Rightarrow T'$ such that 

$$
\array{
  A (S,-) &\to& B(-,T)
  \\
  {}^{\mathllap{A(\phi,-)}}\downarrow &&\downarrow {}^{\mathrlap{B(-,\psi)}}
  \\
  A(S',-)&\to & B(-,T')
}
$$

where the horizontal arrows are the natural bijections given by the adjunctions. [Eilenberg and Moore](#EilenbergMoore) would write $\phi\dashv\psi$ and talk about "adjointness for morphisms" (of functors), which is of course relative to the given adjunctions among functors. MacLane calls the correspondence *conjugation* ([[Categories for Working Mathematician]], 99-102). 

If $\eta,\eta'$ and $\epsilon,\epsilon'$ are their 
[[unit of an adjunction|unit]] and counit of course the upper arrow is $(SM\stackrel{f}\to N)\mapsto Tf\circ \eta_M$ and the lower arrow $(S'M\stackrel{g}\to N)\mapsto T'g\circ\eta'_M$. Thus the condition renders as 

$$T'(f\circ\phi_M)\circ\eta'_M = \psi_N\circ Tf\circ\eta_M$$ 

or $T'f\circ T'\phi_M\circ\eta'_M = T'f\circ \psi_{SM}\circ\eta_M$. Given $\phi$, the uniqueness of $B(-,\psi)$ is clear from the above [[diagram]], as the horizontal arrows are [[isomorphism|invertible]]. $B(-,\psi)$ determines $\psi$, namely $\psi_N = B(-,\psi)(id_N)$. For the existence of $\psi$ (given $\phi$) satisfying the above equation, one proposes that $\psi$ is the composition
$\psi  = T'\epsilon \circ T'\phi T \circ \eta'T$, i.e.

$$
T\stackrel{\eta' T}\longrightarrow T'S' T\stackrel{T'\psi T}\longrightarrow T'ST \stackrel{T'\epsilon}\longrightarrow T'
$$
and checks that it works. The inverse is similarly given by the composition
$$
S'\stackrel{S'\eta}\longrightarrow S' TS\stackrel{S'\psi S}\longrightarrow S'T'S\stackrel{\epsilon' S}\longrightarrow S
$$

> Zoran: The mechanism strongly reminds of [[mate]]s, but it is not (classical) mates (in their case one starts with one adjunction). Maybe somebody can elucidate the connection, maybe in some framework it is the same.

This correspondence now enables in our special case to dualize $\mu^T$ to $\delta^G$, and similarly unit to the counit. 

## Adjoint monad and comonad from an adjoint triple of functors

Every [[adjoint triple]] $F^*\dashv F_* \dashv F^!$ induces an [[adjoint pair]] $F_* F^*\dashv F_* F^!$. The endofunctor $F_* F^*$ is underlying a monad induced by the adjunction $F^*\dashv F_*$ and $F_* F^!$ is underlying a comonad induced by the adjuntion $F_*\dashv F^!$. This pair of a monad and a comonad are adjoint. 

## General adjoint algebras and coalgebras in $End(A)$

Given a small category $A$, the category $End(A)$ of endofunctors and natural transformations of endofunctors (with vertical composition as composition) is monoidal with respect to the composition as the tensor product of objects (endofunctor) and Godement product (horizontal composition) as the tensor product of morphisms (natural transformations). Hence we can consider operads and algebras over operads, as well as, dually, coalgebras over cooperads; or some other framework for general algebras and coalgebras (or even props). 

In any case, given an adjunction $T\dashv G$, operations $T^n\to T$ dualize to cooperations $G\to G^n$, and more generally multioperations $T^k\to T^l$ dualize to the multioperations $T^l\to T^k$. We would like to sketch the proof that the identities for operations on $T$, correspond to the identities on cooperations on $G$ (and more generally there is a duality among the identities for multioperations). This is essentially the consequence of 


__Lemma.__ ([[Zoran Škoda|Zoran]]) Given the adjunction $T\dashv G$ with unit $\eta$ and counit $\epsilon$, and the sequence

$$
T^k \stackrel{\alpha}\longrightarrow T^l\stackrel\beta\longrightarrow T^s
$$

the composition $\alpha^*\circ\beta^*$ of the dual (in the above sense) sequence

$$
G^k \stackrel{\alpha^*}\longleftarrow G^l\stackrel{\beta^*}\longleftarrow G^s
$$

equal to the dual $(\beta\circ\alpha)^*$ of $\beta\circ\alpha$,

*Proof*. We need to prove that the composition

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

## References

There is a section 3, "adjoint triples" in

* [[Samuel Eilenberg]], [[John Moore]], _Adjoint functors and triples_, Illinois J. Math. __9__, 3 (1965), 381-398, 
 {#EilenbergMoore}

where triple is in the sense of [[monad]]. So we say instead a __monad adjoint to a comonad__. Distinguish from the [[adjoint triple]] of functors. 



[[!redirects adjoint monads]]
[[!redirects adjoint comonad]]
[[!redirects adjoint comonads]]