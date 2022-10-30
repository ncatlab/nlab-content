# The Continuum Hypothesis
* table of contents
{: toc}

## Idea

The *continuum hypothesis* is a statement of [[set theory]] which says, roughly, that every set of real numbers is either countable or has the same cardinality as all the reals.  It cannot be proven *or* disproven from any of the usual axioms of set theory.


## Statement

+-- {: .num_defn}
###### Definition

Let $E$ be an [[elementary topos]] with [[subobject classifier]] $\Omega$ and [[natural numbers object]] $N$.  The (external) **continuum hypothesis** in $E$ asserts that there is no sequence of [[monomorphisms]]

$$N \hookrightarrow B\hookrightarrow \Omega^n$$

which are not isomorphisms.

In the classical case (that is, in the topos [[Set]] with the [[axiom of choice]]), this equivalently asserts that there is no strict inequality of [[cardinal numbers]]

$${|\mathbb{N}|} \lt \alpha\lt {|\Omega^\mathbb{N}|}$$

which it is more common to write as

$$ \aleph_0 \lt \alpha \lt 2^{\aleph_0} $$
=--


## Unprovability

+-- {: .num_theorem}
###### Theorem

There exists a boolean topos in which the axiom of choice holds and the continuum hypothesis fails.

=--

One topos for which the theorem holds is called the *Cohen topos*; it is the topos of sheaves with respect to the [[dense topology]] (also called the $\neg\neg$-topology) on the Cohen poset.  Thus, in this topos, there exist monomorphisms $\mathbb{N} \hookrightarrow B\hookrightarrow 2^{\mathbb{N}}$ that are not isomorphisms.

The Cohen topos will be constructed from the topos [[Set]] of sets.  For this, recall that the subobject classifier of $Set$ is $2\coloneqq \{0,1\}$.
 
+-- {: .num_defn}
###### Definition
**(Cohen poset)**

Let $\mathbb{N}$ be the set of natural numbers; i.e. the natural-numbers object in $Set$. Let $B$ be a set with strictly larger cardinality ${|B|}\gt {|\mathbb{N}|}$; e.g. $B\coloneqq 2^{2^{\mathbb{N}}}$ will do because of the [[diagonal argument]].  Then the *Cohen poset* $P$ is defined to be the set of morphisms

$$p:F_p\to 2$$

where $F_p\subseteq B\times \mathbb{N}$ is any [[finite set|finite]] subset.
The order relation on $P$ is defined by

$$q\le p\; iff\; F_q\supseteq F_p\;and\;q|_{F_p}=p$$

where the right-hand condition means that $q$ restricted to $F_p$ must coincide with $p$.
=--

We think of each element of $P$ as an approximation to the function $F:B\times\mathbb{N}$ that is the [[exponential|transpose]] of the putative monomorphism

$$f:B\to 2^\mathbb{N}$$

with "smaller" elements considered as better approximations. The very rough intuition is that $p\to q\to \dots$ (if $p\ge p\ge \dots$) forms a [[codirected diagram]] of monomorphisms with domains of increasing size whose colimit is $f$, and that by [[free cocompletion]] (i.e. forming (pre)sheaves) we obtain a topos in which this colimit exists.


+-- {: .num_lemma}
###### Lemma
The [[dense topology|dense]] [[Grothendieck topology]] on $P$ is [[subcanonical topology|subcanonical]].  In other words: For any $p\in P$ we have $y(p)=hom(-,p)\in\Sh(p,\neg\neg)$ 
=--

+-- {: .num_lemma}
###### Lemma
Let $k_{B\times\mathbb{N}}:\begin{cases}P\to Set \\ p \mapsto B\times\mathbb{N}\end{cases}$ denote the functor constant on $B\times\mathbb{N}$. Let

$$A:\begin{cases}
P\to Set
\\
p\mapsto \{(b,n)|p(b,n)=0\}\subseteq B\times \mathbb{N}
\end{cases}$$

Then we have $\neg\neg A=A$ in $Sub(k_{B\times\mathbb{N}})$; i.e. $A$ is a closed subobject with respect to the dense topology $\neg\neg$ in the [[algebra of subobjects]] of $k_{B\times\mathbb{N}}$.
=--

+-- {: .num_lemma}
###### Lemma
Let $\Omega$ denote the [[subobject classifier]] of $Psh(P)$. Let $\Omega_{\neg\neg}$ denote the subobject classifier of $Sh(P,\neg\neg)$. Recall that $\Omega_{\neg\neg}$ is the equalizer $\Omega_{\neg\neg}=eq(id_\Omega,\neg\neg)$.

The [[characteristic morphism]] $\chi_a$ of the subobject $a:A\hookrightarrow k_{B\times\mathbb{N}}=k_B\times\k_\mathbb{N}$ factors through some $f:k_{B\times\mathbb{N}}\to \Omega_{\neg\neg}$.

Then the adjoint $g:k_B\to \Omega_{\neg\neg}^{k_{\mathbb{N}}}$ of $f$ is a monomorphism.
=--

+-- {: .num_corollary}
###### Corollary
The associated-sheaf functor sends $g$ to a monomorphism in the Cohen topos.
=--

## Unrefutability

If $V$ is a model of [[ZF]], then the continuum hypothesis and the [[axiom of choice]] both hold in G&#246;del's [[constructible universe]] $L$ built from $V$.


## References

* [[Saunders Mac Lane]], [[Ieke Moerdijk]], [[Sheaves in geometry and logic]], VI.2, VI.3

* M.C. Fitting, "Intuitionistic logic, model theory and forcing" , North-Holland (1969)

[[!redirects CH]]
