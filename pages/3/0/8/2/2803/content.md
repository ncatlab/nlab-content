* toc
{:toc}

# Statement

The **Yoneda lemma for bicategories** is a version of the [[Yoneda lemma]] that applies to [[bicategories]], the most common algebraic sort of weak [[2-category]].  It says that for any bicategory $C$, any object $x\in C$, and any [[pseudofunctor]] $F\colon C^{op}\to Cat$, there is an equivalence of categories

$$ [C^{op},Cat](C(-,x), F) \simeq F(x) $$

which is pseudonatural in $x$ and $F$, and which is given by evaluation at $1_x$, i.e. $\alpha\colon C(-,x)\to F$ maps to $\alpha_x(1_x)$.

For bicategories $A$ and $B$, $[A,B]$ denotes the bicategory of [[pseudofunctors]], [[pseudonatural transformations]], and [[modifications]] from $A$ to $B$.  Note that it is a strict 2-category as soon as $B$ is.

# Implications

In particular, the Yoneda lemma for bicategories implies that there is a [[Yoneda embedding]] for bicategories $C\to [C^{op},Cat]$ which is [[2-fully-faithful]], i.e. an equivalence on hom-categories.  Therefore, $C$ is [[equivalence|equivalent]] to a sub-bicategory of $[C^{op},Cat]$.  Since $Cat$ is a [[strict 2-category]], it follows that $C$ is equivalent to a strict 2-category, which is one form of the [[coherence theorem for bicategories]].  (Conversely, another form of the coherence theorem can be used to prove the Yoneda lemma; see below.)

# Proof

A detailed proof of the bicategorical Yoneda lemma seems to be hard to find in the liturature.  (Anyone have references to add?)

## Explicit proof

An explicit proof, involving many diagrams, has been written up by [[Igor Bakovic]] and can be found [here](http://www.irb.hr/korisnici/ibakovic/yoneda.pdf).

## High-technology proof

We will take it for granted that $[C^{op},Cat]$ is a well-defined bicategory; this is a basic fact having nothing to do with the Yoneda lemma.  We also take it as given that "evaluation at $1_x$" functor
$$ [C^{op},Cat](C(-,x), F) \to F(x) $$
is well-defined and pseudonatural in $F$ and $x$; our goal is to prove that it is an equivalence.  (Granted, these basic facts require a fair amount of verification as well.)

We will use part of the [[coherence theorem for pseudoalegbras]], which says that for a suitably well-behaved strict [[2-monad]] $T$, the inclusion $T$-$Alg_{strict} \hookrightarrow Ps$-$T$-$Alg$ of the 2-category of strict $T$-algebras and strict $T$-morphisms into the 2-category of pseudo $T$-algebras and pseudo $T$-morphisms has a left adjoint, usually written as $(-)'$.  Moreover, for any pseudo $T$-algebra $A$, the unit $A\to A'$ is an equivalence in $Ps$-$T$-$Alg$.

First, there is a 2-monad $T$ such that strict $T$-algebras are strict 2-categories, strict $T$-morphisms are strict 2-functors, pseudo $T$-algebras are [[unbiased bicategories]], and pseudo $T$-morphisms are [[pseudofunctors]].  By Mac Lane's coherence theorem for bicategories, any ordinary bicategory can equally well be considered as an unbiased one.  Thus, since $Cat$ is a strict 2-category, for any bicategory $C$ there is a strict 2-category $C'$ such that pseudofunctors $C\to Cat$ are in bijection with strict 2-functors $C'\to Cat$.

Now note that a pseudonatural transformation between two pseudofunctors (resp. strict 2-functors) $C\to D$ is the same as a single pseudofunctor (resp. strict 2-functor) $C\to Cyl(D)$, where $Cyl(D)$ is the bicategory whose objects are the 1-cells of $D$, whose 1-cells are squares in $D$ commuting up to isomorphism, and whose 2-cells are "cylinders" in $D$.  Likewise, a modification between two such transformations is the same as a single functor (of whichever sort) $C\to 2Cyl(D)$, where the objects of $2Cyl(D)$ are the 2-cells of $D$, and so on.  Therefore, $C'$ classifies not only pseudofunctors out of $C$, but transformations and modifications between them; thus we have an isomorphism
$$[C^{op},Cat] \cong [(C')^{op},Cat]_{strict,pseudo}$$
where $[A,B]_{strict,pseudo}$ denotes the 2-category of strict 2-functors, pseudonatural transformations, and modifications between two strict 2-categories.  Thus we can equally well analyze the functor
$$ [(C')^{op},Cat]_{strict,pseudo}(\overline{C(-,x)}, \overline{F}) \to \overline{F}(x) = F(x) $$
given by evaluation at $1_x$.  Here $\overline{C(-,x)}$ and $\overline{F}$ denote the strict 2-functors $(C')^{op}\to Cat$ corresponding to the pseudofunctors $C(-,x)$ and $F$ under the $(-)'$ adjunction.  However, we also have a strict 2-functor $C'(-,x)$, and the equivalence $C\simeq C'$ induces an equivalence $C'(-,x)\simeq \overline{C(-,x)}$.  Therefore, it suffices to analyze the functor
$$ [(C')^{op},Cat]_{strict,pseudo}(C'(-,x), \overline{F}) \to \overline{F}(x). $$
Now for any $A$ and $B$, we have an inclusion functor $[A,B]_{strict,strict} \to [A,B]_{strict,pseudo}$ where $[A,B]_{strict,strict}$ denotes the 2-category of strict 2-functors, strict 2-natural transformations, and modifications.  This functor is bijective on objects and locally fully faithful.  Moreover, the composite
$$ [(C')^{op},Cat]_{strict,strict}(C'(-,x), \overline{F}) \to [(C')^{op},Cat]_{strict,pseudo}(C'(-,x), \overline{F}) \to \overline{F}(x). $$
is an *isomorphism*, by the [[Yoneda lemma for enriched categories]], in the special case of $Cat$-enrichment.  Since   
$$[(C')^{op},Cat]_{strict,strict}(C'(-,x), \overline{F}) \to [(C')^{op},Cat]_{strict,pseudo}(C'(-,x), \overline{F})$$
is fully faithful, if we can show that it is essentially surjective, then the [[2-out-of-3 property]] for equivalences of categories will imply that the desired functor is an equivalence.

Here we at last descend to something concrete.  Given $\alpha\colon C'(-,x)\to \overline{F}$, we have an obvious choice for a strict transformation for it to be equivalent to, namely $\beta$ whose components $\beta_y\colon C'(y,x)\to \overline{F}(y)$ is given by $f \mapsto \overline{F}(f)(a)$ where $a = \alpha_x(1_x)\in \overline{F}(x)$.  Since $\alpha$ is pseudonatural, for any $f\colon y\to x$ in $C'$ we have an isomorphism
$$\alpha_y(f) = \alpha_y(f\circ 1_x) \cong \overline{F}(f)(\alpha_x(1_x)) = \overline{F}(f)(a) = \beta_y(f).$$
We then simply verify that these isomorphisms are the components of an (invertible) modification $\alpha\cong \beta$.  This completes the proof.


[[!redirects bicategorical Yoneda lemma]]
[[!redirects 2-Yoneda lemma]]
