<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

+-- {: .standout}

[[Urs Schreiber]]. This is something I thought about in the context of my discussion at [[schreiber:Chevalley-Eilenberg algebra]]. 

=--

#Idea#

We give a description of the [[Chevalley?Eilenberg algebra]] of the [[Lie algebra]] of a [[Lie group]] as the [[∞-quantity]] of functions $C^\infty(\mathbf{B}G_e^{(1)})$ on the [[simplicial object|simplicial space]] of infinitesimal neighbourhoods of the identity in the sense of [[synthetic differential geometry]] in the simplicial smooth space $\mathbf{B}G$ that is the [[Lie ∞-groupoid]] incarnation of the [[delooping]] of the [[Lie group]].

The derivation is analogous to and usefully compared with how the deRham algebra of differential forms on a [[manifold]] $X$ is the [[∞-quantity]] of functions on the [[infinitesimal singular simplicial complex]] $X^{\Delta^\bullet_{diff}} \hookrightarrow \Pi(X)$ of $X$, as described at [[differential forms in synthetic differential geometry]].

We proceed entirely by using theorems and propositions from the book

* [[Anders Kock]], _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

in particular section 6.8 combined with section 4.3. We effectively show that these statements are precisely the ones needed to unwrap what the normalized [[Moore complex|Moore cochain complex]] of the [[cosimplicial algebra]] $C^\infty(\mathbf{B} G_e^{(1)})$ in the [[monoidal Dold?Kan correspondence]] is like.

# Definitions and setup #

Let $G$ be a [[Lie group]] (by which we mean a finite dimensional Lie group). Write $\mathbf{B}G$ for the [[simplicial object|simplicial]] [[smooth space]] which in degree $k$ is the cartesian [[product]] $G^k$ with the standard face and degeneray map (see the examples at [[nerve]] for details).

Let $T$ be some [[topos]] that models the axioms of [[synthetic differential geometry]] and which has a [[full and faithful functor|full and faithful]] embedding [[Diff]] $\hookrightarrow T$.

Consider then $\mathbf{B}G$ as a simplicial object in $T$. As usual, we shall call objects in $T$ [[space]]s in the following.

Let $G_e^{(1)} \hookrightarrow G$ be the space that is the first infinitesimal neighbourhood of the neutral element $e$ in $G$. By definition this space is ismorphic to the [[infinitesimal space]] 

$$
  D(n) = \{(d_1, \cdots, d_n) \in R^n | \forall i,j : d_i d_j = 0\}
$$ 

for $n$ the dimension of $D$. By the [[log-exp bijection in synthetic differential geometry]] this space is canonically identified with the [[vector space]] $g := Lie(G)$ underlying the [[Lie algebra]] of $G$.

Moreover, by the [[Kock-Lawvere axiom]] morphisms $f : D(n) \simeq G_e^{(1)} \to R$ are necessarily linear $f : d \mapsto f_0 \to f_1 \cdot d$, hence under the $log$--$exp$ bijection are nothing but elements in the dual vector space $g^*$.

Recall that the ordinary [[Chevalley?Eilenberg algebra]] of $g$ is the [[differential graded algebra]] whose underlying graded-commutative algebra is the [[Grassmann algebra]] $\wedge^\bullet g^* = \mathbb{R} \oplus g^* \oplus g^* \wedge g^* \oplus \cdots$. 

So the subset of $C^\infty(G_e^{(1)})$ that vanishes at 0 is naturally isomorphic to the degree-$1$ part of the Chevalley--Eilenberg algebra.

Notice now that the multiplication on the group $G$ does not restrict to a multiplication on $G_e^{(1)}$ because the sum $d_1 + d_2$ of two elements that each square to 0 is does in general not square to 0, -- $(d_1 + d_2)^2 = 2 d_1 d_2$ but only its cube $(d_1 + d_2)^3 = 0 $ does. Therefore the group multiplication induces a composition

$$
 \cdot :  G_e^{(1)}\times G_2^{(1)} \to G_e^{(2)}
 \,.
$$

Consider therefore the space of "infinitesimal $1$-cells of $\mathbf{B}G$ whose composite is again an infinitesimal $1$-cell", i.e. the [[pullback]]

$$
  \array{
    (G \times G)_e^{(1)}
    &\to&
    G_e^{(1)} \times G_e^{(1)}
    \\
    \downarrow
    &&
    \downarrow^{\cdot}
    \\
    G_e^{(1)}
    &\hookrightarrow&
    G_e^{(2)}
  }
  \,.
$$

By item 3) of [theorem (6.8.1)](http://home.imf.au.dk/kock/SGM-final.pdf#page=226) this pullback is precisely the space of elements $(x,y) \in G_e^{(1)} \times G_e^{(1)}$ such that not only $x$ and $y$ are infinitesimal neighbours of the neutral element $e$, but also of each other.

By the [[Kock-Lawvere axiom]] (entirely analogous to the similar step in the derivation of simplicial [[differential forms in synthetic differential geometry]]) it should follow from this that maps $(G \times G)_e^{(1)} \to R$ that vanish on degenerate elements are in bijection with antisymmetric maps that are canonically identified with elements in $g^* \wedge_{\mathbb{R}} g^*$ (need to say this in more detail...)

Continuing in this manner (...details for higher degrees to be filled in...) we define the simplicial space

$$
  \mathbf{B}G_e^{(1)}
  :=
  (
    \cdots (G \times G)_e^{{1}}
    \stackrel{\to}{\stackrel{\to}{\to}}
    G_e^{(1)}
    \stackrel{\to}{\to}
    {*}
  )
  \,.
$$

The _normalized_ Moore cochain complex $N^\bullet(C^\infty(\mathbf{B}G_e^{(1)}))$ of the cosimplicial algebra

$$
  C^\infty(\mathbf{B}G_e^{(1)})
  :=
  (
    \cdots C^\infty((G \times G)_e^{{1}})
    \stackrel{\leftarrow}{\stackrel{\leftarrow}{\leftarrow}}
    C^\infty(G_e^{(1)})
    \stackrel{\leftarrow}{\leftarrow}
    {*}
  )
$$

is in degree $k$ given by the kernel of the joint degeneracy maps. As in the discussion at [[differential forms in synthetic differential geometry]] this picks out the functions that vanish on degenerate simplices. So from the above we get

$$
  N^\bullet(C^\infty(\mathbf{B}G_e^{(1)}))
  =
  (\cdots
    g^* \wedge g^*
    \stackrel{d = \sum_i (-1)^i d_i}{\leftarrow}
    g^*
    \stackrel{0}{\leftarrow}
    \mathbb{R}
  )
  \,.
$$

Recall that the differential of the [[Chevalley?Eilenberg algebra]] is on $g^*$ just the dual $[-,-]^* : g^* \to g^* \wedge g^*$ of the Lie bracket $[-,-] : g \otimes g \to g$. 

We need to check that this is reproduced by the differential  of the Moore cochain complex, which is the alternating sum of the face maps $d = \sum_i (-1)^i d_i$. Let $f \in g^*$. Then we find for all $(x,y) \in (G \times G)_e^{(1)}$ that

$$
  (d f) (x,y) = f(p_1(x,y)) - f(x \cdot y) + f(p_2(x,y)) 
  = f (x) + f(y) - f(x \cdot y)
  \,.
$$

Now we use the crucial [formula (6.8.2)](http://home.imf.au.dk/kock/SGM-final.pdf#page=227) from Anders Kock's book, which says that the group product on the infinitesimal elements $x,y$ is given by

$$
  x \cdot y = x + y + \frac{1}{2}\{x,y\}
  \,,
$$

where the last term is the group commutator

$$
  \{x,y\}:= x \cdot y \cdot x^{-1} \cdot y^{-1}
  \,.
$$

So this is the term that remains in the formula for $d f$:

$$
  (d f)(x,y) = -\frac{1}{2} f(\{x,y\})
  \,.
$$

On that we apply [theorem 6.6.1](http://home.imf.au.dk/kock/SGM-final.pdf#page=222) of Kock's book, which says (in its third item) that under the $log$--$exp$ bijection by which we identified the infinitesimal neighbourhood $G_e^{(1)}$ (and functions on it) with the tangent space $T_e(G)$ (and linear functions on it) the group commutator maps to the Lie algebra commutator. So indeed under the identification of $f$ with an element in $g^*$ we find

$$
  d f = [-,-]^* f
  \,.
$$

This is indeed the differential of the [[Chevalley?Eilenberg algebra]].

(discussion needs to be completed: situation in higher degree and cup-product mapping to wedge product needs to be discussed...)


[[!redirects Chevalley-eilenberg algebra in synthetic differential geometry]]
[[!redirects Chevalley-Eilenberg algebra in synthetic differential geomet]]
[[!redirects Chevalley-eilenberg algebra in synthetic differential geomet]]