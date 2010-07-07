#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **valuation ring** is an [[integral domain]] $O$ such that, for every nonzero element $x$ in its [[field of fractions]] $K$, either $x \in O$ or $x^{-1} \in O$. 

+-- {: .un_prop}
######Proposition 
A valuation ring $O$ is a [[local ring]]. 
=-- 

+-- {: .proof} 
######Proof 
Suppose $x$, $y$ are nonzero non-unit elements of $R$. Either $x/y$ or $y/x$ belongs to $O$, say $x/y$. Then $(x+y)/y$ belongs to $O$ as well. If $x+y$ were a unit of $O$, it would follow that $1/y$ belongs to $O$, i.e., both $y$ and $1/y$ belong to $O$, so that $y$ is a unit of $O$, contradiction. It follows that non-unit elements of $O$ are closed under addition. It is also clear that if $x$ is a non-unit element of $O$ and $y$ is any element of $O$, then $x y$ is a non-unit element of $O$. Therefore the non-units form an ideal of $O$, clearly the unique maximal ideal of $O$. 
=--

## The valuation function 

The nonzero elements of $K$ may be partially ordered as follows: write $x \leq y$ if $x/y$ belongs to $R$. For any two nonzero elements $x$, $y$ of K$, exactly one of the following conditions holds: 

* $x/y$ is a non-unit of $R$; 

* $x/y$ is a unit of $R$: $x/y$ and $y/x$ belong to $R$; 

* $y/x$ is a non-unit of $R$. 

We call this the _trichotomy law_. Thus, if we write $O^*$ for the units of $R$, it follows from trichotomy that the partial order on $K^*$ descends to a [[total order]] on the quotient group $G = K^*/O^*$. This totally ordered group is called the **value group** of the valuation ring $O$. When the value group is isomorphic to $\mathbb{Z}$, the ring $O$ is called a **discrete valuation ring**. Many local rings which arise in practice, for example localizations of rings of [[algebraic integer]]s $O$ with respect to a prime ideal $\mathcal{p}$, or their completions as rings of $\mathcal{p}$-adic integers $O_{(\mathcal{p})}$, are discrete valuation rings. 

We may then define a **valuation** function 

$$v: K \to K^*/O^* \cup \{0\}$$ 

where $v(x)$ is the coset $x O^*$ if $x \in K^*$, and $v(0) = 0$. The codomain becomes a totally ordered monoid if $0$ is regarded as the bottom element and is _absorbent_ ($0 x = 0$ for all $x$). This function satisfies the following conditions: 

1. $v(x) = 0$ if and only if $x = 0$; 

1. $v(x y) = v(x)v(y)$; 

1. $v(x + y) \leq \max \{v(x), v(y)\}$ 

1. $v$ is surjective. 

## Valuation rings from valuation functions 

Quite generally, we may define a **valuation** on a field $K$ to be a function 

$$v: K \to G \cup \{0\}$$ 

(where $G$ is a totally ordered group, extended to a totally ordered monoid $G \cup \{0\}$ as above), satisfying conditions 1 - 4 listed above. Two valuations $v$, $v'$ are **equivalent** if there is an isomorphism 

$$\phi: G \cup \{0\} \to G' \cup \{0}$$ 

of totally ordered monoids such that $v' = \phi \circ v$. In fact, valuations $v$ may be [[preorder|preordered]]: if we regard $v$ as a special sort of group homomorphism $v: K^* \to G$, then define $v \leq v'$ if there is a surjective homomorphism of ordered groups $\phi: G \to G'$ such that $v' = \phi \circ v$. 

From the data of a valuation on $K$, we may construct a valuation ring $O_v$ inside $K$: 

$$O_v = \{x \in K: v(x) \leq 1\}$$ 

where $1$ is the identity element of $G$. (The fact that $O_v$ is a ring follows straightforwardly from the axioms 1 - 3, and that $O_v$ is a valuation ring follows from the fact that $G$ is totally ordered.) 

In summary, we have the following result whose proof is straightforward: 

+-- {: .un_prop}
######Proposition 
There is a natural bijective correspondence between equivalence classes of valuations on $K$ and valuation rings in $K$. 
=-- 

To express the naturality more precisely: there are two functors 

$$V: Field^{op} \to Pos, \qquad V': Field^{op} \to Pos$$ 

from fields to posets. Here $V$ assigns to a field $K$ the poset of equivalence classes of valuations on $K$, where the partial order is inherited from the preorder described above; $V'$ assigns to a field $K$ the poset of valuation rings inside $K$, ordered by inclusion. If $i: K \to K'$ is a field homomorphism, then $V'(i): V'(K') \to V'(K)$ takes a valuation ring $O' \subseteq K$ to the valuation ring $i^{-1}(O') \subseteq K$, and $V(i)$ is defined similarly. The proposition asserts that the functors $V$, $V'$ are naturally isomorphic. We freely conflate them, denoting either functor as $Val: Field^{op} \to Pos$. 

### Example: compact Riemann surfaces 

One of the first lessons from Mumford's famous Red Book is the "amazing" correspondence between 

* Fields which arise as finite algebraic extensions of the field of rational functions $\mathbb{C}(x)$; 

* Compact Riemann surfaces (compact complex manifolds of complex dimension 1, or "curves"). 

The correspondence goes roughly as follows: to each compact Riemann surface $C$, one may associate the field of meromorphic functions $Mer(C)$, or holomorphic functions $C \to \mathbb{P}^1(\mathbb{C})$. Moreover, for each such $C$, there exists a finite branched covering 

$$\phi: C \to \mathbb{P}^1(\mathbb{C})$$ 

which contravariantly induces a field homomorphism $\mathbb{C}(x) \to Mer(C)$. 

In the other direction, to each field $K$ of transcendence degree 1 over $\mathbb{C}$, there is a Riemann surface whose points may be identified with valuation rings in $K$. (More precisely, with the _discrete_ valuation rings in $K$. All valuation rings of $K$ are discrete except for $K$ itself, which plays the role of a "generic point".) 

Much more could be added here... 

## Generalized power series 

There is a very general construction which takes as input an arbitrary field $k$ and a totally ordered group $G$, and produces as output a valuation ring whose units are identified with nonzero elements of $k$ and whose value group $K^*/k^*$ is naturally identified with $G$. This is the ring of Hahn series. 

More to be added. 
