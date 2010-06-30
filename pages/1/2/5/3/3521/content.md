
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The **d&#233;calage** construction $Dec X \to X$ on a [[simplicial set]] $X$ is an explicit formula for the based [[path space object]] $X^{I} \times_{X} X_0$ of $X$.

In particular if $X$ is a [[connected]] [[Kan complex]] hence the [[delooping]] $\mathbf{B}G$ of an [[∞-group]] $G$, then $Dec \mathbf{B}G = \mathbf{E}G $ is the [[principal bundle|principal]] [[generalized universal bundle]] of $G$.

If $G$ happens to be the incarnation of an [[∞-group]] with strict group operations, i.e. a [[simplicial group]], then $\mathbf{B}G$ is traditionally denoted $\overline{W}G$ and $Dec \mathbf{B}G = \mathbf{E}G$ is traditionally denoted $W G$.

## Definition 

+-- {: .un_defn}
###### Definition

The **d&#233;calage** $Dec\, Y$ of a [[simplicial set]] $Y$, is the simplicial set obtained by shifting every dimension down by one, 'forgetting' the last face and degeneracy  of $Y$ in each dimension:

* $(Dec \, Y)_n = Y_{n+1}$;
* $d_k^{n,Dec \,Y}  = d^{n+1,Y}_{k}$;
* $s_k^{n,Dec \,Y}  = s^{n+1,Y}_{k}$.


This simplicial set comes with a natural projection, $d_{last} : Dec\, Y \to Y$, given by the 'left over' face map.     

=--

## Properties

The main statement about $Dec X$ is that it is the based [[path space object]] of $X$, as we show in the following proposition. To appreciate this statement, it may be useful to recall the following:

the full subcategory of [[sSet]] on [[Kan complex]]es is naturally a [[category of fibrant objects]]. Given a [[connected]] object $C$ in $KanCplx$ and a morphism $f : B \to C$ the [[homotopy fiber]] of $f$, i.e. the [[homotopy pullback]] in $KanCplx$, hence the  [[(∞,1)-pullback]] in [[∞Grpd]]

$$
  \array{
    hoker f &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    B &\stackrel{f}{\to}& C
  }
$$

is known (see [[homotopy limit]]) to be computed by the ordinary [[limit]] 

$$
  \array{
    hoker f &\to& C^{\Delta[1]}\times_C * &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    && C^{\Delta[1]} &\to& C 
    \\
    \downarrow && \downarrow
    \\
    B &\stackrel{f}{\to}& C
  }
  \,.
$$

This in turn may be computed as two consecutive [[pullback]]s, as indicated (both sub-rectangles in the above limit diagram are pullbacks). The following proposition asserts that the intermediate pullback here is the decalage construction.

It is a general fact in a [[category of fibrant objects]], part of the statement known as the [[category of fibrant objects|factorization lemma]] that if $C$ is a [[Kan complex]] then $C^{\Delta[1]} \times_C * \to C$ is a [[Kan fibration]] that is a replacement of $* \to C$ in that there is a commuting diagram

$$
  \array{
    * &\stackrel{\simeq}{\to}& C^{\Delta[1]}\times_C *
    \\
    \downarrow && \downarrow
    \\
    C &\stackrel{=}{\to}& C
  }
$$

where the top morphism is a [[weak homotopy equivalence]]. For more on this see [[generalized universal bundle]].


+-- {: .un_prop}
###### Proposition

For any $Y \in sSet$, the decalage construction computes the based path object in that

$$
  Dec Y \simeq Y^{\Delta[1]} \times_Y Y_0
  \,.
$$


=--


+-- {: .proof}
###### Proof


First we check that this pullback 

$$
  \array{
    Q &\to& const(Y_0)
    \\
    \downarrow && \downarrow
    \\
    Y^{\Delta[1]} &\stackrel{d_1}{\to}& Y
  }
$$


has the property that $Q_n = Y_{n+1}$.

For this use expression of the $(n+1)$-[[simplex]] as the [[cone]] over the $n$-simplex, which is exhibted by the [[pushout]] diagram

$$
  \array{
    \Delta[n] \times \{1\} &\to& \Delta[n] \times \Delta[1]
    \\
    \downarrow && \downarrow
    \\
    \Delta[0] &\to& \Delta[n+1]
  }
  \,.
$$

This identifies the nondegenerate $(n+1)$-cell of $\Delta[n+1]$ as the map 

$$
  (0,0,1,2, \cdots,n-1,n), (0,1,1, \cdots,1,1) : [n+1] \to [n] \times [1]
  \,.
$$

(See for instance page 25 [here](http://arxiv.org/PS_cache/arxiv/pdf/0809/0809.4221v1.pdf#page=25)).

Applying the [[hom-functor]] $Hom_{\Delta}(-,Y)$ to this pushout diagram yields the pullback diagram

$$
  \array{
    Y_{n+1} &\to& Y_0
    \\
    \downarrow && \downarrow
    \\
    (Y^{\Delta[1]})_n &\to& Y
  }
$$

in [[Set]]. Since pushouts of simplicial sets are computed degreewise in sets we have that $Q_n = Y_{n+1}$ for all $n$. 

Now check that the face and degeneracy maps act as given by the formula for the decalage. Under the above identification with $\Delta[n+1]$ by a pushout, the face map $\delta_i :\Delta[n+1] \to \Delta[n+2]$ is that induced by the morphism of pushout diagrams

$$
  \array{
     \Delta[n] \times \Delta[1] &\stackrel{(\delta_i,Id_{\Delta[1])}}{\to}&
      \Delta[n+1] \times \Delta[1]
     \\
     \uparrow && \uparrow
     \\
     \Delta[n] \times \{1\} &\stackrel{(\delta_i,Id_{\Delta[0])}}{\to}& 
      \Delta[n+1] \times \{1\}
     \\
     \downarrow && \downarrow
     \\
     \Delta[0] &\to& \Delta[0]
  }
  \,.
$$

The induced morphism on the pushouts takes the nondegenerate cell $(0,0,1,2, \cdot,n-1,n), (0,1,1, \cdots, 1,1) : [n+1] \to [n] \times [1]$ of $\Delta[n+1]$ to the cell

$$
  \delta_i(0,0,1,2, \cdot,n-1,n), (0,1,1, \cdots, 1,1) : [n] \to [n+1] \times [1].
$$

That produces all the faces except that of the form $(0,1,2, \cdots, n-1,n),(0,0, \cdots, 0,0) : [n] \to [n+1] \times [1]$, hence except for the 0-face. So this is indeed as in the decalage.

An entirely analogous argument applies for the degeneracy maps.

=--

By the general properties in a [[category of fibrant objects]] we have for $Y$ a [[Kan complex]] that the projection $d_0 : Y^{\Delta[1]} \to Y$  is an acyclic Kan fibration. Since these are stable under pullback, we have

+-- {: .un_cor}
###### Corollary

For $Y$ a [[Kan complex]] the canonical morphism, $Dec Y \to const Y_0$ is an acyclic fibration, hence in particular a [[weak homotopy equivalence]].

=--

Similarly the following is a special case of the general factorization lemma


+-- {: .un_cor}
###### Corollary

For $C$ a [[Kan complex]], the canonical morphism $Dec C \to C$ is a [[Kan fibration]].

=--

 

## Decalage comonad 

Decalage also has an abstract [[category theory|category theoretic]] description as follows. The [[simplex category]], as a [[monoidal category]] $(\Delta, +, 0)$ equipped with the [[monoid]] $1$, is the "[[walking structure|walking]] [[monoid]]", i.e., is initial among monoidal categories equipped with a monoid. Therefore $\Delta^{op}$ is the walking [[comonoid]]; as a result, there is a [[comonad]] 

$$- + 1: \Delta^{op} \to \Delta^{op}$$ 

which induces a comonad on simplicial sets whose underlying functor is precisely decalage: 

$$Dec: Set^{\Delta^{op}} \to Set^{\Delta^{op}}$$

The map $d_{last}: Dec \to Id$ is the counit of this comonad. The comonad itself is analogous to a kind of unbiased path space comonad $P$ on $Top$ whose value at a space $X$ is a pullback 

$$\array{
P X & \to & X^I \\
\downarrow & & \downarrow eval_0 \\
|X| & \stackrel{i}{\to} & X
}$$

where $i$ is the set-theoretic identity inclusion of $X$ equipped with the discrete topology. Thus we have 

$$P X = \sum_{x_0 \in X} P(X, x_0),$$ 

the sum over all possible basepoints $x_0$ of path spaces based at $x_0$. The analogy is made precise by a canonical isomorphism 

$$Dec \circ S \cong S \circ P$$ 

where $S: Top \to Set^{\Delta^{op}}$ is simplicial singularization. 

A $P$-coalgebra partitions $X$ into path components and exhibits contractibility of each component. Similarly, a coalgebra of the decelage comonad exhibits the acyclicity of the underlying simplicial set. 

####Total D&#233;calage####

 Using either the simplicial [[comonadic resolution]] generated by the above comonad or directly using ordinal sum, we get a [[bisimplicial set]] known as the [[total decalage|total décalage]] of $Y$. This will be explored more fully in a separate entry.

## Examples

### Simplicial groups

If $Y = G$ is a [[simplicial group]] then $d_{last} : Dec\, G \to G$, is an [[epimorphism]].  Taking the [[kernel]] of this and then applying $\pi_0$ (taking [[connected]] components), yields a [[crossed module]] constructed from the [[Moore complex]] of $G$

$$NG_1/d_2(NG_2)\to NG_0,$$

which has kernel $\pi_1(G)$ and cokernel $\pi_0(G)$.



### Universal simplicial bundles

If $G$ is a [[simplicial group]] and $\mathbf{B}G := \overline{W}G \in KanCplx$ its [simplicial delooping](http://ncatlab.org/nlab/show/simplicial+group#Delooping) then $Dec \overline{W}G \to \overline{W}G$ is the Kan fibration traditionally denoted

$$
  W G \to \overline{W}G
$$

which is the [universal simplicial G-principal bundle](http://ncatlab.org/nlab/show/simplicial+group#PrincipalBundles).




## Literature

A reasonably full discussion of the d&#233;calage can be found in Luc Illusie's thesis, 

* L. Illusie, 1971, _Complexe cotangent et deformations I_, volume 239 of Lecture Notes in Maths ,  Springer-Verlag. and  1972, _Complexe cotangent et deformations II_, volume 283 of Lecture Notes in 
Maths , Springer-Verlag. 

It is used in Duskin's Memoir, 

* [[John Duskin]], 1975, _Simplicial methods and the interpretation of "triple" cohomology_, number  163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc.

Page 85 of that article seems to be one of the few places in the literature where the (straightforward) observation that $W G$ is $Dec \overline{W}G$ is made explicit.

The notion of decalage is widely appearing since the paper introducing the method of [[cohomological descent]] in [[Hodge theory]]:

* [[Pierre Deligne]], _Th&#233;orie de Hodge. III_, Inst. Hautes &#201;tudes Sci. Publ. Math. __44__ (1974), 5--77. 

An application in theory of stacks is in

* [[Anders Kock]], _The stack quotient of a groupoid_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, __44__ no. 2 (2003), p. 85--104 [numdam](http://www.numdam.org/item?id=CTGDC_2003__44_2_85_0)


See also 

* Ehlers, _Algebraic Homotopy in Simplicially Enriched Groupoids_, 1993, 
University of Wales Bangor, available [[Ehlers-thesis.pdf|here:file]], (see also the reference below and the Tim Porter's [[Menagerie]] notes 


[[!redirects decalage]]
[[!redirects décalage]]
