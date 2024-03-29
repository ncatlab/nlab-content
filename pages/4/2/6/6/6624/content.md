
# Simulations
* table of contents
{: toc}

## Idea

A simulation is a [[morphism]] of [[coalgebra for an endofunctor|coalgebras for an endofunctor]].


## Definition

Let $C$ be a [[category]], and let $F\colon C \to C$ be an [[endofunctor]].  Recall that a [[coalgebra for an endofunctor|coalgebra]] of $F$ is an [[object]] $X$ of $C$ equipped with a [[morphism]] $\theta\colon X \to F(X)$.

+-- {: .un_defn}
###### Definition

Given two coalgebras $X, X'$ of $F$, a __simulation__ of $X$ in $X'$ is a morphism $s\colon X \to X'$ in $C$ such that $F(s) \circ \theta = \theta' \circ s$.  That is, this [[commutative diagram|diagram commutes]]:
$$ \array {
            X & \overset{\theta}\to & F(X) \\
            \llap{s}\downarrow & & \downarrow\rlap{F(s)} \\
            X' & \underset{\theta'}\to & F(X')
          } $$
=--

The terminology comes from [[computer science]], and we should probably explain what it's about.


## Examples 

### Relations

Consider the [[category of sets]] and the (covariant) [[power set]] functor $\mathcal{P}$.  A coalgebra of $\mathcal{P}$ is a [[set]] $X$ equipped with a [[function]] $\theta\colon X \to \mathcal{P}(X)$, which is the same thing as a [[binary relation]] $\prec$ on $X$.  To fix the notation, we write $a \prec b$ ($a$ __precedes__ $b$) if $a \in \theta(b)$.

Then in concrete terms, a simulation of $X$ in $X'$ is a function $s\colon X \to X'$ such that

* $s(a) \prec' s(b)$ whenever $a \prec b$, and
* $t = s(a)$ for some $a \prec b$ whenever $t \prec' s(b)$.

Simulations are commonly used as morphisms between sets equipped with [[well founded relation|well-founded]] or [[extensional relation|extensional]] relations.  In particular, between [[well-ordered sets]] (sets equipped with relations that are both well-founded and extensional, as well as [[transitive relation|transitive]]), a simulation (if it exists) is unique, and we recover the usual [[poset|ordered]] [[proper class|class]] of [[ordinal numbers]] as a [[thin category]].

### Open maps in algebraic set theory 

In their book _Algebraic Set Theory_, Joyal and Moerdijk present the notion of a pretopos equipped with a class of open maps. As they remark, every presheaf category carries a canonical class of open maps. We reformulate their notion of canonical open map for an example of primary interest to them, the category of forests, in coalgebraic terms. 

The [[category of forests]] is by definition the [[presheaf|category of presheaves]] over the first infinite ordinal $\omega$. Concretely, a forest $F$ is a diagram of sets and functions 

$$\ldots \to F_{n+1} \to F_n \to \ldots \to F_1 \to F_0.$$ 

If $y \in F_{n+1}$ maps to $x \in F_n$, we call $y$ a **predecessor** of $x$. 

The successor map $s: \omega \to \omega$ induces a pullback functor 

$$s^\ast = Set^{s^{op}}: Set^{\omega^{op}} \to Set^{\omega^{op}}.$$ 

Let $P$ be the covariant power-object functor on the presheaf [[topos]]. Each forest $F$ carries a canonical coalgebra structure over the endofunctor $P s^\ast$. Namely, the structure is a presheaf map $\theta_F \to P s^\ast F$ that corresponds to the subobject 

$$R \hookrightarrow F \times s^\ast F$$ 

where the subset $R_n$ is the set of pairs $(x, y) \in F_n \times F_{n+1}$ such that $y$ is an immediate predecessor of $x$. 

If $\phi: F \to G$ is a map of forests, in other words if the functions $\phi_n: F_n \to G_n$ collectively preserve the predecessor relation, then we have an inclusion 

$$\array{
F & \stackrel{\phi}{\to} & G \\
 ^\mathllap{\theta_F} \downarrow & \leq & \downarrow^\mathrlap{\theta_G} \\
P s^\ast F & \underset{P s^\ast \phi}{\to} & P s^\ast G
}$$ 

where $\leq$ comes from the internal poset structure of $P s^\ast G$. If this inclusion is an equality; in other words, if $\phi$ is a coalgebra map or simulation over $P s^\ast$, then we also say (following Joyal and Moerdijk) that $\phi$ is _open_. Alternatively, we could say that $\phi$ is open if the maps $\phi_n$ collectively preserve and reflect the predecessor relation. 

Pursuing this more concretely: the composite $\theta_G \circ \phi$ corresponds to the subobject $S$ of $F \times s^\ast G$ occurring in the pullback 

$$\array{
S & \to & R_G \\
\downarrow & & \downarrow \\
F \times s^\ast G & \underset{\phi \times 1}{\to} & G \times s^\ast G
}$$ 

so that $S_n \subseteq F_n \times G_{n+1}$ consists of pairs $(x, y)$ such that $y$ is a predecessor of $\phi_n(x)$ in $G$. The composite $P s^\ast(\phi) \circ \theta_F$ corresponds to the subobject $S'$ of $F \times s^\ast G$ occurring in an image factorization 

$$\array{
R_F & \twoheadrightarrow & S' \\
\downarrow & & \downarrow \\
F \times s^\ast F & \underset{1 \times s^\ast \phi}{\to} & F \times s^\ast G
}$$

so that (taking advantage of the fact that image factorizations in a presheaf topos are computed objectwise) $S_{n}' \subseteq F_n \times G_{n+1}$ consists of pairs $(x', y')$ such that $y' = \phi_{n+1} y$ for some predecessor $y$ of $x$ in $F$. The equality of subobjects $S = S'$ matches the notion of open map given in _Algebraic Set Theory_. 

**Remark:** Joyal and Moerdijk actually refine this idea as follows. Instead of taking forests to be set-valued presheaves, they take them to be presheaves over $\omega$ valued in a given [[pretopos]] $C$ equipped with a class of _small maps_ (which are defined axiomatically). Then, a _small forest_ is a diagram in $C$ of the form 

$$\ldots \to F_{n+1} \to F_n \to \ldots \to F_1 \to F_0$$ 

where each map $F_{n+1} \to F_n$ and $F_0 \to 1$ is small. On the other hand, the small map axioms guarantee that small subobjects are representable by a functor $P_{small}: C \to C$. This induces a functor $P_{small}: C^{\omega^{op}} \to C^{\omega^{op}}$ on the category of forests, and analogous to what we described above, a small forest can be construed in terms of a coalgebra structure $F \to P_{small} (s^\ast F)$. 

## Related Concepts

* [[bisimulation]]

[[!redirects simulation]]
[[!redirects simulations]]
