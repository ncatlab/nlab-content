{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

# Infinitary Lawvere theories
* table of contents
{: toc}

## Idea

An infinitary Lawvere theory is a generalisation of a [[Lawvere theory]] to allow infinitary operations.  As a motivating example, consider the theory of [[suplattices]], where we have, for every [[cardinal number]] $n$, an operation to take the [[supremum]] of $n$ elements.

Size issues can be tricky for infinitary Lawvere theories.  Na&#239;vely, you would expect an infinitary Lawvere theory of [[complete lattices]] too, but there is none, because a smallness condition fails.  (This is connected to the nonexistence of [[free complete lattices]].)

In accordance with the [[red herring principle]], an infinitary Lawvere theory should not be thought of a special case of a [[Lawvere theory]].  To avoid this, one may call the latter a *finitary* Lawvere theory.

There are also many-sorted infinitary Lawvere theories, as well as $\kappa$-ary Lawvere theories for any [[regular cardinal]] $\kappa$.


## Definitions

A __many-sorted infinitary Lawvere theory__ is a [[locally small category]] $\mathcal{D}$ with all small [[products]] and equipped with a small family $\mathcal{R}$ of objects (called __sorts__) such that every object is a small product of these sorts.

Given a small [[set]] $S$, an __$S$-sorted infinitary Lawvere theory__ is a locally small category $\mathcal{D}$ with all small products and equipped with a [[functor]] from $S$ to $\mathcal{D}$ such that every object in $\mathcal{D}$ is a small product of objects in the image of $S$.  Note than any many-sorted infinitary Lawvere theory $(\mathcal{D},\mathcal{R})$ may be interpreted as an $S$-sorted infinitary Lawvere theory, where $S$ is the index set of the family $\mathcal{R}$.

An __unsorted infinitary Lawvere theory__ is a locally small category $\mathcal{D}$ with all small products and equipped with an object $R$ (so that $(\mathcal{D},R)$ is a [[pointed category]]) such that every object is [[isomorphic]] to $R^n$ for some small cardinal number $n$.  An __infinitary Lawvere theory__ is by default an unsorted infinitary Lawvere theory, invoking the [[red herring principle]].  Note that an unsorted infinitary Lawvery theory is the same thing as a $1$-sorted infinitary Lawvere theory.

We will give the definitions of further special cases for unsorted infinitary Lawvere theories, but these definitions may also be generalised to the many-sorted case.

Given a [[regular cardinal]] $\kappa$, a __$\kappa$-ary Lawvere theory__ is a locally small pointed category $(\mathcal{D},R)$ with all $n$-ary products for $n \lt \kappa$ such that every object is isomorphic to $R^n$ for some $n \lt \kappa$.  Every $\kappa$-ary Lawvere theory may be interpreted as an infinitary Lawvere theory by using the free category with all small products on $\mathcal{D}$.  More generally, every $\kappa$-ary Lawvere theory may be interpreted as a $\lambda$-ary Lawvere theory if $\kappa \leq \lambda$.

A __bounded infinitary Lawvere theory__ is an infinitary Lawvere theory which is (under the interpretation above) [[equivalence of categories|equivalent]] to some $\kappa$-ary Lawvere theory.

A __finitary Lawvere theory__ is a locally small pointed category $(\mathcal{D},R)$ with all finitary products such that every object is isomorphic to $R^n$ for some [[natural number]] $n$.  A __[[Lawvere theory]]__ is by default a finitary Lawvere theory, invoking the [[red herring principle]].  Note that a finitary Lawvere theory is the same thing as an $\aleph_0$-ary Lawvere theory.


## Size issues

[Freyd and Street (1995)](http://tac.mta.ca/tac/volumes/1995/n9/1-09abs.html) have shown that a category $\mathcal{D}$ is [[small category|small]] if and only if both $\mathcal{D}$ and the [[functor category]] $[\mathcal{D},Set]$ are locally small.  Analogously, it seems that a category $\mathcal{D}$ with products may be given the structure of a many-sorted infinitary Lawvere theory if and only if both $\mathcal{D}$ and $Prod[\mathcal{D},Set]$ (the category of [[product-preserving functor]]s from $\mathcal{D}$ to $Set$, a [[full subcategory]] of $[\mathcal{D},Set]$) are locally small.  In both cases, the 'only if' part is straightfoward, but we haven't yet proved the 'if' part.

See [the n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=1673) for more preliminary results.

## Algebraic Categories

+-- {: .un_lemma}
###### Conjecture
A multi-sorted infinitary Lawvere theory $\mathcal{D}$ defines an [[algebraic category]] over [[Set]] by taking the [[functor category]] consisting of all **product-preserving** covariant functors from $\mathcal{D}$ in to $Set$.
=--

Let us write this functor category as $Prod[\mathcal{D},Set]$ and start by showing that it is a [[locally small category]].

+-- {: .num_lemma #ProdLocSmall}
###### Lemma
The category $Prod[\mathcal{D},Set]$ of product-preserving functors and natural transformations is locally small.
=--

+-- {: myproof}
###### Proof
Let $V_1, V_2 \colon \mathcal{D} \to Set$ be two product-preserving covariant functors.
From the definition of a multi-sorted infinitary category we see that we may choose a set of sorts, say $S$.
Let $D_s \in \mathcal{D}$ be the image of $s \in S$.

As $S$ is a set, the product
$$
\prod_{s \in S} Set(V_1(D_s), V_2(D_s))
$$
is a set.  We define a function $[V_1,V_2] \to \prod_{s \in S} Set(V_1(D_s), V_2(D_s))$ by sending a natural transformation $\alpha \colon V_1 \to V_2$ to the product of its values at each $D_s$.  That is,
\begin{equation}
\label{eq:natrans}
\alpha \mapsto \big(\alpha_{D_s}\big)_{s \in S}.
\end{equation}

Let $D \in \mathcal{D}$ be an arbitrary object.  From the definition of a multi-sorted infinitary Lawvere theory, there is an isomorphism
$$
d \colon D \cong \prod_{s \in S} D_s^{X_s}
$$
for some sets $X_s$.   For each $s \in S$ and $x \in X_s$, there is a projection $p_{s,x} \colon \prod_{s \in S} D_s^{X_s} \to D_s$.
As $V_1$ and $V_2$ are product-preserving, we have isomorphisms
$$
V_i\left( \prod_{s \in S} D_s^{X_s}\right) \cong  \prod_{s \in S} V_i(D_s)^{X_s}
$$
commuting with the projections.
Thus for each $s \in S$ and $x \in X_s$, we have the following commutative diagram.

*insert diagram here*

Since this holds for all $s \in S$ and $x \in X_s$, by the basic properties of products, there is a unique morphism $\prod_{s \in S} V_1(D_s)^{X_s} \to   \prod_{s \in S} V_2(D_s)^{X_s}$ making the diagram commute.  This morphism is normally written $\prod_{s \in S} \alpha_{D_s}^{X_s}$.  Thus under the isomorphism $d$ above, $\alpha_D$ is taken to $\prod_{s \in S} \alpha_{D_s}^{X_s}$.  As this holds for all $D \in \mathcal{D}$, $\alpha$ is completely determined by the $\alpha_{D_s}$, whence the map in \ref{eq:natrans} is injective.

Hence $[V_1,V_2]$ is a subset of a set and thus a set.
=--

Now that we have a locally small category, the next step is to show that the forgetful functor has a [[left adjoint]].  Firstly, we need to _define_ this forgetful functor.  As we are in the most general case, the forgetful functor does not go to $Set$ but to $S$-indexed tuples of sets (or an $S$-graded set), where $S$ is a choice of set of sorts for $\mathcal{D}$.  To make things a little simpler, we assume that the _sorting_ functor $S \to \mathcal{D}$ is injective on isomorphism classes so that if $s \ne s'$ in $S$ then $D_s \ncong D_{s'}$ in $\mathcal{D}$.  With this assumption, the forgetful functor $Prod[\mathcal{D},Set] \to Set^S$ is the evaluation functor:
$$
V \mapsto \big(s \mapsto V(D_s)\big), \qquad \alpha \mapsto \big(s \mapsto \alpha_{D_s}\big).
$$

+-- {: .num_lemma #ProdFree}
###### Lemma
The forgetful functor $Prod[\mathcal{D},Set] \to Set^S$ has a left adjoint.  The left adjoint is given on objects by:
$$
\big(s \mapsto X_s\big) \mapsto \mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, -\right)
$$
=--

+-- {: myproof}
###### Proof
To ease the notation, let us write $U$ for the forgetful ("underlying set(s)") functor and $F$ for the free functor.

To show the adjunction, we define the unit and counit natural transformations:
$$
\eta \colon I \to U F, \qquad \epsilon \colon F U \to I
$$

Let us consider $\eta$.  To define this, we evaluate it at an $S$-graded set, $X$, to get a morphism of graded sets, $\eta_X$.  Such a morphism is itself a natural transformation so we evaluate again at $s_0 \in S$.  At this point, we have a function (in $Set$)
$$
\eta_{X,s_0} \colon  X_{s_0} \to \mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, D_{s_0}\right).
$$
This is simple to describe: it is assignment to $x \in X_{s_0}$ of the projection onto the $x$th $D_{s_0}$-factor:
$$
\prod_{s \in S} D_s^{X_s} \to D_{s_0}^{X_{s_0}} \overset{p_x}{\to} D_{s_0}.
$$

The counit, $\epsilon$, is a little more complicated to describe.  Let $V \colon \mathcal{D} \to Set$ be a covariant product-preserving functor.  Evaluated at $V$, $\epsilon_V$ is a natural transformation
$$
\mathcal{D}\left(\prod_{s \in S} D_s^{V(D_s)}, -\right) \to V
$$
By the [[Yoneda lemma]], such natural transformations are in bijective correspondence with elements of $V\left(\prod_{s \in S} D_s^{V(D_s)}\right)$.  As $V$ is product-preserving, there is a natural isomorphism:
$$
V\left(\prod_{s \in S} D_s^{V(D_s)}\right) \cong \prod_{s \in S} V(D_s)^{V(D_s)}
$$
Now for any set $Z$, there is an obvious element in $Z^Z$: the one that has a $z$ in the $z$th place (which corresponds to the identity function $Z \to Z$).  Taking the product of these gives an element in $\prod_{s \in S} V(D_s)^{V(D_s)}$ which we use to define $\epsilon_V$.

Let us now prove that these provide the desired adjunction.  For one half, we need to consider the composition:
$$
F \overset{F \eta}{\to} F U F \overset{\epsilon F}{\to} F
$$
Let us apply this to a graded set $X = (s \mapsto X_s)$.  Then we are looking at a natural transformation from
$$
\mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, -\right)
$$
to itself.  By the standard Yoneda argument, it is sufficient to look at the induced function on
$$
\mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, \prod_{s \in S} D_s^{X_s}\right)
$$
and in particular at the image of the identity therein.

The first part comes from $F\eta$ at $F(X)$.  For each $s_0 \in S$, we have a function $\eta_{X,s_0} \colon X_{s_0} \to \mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, D_{s_0}\right)$ and thus a morphism
$$
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}  \to \prod_{s \in S} D_s^{X_s}
$$
What this does is the following: it sends component corresponding to the $(s,x)$th projection to the $x$th component and all other components are forgotten.
Thus we have a morphism:
$$
\mathcal{D}\left( \prod_{s \in S} D_s^{X_s},  \prod_{s \in S} D_s^{X_s}\right) \to \mathcal{D}\left(
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}, \prod_{s \in S} D_s^{X_s}\right)
$$
Under this, the identity morphism goes to the projection morphism described just above.

Now we apply $\epsilon F$.  

_in progress_
=--