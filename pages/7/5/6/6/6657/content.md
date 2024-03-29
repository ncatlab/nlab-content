
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Factorization structures for sinks and cosinks
* table of contents
{: toc}

## Idea

A *factorization structure* is a strengthening of an [[orthogonal factorization system]] which allows us to factor, not only single [[morphisms]], but arbitrary [[sinks]] (or cosinks).

## Definition

Let $\{e_i \colon X_i \to Y\}_{i\in I}$ be a [[sink]] and $m\colon A \to B$ a [[morphism]] in some [[category]].  We say that $\{e_i\}$ is *orthogonal* to $m$ if for any sink $\{f_i \colon X_i \to A\}_{i\in I}$ and morphism $g\colon Y\to B$ such that $m f_i = g e_i$ for all $i\in I$:
$$\array{X_i & \overset{f_i}{\to} & A\\
  ^{e_i}\downarrow && \downarrow^m\\
  Y & \underset{g}{\to} & B}$$
there exists a unique arrow $h\colon Y\to A$ such that $h e_i = f_i$ for all $i$ and $m h = g$.  Clearly, if ${|I|}=1$ this reduces to the usual notion of orthogonality for morphisms.

Let $(E,M)$ be an [[orthogonal factorization system|(orthogonal) factorization system]]; we say it extends to a **factorization structure for sinks** if every sink $\{f_i \colon X_i \to Y\}_{i\in I}$ can be factored as $f_i = m e_i$, where $m\in M$ and the sink $\{e_i \colon X_i \to Z\}_{i\in I}$ is orthogonal to $M$.  Note there is no restriction on the sinks involved to be [[small category|small]].

Some authors write $\mathbf{E}$ for the collection of sinks orthogonal to $M$, and say that $(\mathbf{E},M)$ is a factorization structure for sinks, or that the category $C$ is an "$(\mathbf{E},M)$-category".  However, since $\mathbf{E}$ is uniquely determined by $(E,M)$, and $E$ is precisely the 1-ary sinks in $\mathbf{E}$, there is little harm in saying that $(E,M)$ is a factorization structure for sinks.

The dual notion is a **factorization structure for cosinks** ("sources").

### On size and foundations

Observe that if $C$ is [[large category|large]], then the collection $\mathbf{E}$ contains [[proper classes]] as elements.  Therefore, in some [[foundations]] such as [[ZF]], it is not definable as a single thing.  In [[NBG]] one may treat it as a "hyperclass" defined by a first-order formula, in the same way that one treats classes in ZF.  If we use a [[Grothendieck universe]] to define smallness, of course, there is no problem.

## Constructions

Many well-known factorization systems, and ways to construct factorization systems, extend to factorization structures for sinks and/or cosinks.

* [This theorem](/nlab/show/M-complete+category#ConstructingOFS) implies that if a category is [[M-complete category|M-complete]] for a class $M$ of morphisms which consists of monomorphisms and is closed under composition and pullback, then $M$ is the right class in a factorization structure for sinks.

* If $p\colon A\to B$ is a [[Grothendieck fibration]], then factorization structures for sinks can be lifted from $B$ to $A$.  Dually, if $p$ is an opfibration, we can lift factorization structures for cosinks.  For the "mismatched" types of lifting, we require more: $p$ must be a [[topological concrete category|topological functor]].

## Examples

* In [[Set]], the factorization system (epi, mono) extends to both a factorization structure for sinks and one for cosinks.  The epi-sinks are those that are jointly epimorphic, and the mono-sinks are those that are jointly monomorphic.

* By lifting (epi,mono) to [[Top]] (or any other topological category over $Set$), we obtain two factorization structures for sinks: (jointly surjective, subspace inclusions) and (final topologies, injections).  Dually, we have two factorization structures for cosinks: (surjections, initial topologies) and (quotient maps, jointly injective).

## Properties

### $M$ consists of monics

Recall that a factorization system $(E,M)$ is called *proper* if $E\subseteq Epi$ and $M\subseteq Mono$.  In the case of a factorization structure for sinks, the second of these is automatic.

+-- {: .un_theorem}
###### Theorem
If $(E,M)$ is a factorization structure for sinks, then $M$ consists of monomorphisms.
=--
+-- {: .proof}
###### Proof
Let $m\colon A\to B$ be in $M$, and suppose that $m r = m s$ for some $r,s\colon X\to A$, but $r\neq s$.  Consider the sink $\{m r: X \to B \}_{f\in Mor(C)}$ consisting of one copy of $m r$ ($= m s$) for each arrow of the ambient category $C$, and factor this sink as an $E$-sink $\{e_f\colon X \to Y\}_{f\in Mor(C)}$ followed by an $M$-morphism $n\colon Y\to B$.

Now there are at least $2^{|Mor(C)|}$ different sinks $\{g_f\colon X \to A\}_{f\in Mor(C)}$ such that $m g_f = n e_f$, since we may take each $g_f$ to be either $r$ or $s$.  Therefore, by orthogonality, there are at least $2^{|Mor(C)|}$ different morphisms $Y\to A$, a contradiction to [[Cantor's theorem]], since there can be at most $Mor(C)$.
=--

This proof is of course quite reminiscent of Freyd's theorem that any [[complete small category]] is a [[preorder]].  In fact, Freyd's theorem is a consequence of this one (or at least of its proof).  For given a complete small category, there is a factorization structure acting at least on *small* sinks, where $M$ is the class of all morphisms and $E$ the class of families of injections into coproducts.  (Any complete small category is also cocomplete, by the [[adjoint functor theorem]].)  Therefore, all morphisms in a complete small category are monic, including the unique maps to the [[terminal object]]; hence the category is a preorder.

Since Freyd's theorem can fail in [[constructive mathematics]], we should expect the use of [[excluded middle]] to also be essential in proving the above property of factorization structures.

[[!redirects factorization structures]]
[[!redirects factorization structure for sinks]]
[[!redirects factorization structure for sources]]
[[!redirects factorization structure for cosinks]]
[[!redirects factorization structures for sinks]]
[[!redirects factorization structures for sources]]
[[!redirects factorization structures for cosinks]]
