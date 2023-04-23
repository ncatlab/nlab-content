
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--



#Contents
* table of contents
{:toc}

## Idea

What is known as *left Bousfield localization of model categories* ([Hirschhorn (2002), §3.3](#Hirschhorn02) following [Bousfield  (1975)](#Bousfield75)) is a special case of *[[localization of model categories]]* corresponding to *[[reflective localization]]*, namely  it is a [[Quillen reflection]] inducing a [[reflective sub-(infinity,1)-category|reflective sub-$\infty$-category]] inclusion in the [[simplicial localization|associated]] [[(infinity,1)-categories|$\infty$-categories]].

Recall that the [[reflective localization]] of a category $C$ at a [[set]] of morphisms $S$ can be presented as the [[category of fractions]] of $C$ with respect to the class of $S$-local equivalences. In complete analogy to this, the left Bousfield localization of a [[model category]] (and, more generally, of a [[relative category]] $C$) at a set of morphisms $S$ can be presented as the same underlying category of $C$ equipped with the larger class of [[weak equivalences]], called the $S$-[[local morphisms]].

Here the process of enlarging the class of weak equivalences can be seen as the homotopy coherent analogue of the classical [[category of fractions]].

The historically original example is the [[Bousfield localization of spectra]] &lbrack;[Bousfield  (1975)](#Bousfield75)&rbrack;, but the notion is much more general, as explained above. 

The existence of Bousfield localizations for [[cellular model categories]] was established in [Hirschhorn (2002), Ch. 4](#Hirschhorn02) and for [[combinatorial model categories]] in [Barwick (2010), Prop. 2.2](#Barwick10) (Thm. 2.11 in the preprint, based on [Smith's theorem](combinatorial+model+category#SmithTheorem)) with discussion for the special case of [[simplicial model categories]] also in [Lurie (2009), around A.3.7.3](#Lurie).

## Left and right localization at a class of morphisms

\begin{definition}\label{LeftLocalization}
The __[[localization of a model category|left localization]]__ of a [[model category]] $C$ with respect to a class of morphisms $S$ in $C$ is the [[initial object]] (if it exists) $C \to L_S C$ in the following category:

* The [[objects]] are [[left Quillen functors]] $C\to D$ whose [[left derived functor]] sends elements of $S$ to weak equivalences in $D$

* the [[morphisms]] are commutative triangles of left Quillen functors.

\end{definition}
([Hirschhorn 2002, Def. 3.3.1](#Hirschhorn02))

This definition \ref{LeftLocalization} immediately implies that left localizations, if they exist, are unique up to a unique isomorphism.

The adjective "left" in Def. \ref{LeftLocalization} refers to the fact that the localization functor is implemented as the [[left derived functor]] of $C\to L_S C$,
in complete analogy to how the localization functor for a [[reflective localization]] is a [[left adjoint]] functor.

Right localizations are defined analogously and generalize [[coreflective localizations]].


## Local objects and local equivalences

Let $C$ be a [[model category]] with a class of morphisms $S$.

We want to characterize objects in $C$ that “see elements of $S$ as weak equivalences”.

\begin{lemma}
In an ordinary category $C$, by the [[Yoneda lemma]] a morphism $f \colon A \to B$ is an [[isomorphism]] precisely if for all objects $X$ the morphism
$$
  Hom_C(f,X) \colon Hom_C(B,X) \to Hom_C(A,X)
$$
is an [[isomorphism]] (of sets, i.e., a [[bijection]]).
\end{lemma}

So we can “test isomorphism by homming them into objects”.

More generally, recall the following facts about [[reflective localizations]].
If $C$ is a category and $S$ is a class of morphisms in $C$, then an $S$-local object is an object $X\in C$ such that for every $f\colon A\to B$ in $S$, the map $C(B,X)\to C(A,X)$ is an isomorphism.  An $S$-local equivalence is a morphism $g\colon E\to F$ such that for every $S$-local object $X\in C$, the map $C(F,X)\to C(E,X)$ is an isomorphism.  The reflective localization of $C$ at $S$ (if it exists) is defined as an initial object in the category whose objects are left adjoint functors $C\to D$ that send elements of $S$ to isomorphisms in $D$, and morphisms are commutative triangles of left adjoint functors.
The functor from the full subcategory of $S$-local objects in $C$ into the [[category of fractions]] of $C$ with respect to $S$-local equivalences is an equivalence of categories.  Thus, both domain and codomain of the above functor are models for the [[reflective localization]] of $C$ at $S$.

The following definitions offer a completely analogous picture for [[model categories]].

+-- {: .num_defn }
###### Definition
**($S$-local objects and $S$-local weak equivalences)**
We say that

* an object $X$ is an $S$-[[local object]] if for all $s : A \hookrightarrow B$ in $S$ the morphism
$$RMap(s,X) : RMap(B,X) \to RMap(A,X)$$
is a weak equivalence of [[simplicial sets]], where $RMap$ denotes the [[homotopy function complex]], implemented, for example, as the [[hammock localization]];

* conversely, say that a map $f : A \hookrightarrow B$ is an $S$-local weak equivalence if for all $S$-local objects $X$ the morphism $RMap(f,X) : RMap(B,X) \to
RMap(A,X)$ is a weak equivalence of simplicial sets.

=--

([Hirschhorn 2002, Def. 3.1.4](#Hirschhorn02))


We write $W_S$ for the collection of $S$-local weak equivalences.

+-- {: .num_remark }
###### Remark

For every weak equivalence $f : A \stackrel{\simeq}{\to} B$ between cofibrant objects and every fibrant object $X$ in a [[simplicial model category]] $C$
the map
$$C(f,X) : C(B,X) \to C(A,X)$$
is a weak equivalence of simplicial sets.
This is described in detail at
[enriched homs from cofibrants to fibrants](http://ncatlab.org/nlab/show/%28infinity%2C1%29-categorical+hom-space#EnrichedHomsCofToFib).

=--

\begin{lemma}
Every ordinary weak equivalence is also $S$-local weak equivalence.
$$W \subset W_S.$$
\end{lemma}
([Hirschhorn 2002, Prop 3.1.5](#Hirschhorn02))


## Left and right Bousfield localizations
{#Definition}

+-- {: .num_defn }
###### Definition
**(left Bousfield localization)**

The left Bousfield localization $L_S C$ of a [[model category]] $C$ **at a class of morphisms $S$** is, if it exists, the new model category structure on $C$ with

* cofibrations are the same as before, $cof_{L_S C } = cof_C$;

* weak equivalences are $S$-local equivalences.

=--

Again, the adjective “left” refers to the fact that the localization is implemented by the [[left derived functor]], generalizing [[reflective localizations]].

Right Bousfield localizations are defined analogously and generalize [[coreflective localizations]].

\begin{proposition}
Any left Bousfield localization of $M$ at $S$ is also a left localization of $M$ at $S$.
Likewise for right localizations.
\end{proposition}
([Hirschhorn 2002, Thm. 3.3.19](#Hirschhorn02))

In practice, left localizations are always constructed as left Bousfield localizations.
Therefore, both notions are used interchangeably.

## Third definition

\begin{definition}\label{DefinitionOfLeftBousfieldLocalizations}
A _left Bousfield localization_ $C_{loc}$ of a model category $C$ is another model category structure on the same underlying category with the same cofibrations,
$$cof_{C_{loc}} = cof_c$$
but more weak equivalences
$$W_{C_{loc}} \supset W_C.$$
\end{definition}

While that's a very simple definition, it turns out that something interesting happens to the fibrations when we keep the cofibrations fixed and increase the weak equivalences.

+-- {: .num_remark #ImmediateImpiciationsOfLeftBousfieldLocalization}
###### Remark

It follows directly that

* $C_{loc}$ has as [[fibrations]] a sub-class of  the fibrations of $C$

  $$
    fib_{C_{loc}} = rlp(cof_{C_{loc}} \cap W_{C_{loc}})
    \subset rlp(cof_{C_{loc}} \cap W_C) = fib_{C}
    \,.
  $$

* $C_{loc}$ has the same [[acyclic fibrations]] as $C$

  $$
    fib_{C_{loc}} \cap W_{C_{loc}}
    =
    rlp(cof_{C_{loc}}) = rlp(cof_C) = fib_C \cap W_C
    \,.
  $$

* on the underlying categories

  * the identity functor $Id : C \to C_{loc}$ preserves cofibrations and weak equivalences

  * the identity functor $Id : C_{loc} \to C$ preserves fibrations and acyclic fibrations

  so that this pair of functors is a [[Quillen adjunction]]

  $$
    C_{loc} \stackrel{\leftarrow}{\to} C
    \,,
  $$

=--

and a very special one: With $C^\circ$ the [[full subcategory]] on fibrant-cofibrant objects, under left Bousfield localization the fibrant-cofibrant objects of $C_{loc}$ are a subcollection of those of $C$, so that we have the full subcategory

$$
  (C_{loc})^\circ \subset C^\circ
  \,.
$$

Moreover, as we shall see, every object in $C$ is weakly equivalent in $C_{loc}$ to one in $C_{loc}$: it _reflects into $C_{loc}$_ .

+-- {: .standout}

Bousfield localization is a model category version of _reflection onto [[local objects]]_, in the sense discussed at _[[reflective localization]]_.

=--

Indeed, the Quillen adjunction given by a left Bousfield localization under [[presentable (infinity,1)-category|passage to the sub-category of fibrant-cofibrant objects]] becomes the inclusion of a [[reflective (∞,1)-subcategory]]
$$
  {C_{loc}}^\circ \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  C^\circ
$$
hence of a [[localization of an (∞,1)-category]].

Such a localization is determined by the collection $S$ of _[[local object|local weak equivalences]]_ in $C$, and alternatively by the collection of $S$-[[local object]]s in $C$. Indeed, ${C_{loc}}^\circ$ is the full $(\infty,1)$-subcategory on the cofibrant and fibrant and $S$-local objects of $C$.


## Properties {#Properties}

Assume that the left Bousfield localization $L_S C$ of a given model category at a class $S$ of morphisms in $C$ exists. Then it has the following properties.

#### Fibrants in $L_S C$ are the $S$-local fibrants in $C$

+-- {: .num_prop }
###### Proposition

The fibrant objects in $L_S C$ are precisely the fibrant objects in $C$ that are $S$-[[local object|local]].

=--

+-- {: .proof}
###### Proof

To see this, we modify, if necessary, the set $S$ in a convenient way without changing the class $W_S$ of $S$-[[local object|local weak equivalence]]s that it defines.


**Lemma** We may add to $S$ any set of $S$-local cofibrations without changing the collection of $S$-[[local object]]s and hence without changing the collection of $S$-local weak equivalences themselves. In particular, we may add to $S$ without changing $W_S$

* all generating acyclic cofibrations of $C$, i.e. $J \subset S$;


* for every original morphism $f : A \to B$ in $S$ and for every $n \in \mathbb{N}$ also the canonical morphism

  $$
    \tilde f 
    \;\colon\; 
    \big(
       Q_f 
         \coloneqq 
       A \cdot \Delta^n 
         \coprod_{A \cdot \partial \Delta^n}
       B \cdot \partial \Delta^n
    \big) \to B \cdot \Delta^n
    \,,
  $$

  where $A \cdot \Delta^n$ etc. denotes
  the [[copower|tensoring]] of $C$ over [[SSet]].

**Proof of the Lemma**

We discuss why these morphisms of the latter type are indeed $S$-local cofibrations with cofibrant domain:

to see that $\tilde f$ is indeed a cofibration notice that for every commuting diagram

$$
  \array{
    Q_f &\to& X
    \\
    \downarrow && \downarrow^{\in \mathrlap{fib_C \cap W_C}}
    \\
    B \cdot \Delta^n
    &\to&
    Y
  }
$$

we get as components of the top morphism the left square of

$$
  \array{
    \partial \Delta^n &\to& C(B,X) &\to& C(B,Y)
    \\
    \downarrow &&
    \downarrow &&
    \downarrow
    \\
    \Delta^n &\to& C(A,X) &\to& C(A,Y)
  }
$$

and similarly the components of the bottom morphism consitute a morphism $\Delta^n \to C(B,X)$ which by the commutativity of the original square is a lift of the outer diagram here. The top left triangle of this lift in turn gives a square

$$
  \array{
    \partial \Delta^n &\to& C(B,X)
    \\
    \downarrow^{\mathllap{\in cof_{SSet} \cap W_{SSet}\quad}}
    && \quad \downarrow^{\in fib_{SSet}}
    \\
    \Delta^n &\to& C(A,X)
  }
  \,.
$$

So this last diagram has a lift $(\Delta^n \to C(B,X))$ and this is adjunct to the lift $B \cdot \Delta^n \to X$ of the original lifting problem that we are looking for.

Therefore $\tilde f : Q_f \to B \cdot \Delta^n $ is indeed a cofibration.

Notice that in these arguments we made use of

* the [[power]]ing and [[copower]]ing of the [[simplicially enriched category]] $C$ over [[SSet]]

* and of the [[Quillen bifunctor]] property of the [[copower]]ing which ensures that the fibrations and cofibrations are as indicated.

Next, again using the [[Quillen bifunctor]] property of the [[copower|tensoring]] of $C$ over [[SSet]] we find that with $A$ cofibrant in $C$ and $\Delta^n$ being cofibrant in [[SSet]] it follows that $A \cdot \Delta^n$ is cofibrant; similarly for the other cases. The coproduct of two cofibrant objects is cofibrant because cofibrations are preserved under pushout. Therefore $Q_f$ is indeed a cofibrant domain of our cofibration.

With $\tilde f$ being a cofibration, we can check $S$-locality by homming into fibrant $S$-local objects and checking if that produces an acyclic Kan fibration.

So let $X$ be a fibrant and $S$-local object of $C$. Homming the defining [[pushout]] diagram for $Q_f$ into $X$ produces the [[pullback]] diagram

$$
  \array{
    [\partial \Delta^n,[A,X]]
    &\stackrel{\in W}{\leftarrow}&
    [\partial \Delta^n, [B,X]]
    \\
    \uparrow^{\mathrlap{\in fib}} &&
    \uparrow
    \\
    [\Delta^n,[A,X]]
    &\stackrel{\in W}{\leftarrow}&
    [A \cdot \Delta^n \coprod_{A \cdot \partial \Delta^n} B \cdot \partial \Delta^n, X]
    \\
    &{}_{\in W}\nwarrow&& \nwarrow
    \\
    &&&& [B \cdot \Delta^n, X]
  }
$$

in [[SSet]]. Here the top and the lowest morphisms are weak equivalences by the fact that $[B,X] \to [A,X]$ is an acyclic Kan fibration by the characterization of $S$-[[local object|local cofibrations]] and the fact that [[SSet]] is an [[SSet]]-[[enriched model category]]. Similarly for the fibration on the left, which implies by right [[proper model category|properness]] of [[SSet]] that the bottom horizontal morphism is a weak equivalence, which finally implies by [[category with weak equivalences|2-out-of-3]] that the morphism in question is a weak equivalence.

**end of the proof of the lemma**

This shows that we can assume that $S$ contain the generating acyclic cofibrations and the morphism called $\tilde f$.

As usual, we say that given a set of morphisms $S$ and an object $X$ that $X$ has the _extension property_ with respect to $S$ if every diagram

$$
  \array{
    A &\to& X
    \\
    \downarrow^{\mathrlap{\in S}} && \downarrow
    \\
    B &\to& {*}
  }
$$

has a lift.

We claim now that the the objects of $C$ that have the extension property with respect to our set $S$ are precisely the fibrant and $S$-[[local object]]s.
The argument proceeds along the same lines as the proof of the above lemma.

In one direction, if $X$ that has the extension property with respect to $S$ it has it in particular with respect to the generating acyclic cofibrations $J \subset S$ and hence is fibrant, and it, in particular, has the extension property with respect to  $\tilde f : A \cdot \Delta^n \coprod_{A \cdot \partial \Delta^n} B \cdot \partial \Delta^n \to B \cdot \Delta^n$. Observe that by the pushout definition of $Q_f$ a morphism

$$
  Q_f \to X
$$

consists of two component maps $(A \cdot \Delta^n \to X)$ and $(B \cdot \partial \Delta^n \to X)$ such that

$$
  \array{
    \partial \Delta^n &\to& C(B,X)
    \\
    \downarrow && \downarrow
    \\
    \Delta^n &\to& C(A,X)
  }
  \,,
$$

and in terms of this a lift

$$
  \array{
     Q_f &\to& X
     \\
     \downarrow & \nearrow_{\exists}
     \\
     B \cdot \Delta^n
  }
$$

consists of a lift

$$
  \array{
    \partial \Delta^n &\to& C(B,X)
    \\
    \downarrow &\nearrow_\exists & \downarrow
    \\
    \Delta^n &\to& C(A,X)
  }
  \,.
$$

Since $\{\partial \Delta^n \to \Delta^n | n \in \mathbb{N}\}$ are the generating acylic fibrations in the standard [[model structure on simplicial sets]], this shows the extension property of $S$ with respect to all $\tilde f$ means that all $C(s,X) : C(B,X) \to C(A,X)$ are acyclic [[Kan fibration]]s.

Conversely, if $X$ is fibrant and $S$-local, then for all $A \to B$ in $S$ the map $[B,X] \to [A,X]$ in $SSet$ is an acyclic [[Kan fibration]] hence in particular its underlying map of sets $Hom_C(B,X) \to Hom_C(A,X)$ is a surjection, so $X$ has the extension property.

Now every fibrant object $X$ in $L_S W$ has the extension property with respect to $cof_C \cap W_S$ hence in particular with respect to $S \subset cof_c \cap W_S$, so is $S$-local and fibrant in $C$.

Conversely, if it is $S$-local and fibrant in $C$; then, as mentioned before, for all $f \in cof_C \cap W_S$ the map $[f,X]$ is an acyclic Kan fibration in [[SSet]] so that in particular $Hom_C(f,X)$ is a surjection, which means that $X$ has the extension property with respect to all $f$ and is hence fibrant in $L_S C$.


=--


#### Fibrant replacement in $L_S W$ -- localization of objects

If $S$ is a small set, we may apply the [[small object argument]] to $S$. If we apply it to factor all morphisms $X \to {*}$ to the [[terminal object]] we obtain a functorial factorization componentwise of the form

$$
  X \stackrel{\eta_X \in cell(S)\subset W_S}{\to}
  T X \stackrel{inj(S)}{\to} {*}
  \,.
$$

We had remarked already in the previous argument that objects with the extension property relative to $S$, i.e. objects whose morphism to the terminal object is in $inj(S)$, are fibrant as well as $S$-[[local object|local]] in $C$.

Therefore $T$ is in particular a **fibrant approximation functor** in $L_S W$ and $\eta_S$ is the weak equivalence

$$
  \eta_S : X \stackrel{\simeq_{W_S}}{\to} T X
$$

in $L_S C$ relating an object to its fibrant approximation.

More precisely:


+-- {: .num_prop #DerivedAdjunctionUnitOfLftBousfieldLoclization}
###### Proposition

Let 

$$
  \mathcal{C}_{loc}
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

be a [[Quillen adjunction]] which exhibits a left [[Bousfield localization of model categories]], and assume that $\mathcal{C}_{loc}$ admits [[functorial factorization]] (for instance if $\mathcal{C}$ is a [[combinatorial model category]], whence $\mathcal{C}_{loc}$ is, then via the [[small object argument]]), hence in particular a fibrant replacement [[natural transformation]]

$$
  (-) \longrightarrow (-)^{fib}
  \,.
$$

Then the derived adjunction unit, i.e. the [[adjunction unit]] $\eta^{der}$ of [[adjoint pair]] of the [[derived functors]] on the [[homotopy category of a model category|homotopy category]] (as discussed there)

$$
  Ho(\mathcal{C}_{loc})
    \underoverset
      {\underset{}{\hookrightarrow}}
      {\overset{}{\longleftarrow}}
      {\bot}
  Ho(\mathcal{C})
$$

is isomorphic to the image of the fibrant replacement morphism in $\mathcal{C}_{loc}$:

$$
  \eta^{der}_X
  \simeq
  \ell(X \to X^{fib})
  \,,
$$

where $\ell \;\colon\; \mathcal{C}_{loc} \to Ho(\mathcal{C}_{loc})\;$ is the [[localization]] functor (as discussed at _[[homotopy category of a model category]]_).

=--

+-- {: .proof}
###### Proof

First consider the general prescription (from _[[homotopy category of a model category]]_) of computing the right (left) [[derived functors]] by applying the Quillen functors to fibrant (cofibrant) replacements, where we apply the fibrant replacement functorially also to the non-cofibrantly replaced object:

Let

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a general [[Quillen adjunction]] betwen [[model categories]] which admit [[functorial factorization]].

Let $X \in \mathcal{D}$ be any [[object]]. First consider a cofibrant replacement

$$
  \array{
    X_{cof}
    \\
    \downarrow^{\mathrlap{\in \mathrm{W} \cap Fib}}
    \\
    X
  }
  \,.
$$

Then apply $L$ to this

$$
  \array{
    L(X_{cof})
    \\
    \downarrow^{}
    \\
    L(X)
  }
  \,.
$$

Then apply fibrant replacement functorially


$$
  \array{
    L(X_{cof})
     &\overset{\in W \cap Cof}{\longrightarrow}&
    (L(X_{cof}))^{fib}
    \\
    \downarrow^{}
      &&
    \downarrow
    \\
    L(X)
      &\underset{\in W \cap Cof}{\longrightarrow}&
    (L(X))^{fib}
  }
  \,.
$$

Then apply $R$

$$
  \array{
     R L (X_{cof})
       &\overset{}{\longrightarrow}&
     R (L X_{cof})^{fib}
     \\
     \downarrow^{\mathrlap{}}
       &&
     \downarrow
     \\
     R L X &\underset{}{\longrightarrow}& R((L X)^{fib})
  }
$$

Finally, precompose with the ordinary [[adjunction unit]].
The derived adjunction unit is now modeled by the top composite morphism in the following diagram:

$$
  \array{
     X_{cof}
      &\overset{\eta_{X_{cof}}}{\longrightarrow}&
     R L (X_{cof})
       &\overset{R (j \in W \cap Cof)}{\longrightarrow}&
     R (L X_{cof})^{fib}
     \\
     \downarrow
     &&
     \downarrow^{\mathrlap{\in W \cap Fib}}
       &&
     \downarrow
     \\
     X
      &\underset{\eta_X}{\longrightarrow}&
     R L X &\underset{}{\longrightarrow}& R((L X)^{fib})
  }
  \,.
$$

Now in the special case that $(L \dashv R)$ is a [[left Bousfield localization of model categories]], then as plain [[categories]] $\mathcal{D} = \mathcal{C} $ and as plain functors $L = id$ and $R = id$ are trivial and so in this special case the derived adjunction unit is modeled simply by the top morphism in the following diagram

$$
  \array{
    X_{cof} 
      &\overset{\in Cof}{\longrightarrow}&
    (X_{cof})^{fib}
     \\
    {}^{\mathllap{\in W \cap Fib}}\downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Fib}}
    \\
    X 
      &\underset{\in W Cof}{\longrightarrow}&
    X^{fib}
  }
  \,.
$$

But now since the vertical morphisms are weak equivalences,
this means that already the [[fibrant replacement]] $X \to X^{fib}$
is isomorphic, in the [[homotopy category of a model category|homotopy category]], to the [[derived adjunction unit]], i.e. applying the [[localization]] $\ell$ to the above diagram in $\mathcal{C}$ yields the diagram

$$
  \array{
    \mathcal{l}(X_{cof})
      &\overset{\eta^{der}_X}{\longrightarrow}&
    \mathcal{l}((X_{cof})^{fib})
     \\
    {}^{\simeq}\downarrow
    &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathcal{l}(X) 
      &\underset{}{\longrightarrow}&
    \mathcal{l}(X^{fib})
  }
  \,.
$$

=--



#### $S$-local weak equivalences between $S$-local objects are weak equivalences



+-- {: .num_prop #LocalWeakEquivalencesBetweenLocalObjects}
###### Proposition

The $S$-local weak equivalences between $S$-local fibrant objects are precisely the original weak equivalences between these objects.

=--

+-- {: .proof}
###### Proof

Consider the full subcategory $Ho_S(C) \subset Ho(C)$
of the [[homotopy category]] of $C$ on the $S$-[[local object]]s. The image of an $S$-local weak equivalence
$f : A \to B$ in there satisfies for _every_ object $X$
in there that $Hom_{Ho_S(C)}(f,X)$ is an [[isomorphism]].
By the [[Yoneda lemma]] this implies that $f$ is an
isomorphism in $Ho_S(C)$. Since that is a [[full subcategory]], it follows that $f$ is also an isomorphism in $Ho(C)$. But that means precisely that it is a weak equivalence in $C$.

=--

It follows that also the fibrations between local objects remain the same:

+-- {: .num_prop #LocalFibrationsBetweenLocalObjectsAreGlobalFibrations }
###### Proposition

Consider a left Bousfield localization
with [[functorial factorization]] (e.g. of a [[combinatorial model category]], via the [[small object argument]]).

Then 
if $X, Y \in Fib_{loc}$ are [[local objects]], a morphism
$p \colon X\longrightarrow Y$ between them is a fibration with respect to the local model structure precisely already if it is a fibration with respect to the original model structure.

=--

+-- {: .proof}
###### Proof

From remark \ref{ImmediateImpiciationsOfLeftBousfieldLocalization} we already know that $Fib_{loc} \subset Fib$, generally. Hence we need to show that if $p \in Fib$ with $X$ and $Y$ local, then $p \in Fib_{loc}$.

So given a [[lifting problem]] of the form

$$
  \array{
     A &\overset{f}{\longrightarrow}& X \mathrlap{\in Fib_{loc}}
     \\
     {}^{\mathllap{\in W_{loc} \cap Cof}}\downarrow
       &&
     \downarrow^{\mathrlap{\in Fib}}
     \\
     B &\underset{g}{\longrightarrow}& Y \mathrlap{\in Fib_{loc}}
  }
$$

we need to exhibit a lift. (In labeling the arrows we use throughout that $Cof_{loc} = Cof$.)

By assumption of [[functorial factorization]] we may factor this diagram
as follows:

$$
  \array{
     A
       &\overset{\in W_{loc} \cap Cof }{\longrightarrow}&
     \widehat{A}
       &\overset{\in Fib_{loc}}{\longrightarrow}&
     X \mathrlap{\in Fib_{loc}}
     \\
     {}^{\mathllap{\in W_{loc} \cap Cof}} \downarrow
       &&
       \downarrow^{\mathrlap{  }}
       &&
     \downarrow^{\mathrlap{\in Fib}}
     \\
     B
       &\underset{\in W_{loc} \cap Cof}{\longrightarrow}&
     \widehat{B}
       &\underset{ \in Fib_{loc} }{\longrightarrow}&
     Y \mathrlap{\in Fib_{loc}}
  }
$$



It follows that $\widehat{A}, \widehat{B} \in Fib_{loc}$.


Consider next the further factorization of the middle vertical morphism 
as $\overset{W_{loc} \cap Cof}{\longrightarrow} \overset{\in Fib_{loc}}{\longrightarrow}$

$$
  \array{
     A
       &\overset{\in W_{loc} \cap Cof }{\longrightarrow}&
     \widehat{A}
       &\overset{\in Fib_{loc}}{\longrightarrow}&
     X \mathrlap{\in Fib_{loc}}
     \\
     {}^{\mathllap{id}}\downarrow
       &&
     {}^{\mathllap{\in W \cap Cof}}\downarrow
       &&
     \downarrow^{\mathrlap{\in Fib}}
     \\
     A
       &\longrightarrow&
     \widehat{\widehat{A}}
       &\longrightarrow&
     Y
     \\
     {}^{\mathllap{\in W_{loc} \cap Cof}}\downarrow
        &&
     \downarrow^{\mathrlap{\in Fib_{loc}}}
       &&
     \downarrow^{\mathrlap{id}}
     \\
     B
       &\underset{\in W_{loc} \cap Cof}{\longrightarrow}&
     \widehat{B}
       &\underset{ \in Fib_{loc} }{\longrightarrow}&
     Y \mathrlap{\in Fib_{loc}}
  }
$$

Since it follows that  $\widehat A, \widehat{\widehat A} \in Fib_{loc}$ we invoke prop. \ref{LocalWeakEquivalencesBetweenLocalObjects}
to conclude that the top middle morphism is not just in $W_{loc} \cap Cof$ 
but indeed in $W \cap Cof$, as shown. 
This means that we have [[lifting]] in the top right square. Moreover, 
we also evidently have lifting in the bottom left square. 

$$
  \array{
     A
       &\overset{\in W_{loc} \cap Cof }{\longrightarrow}&
     \widehat{A}
       &\overset{\in Fib_{loc}}{\longrightarrow}&
     X \mathrlap{\in Fib_{loc}}
     \\
     {}^{\mathllap{id}}\downarrow
       &&
     {}^{\mathllap{\in W \cap Cof}}\downarrow
       &{}^{\mathllap{\exists}}\nearrow&
     \downarrow^{\mathrlap{\in Fib}}
     \\
     A
       &\longrightarrow&
     \widehat{\widehat{A}}
       &\longrightarrow&
     Y
     \\
     {}^{\mathllap{\in W_{loc} \cap Cof}}\downarrow
        &{}^{\mathllap{\exists}}\nearrow&
     \downarrow^{\mathrlap{\in Fib_{loc}}}
       &&
     \downarrow^{\mathrlap{id}}
     \\
     B
       &\underset{\in W_{loc} \cap Cof}{\longrightarrow}&
     \widehat{B}
       &\underset{ \in Fib_{loc} }{\longrightarrow}&
     Y \mathrlap{\in Fib_{loc}}
  }
$$


Together, these lifts
constitute the desired total lift.

=--

#### Every Bousfield localization is of this form {#LocHasToBeSLoc}

We have considered two definitions of left Bousfield localization: in the first we just required that cofibrations are kept and weak equivalences are increased. In the second we more specifically took the weak equivalences to be $S$-local weak equivalences.

We now show that every localization in the first sense is indeed of the second kind if we demand that both the original and the localized category are left proper, cofibrantly generated simplicial model categories.

+-- {: .num_prop }
###### Proposition

In the context of left proper, cofibrantly generated simplicial model categories,

for $C_{loc}$ a left Bousfield localization of $C$ (i.e. a structure with the same cofibrations as $C$ and more weak equivalences), there is a set $S \subset Mor(C)$ such that

$$
  C_{loc} = L_S C
  \,.
$$

=--

+-- {: .proof}
###### Proof

We show that choosing $S = J_{C_{loc}}$ to be the set of generating acyclic cofibrations does the trick.

First, the cofibrations of $C_{loc}$ and $L_S C$ coincide.
Moreover, the acyclic cofibrations of $L_S C$ contain all the acyclic cofibrations of $C_{loc}$ because

$$
  cof_{L_S C} \cap W_{L_S C} = llp(rlp(J_{L_S C}))
  \subset llp(rlp(S)) = llp(rlp(J_{C_{loc}}))
  \,.
$$

It remains to show that, conversely, every acyclic cofibration $f : X \to Y$ in $L_S C$ is an acyclic cofibration in $C_{loc}$.

Choose a cofibrant replacement for $X$ and $Y$

$$
  \array{
    X' &\stackrel{\in cof_C}{\to}& Y'
    \\
    \downarrow^{\mathrlap{\in W_C}}
     && \downarrow^{\mathrlap{\in W_C}}
    \\
    X &\stackrel{f}{\to}& Y
  }
$$

Then by 2-out-of-3 and since $W_{L_S C} \supset W_C$ the morphism $f' : X' \to Y'$ is still an acyclic cofibration on $L_S C$. Again by 2-out-of-3 and since $W_{C_{loc}} \supset W_C$, it is sufficient to show that $f'$ is an acyclic cofibration in $C_{loc}$.

To show that it is an acyclic cofibration in $C_{loc}$ it suffices to show that for every fibrant object $Z \in C_{loc}$ the morphism

$$
  C(Y',Z) \to C(X',Z)
$$

is a trivial fibration. Either by assumption or by the [characterization of S-local cofibrations](http://ncatlab.org/nlab/show/local+object#PropInModCat) this is the case if $Z$ is $S$-local and fibrant in $C$. The first statement is one of the direct consequences of the definition of $C_{loc}$ and the second follows because $S = J_{C_{loc}}$.


=--

#### Functoriality of localization
 {#FunctorialityOfLocalization}

+-- {: .num_prop }
###### Proposition

Let $C$ and $D$ be categories for which left Bousfield localization exists, and let

$$
  (L \dashv R)
  :
  C
  \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  D
$$

be a [[Quillen equivalence]]. Then for every small set $S \subset Mor(D)$ there is an induced Quillen equivalence of left Bousfield localizations

$$
  (L \dashv R)
  :
  C_{L(S)}
  \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  D_{S}
  \,.
$$

=--

This is due to [Hirschhorn (2002)](#Hirschhorn02).

#### Further properties

+-- {: .num_prop }
###### Proposition (Bousfield localization is indeed a localization)

If the left Bousfield localization exists, i.e. $L_S C$ is indeed a [[model category]] with the above definitions of cofibrations and weak equivalences, then it is indeed a [[localization of a model category]] in that there is a _left Quillen functor_

$$
  j \colon C \to L_S C
$$

(i.e. $j$ preserves cofibrations and trivial cofibrations and has a [[right adjoint]])

such that the total left [[derived functor]]

$$
  L j \colon Ho C \to Ho L_S C
$$

takes the images of $S \subset Mor(C)$ in $Ho(C)$ to [[isomorphism]]s

and every other left Quillen functor with this property factors by a unique left Quillen functor through $j$.

Moreover, the identity functor $Id_C$ on the underlying category is a [[Quillen adjunction]]

$$
  Id_C : L_S C \stackrel{\leftarrow }{\to} C : Id_C
$$

(and is itself a localization functor).

=--

+-- {: .proof}
###### Proof

The first part is theorem 3.3.19 in [Hirschhorn (2002)](#Hirschhorn02). The second part is prop 3.3.4, which follows directly from the following proposition.

=--


## Existence of localizations for combinatorial model categories {#Existence}

We discuss the existence of left Bousfield localization in the context of [[combinatorial model category|combinatorial model categories]] &lbrack;[Barwick (2010), Prop. 2.2 (Thm. 2.11 in preprint)](#Barwick10)&rbrack;. 

A similar existence result is available in the context of [[cellular model categories]] &lbrack;[Hirschhorn (2002)](#Hirschhorn02)&rbrack;, but for the combinatorial case a somewhat better theory is available.

By the corollary to [[Dugger's theorem]] on presentations for [[combinatorial model categories]] we have that every combinatorial model category is [[Quillen equivalence|Quillen equivalent]] to a [[proper model category|left proper]] [[simplicial model category|simplicial]] combinatorial model category.

Therefore there is little loss in assuming this extra structure, which the following statement of the theorem does.


\begin{theorem}
\label{ExistenceForLeftProperCombinatorialSimplicialModelCategories}
If $C$ is a

* [[left proper model category|left proper]]

* [[combinatorial model category|combinatorial]]

* [[simplicial model category|simplicial]]

[[model category]]

* and $S \subset Mor(C)$ is a [[small set]] of morphisms,

then the left Bousfield localization $L_S C$ does exist as a [[combinatorial model category]].

Moreover, it satisfies the following conditions:

* the fibrant objects of $L_S C$ are precisely the $S$-[[local object]]s of $C$ that are fibrant in $C$;

* $L_S C$ is itself a left [[proper model category]];

* $L_S C$ is itself a [[simplicial model category]].


\end{theorem}

(Without the assumption or conclusion of simplicial enrichment, this is [Barwick (2010), Prop. 2.2 (Thm. 2.11 in preprint)](#Barwick10), see also [Beke (2000), Thm. 1.7, Prop. 1.15 & 1.19](#Beke00)).

+-- {: .proof}
###### Proof

A proof of this making use of [Jeff Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#SmithTheorem) for [[combinatorial model category|combinatorial model categories]] appears
as [[Higher Topos Theory|HTT, prop. A.3.7.3]] and
as theorem 2.11 in [Bar07](http://arxiv.org/abs/0708.2067) and as theorem 4.7 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).

We follow [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf) for the proof that the assumptions of Smith's recognition theorem are satisfied and follow [[Higher Topos Theory|HTT, prop. A.3.7.3]] for the characterization of the fibrant objects. The details are spelled out in the following subsections.

=--


### Prerequisites for the proof

The proof we give is self-contained, except that it builds on the following notions and facts.

#### Small objects

A [[cardinal number]] $\kappa$ is _regular_ if it is not the cardinality of a union of $\lt \kappa$ sets of size $\lt \kappa$.

A [[poset]] $J$ is a $\kappa$-[[directed set]] if all subsets of cardinality $\lt \kappa$ have a common upper bound. A $\kappa$-[[directed colimit]] is a [[colimit]] $\lim_\to F$ over a functor $F : J \to C$.

An object $X$ in a category $C$ is a $\kappa$-[[compact object]] if $C(X,-) : C \to C$ commutes with all $\kappa$-[[directed colimit]]s. For $\lambda \gt \kappa$ every $\kappa$-compact object is also $\lambda$-compact.

This means that a morphism from a $\kappa$-compact object into an object that is a $\kappa$-directed colimit over component objects always lifts to one of these component objects.

An object is a [[small object]] if it is $\kappa$-compact for some $\kappa$.

A [[locally small category|locally small]] but possibly non-[[small category]] $C$ is an [[accessible category]] if it has a small sub-[[set]] of generating $\kappa$-[[compact object]]s such that every other object is a $\kappa$-[[directed colimit]] over such generators.

If such a category has all small colimits, it is called a [[locally presentable category]].

In particular, in a locally presentable category the [[small object argument]] for factoring of morphisms applies with respect to every set of morphisms.


#### Combinatorial model categories

A [[combinatorial model category]] is a [[locally presentable category]] that is equipped with a [[cofibrantly generated model category]] structure. So in particular there is a set of generating (acyclic) cofibrations that map between [[small objects]].

[Smith's recognition theorem](combinatorial+model+category#SmithTheorem) says that a [[locally presentable category]] has a combinatorial model category structure already if it has weak equivalences and generating cofibrations satisfying a simple condition and if weak equivalences form an [[accessible category|accessible]] [[subcategory]] of the [[arrow category]]. This means that only two thirds of the data for a generic combinatorial model category needs to be checked and greatly facilitates checking model category structures.

[Dugger's theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem) implies that every combinatorial model category is [[Quillen equivalence|Quillen equivalent]] to a [[proper model category|left proper]] [[simplicial model category|simplicial]] combinatorial model category.

So we may assume without much restriction of generality that we are dealing with the localization of a [[proper model category|left proper]] [[combinatorial simplicial model category]].

Since the [[small object argument]] applies, a [[combinatorial model category]] has fibrant- and cofibrant-replacement functors $P,Q : C \to C$
([[functorial factorization]]).

By the axioms of an [[enriched model category]] it follows that the functor

$$
  \mathbf{R}Hom_C \coloneqq C(Q(-),P(-)): C^{op} \times C \to SSet
$$

takes values in [[Kan complexes]]. This is called the [[derived hom space]] functor of $C$: we think of $\mathbf{R}Hom(X,Y)$ as the [[∞-groupoid]] of maps from $X$ to $Y$, homotopies of maps, homotopies of homotopies, etc.


#### Local objects

An ordinary [[reflective subcategory]] $C_{loc} \stackrel{\stackrel{T}{\leftarrow]}}{\hookrightarrow} C$ is specified by the preimages $S = T^{-1}(isos)$ of the isomorphisms under $T$ as the full subcategory on the $S$-[[local object]]s $X$: those such that $Hom_C(A \stackrel{s \in S}{\to}B, X)$ are isomorphisms.

The analogous statement in the context of model categories uses the [[derived hom space]] functor instead: given a collection $S \subset Mor(C)$ an object $X$ is called an $S$-[[local object]] if $\mathbf{R}Hom_C(A \stackrel{s \in S}{\to} B, X)$ are weak equivalences.

Similarly, the collection $W_S$  of morphisms $f : E \to F$ such that for all $S$-local objects $X$ $\mathbf{R}Hom_C(f,X)$ is a weak equivalence is called the collection of $S$-[[local object|local weak equivalence]]s.

A [lemma by Lurie](http://ncatlab.org/nlab/show/local+object#PropInModCat) says that for $A \stackrel{s \in S}{\hookrightarrow} B$ a cofibration and $X$ fibrant, $X$ is $S$-local precisely if $C(s,X) : C(B,X) \to C(A,X)$ is an [[Kan fibration|acyclic Kan fibration]]. This helps identifying the $S$-local fibrant objects.

#### Homotopy (co)limits

In an ordinary category, a [[limit]] diagram is one such that applying $Hom_C(X,-) : C \to C $ to it produces a limit diagram in [[Set]], for all objects $X$. Similarly a colimit diagram is one sent to Set-limits under all $Hom_C(-,X)$.

In a model category, this has an analog with respect to the [[derived hom space]] functor $\mathbf{R}Hom_C$. A [[homotopy limit]] diagram is one sent by all $\mathbf{R}Hom_C(-,X)$ to a homotopy limit (...). Similarly for homotopy colimits.

Sometimes ordinary (co)limits in a model category are already also homotopy colimits:

* an [observation by Barwick](http://ncatlab.org/nlab/show/local+object#PropInModCat) shows that in a [[proper model category|left proper]] [[simplicial model category]] ordinary [[pushout]]s along cofibrations are already homotopy colimits.

* an [observation by Dugger](http://ncatlab.org/nlab/show/combinatorial+model+category#hocolims) shows that [[transfinite composition]] colimits of length $\kappa$ in a combinatorial model category are automatically homotopy colimits for sufficiently large $\kappa$.

Since these are the two operations under which $cell(cof_c \cap W_C)$ is closed, this facilitates finding this closure given that by the above the elements of $cof_C \cap W_S$ are characterized by their images under $\mathbf{R}Hom_C(-,X)$ for $S$-local $X$.


#### Size issues

The following proof uses the [[small object argument]] several times. In particular, at one point it is applied relative to the collection $S$ of morphisms at which we localize. It is at this point that we need that assumption that $S$ is indeed a (small) [[set]], and not a proper [[class]].

For the small object argument itself, this requirement comes from the fact that it involves colimits indexed by $S$. These won't in general exist if $S$ is not a set.

The collection of $S$-local weak equivalences $W_S$, however, won't be a small set in general even if $S$ is. But for [Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#SmithTheorem) to apply we need to check that the full subcategory of $Arr(C)$ on $W_S$ is, while not small, [[accessible category|accessible]].

To establish this we need two [properties of accessible categories](http://ncatlab.org/nlab/show/accessible+category#Properties): the inverse image of an accessible subcategory under a functor is accessible, and the collections of fibrations, weak equivalences and acyclic fibrations in a combinatorial model category are accessible.


### The proof itself


+-- {: .standout}

**Beginning of the proof** of the existence of the left Bousfield localization of a left proper combinatorial simplicial model category at a set $S$ of morphisms.

=--


#### Recognition of the combinatorial model structure

Using [Smith's recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#SmithTheorem), for establishing the [[combinatorial model category]] structure, it is sufficient to

* exhibit a [[set]] $I$ of cofibrations of $L_S C$ such that $inj(I) \subset W_{L_S C}$ and such that $cof(I) \cap W_{L_S C}$ is closed under [[pushout]] and [[transfinite composition]].

* check that the weak equivalences form an accessibly embedded accessible subcategory.

For the first item choose $I \coloneqq I_C$ with $I_C$ any set of generating cofibrations of $C$, that exists by assumption on $C$.
Then $inj(I) = inj(I_C) = fib_C \cap W_C \subset W_C \subset W_{L_S C}$.

It remains to demonstrate closure of $cof(I) \cap W_{L_S C} = cof_C \cap W_{L_S C}$ under pushout and transfinite composition.

One elegant way to see this, following [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf), is to notice that the relevant ordinary [[colimit]]s all happen to be [[homotopy colimit]]s:

* all [[pushout]]s along cofibrations in a left [[proper model category]] are homotopy pushouts (details are [here](http://ncatlab.org/nlab/show/proper+model+category#homotopy_colimits_in_proper_model_categories_9));

* all [[transfinite composition]] colimits in a [[combinatorial model category]] are homotopy colimits (details are [here](http://ncatlab.org/nlab/show/combinatorial+model+category#properties_17))

By their definition in terms of the [[derived hom space]] functor, $S$-local weak equivalences in $C$ are preserved under [[homotopy limit|homotopy colimit]]s:

for $K \stackrel{}{\to}L$ an $S$-local morphism -- a morphism in $W_{L_S C}$ -- and for

$$
  \array{
    K &\stackrel{\simeq_S}{\to}& L
    \\
    \downarrow && \downarrow
    \\
    K' &\to& L'
  }
$$

a [[homotopy limit|homotopy pushout]] diagram, we have (by the universal property of homotopy limits) for every object $Z$ -- in particular for every every $S$-[[local object]] $Z$ -- a [[homotopy limit|homotopy pullback]]

$$
  \array{
    \mathbf{R}Hom(L',Z) &\to&
    \mathbf{R}Hom(K',Z)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{R}Hom(L,Z) &\stackrel{\simeq}{\to}&
    \mathbf{R}Hom(K,Z)
  }
  \,,
$$

of $\infty$-groupoids. where the bottom morphism is a weak equivalence by assumption of $S$-locality of $Z$ and $(K \to L)$. But then also the top horizontal morphism is a weak equivalence for all $S$-local $Z$ and therefore $K' \to L'$ is in $W_{L_S C}$.

Similarly for [[transfinite composition]] colimits.

Therefore, indeed, $cof(I) \cap W_{L_S C}$ is closed under pushouts and transfinite composition.


#### Accessibility of the $S$-local weak equivalences

For the [Smith recognition theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#SmithTheorem) to apply we still have to check that the $S$-[[local object|local weak equivalences]] $W_S$ span an [[accessible category|accessible full subcategory]] $Arr_S(C) \subset Arr(S)$ of the [[arrow category]] of $C$.

By the general [properties of accessible categories](http://ncatlab.org/nlab/show/accessible+category#Properties) for that it is sufficient to exhibit $Arr_S(C)$ as the inverse image of under functor $T : Arr_S(C) \hookrightarrow Arr(C)$ of the accessible category $Arr_W(C)$ spanned by ordinary weak equivalences in $C$.

That functor we take to be the $S$-local fibrant replacement functor from above

$$
  T : (X \to Y) \mapsto (T X \stackrel{T f}{\to} T Y)
  \,.
$$

By one of the above propositions, $S$-local weak
equivalence between $S$-local objects are precisely
the ordinary weak equivalences.
This means that the inverse image under $T$ of the weak equivalences in $C$ are all $S$-local weak equivalences

$$
  T^{-1}(Arr_{W_C}(C) = Arr_S(C)
  \,.
$$

Therefore this is an [[accessible category]].

+-- {: .standout}

**End of the proof** of the existence of the left Bousfield localization of a left proper combinatorial simplicial model category at a set $S$ of morphisms.

=--



### Further properties

+-- {: .num_lemmaa }
###### Lemma (localization at cofibrations is sufficient)

Every combinatorial localization $B = L_{R} A$ of $A$ is already of the form $L_{S}A $ for $S$ a set of just cofibrations.

=--

+-- {: .proof}
###### Proof

See [[Higher Topos Theory|HTT, prop. A.3.7.4]]

We demonstrate that $S \coloneqq J_B$ does the trick.


...

=--



### Using large cardinal axioms

If one assumes [[large cardinal]] axioms then the existence of Bousfield localization follows much more generally.

+-- {: .num_theorem}
###### Theorem

[[Vopěnka's principle]] implies the statement:

Let $C$ be a [[left proper model category|left proper]] [[combinatorial model category]] and $Z \in Mor(C)$ a [[class]] of [[morphism]]s. Then the [[Bousfield localization of model categories|left Bousfield localization]] $L_Z W$ exists.

=--

This is theorem 2.3 in ([RosickyTholen](#RosickyTholen)).







## Existence of localizations for tractable ennriched model categories

The above statement is generalized to the context of [[enriched model category]] theory by the following result:


+-- {: .num_theorem }
###### Theorem (existence of enriched Bousfield localization)

Let

* $V$ be a [[tractable model category|tractable]] [[symmetric monoidal category|symmetric]] [[monoidal model category]];

* $C$ a [[tractable model category|tractable]] [[proper model category|left proper]] $V$-[[enriched model category]]

* $S \subset Mor(C)$ a small set

(all with respect to a fixed [[Grothendieck universe]]).

Then the left enriched Bousfield localization $L_{S/V} C$ does exist and is [[proper model category|left proper]] and [[tractable model category|tractable]].

=--


This is ([Barwick 2007a, theorem 4.46](#Barwick07a)).





















## Examples and Applications

### Categories to which the general existence theorem applies

The following [[model category|model categories]] $C$ are left [[proper model category|proper]] [[cellular model category|cellular]]/[[combinatorial model category|combinatorial]], so that the above theorem applies and for every [[set]] $S \subset Mor(C)$ the Bousfield localization $L_S C$ does exist.

* [[Top]] with its standard [[model structure on topological spaces]];

* [[SSet]] with its standard [[model structure on simplicial sets]];

* the category of [[symmetric monoidal smash product of spectra|symmetric spectra]] in a pointed left-proper cellular model category

* and so on...

If $C$ is a left [[proper model category|proper]] ([[simplicial model category|simplicial]]) [[cellular model category]], then so is

* the [[functor category]] $[D,C]$ for any ([[simplicially enriched category|simplicial]]) [[small category]]  $D$ (using the [[global model structure on functors]]);

* the [[over category]] $C/s$ for any object $x \in C$ .

### At derived idempotent monads

The [[Bousfield-Friedlander theorem]] gives Bousfield localizations at the [[derived functor]]-version of [[idempotent monads]].

See there for more examples of this general construction.

### Localization of spectra

see _[[Bousfield localization of spectra]]_


### Local model structure on presheaves

Left Bousfield localization produces the _local_ [[model structure on homotopical presheaves]]. For instance the [[local model structure on simplicial presheaves]].




## Relation to other concepts

### Locally presentable $(\infty,1)$-categories {#LocPresInf}

As described at [[presentable (∞,1)-category]], an [[(∞,1)-category]] $\mathbf{C}$ is presentable precisely if, as an [[simplicially enriched category]], it arises as the full subcategory of fibrant-cofibrant objects of a [[combinatorial simplicial model category]].

The _proof_ of this proceeds via Bousfield localization, and effectively exhibits Bousfield localization as the procedure that models [[localization of an (∞,1)-category]] when $(\infty,1)$-categories are modeled by model categories.

For notice that

1. a presentable $(\infty,1)$-category $\mathbf{C}$ is one arising as the [[localization of an (∞,1)-category|localization]]

   $$
     \mathbf{C} \simeq S^{-1} Funct(K,\infty Grpd) = S^{-1}PSh_{(\infty,1)}(K)
   $$

   of an [[(∞,1)-category of (∞,1)-presheaves]]

1. every [[(∞,1)-category of (∞,1)-presheaves]]
   $PSh_{(\infty,1)}(K)  \simeq ([K,SSet]_{inj})^\circ$ arises as
   the subcategory of fibrant-cofibrant objects of the
   global [[model structure on simplicial presheaves]];

1. in terms of the [[simplicial model category]]
   $[K,SSet]_{inj}$ the prescription for
   [[localization of an (∞,1)-category|localization as an (∞,1)-category]] and passing to the subcategory of fibrant-cofibrant objects of the Bousfield localization $L_S [K,SSet]_{inj}$ is literally the same: in both cases one passes to the full subcategory on the $S$-[[local object]]s.

Moreover, by [Dugger's theorem on combinatorial model categories](http://ncatlab.org/nlab/show/combinatorial+model+category#duggers_theorem_13) every [[combinatorial simplicial model category]] arises this way.

This is the argument of [[Higher Topos Theory|HTT, prop A.3.7.6]].

This gives a good conceptual interpretation of Bousfield localization, since the [[localization of an (∞,1)-category]] is nothing but an adjunction

$$
  \mathbf{C} \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  \mathbf{D}
$$

that exhibits $\mathbf{C}$ as a [[reflective (∞,1)-subcategory]] of $\mathbf{D}$.

So we find the diagram

+-- {: .standout}

**Localization of $(\infty,1)$-presheaf categories**

$$
  \array{
      Sh_{(\infty,1)}(K)
     &\stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
     &
     PSh_{(\infty,1)}(K)
     &&&
     abstract\;higher\;categorical\;def
     \\
     \uparrow^{\simeq}
     &&
     \uparrow^{\simeq}
     &&& Lurie's \;theorem
     \\
     ([K^{op},SSet]_{inj}^{loc})^\circ
     &\stackrel{\stackrel{Bousfield\;loc.}{\leftarrow}}
     {\to}&
     ([K^{op},SSet]_{inj})^\circ
     &&&
     concrete\;realization
  }
  \,.
$$

=--


Here $(-)^\circ$ denotes passing to the full [[simplicially enriched category|simplicially enriched]] [[subcategory]] on the fibrant-cofibrant objects, regarding that as an [[(∞,1)-category]]. (If one wants to regard that as a [[quasi-category]], then $(-)^\circ$ also involves taking the [[homotopy coherent nerve]] of this simplicially enriched category.)


### Localization of triangulated categories

There is also a notion of
[[Bousfield localization of triangulated categories]].

Under suitable conditions it should be true that for $C$ a model category whose [[homotopy category]] $Ho(C)$ is a [[triangulated category]] the homotopy category of a left Bousfield localization of $C$ is the left Bousfield localization of $Ho(C)$. See [this answer on MO](http://mathoverflow.net/a/136517/1291).


## Related entries

* [[localization]], [[colocalization]]

* [[right Bousfield delocalization]]

* [[localization at an object]]

* [[semi-left-exact left Bousfield localization]]


## References
 {#References}

The original article:

* {#Bousfield75} [[A. K. Bousfield]], *The localization of spaces with respect to homology*, Topology **14** (1975), 133–150 &lbrack;<a href="http://dx.doi.org/10.1016/0040-9383(75)90023-3">doi:10.1016/0040-9383(75)90023-3</a>&rbrack;

Detailed discussion (including existence results for [[left proper model category|left proper]] [[cellular model category|cellular model categories]]):

* {#Hirschhorn02} [[Philip Hirschhorn]], Section 3.3 and Chapter 4 of: _[[Model Categories and Their Localizations]]_, AMS Math. Survey and Monographs 99 (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;

Existence results for (plain an [[enriched model category|enriched]]) [[combinatorial model categories]]:

* {#Barwick10} [[Clark Barwick]], *On left and right model categories and left and right Bousfield localizations*, Homology, Homotopy and Applications **12** 2 (2010) 245–320
&lbrack;[doi:10.4310/hha.2010.v12.n2.a9](https://doi.org/10.4310/hha.2010.v12.n2.a9), subsuming: [arXiv:0708.2067](https://arxiv.org/abs/0708.2067), [arXiv:0708.2832](https://arxiv.org/abs/0708.2832), [arXiv:0708.3435](http://arxiv.org/abs/0708.3435)&rbrack;

see also

* {#Beke00} [[Tibor Beke]], Theorem 1.7, Prop. 1.15, 1.19 in: *Sheafifiable homotopy model categories*,  Math. Proc. Cambridge Philos. Soc. __129__ 3 (2000) 447-475 &lbrack;[arXiv:math/0102087](http://arxiv.org/abs/math/0102087), [doi:10.1017/S0305004100004722](https://doi.org/10.1017/S0305004100004722)&rbrack; 

and specifically for combinatorial [[simplicial model categories]]:

* {#Lurie} [[Jacob Lurie]], around prop. A.3.7.3 of: *[[Higher Topos Theory]]* (2009)

The relation to [[localization of an (infinity,1)-category]] is also in *[[Higher Topos Theory]]*, for the time being see discussion at [[models for ∞-stack (∞,1)-toposes]].
 
On [[right Bousfield localization]]:

* {#Barwick07b} [[Clark Barwick]], *On the Dreaded Right Bousfield Localization* &lbrack;[arXiv:0708.3435](http://arxiv.org/abs/0708.3435), [pdf](https://www.maths.ed.ac.uk/~cbarwick/papers/complete.pdf)&rbrack;

The relation to [[Vopěnka's principle]]:

* {#RosickyTholen} [[Jiří Rosický]], [[Walter Tholen]], _Left-determined model categories and universal homotopy theories_,  Transactions of the American Mathematical Society **355** 9 (2003) 3611-3623 &lbrack;[jstor:1194855](http://www.jstor.org/stable/1194855)&rbrack;

Bousfield localization specifically for [[stable model categories]] (such as [[model structures on spectra]]):

* [[Luca Pol]], [[Jordan Williamson]], *The Left Localization Principle, completions, and cofree $G$-spectra*, J. Pure Appl. Algebra **224** 11 (2020) 106408 &lbrack;[arXiv:1910.01410](https://arxiv.org/abs/1910.01410), [doi:10.1016/j.jpaa.2020.106408](https://doi.org/10.1016/j.jpaa.2020.106408)&rbrack;


Comprehensive review:

* {#Lawson2022} [[Tyler Lawson]], *An introduction to Bousfield localization*, in: *[[Stable categories and structured ring spectra]]*, MSRI Book Series, Cambridge University Press (2022) &lbrack;[arXiv:2002.03888](https://arxiv.org/abs/2002.03888)&rbrack;





[[!redirects bousfield localization]]
[[!redirects Bousfield localisation]]

[[!redirects left Bousfield localization]]
[[!redirects left Bousfield localizations]]

[[!redirects left Bousfield localization of model categories]]
[[!redirects left Bousfield localizations of model categories]]


[[!redirects right Bousfield localization]]
[[!redirects right Bousfield localizations]]
[[!redirects left Bousfield localisation]]
[[!redirects left Bousfield localisations]]
[[!redirects right Bousfield localisation]]
[[!redirects right Bousfield localisations]] 


[[!redirects localization of a simplicial model category]]
[[!redirects localization of simplicial model categories]]

[[!redirects Bousfield localization of a simplicial model category]]
[[!redirects Bousfield localization of simplicial model categories]]




