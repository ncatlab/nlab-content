
> This article is about ends (and coends) in [[category theory]].  For ends in [[topology]], see at *[[end compactification]]*.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+-- {: .hide}
[[!include enriched category theory contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea

An _end_ is a special kind of [[limit]] over a [[functor]] of the form $F : C^{op} \times C \to D$ (sometimes called a _[[bifunctor]]_).

If we think of such a functor in the sense of [[profunctors]] as encoding a left and right [[action]] on the object

$$
  \prod_{c \in C} F(c,c),
$$

then the _end_ of the functor picks out the universal [[subobject]] on which the left and right actions coincide. Dually, the _coend_ of $F$ is the universal quotient of $\coprod_{c \in C} F(c,c)$ that forces the two actions of $F$ on that object to be equal.

A classical example of an _end_ is the $V$-object of [[natural transformations]] between $V$-[[enriched functors]] in [[enriched category theory]]. Perhaps the most common way in which ends and coends arise is through homs and tensor products of (generalized) modules, and their close cousins, [[weighted limits]] and [[weighted colimits]]. These concepts are fundamental in enriched category theory. 



## Definition

### In ordinary category theory

#### Definition via extranatural transformations
In ordinary [[category theory]], given a [[functor]] $F: C^{op} \times C \to X$, an __end__ of $F$ in $X$ is an object $e$ of $X$ equipped with a [[universal construction|universal]] [[extranatural transformation]] from $e$ to $F$. This means that, given any extranatural transformation from an object $x$ of $X$ to $F$, there exists a unique map $x \to e$ which respects the extranatural transformations. 

In more detail: the end of $F$ is traditionally denoted $\int_{c: C} F(c, c)$, and the components of the universal extranatural transformation, 
$$\pi_c: \int_{c: C} F(c, c) \to F(c, c),$$ 
are called the _projection maps_ of the end. Then, given any extranatural transformation with components 
$$\theta_c: x \to F(c, c),$$ 
there exists a unique map $f: x \to e$ such that 
$$\theta_c = \pi_c f$$ 
for every object $c$ of $C$.

The notion of __coend__ is dual to the notion of end. The coend of $F$ is written $\int^{c: C} F(c, c)$, and comes equipped with a universal extranatural transformation with components
$$\iota_c \colon F(c,c) \to \int^{c: C} F(c,c).$$

#### Explicit definition
We unwrap the definition of an extranatural transformation to obtain a more explicit description of an end.

+-- {: .num_defn #wedge}
###### Definition
Let $F: C^{op} \times C \to X$ be a [[functor]]. A **wedge** $e: w \to F$ **over F** is an object $w$ and maps $e_c: w\to F(c, c)$ for each object $c$, such that, given any morphism $f: c \to c'$, the following diagram commutes:
$$
\array{
w & \overset{e_{c'}}{\to} & F(c', c')\\
^\mathllap{e_c}\downarrow & & \downarrow^\mathrlap{F(f, c')}\\
F(c, c) & \underset{F(c, f)}{\to} & F(c, c')
}
$$
=--

Given a wedge $e: w \to F$ and a map $f: v \to w$, we obtain a wedge $e f: v \to F$ by composition. We define the end as follows:

+-- {: .num_defn}
###### Definition
Let $F: C^{op} \times C \to X$ be a functor. An **end** of $F$ is a universal wedge over $F$, i.e., a wedge $e: w \to F$ such that each other wedge $e': w' \to F$ factors through $e$ via a unique map $w' \to w$.
=--

Dually, a cowedge is given by maps $F(c, c) \to w$ satisfying similar commutativity conditions, and a coend is a universal cowedge.

#### Ends as right adjoint functors

In complete analogy to how [[limits]] are right adjoint functors to the [[diagonal functor]] for the diagram, ends are right adjoint functors to the hom functor.

In more detail, suppose $C$ and $X$ are categories.

If every diagram $C^{op}\times C\to X$ admits an end,
then we have a functor
$$end\colon Fun(C^{op}\times C,X)\to X$$
whose left adjoint is the hom functor
$$hom\colon X\to Fun(C^{op}\times C,X)$$
that sends an object $x\in X$
to the functor $hom(x)\colon C^{op}\times C\to X$
that sends $(c,d)$ to $\coprod_{hom(c,d)}x=hom(c,d)\otimes x$.
(For coends, one uses $x^{hom(c,d)}$ instead.)

This immediately implies a Fubini theorem for ends and coends.

### In enriched category theory

There is a definition of _end_ in [[enriched category theory]] as follows. 

#### End of $V$-valued functors 

Let $V$ be a [[symmetric monoidal category]], and let $C$ be a $V$-[[enriched category]]. Assuming $V$ is also [[closed monoidal category|closed monoidal]], $V$ may be considered as $V$-enriched. In that case, suppose $F: C^{op} \otimes C \to V$ is a $V$-[[enriched functor]]. 

Then there is a covariant [[action]] of $C$ on $F$, with components
$$\lambda_{c, d, e}: F(c, d) \otimes C(d, e) \to F(c, e),$$
(where $C(d, e)$ is customary notation for the [[hom-object]] $\hom_C(d, e)$ of $C$ in $V$), and a contravariant action of $C$ on $F$, with components
$$\rho_{c, d, e}: F(d, e) \otimes C(c, d) \to F(c, e).$$ 

In detail, the covariant action is the [[adjunct]] of the morphism 

$$
  (F(c,-) 
    \colon 
  C(d,e) \to [F(c,d), F(c,e)]) 
    \in 
  Hom_V(C(d,e),[F(c,d), F(c,e)])
$$ 

under the [[closed monoidal category|Hom-adjunction]] 

$$
  Hom_V(C(d,e),[F(c,d), F(c,e)]) 
    \stackrel{\simeq}{\longrightarrow} 
  Hom_V(C(d,e)\otimes F(c,d),F(c,e))
$$ 

in $V$. Similarly for the contravariant action. 

+-- {: .un_remark}
###### Remark 
Even if $V$ is not closed monoidal, we can still define a **notion** of covariant $C$-action, sometimes called a "left" $C$-[[module]], as consisting of a function $F \colon Ob(C) \to Ob(V)$ together with an $Ob(V) \times Ob(V)$-indexed collection of morphisms 

$$F(c) \times C(c, d) \to F(d)$$ 

satisfying some evident unit and associativity axioms, and regard this notion as a stand-in for the notion of $V$-functor $C \to V$. Similarly, we have an evident notion of contravariant $C$-action as a stand-in for a $V$-functor $C^{op} \to V$. Notice that we don't even require symmetry to make sense of this. Finally, we can combine these notions into one of $C$-bimodule, where we have a function $F \colon Ob(C) \times Ob(C) \to Ob(V)$ together with a collection of morphisms 

$$C(a, b) \otimes F(b, c) \otimes C(c, d) \to F(a, d)$$ 

with evident axioms for a bimodule structure, as a stand-in for a $V$-functor of the form $C^{op} \otimes C \to V$. 
=-- 


A $V$- **extranatural transformation**
$$\theta: v \stackrel{\bullet}{\to} F$$ 
from $v$ to $F$ consists of a family of arrows in $V$, 
$$\theta_c: v \to F(c, c),$$ 
indexed over objects $c$ of $C$, such that for every pair of objects $(c, d)$ in $C$, the composites of (1) and (2) agree: 
$$v \otimes C(c, d) \stackrel{\theta_c \otimes 1}{\to} F(c, c) \otimes C(c, d) \stackrel{\lambda_{c, c, d}}{\to} F(c, d) \qquad (1)$$ 
$$v \otimes C(c, d) \stackrel{\theta_d \otimes 1}{\to} F(d, d) \otimes C(c, d) \stackrel{\rho_{c, d, d}}{\to} F(c, d) \qquad (2)$$

A $V$-enriched **end** of $F$ is an object $\int_{c: C} F(c, c)$ of $V$ equipped with a $V$-extranatural transformation 
$$\pi: \int_{c: C} F(c, c) \stackrel{\bullet}{\to} F$$ 
such any $V$-extranatural transformation $\theta$ from $v$ to $F$ is obtained by pulling back the components of $\pi$ along $f: v \to \int_{c: C} F(c, c)$, for some unique map $f$. That is,
$$\theta_c = \pi_c f$$ 
for all objects $c$ of $C$. 


#### Ends of $C$-valued functors for $C \in V\Cat$ 

If $X$ is any $V$-enriched category and $F: C^{op} \otimes C \to X$ is a $V$-enriched functor, then the **end** of $F$ in $X$ is, if it exists, an object $\int_{c: C} F(c, c)$ of $X$ that [[representable functor|represents]] the functor

$$
\int_{c: C} X(-,F(c,c))\,.
$$

That means that the end $\int_{c: C} F(c,c)$ comes equipped with an $Ob(C)$-indexed family of arrows

$$
\pi_c: I \to X(\int_{c: C} F(c, c), F(c, c))
$$ 

in $V$, such that, for every object $x$ of $X$, the family 
of maps 

$$
X(x, \pi_c): X(x, \int_{c: C} F(c, c)) \to X(x, F(c, c))
$$ 

are the projection maps realizing $X(x, \int_{c: C} F(c, c))$ as the corresponding end $\int_{c: C} X(x, F(c, c))$ in $V$. 


#### End as an equalizer

##### Ordinary ends as equalizers

Now we motivate and define the _end_ in [[enriched category theory]] in terms of [[equalizers]].

Recall from the discussion at the end of [[limit]] that the [[limit]] over an (ordinary, i.e., not enriched) [[functor]]

$$
  F : C^{op} \to Set
$$

is given by the [[equalizer]] of 

$$
  \prod_{c \in Obj(C)}
  F(c)
  \stackrel{\prod_{f \in Mor(c)} (F(f) \circ p_{t(f)}) }{\to}  
  \prod_{f \in Mor(C)}
  F(s(f))
$$

and

$$
  \prod_{c \in Obj(C)}
  F(c)
  \stackrel{\prod_{f \in Mor(c)} (p_{s(f)}) }{\to}  
  \prod_{f \in Mor(C)}
  F(s(f))  
  \,.
$$

If we want to generalize an expression like this to [[enriched category theory]], the explicit indexing over the set of morphisms has to be replaced by something that makes sense in an [[enriched category]]. 

To that end, observe that we have a canonical isomorphism (of sets, still)

$$
  \prod_{{(c_1 \stackrel{f}{\to} c_2)} \in Mor(C)} F(c_1)
  \simeq
  \prod_{c_1,c_2 \in Obj(C)} F(c_1)^{C(c_1,c_2)}
  \,.
$$

If we write for the [[hom-set]] instead

$$
 [C(c_1,c_2), F(c_1)] := F(c_1)^{C(c_1,c_2)}
$$ 

with $[-,-]$ the [[internal hom]] in [[Set]], then the expression starts to make sense in any $V$-[[enriched category]].

Still equivalently, but suggestively rewriting the above, we now obtain the limit over $F$ as the [[equalizer]] of

$$
  \prod_{c \in Obj(C)}
  F(c)
  \stackrel{\stackrel{\rho}{\to}}{\stackrel{\lambda}{\to}}  
  \prod_{c_1,c_2 \in Obj(C)}
  [C(c_1,c_2),F(c_1)]
  \,,
$$

where in components

$$
  \rho_{c_1, c_2} : F(c_1) \to [C(c_1,c_2), F(c_1)]
$$

is the [[adjunct]] of

$$
  C(c_1, c_2) \to * \to [F(c_1), F(c_1)]
$$

(with the last map the [[adjunct]] of $Id_{F(c_1)}$), and where 

$$
  \lambda_{c_1, c_2} : F(c_2) \to [C(c_1,c_2), F(c_1)]
$$

is the [[adjunct]] of

$$
  F_{c_1, c_2} : C(c_1, c_2) \to [F(c_2), F(c_1)]
  \,.
$$

So, for definiteness, the equalizer we are looking at is that of 

$$
  \rho := \prod_{c_1, c_2 \in C} \rho_{c_1,c_2}\circ pr_{F(c_1)}
$$

and

$$
  \lambda := \prod_{c_1, c_2 \in C} \lambda_{c_1,c_2}\circ pr_{F(c_2)}
$$

This way of writing the [[limit]] clearly suggests that it is more natural to have $\lambda$ and $\rho$ on equal footing. That leads to the following definition.


##### Enriched ends over $V$-valued functors as equalizers

For $V$ a [[symmetric monoidal category]], $C$ a $V$-[[enriched category]] and 
$F \colon C^{op} \times C \to V$ a  $V$-[[enriched functor]],
the **end** of $F$ is the [[equalizer]]

$$
  \int_{c \in C}
  F(c,c)
    \longrightarrow
  \prod_{c \in Obj(C)}
  F(c,c)
   \underoverset
    {\underset{\lambda}{\longrightarrow}}  
    {\overset{\rho}{\longrightarrow}}
    {}
  \prod_{c_1,c_2 \in Obj(C)}
    [C(c_1,c_2),F(c_1,c_2)]
  \label{endeq}
$$

with $\rho$ in components given by

$$
  \rho_{c_1, c_2} \colon F(c_1,c_1) \longrightarrow [C(c_1,c_2), F(c_1,c_2)]
$$

being the [[adjunct]] of

$$
  F(c_1,-) \colon  C(c_1, c_2) \longrightarrow [F(c_1,c_1), F(c_1,c_2)]
$$

and

$$
  \lambda_{c_1, c_2} \colon F(c_2,c_2) \longrightarrow [C(c_1,c_2), F(c_1,c_2)]
$$

being the [[adjunct]] of

$$
  F(-,c_2) \colon C(c_1, c_2) \longrightarrow [F(c_2,c_2), F(c_1,c_2)]
  \,.
$$

This definition manifestly exhibits the **end as the equalizer of the left and right action** encoded by the [[distributor]] $F$.

Dually, the coend of $F$ is the [[coequalizer]]

$$
\coprod_{c_1,c_2} C(c_2,c_1) \otimes F(c_1,c_2)\, \rightrightarrows\,
\coprod_c F(c,c)\,\to\,
\int^c F(c,c)
\label{coendcoeq}
$$

with the parallel morphisms again induced by the two actions of $F$.

#### End as a weighted limit 

The end for $V$-functors with values in $V$ serves, among other things, to define [[weighted limits]], and weighted limits in turn define ends of bifunctors with values in more general $V$-categories.

For $C$ and $D$ both $V$-categories and $F : C^\op \times C \to D$ an $V$-[[enriched functor]], the **end** of $F$ is the [[weighted limit]] of $F$

$$
  \int_{c \in C} F(c,c)
  \coloneqq
  \{Hom_C, F\} =
  lim^{Hom_C} F
  \,,
$$

with weight $Hom_C : C^{op} \times C \to V$.  The **coend** of $F$ is the colimit

$$
\int^{c \in C} F(c,c) \coloneqq Hom_{C^{op}} \ast F =  \colim^{Hom_{C^{op}}} F
$$
of $F$ weighted by the hom functor of $C^{op}$.

#### Connecting the two definitions

If $C$ is a $V$-category, then the hom functor $C(-,-) \colon C^{op} \times C \to V$ is the [[coequalizer]] in

$$
\coprod_{c,c'} C(-,c) \times C(c,c') \times C(c',-)
\,\rightrightarrows\,
\coprod_c C(-,c) \times C(c,-) \,\to\, C(-,-)
$$

It is also a general fact (see e.g. [Kelly, ch. 3](#Kelly82)) that weighted (co)limits are cocontinuous in their weight: that is,
$$ \{W \ast V, F\} \cong \{W, \{V-, F\}\}$$
and
$$ (W \ast V) \ast G \cong W \ast (V \ast G)$$
This implies that $\{-,F\}$ takes the coequalizer above to an equalizer, which, after some fiddling with the [[Yoneda lemma]], turns out to be isomorphic to (eq:endeq).
Similarly, $(- \ast F)$ takes the analogous coequalizer presentation of $C^{op}(-,-)$ to (eq:coendcoeq).


## Properties {#Properties}

### $Set$-enriched coends as ordinary colimits {#SetCoendsAsColimits}

Let the enriching category be $\mathcal{V} = $ [[Set]]. We describe a special way in this case to express ends/coends that give [[weighted limits]]/colimits in terms of ordinary (co)limits over categories of elements.

Consider

* $C$ a $Set$-enriched category/[[locally small category]] 
  [[tensoring|tensored]] over [[Set]]; 

* $D$ be a [[small category]];

* $F : D \to C$ a functor;

* $W : D^{op} \to Set$ another functor;

* $el W$ the [[category of elements]] of $W$.

\begin{proposition}\label{CoendAsColimitOverCategoryOfElements}
**(coend as [[colimit]] over [[category of elements]])** \linebreak
There is a [[natural isomorphism]] in $C$

$$
  \int^{d \in D} W(d) \cdot F(d)
  \simeq
  \lim_{\to}(
    (el W)^{op} \to D \stackrel{F}{\to} C
  )
$$

between the coend, as indicated, and the [[colimit]] over the [[opposite category|opposite]] of the [[category of elements]] of $W$.

\end{proposition}

This is equation (3.34) in ([Kelly](#Kelly82)) in view of (3.70).

+-- {: .num_cor #ConPres}
###### Corollary
Any [[continuous functor]] preserves ends, and any cocontinuous functor preserves coends. In particular, for functors $F: D^{op} \times D \to C$ and $c \in C$, we have the isomorphisms
$$
\begin{aligned}
  C(\int^x F(x, x), c) &\cong \int_x C(F(x, x), c)\\
  C(c, \int_x F(x, x)) &\cong \int_x C(c, F(x, x)).
\end{aligned}
$$
=--

+-- {: .num_example}
###### Example

If $W = D(-,e)$ is a [[representable functor]], then 

$$
  (el W)^{op} = D/e
$$

is the [[over category]] over the representing object $e$. This has a [[terminal object]], namely $(e \stackrel{Id}{\to} e$). Therefore

$$
  \lim_\to( D/e \to D \stackrel{F}{\to} C) \simeq F(e)
  \,.
$$

Since this is natural in $e$, the above proposition asserts a [[natural isomorphism]]

$$
  F(-) \simeq \int^{k \in D} D(k,-) \cdot F(k)
  \,.
$$

This statement is sometimes called the [[co-Yoneda lemma]].
=--

More generally, ends and coends may be expressed as limits and colimits from the [[twisted arrow category]]: see there for more details.

### Commutativity of ends and coends

Ordinary [[limit]]s commute with each other, if both limits exist separately. The analogous statement does hold for ends and coends. Since it looks like the commutativity of two integrals, this fact is called the _Fubini theorem_ for ends (for instance [Kelly, p. 29](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf#page=35)).

\begin{proposition}\label{Fubini}
**(Fubini theorem for ends)**
\linebreak
Let $\mathcal{V}$ be a [[symmetric monoidal category]]. Let $\mathcal{A}$ and $\mathcal{B}$ be small 
$\mathcal{V}$-[[enriched categories]]. 

Let

$$
  T \colon (\mathcal{A} \otimes \mathcal{B})^{op} \otimes 
      (\mathcal{A} \otimes \mathcal{B})
      \to 
      \mathcal{V}
$$

be a $\mathcal{V}$-[[enriched functor]]. Then:

If for all object $B,B' \in \mathcal{B}$ the end $\int_{A \in \mathcal{A}} T(A,B,A,B')$ exists, then 

$$
  \int_{(A,B) \in \mathcal{A} \otimes \mathcal{B}}
   T(A,B,A,B)
  \simeq
  \int_{A \in \mathcal{A}}
  \int_{B \in \mathcal{B}}
  T(A,B,A,B)
$$

if either side exists. In particular, since $\mathcal{A} \otimes \mathcal{B} \simeq \mathcal{B} \otimes \mathcal{A}$, this implies that

$$
  \int_{B \in \mathcal{B}}
  \int_{A \in \mathcal{A}}
  T(A,B,A,B)
  \simeq
  \int_{A \in \mathcal{A}}
  \int_{B \in \mathcal{B}}
  T(A,B,A,B),
$$

if either side exists.
\end{proposition}


## Examples

### Natural transformations

+-- {: .num_prop #NatTrans}
###### Proposition
Let $F, G: C \to D$ be [[functors]] between two categories, and let $[C, D] (F, G)$ be the set of [[natural transformations]] between them. Then, we have
$$
  [C, D] (F, G) = \int_{c \in C} D(F(c), G(c)).
$$
=--

+-- {: .proof}
###### Proof
An element of $\int_{c \in C} D(F(c), G(c))$ is, by definition, a collection $\tau_c: F(c) \to G(c)$ of morphisms in $D$ such that, for any morphism $f: c \to d$ in $C$, the following square commutes:
$$
\array{
F(c) & \overset{F(f)}{\to} & F(d)\\
^\mathllap{\tau_c}\downarrow & & \downarrow^\mathrlap{\tau_d}\\
G(c) & \underset{G(f)}{\to} & G(d)
}
$$
which is, by definition, a natural transformation $F \to G$.
=--

### Enriched functor categories 
In light of Proposition \ref{NatTrans}, we can define the natural transformations object for [[enriched functors]] as an end:

For $C$ and $D$ both $V$-[[enriched category|enriched categories]], the $V$-[[enriched functor category]] $[C,D]$ is the $V$-[[enriched category]] whose

* objects are $V$-[[enriched functors]] $F : C \to D$;

* [[hom-objects]] in $V$ are given by the end-formula $[C,D](F,G) := \int_{c \in C} D(F(c), G(c))$.

+-- {: .num_example}
###### Example
For $V = Set$ this reproduces of course the ordinary [[functor category]].
=--

+-- {: .num_example}
###### Example
For $V = \mathbb{R}_{\geq 0}\cup \{\infty\}$ with the monoidal product given by addition, a $V$-enriched category $X$ is a [[metric space]], with the distance between points $x, y \in X$ given by $X(x, y)$. Given two metric spaces $X, Y$ and maps $f, g: X \to Y$, the distance between the maps is
\[
  [X, Y](f, g) = \int_{x \in X} Y(f(x), g(x)) = \sup_{x \in X} Y(f(x), g(x)).
\]
=--

### Kan extension

If the $V$-[[enriched category]] $D$ is [[copower|tensor]]ed over $V$, then the (left) [[Kan extension]] of a [[functor]] $F : C \to D$ along a functor $p : C \to B$ is given by the coend

$$
  Lan F : b \mapsto  \int^{c \in C} hom(p(c),b) \cdot F(c)
  \,.
$$

See [[Kan extension]] for more details.


### Geometric realization

A special case of the example of Kan extension is that of [[geometric realization]].

Very generally, geometric realization is the left Kan extension of a functor $F : C \to D$ along the [[Yoneda embedding]] $Y : C \to [C^{op},V]$.

The "geometric realization" of an object $X \in [C^{op},V]$ with respect to $F$ is then the coend 

$$
  |X| := \int^{c \in C} F(c) \cdot hom(Y(c),X)
  \simeq \int^{c \in C} F(c) \cdot X(c)
  \,,
$$

where the last step on the right uses the [[Yoneda lemma]].

More specifically, this is traditionally thought of as applying to the case where $C = \Delta$ is the [[simplex category]] and where $F : \Delta \to Top$ regards the abstract $n$-[[simplex]] as the standard simplex as a [[topological space]]. 

### Tensor product of functors

If $S : C^\op \to D$ and $T : C \to D$ are functors, their [[tensor product of functors|tensor product]] is the coend
$$ S \otimes_C T = \int^c S(c) \otimes T(c), $$
where the tensor product on the right hand side refers to some [[monoidal structure]] on $D$.

## (Co)end calculus
The formal properties of (co)ends in Propositions \ref{ConPres}, \ref{Fubini} and \ref{NatTrans} allow us to prove certain results by [[abstract nonsense]].

+-- {: .num_example}
###### Example
Let $F: C^op \to Set$ be a functor. We prove the [[co-Yoneda lemma]], that
$$
  F(c) \simeq \int^{c' \in C} C(c,c')\times F(c')
$$
We perform the following manipulations, where each isomorphism is natural:
$$
\begin{aligned}
  Set (\int^{c' \in C} C(c,c')\times F(c'), y) &\simeq \int_{c' \in C} Set (C(c,c')\times F(c'), y)\\
  &\simeq \int_{c' \in C} Set (C(c, c'), Set(F(c'), y))\\
  &\simeq [C, Set] (C(c, -), Set(F(-), y))\\
  &\simeq Set(F(c), y).
\end{aligned}
$$
So by the [[Yoneda lemma]], we have
$$
  F(c) \simeq \int^{c' \in C} C(c,c')\times F(c').
$$
=--

For more examples see e.g. [Loregian (2021)](#Loregian21).

## Related concepts

* [[lax biend]]

* [[(∞,1)-end]]

[[!include homotopy-homology-cohomology]]


## References

The notion of (co)ends as introduced in

* [[Nobuo Yoneda]], §4 of: *On ext and exact sequences* (PhD thesis), Journal of the Faculty of Science, Section I. **8** University of Tokyo (1960) 507–576 &lbrack;[pdf](http://alpha.math.uga.edu/~lorenz/YonedaExtExactSequences.pdf), [CiNii:naid/500000325773](https://ci.nii.ac.jp/naid/500000325773)&rbrack;


An early account with an eye towards application in [[geometric realization of simplicial topological spaces]]:

* {#MacLane70} [[Saunders MacLane]], Section 2 of: _The Milgram bar construction as a tensor product of functors_,  In: F.P. Peterson  (eds.) *The Steenrod Algebra and Its Applications: A Conference to Celebrate N.E. Steenrod's Sixtieth Birthday*, Lecture Notes in Mathematics *168*,  Springer 1970 ([doi:10.1007/BFb0058523](https://doi.org/10.1007/BFb0058523), [pdf](https://link.springer.com/content/pdf/10.1007/BFb0058523.pdf))


Textbook accounts:

* {#Kelly82} [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

   
  * ends of $V$-valued bifunctors are discussed in section 2.1

  * the enriched functor category that they give rise to is discussed in section 2.2;

  * enriched [[weighted limits]] in terms of enriched functor categories are in section 3.1

  * the end of general $V$-enriched functors in terms of weighted limits is in section 3.10 .


* [[Francis Borceux]], Def. 6.6.8 in: *[[Handbook of Categorical Algebra]]*, Vol. 2:  *Categories and Structures*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865))

* [[Emily Riehl]], §4.1 in: *[[Categorical Homotopy Theory]]*, Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457), [pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)&rbrack;


* {#Loregian21} [[Fosco Loregian]], *Coend calculus*, Cambridge University Press (2021) &lbrack;[arXiv:1501.02503](http://arxiv.org/abs/1501.02503), [doi:10.1017/9781108778657](https://doi.org/10.1017/9781108778657), ISBN:9781108778657)&rbrack;

See also:

* [Ends](http://golem.ph.utexas.edu/category/2014/01/ends.html), $n$-Category Caf&#233; discussion.


Application in [[conformal field theory]]:

* [[Jürgen Fuchs]], [[Christoph Schweigert]], _Coends in conformal field theory_ ([arXiv:1604.01670](https://arxiv.org/abs/1604.01670))

[[!redirects end]]
[[!redirects ends]]
[[!redirects coend]]
[[!redirects coends]]

[[!redirects Fubini theorem for ends]]
[[!redirects Fubini theorem for coends]]

[[!redirects enriched end]]
[[!redirects enriched ends]]
