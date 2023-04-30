
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# $n$-types cover

* table of contents
{: toc}

## Idea

The property that **$n$-types cover** is a property of a [[higher category theory|higher category]], or an [[axiom]] in its corresponding [[internal logic]], which says roughly that every [[object]] is [[cover|covered]] by one that is [[truncated object|truncated]] at some level.

## In a higher category

A [[n-category|higher category]] is said to satisfy the (external) property that **$n$-types cover**, or to have **enough $n$-types**, if for every [[object]] $X$ there exists an $n$-[[truncated object]] $Y$ and an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] $Y\to X$.  When $n=0$ one also says that **sets cover** or that there are **enough sets**.

Usually the category in question is some sort of [[topos]] or [[higher topos]], or at least a [[pretopos]] of an appropriate sort.  In this case, the property that $n$-types cover means that the [[subcategory]] of $n$-[[truncated objects]] is "generating" in an appropriate sense.

When $n=-1$, however, having enough $n$-types in this sense is not really a useful notion, because $(-1)$-truncated objects ([[subterminal objects]]) are not closed under [[coproducts]].  In this case a better condition is that all maps out of subterminal objects are jointly [[effective epimorphism|effective epimorphic]].

### Examples

If $n\gt 0$, then any [[n-localic (∞,1)-topos]] has enough $(n-1)$-types, since every object is surjected onto by a coproduct of [[representable functor|representables]] which are $n$-truncated.  The converse seems plausible as well.

A specific example of a higher topos in which sets do not cover is the [[slice (∞,1)-topos]] $\infty Gpd / \mathbf{B}^2 \mathbb{Z}$ of [[∞Grpd]] over the double [[delooping]] of the group of [[integers]], which is equivalently the topos of [[∞-actions]] of the [[∞-group]] ([[2-group]]) $\mathbf{B} \mathbb{Z}$.  From this second perspective, a 1-truncated object of this topos is a [[groupoid]] (1-groupoid) together with an [[automorphism]] of its [[identity]] [[functor]], i.e. an element of its [[center]], and a morphism of such is a functor that respects these central elements.  Such an object is 0-truncated if it is essentially discrete, in which case its center is also trivial; thus the 0-truncated objects are just ordinary sets.  However, since functors must respect the central elements, there can be no surjective map from a 0-truncated object to a 1-truncated one whose chosen central element is nontrivial.

## In homotopy type theory

In [[homotopy type theory]], the (internal) axiom of **$n$-types cover** or **enough $n$-types** says that for any type $X$ there [[merely]] exists an $n$-type $Y$ and a surjection (i.e. a [[n-epimorphism|(-1)-connected map]]) $Y\to X$.  In symbols:

$$ \prod_{(X:Type)} {\Vert \sum_{(Y:n Type)} \sum_{(f:Y\to X)} surj(f) \Vert }$$

where $\Vert-\Vert$ denotes the $(-1)$-truncation.  As before, when $n=0$ we say that **[[h-set|sets]] cover** or that there are **enough sets**.


### In models
 {#InModels}

+-- {: .num_theorem}
###### Theorem
If an $(\infty,1)$-topos satisfies the external property that $n$-types cover, then its internal type theory satisfies the internal axiom that $n$-types cover.
=--
+-- {: .proof}
###### Proof
By the [[Kripke-Joyal semantics]] of homotopy type theory, the conclusion requires that for any map $X\to \Gamma$ there is an effective epi $p:\Delta\to \Gamma$, an $n$-truncated map $Y\to \Delta$, and an effective epi $Y\to p^*X$ in the slice category over $\Delta$.  Assuming the hypothesis, we can obtain this by letting $\Delta$ be an (external) $n$-type cover of $\Gamma$ and $Y$ an (external) $n$-type cover of $p^* X$.
=--

The converse, however, is not true.  For the internal axiom, like all internal statements, is preserved by passage to slices (i.e. introduction of a nonempty context), but we saw above that the slice topos $\infty Gpd / \mathbf{B}^2 \mathbb{Z}$ does not have enough sets, even though $\infty Gpd$ does.

For an example of a topos in whose internal logic sets do not cover, let $C$ be the $(2,1)$-category with two objects $a$ and $b$, one morphism $a\to b$, no morphisms $b\to a$, and $C(a,a) = \mathbf{B} \mathbb{Z}$ and $C(b,b)=1$, and consider the presheaf $(\infty,1)$-topos over $C$.  A 1-truncated object therein consists of two groupoids $X_a$ and $X_b$, an element of the center of $X_a$, and a functor $X_b \to X_a$ which relates the chosen central element in $X_a$ with the identity in the center of $X_b$.

If we take $X_b$ to be empty, then $X_a$ is a groupoid with an arbitrary chosen central element, and we can choose it to be one which is nontrivial and hence admits no surjection from a 0-type.  Let $\Gamma = 1$ for this $X$.  Since the terminal object $1$ is a representable (it is $C(-,b)$), it is projective; thus given $\Delta$ and $Y$ as above, we could find a section of $p:\Delta\to\Gamma$ and pull back $Y$ along it to obtain a 0-type cover of $X$ itself, which does not exist.

### Relation to other axioms

The internal axiom that sets cover is related to some forms of the [[axiom of choice]].  Let us denote by

* $AC_0 = $ every surjection between sets merely has a section.
* $AC_\infty = $ every surjection with codomain a set merely has a section.

Then we have

+-- {: .num_theorem}
###### Theorem
$AC_\infty \Leftrightarrow (AC_0$ and sets cover).
=--
+-- {: .proof}
###### Proof
This is a theorem inside homotopy type theory, and likewise for its proof.  Clearly $AC_\infty \Rightarrow AC_0$.  Given $X$, we have a map $X\to {\Vert X \Vert_0}$ which is 0-connected, hence also surjective, and its codomain is a set; thus by $AC_\infty$ it merely has a section.  Any section of a 0-connected map is surjective; thus $X$ is merely covered by $\Vert X\Vert_0$.  (Note that in this case we have a stronger version of "sets cover" in which the first $\sum$ is outside the truncation.)

Conversely, suppose $AC_0$ and sets cover, and let $X\to Z$ be a surjection with codomain a set.  Then there merely exists a set $Y$ and a surjection $Y\to X$, and the composite surjection $Y\to X\to Z$ merely has a section by $AC_0$.  The composite of this section with $Y\to X$ is a section of $X\to Z$.
=--

## Related concepts

* [[cover]]

* [[atlas]]

category: foundational axiom

[[!redirects sets cover]]
[[!redirects enough n-types]]
[[!redirects enough sets]]
