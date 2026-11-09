

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents


## Idea

_Monodromy_ is the name for the [[action]] of the [[homotopy group (of an ∞-stack)|homotopy groups]] of a [[space]] $X$ on [[fibers]] of [[covering spaces]] or [[locally constant ∞-stacks]] on $X$.


## In point-set topology
 {#InPointSetTopology}


We discuss monodromy of [[covering spaces]] in elementary [[point-set topology]].

### Definition

+-- {: .num_defn #CoveringSpaceMonodromy}
###### Definition
**(monodromy of a [[covering space]])

Let $X$ be a [[topological space]] and $E \overset{p}{\to} X$ a [[covering space]]. Write $\Pi_1(X)$ for the [[fundamental groupoid]] of $X$.

Define a [[functor]]

$$
  Fib_E
    \;\colon\;
  \Pi_1(X)
    \longrightarrow
  Set
$$

to the [[category]] [[Set]] of [[sets]] as follows:

1. to a point $x \in X$ assign the [[fiber]] $p^{-1}(\{x\}) \in Set$;

1. to the [[homotopy class]] of a [[path]] $\gamma$ connecting $x \coloneqq \gamma(0)$ with $y \coloneqq \gamma(1)$ in $X$ assign the function $p^{-1}(\{x\}) \longrightarrow p^{-1}(\{y\})$ which takes $\hat x \in p^{-1}(\{x\})$ to the endpoint of a path $\hat \gamma$ in $E$ which lifts $\gamma$ through $p$ with starting point $\hat \gamma(0) = \hat x$

   $$
     \array{
       p^{-1}(x) &\overset{}{\longrightarrow}& p^{-1}(y)
       \\
       (\hat x = \hat \gamma(0)) &\mapsto& \hat \gamma(1)
     }
     \,.
   $$

This construction is well defined for a given representative $\gamma$ due to the unique path-lifting property of covering spaces ([this lemma](covering+space#CoveringSpacePathLifting)) and it is independent of the choice of $\gamma$ in the given homotopy class of paths due to the homotopy-lifting property ([this lemma](covering+space#CoveringSpacesHomotopyLifting)).  Similarly, these two lifting properties give that this construction respects composition in $\Pi_1(X)$ and hence is indeed a [[functor]].

=--

Hence this defines a "[[permutation representation|permutation]] [[groupoid representation]]" of $\Pi_1(X)$.

+-- {: .num_prop}
###### Proposition

Given a [[homomorphism]] between two [[covering spaces]] $E_i \overset{p_i}{\to} X$, hence a [[continuous function]] $f \colon E_1 \to E_2$ which respects [[fibers]] in that the [[diagram]]

$$
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
$$

[[commuting diagram|commutes]], then the component functions

$$
  f\vert_{\{x\}} \;\colon\; p_1^{-1}(\{x\}) \longrightarrow p_2^{-1}(\{x\})
$$

are compatible with the monodromy $Fib_{E}$ (def. \ref{CoveringSpaceMonodromy}) along any [[path]] $\gamma$ between points $x$ and $y$ from def. \ref{CoveringSpaceMonodromy} in that the following [[diagrams]] of [[sets]] [[commuting diagram|commute]]

$$
  \array{
     p_1^{-1}(x) &\overset{f\vert_{\{x\}}}{\longrightarrow}& p_2^{-1}(x)
     \\
     {}^{\mathllap{Fib_{E_1}([\gamma])}}\downarrow
       &&
     \downarrow^{\mathrlap{ Fib_{E_2}([\gamma]) }}
     \\
     p_1^{-1}(y) &\underset{f\vert_{\{y\}}}{\longrightarrow}& p_2^{-1}(y)
  }
  \,.
$$

This means that $f$ induces a [[natural transformation]] between the monodromy functors of $E_1$ and $E_2$, respectively, and hence that constructing monodromy is itself a functor from the [[category]] of [[covering spaces]] of $X$ to that of [[permutation representations]] of the [[fundamental groupoid]] of $X$:

$$
  Fib
   \;\colon\;
  Cov(X)
    \longrightarrow
  Set^{\Pi_1(X)}
  \,.
$$

=--

+-- {: .proof}
###### Proof

For any $\hat x \in p_1^{-1}(x)$ let $\hat \gamma$ be the unique path in $E$ with $\hat \gamma(0) = \hat x$ and $p \circ \hat \gamma = \gamma$. By definition \ref{CoveringSpaceMonodromy} we have

$$
  Fib_{E_1}([\gamma(f)])(\hat x) = \hat \gamma(1)
$$

and hence 

$$
  f(Fib_{E_1}([\gamma(f)])(\hat x)) = f(\hat \gamma(1))
$$

Now $f \circ \hat \gamma$ satisfies $f \circ \hat \gamma(0) = f(\hat x)$ and $p \circ f \circ \hat \gamma = \gamma$ by the fact that $f$ preserves fibers. Hence by uniqueness of path lifting ([this lemma](covering+space#CoveringSpacePathLifting)), $f \circ \hat \gamma$ is the unique lift of $\gamma$ with starting point $f(\hat x)$. By def. \ref{CoveringSpaceMonodromy} this means that 

$$
  Fib_{E_2}([\gamma])(f(\hat x))
  = 
  f (\hat \gamma(1))
  \,.
$$

This is the equality to be shown.

=--


### Properties

+-- {: .num_remark}
###### Remark
**([[fundamental theorem of covering spaces]])**

The [[reconstruction of covering spaces from monodromy]] is an [[inverse functor]] to the monodromy functor. The resulting [[equivalence of categories]]

$$
  Cov(X)
    \underoverset
      {\underset{Fib}{\longrightarrow}}
      {\overset{Rec}{\longleftarrow}}
      {}
  Set^{\Pi_1(X)}
$$

between the [[category of covering spaces]] and the [[permutation representation|permutation]] [[groupoid representations]] of the [[fundamental groupoid]] is known as the _[[fundamental theorem of covering spaces]]_.

=--

+-- {: .num_example #CoveringSpaceFundamentalGroupoid}
###### Example
**([[fundamental groupoid]] of covering space)

Let $E \overset{p}{\longrightarrow} X$ be a covering space.

Then the [[fundamental groupoid]] $\Pi_1(E)$ of the total space $E$ is
[[equivalence of categories|equivalently]] the [[Grothendieck construction]]
of the [[monodromy]] functor $Fib_E \;\colon\; \Pi_1(X) \to Set$

$$
  \Pi_1(E)
   \;\simeq\;
  \int_{\Pi_1(X)} Fib_E
$$

whose

* [[objects]] are pairs $(x,\hat x)$ consisting of a point $x \in X$ and en element $\hat x \in Fib_E(x)$;

* [[morphisms]] $[\hat \gamma] \colon (x,\hat x) \to (x', \hat x')$ are morphisms $[\gamma] \colon x \to x'$ in $\Pi_1(X)$ such that $Fib_E([\gamma])(\hat x) = \hat x'$.

=--


+-- {: .proof}
###### Proof

By the uniqueness of the path-lifting ([this lemma](covering+space#CoveringSpacePathLifting)) and the very definition of the [[monodromy]] functor.

=--

+-- {: .num_prop #MonodromyConnectednessOfCoveringSpace}
###### Proposition

Let $X$ be a [[path-connected topological space]] and let $E \overset{p}{\to} X$ be a [[covering space]]. Then the total space $E$ is 

1. [[path-connected topological space|path-connected]] precisely if the [[monodromy]] $Fib_E$ is a [[transitive action]];

1. [[simply connected topological space|simply connected]] precisely if the [[monodromy]] $Fib_E$ is [[free action]].

=--

+-- {: .proof}
###### Proof

By example \ref{CoveringSpaceFundamentalGroupoid}.

=--


## In homotopy theory
 {#InHomotopyTheory}

More generally, given a [[Serre fibration]] $p$,

$$
  \begin{array}{ccc}
    F &\hookrightarrow& E
    \\
    \big\downarrow 
      &^{_{(pb)}}& 
    \big\downarrow\mathrlap{^p}
    \\
    \ast &\longrightarrow& B
  \end{array}
$$

over a [[connected topological space]] $B$, there is a canonical [[group action]] of the [[fundamental group]] $\pi_1(B)$ of the base space on the higher [[homotopy groups]] $\pi_{\bullet \geq 1}(F)$ of the [[fiber]] space, by [[group]] [[automorphisms]].

(cf. [Steenrod 1951 §17](#Steenrod1951), [Whitehead 1978, §4.2](#Whitehead1978), [Spanier 1981 §7.2](#Spanier1981), [May 1999 May19997.3](#May1999), [UFP 2013 §2.3 & §4.8](#UFP13))

## In homotopy type theory
{#InHomotopyTypeTheory}

In [[homotopy type theory]], [[monodromy]] arises naturally from the [[transport]] of [[dependent type|dependent types]] along [[path|paths]]. This gives an intrinsic formulation of monodromy, without first specifying a path-lifting operation in a topological total space.

Let $B$ be a type and $P:B\to\mathcal{U}$ a [[type family]], with associated [[dependent sum type|dependent sum]] $E\coloneqq\sum_{b:B}P(b)$ and projection $\mathrm{pr}_1:E\to B$. For each $b:B$, the [[homotopy fiber]] of this projection over $b$ is equivalent to $P(b)$, as exhibited by the [[homotopy pullback]] square

$$
\begin{array}{ccc}
P(b) & \longrightarrow & \displaystyle\sum_{x:B}P(x) \\
\big\downarrow && \big\downarrow\mathrlap{^{\mathrm{pr}_1}} \\
\ast & \xrightarrow{\ b\ } & B.
\end{array}
$$

Thus, a family of types over $B$ determines a fibration whose fibers are specified by the family itself.

### Transport and monodromy

For a path $p:x=_B y$, [[transport]] determines a map $p_*:P(x)\to P(y)$. By [[path induction]], transport along a reflexivity path is the identity, while transport along the inverse path provides a homotopy inverse. Hence every path induces an [[equivalence]] $P(x)\simeq P(y)$.

Moreover, transport is compatible with [[path|path composition]]. Given composable paths $p:x=y$ and $q:y=z$, the triangle

$$
\begin{array}{ccc}
P(x) & \xrightarrow{\ p_*\ } & P(y) \\
& \searrow_{\mathrlap{(p\cdot q)_*}} &
\big\downarrow\mathrlap{^{q_*}} \\
&& P(z)
\end{array}
$$

commutes up to [[homotopy]], expressing $(p\cdot q)_*\sim q_*\circ p_*$.

Now fix a basepoint $b_0:B$ and write $F\coloneqq P(b_0)$. Restricting transport to the [[loop space]] $\Omega(B,b_0)\coloneqq(b_0=_B b_0)$ yields the **monodromy map**

$$
\operatorname{mon}_{P,b_0}
:
\Omega(B,b_0)\longrightarrow\operatorname{Aut}(F),
\qquad
\gamma\mapsto\gamma_*.
$$

Here $\operatorname{Aut}(F)$ denotes the type of self-equivalences of $F$. The identity and composition properties of transport give the corresponding compatibility with the loop-space structure. In this sense, monodromy is the action of loops on the fiber induced by the dependent type family.

### Induced equivalences on homotopy groups

Passing from fiber self-equivalences to [[homotopy group|homotopy groups]] introduces a subtlety concerning basepoints.

Given $f_0:F$ and a loop $\gamma:b_0=b_0$, transport determines $f_1\coloneqq\gamma_*(f_0):F$, which need not coincide with $f_0$. Consequently, the fiber self-equivalence canonically determines an equivalence of [[pointed type|pointed types]] $(F,f_0)\simeq_*(F,f_1)$, and hence induces group isomorphisms

$$
\pi_n(F,f_0)\cong\pi_n(F,f_1),
\qquad n\geq 1.
$$

To obtain an automorphism of a single fixed-basepoint homotopy group, one must account for the change of basepoint. A specified path $r:f_1=f_0$, for instance, supplies an additional identification between the two based homotopy groups.

Thus, while transport canonically defines monodromy on the underlying fiber, its formulation as an action of the [[fundamental group]] $\pi_1(B,b_0)$ by automorphisms of $\pi_n(F,f_0)$ requires further attention to the basepoint data and its compatibility with loop composition.

For the underlying constructions in homotopy type theory, see [UFP 2013, §§2.3 and 4.8](#UFP13).

### Formalization in Cubical Agda

A machine-checked Cubical Agda construction of transport-based
monodromy, together with its mathematical exposition and
source-to-formalization correspondence, is available at:

[Agda formalization](PUBLIC_URL)


## In cohesive $\infty$-Toposes

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] and $X \in \mathbf{H}$ any object. Then the [[locally constant ∞-stacks]] on $X$ are represented by morphisms $X \to LConst Core(\infty Grpd)$. By adjunction such morphisms are equivalent to [[(∞,1)-functors]] $\Pi(X) \to Core(\infty Grpd)$  This morphism exhibits the **monodromy** of the [[locally constant ∞-stack]]. 

Specifically, the restriction $\mathbf{B}\Omega_x \Pi(X) \hookrightarrow \Pi(X) \to \infty Grpd$ to the [[delooping]] $\mathbf{B}\Omega_x \Pi(X)$ of the [[loop space object]] $\Omega_x \Pi(X)$ at a chosen baspoint $x : {*} \to X$ is the **monodromy [[action]]** of loops based at $x \in X$ on the fiber of the locally constant $\infty$-stack over $x$.

## References

Discussion in [[topological homotopy theory|topological]] [[homotopy theory]]:

* {#Steenrod1951} [[Norman Steenrod]], Section 17 of: _The Topology of Fibre Bundles_, Princeton Mathematical Series **14**, Princeton University Press (1951) &#91;[jstor:j.ctt1bpm9t5](https://www.jstor.org/stable/j.ctt1bpm9t5)&#93;

* {#Whitehead1978} [[George Whitehead]], Section IV.3 of: _Elements of Homotopy Theory_, Graduate Texts in Mathematics **61**, Springer (1978) &#91;[doi:10.1007/978-1-4612-6318-0](https://doi.org/10.1007/978-1-4612-6318-0)&#93;

* {#Spanier1981} [[Edwin Spanier]], Section 7.2 of: _Algebraic Topology_, McGraw-Hill (1966), Springer (1981) &#91;7[doi:10.1007/978-1-4684-9322-1](https://doi.org/10.1007/978-1-4684-9322-1)&#93;

* {#May1999} [[Peter May]], Section 7.3 of: _[[A Concise Course in Algebraic Topology]]_, University of Chicago Press (1999) &#91;[ISBN:9780226511832](https://press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](https://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf)&#93;

Formulation in [[homotopy type theory]]:

* {#UFP13} [[Univalent Foundations Project]]; section 2.3 & 4.8 of: _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013) &#91;[web](https://homotopytypetheory.org/book/), [pdf](https://homotopytypetheory.org/book/hott-online.pdf)&#93;

See also:

* [[eom]]: _[Monodromy transformation](https://encyclopediaofmath.org/wiki/Monodromy_transformation)_


[[!redirects monodromies]]