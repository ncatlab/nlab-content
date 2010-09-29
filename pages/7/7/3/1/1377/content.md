
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A _lax 2-adjunction_ is an [[adjunction]] 'up to adjointness'.  A
1-categorical adjunction is given by a [[natural isomorphism]] of [[hom-set]]s

$$\phi_{A,B} : D(F A,B) \cong C(A,G B)$$

and a [[strict 2-adjunction]] is analogous, where $C,D$ are instead [[strict 2-category|strict 2-categories]], $F,G$ are [[strict 2-functor|strict 2-functors]], and $\phi$ is a strictly 2-natural isomorphism of hom-categories.  A __lax 2-adjunction__ is given by a (suitably natural) pair of functors

$$\hat\phi_{A,B} : D(F A,B) \overset{\to}{\leftarrow} C(A,G B) :
\check\phi_{A,B} $$

such that $\check\phi\dashv\hat\phi$.


## Definition ##

Just as the notion of [[adjunction]] makes sense not just in $Cat$ but
in any 2-category, lax 2-adjunctions can be defined in any [[3-category]] when the above is suitably reformulated by using the 2-categorical [[Yoneda lemma]].  So, given 0-cells $C,D$ and 1-cells $F:C\to D$, $G:D\to C$ in any 3-category, we say $F$ is __lax left adjoint__ to $G$ if we have

* 2-cells $\eta:C\Rightarrow G F$ and $\epsilon:F G \Rightarrow D$, and

* instead of strict triangle equalities, 3-cells (called _triangulators_)
  $s,t$

  <center markdown="1">[[lax-adj-mdfs.png:pic]]</center>

  satisfying the _swallowtail identities_:

  <center markdown="1">[[lax-adj-swlwtl-eta.png:pic]]</center>

  and

  <center markdown="1">[[lax-adj-swlwtl-eps.png:pic]]</center>

+--{: .query}
[[Mike Shulman|Mike]]: What 3-category are we intended to work in to obtain an equivalence with the original notion?  I guess this is the question of how strict we require $C,D,F,G$ to be and whether "suitably natural" means "strictly 2-natural" or "pseudo natural."

Since on the nLab, everything is weak by default, it seems that we should probably use the unadorned name for the version where $C$, $D$ are weak 2-categories, $F$ and $G$ are weak 2-functors, and $\hat\phi$ and $\check\phi$ are pseudo natural.

[[Finn Lawler|Finn]]:  For Gray, $C,D,F,G$ are all strict, and $\eta,\epsilon$ are lax.  I'm still trying to understand the connection between the two formulations, so I'm not sure how extra weakness on one side translates to the other.  I should have a better idea soon.

[[Mike Shulman|Mike]]: Unfortunately, there is no 3-category, not as usually understood, in which the 2-cells are lax transformations.  The interchange law for whiskering lax transformations holds only laxly, so at most you have some sort of 'lax 3-category.'  Actually, in the case of $2Cat$, what you have is that $2Cat$ with the lax [[Gray tensor product]] is biclosed and hence enriched over itself, and that sort of enrichment is the relevant 3-category-like structure.  (More grist for [[michaelshulman:n-topos for large n|my mill]] that lax things are important!)

[[Finn Lawler|Finn]]:  Yes, that's been worrying me.  Figuring out the relationship between the two definitions will be my mini-project for the coming week -- it's about time I got to grips with this sort of enriched-Yoneda wizardry.

Gray shows that given a strict 2-adjunction between the 2-comma categories $(F\downarrow D)$ and $(C\downarrow G)$ you get lax $\eta,\epsilon$.  Maybe using a stricter comma construction will yield pseudo-natural unit and counit -- I don't know, but I'll try to find out.  (Of course, any hints or suggestions you have will be greatly appreciated!)

[[Mike Shulman|Mike]]: One thing worth pointing out is that there is  no Yoneda lemma for lax transformations (though there is for pseudo ones).  So in order for $\hat\phi$ to be determined by $\eta$, $\hat\phi$ must be pseudo natural in $B$, and likewise for $\check\phi$ to be determined by $\epsilon$, it must be pseudo natural in $A$.  My guess is that laxity in the remaining variable will correspond to laxity of $\eta$ and $\epsilon$, and $s,t$ will come from the adjunction $\check\phi\dashv\hat\phi$.  That suggests that if we do everything in a (strict or weak) 3-category, so that $\eta$ and $\epsilon$ must be at least pseudo, we get the homwise notion where "suitably natural" means strict or pseudo.

It appears that in Seely's paper (referenced below) the functor $G$, at least, is also lax.  Lax functors are even harder to incorporate in a 3-category-like structure than lax transformations are; you can't even whisker any sort of transformation by a lax functor.  Moreover, he also seems to say that $\hat\phi$ and $\check\phi$ are both strict in their _first_ coordinate, rather than one in the first and one in the second as seems (to me) to be necessary for a Yoneda restatement.  Hmm.
=--

## Sources ##

This idea was introduced in Gray's [[Gray-adjointness-for-2-categories|book]] under the name of _transcendental quasi-adjunction_.

+--{: .query}
[[Mike Shulman|Mike]]: Is there a reference for the name "lax 2-adjunction?"  It looks very similar to the notion of "local adjunction"  in

* Renato Betti and John Power, _On Local Adjointness of Distributive Bicategories_

except that they allow $F$ to be an oplax functor, $G$ a lax functor, $\hat\phi$ an oplax transformation, and $\check\phi$ a lax transformation.

[[Finn Lawler|Finn]]:  I'm roughly following Seely, _Modelling computations: a 2-categorical framework_, from [here](http://www.math.mcgill.ca/~rags/WkAdj/LICS.pdf).  He cites Gray and Kelly--Street, _Review of the elements of 2-categories_ (which I haven't seen yet).

[[Mike Shulman|Mike]]: Kelly-Street don't say anything about lax adjunctions.  I want to make sure we think seriously about what this sort of thing should be called, rather than just following one or another author.  As far as I can tell, it doesn't fit into the general precise meaning of 'lax' (being a type of morphism of algebras for a 2-monad), and there are so many possible variations (as in Gray's book) that it might be nice to have a sensible system of nomenclature that would include them all.  Maybe.  On the other hand, I actually never really took Gray's stuff very seriously because I couldn't think of any examples; maybe I should look more closely at Seely's paper.

[[Finn Lawler|Finn]]:  Yes, that would be nice, but I for one don't know enough yet about the big picture to make any suggestions that would generalize easily.

I'm interested in this stuff because I want to use strict 2-categories with lax structure to model rewrite systems, as Seely does.  These lax/quasi/local adjunctions are one way of specifying lax structure, but there are probably others (3-monads on 2-Cat?  Lawvere 3-theories?).

[[Mike Shulman|Mike]]: I don't understand how Seely's definitions give you a 2-category; all I can see is a 'lax 2-category' of some sort.  If the composite of lambda terms $f$ and $g$ is defined by $(\lambda x) (g(f x))$, then we have
$$\begin{aligned}
  h\circ (g\circ f) &= (\lambda x)(h(((\lambda y)(g(f y)))x))\\
  (h\circ g) \circ f &= (\lambda x)(((\lambda y)(h(g y)))(f x))
\end{aligned}$$
which are (as far as I can tell) not the same, but both admit a beta reduction to $(\lambda x)(h(g(f x)))$.  Is there some other way of defining composition so that it is associative?

[[Finn Lawler|Finn]]:  The composite $f\circ g$ is defined to be the _substitution_ $f[x:=g]$ of $g$ for the free variable $x$ of $f$.  Associativity follows.  Substitution is meta-notation, and not part of the syntax of $\lambda$-calculus.

If $\hat\phi:f\mapsto \lambda x.f$ and $\check\phi:g\mapsto g\cdot x$ (where $\cdot$ is application and $x$ is a fresh variable), then the 'local' adjunctions give
$$\begin{aligned}
  (\lambda x.f)\cdot x & \Rightarrow f \\
  f & \Rightarrow \lambda x.(f\cdot x)
\end{aligned}$$
which when combined with the definition of composition as substitution give you exactly the $\beta$-reduction and $\eta$-expansion laws.

[[Mike Shulman|Mike]]: Ah, I didn't notice that the morphisms from $A$ to $B$ are terms of type $B$ with a free variable of type $A$, rather than the (to me) more obvious choice of terms of type $A\Rightarrow B$.  I don't follow your second paragraph, though.

(Of course, on a moment's reflection that choice makes perfect sense; those are the same as the morphisms in any other category of [[context]]s.)

[[Finn Lawler|Finn]]:  Right -- it's the usual functorial semantics interpretation: composition is substitution.

The second paragraph was just pointing out an example of how a lax adjunction arises in typed $\lambda$-calculus.  You want types to map to 0-cells and terms to 1-cells as usual, and rewrite relations $t red u$ to map to 2-cells $t\Rightarrow u$.  So the term model will be a strict 2-category with (strict or lax) products, together with $(-\times A)$ lax left adjoint to $[A\to -]$ for all $A$.  Then the first definition of lax adjunction should give you the $\beta$ and $\eta$ rewrites as the counit and unit of each adjunction $\check\phi\dashv\hat\phi$.  As I've said above, I'm still working out the details wrt pseudo versus lax naturality, but this is roughly what you should get.
=--

[[!redirects lax 2-adjunctions]]