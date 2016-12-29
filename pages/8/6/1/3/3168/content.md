
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}


## Idea

In [[category theory]] and specifically in [[topos theory]], the notion of _inhabited object_ in a general [[topos]] is a generalization of the notion of [[inhabited set]] from the archetypal topos [[Set]]. It is the [[semantics]] of an [[inhabited type]] in [[type theory]].


## Definition

An object $X$ in a [[topos]] $\mathcal{T}$ is said to be **internally inhabited** if in the [[internal logic]] of the topos it is true that

$$
  \exists x \in X.
$$

This is equivalent to saying that the unique map $X \to 1$ is an [[epimorphism]].  More generally, we can make the same definition in any [[regular category]], in which case it is equivalent to $X\to 1$ being a [[regular epimorphism]].

The term **well-supported** is also used for this notion (in general, the [[support]] of $X$ is the [[image]] of $X\to 1$).

In terms of [[(∞,1)-category theory]], internally inhabited means _[[(-1)-connected]]_.

On the other hand, $X$ is said to be **externally** or **globally inhabited** if there exists a morphism $1\to X$, i.e. a [[global element]].  The adjective "externally" is perhaps misleading, since this notion can also be expressed in the internal [[type theory]] of the topos (as having an [[element]]/[[term]] $x:X$), though not in its more usual internal [[higher-order logic]].  The internal assertion "every internally inhabited object is globally inhabited" is a version of the [[propositional axiom of choice]] (PAC).

Every globally inhabited object is internally inhabited, since every [[split epimorphism]] is a regular epimorphism.  The converse is true if $1$ is [[projective object|projective]], as is the case in a [[well-pointed topos]] (such as [[Set]]).  (This may seem to contradict the above, since PAC can fail even in (constructively) well-pointed toposes, but the point is that PAC also says something about *families* of inhabited objects rather than single "globally defined" objects.)

Some sources use "$X$ is inhabited" in the global sense, while others use the term "inhabited" only internally.  Regardless, a [[pointed object]] always means one _equipped with_ a global element $1\to X$ (which is the same whether interpreted internally or externally), and the terms "global element" and "well-supported" are always unambiguous.


## Examples

For [[Grothendieck topos|sheaf toposes]] with [[point of a topos|enough points]], in which epimorphisms are [[stalk]]wise epimorphisms, an object is (internally) inhabited if the [[germ]] of $X$ over every [[stalk]] is an [[inhabited set]].

One situation where this plays a role is in the study of certain [[smooth topos]]es with objects $\mathbb{I}$ of _invertible infinitesimals_ . There is an immediate definition of such a topos, the topos called $\mathcal{Z}$ at [[Models for Smooth Infinitesimal Analysis]], for which this object exists, but is not inhabited. Only the weaker internal statement $\not \not \exists x \in \mathbb{I}$ is true.

But for some useful constructions in these toposes, such as for giving an internal definition of [[distribution]]s as genuine functions (internally), it is desirable to have $\mathbb{I}$ be inhabited. In the above situation this is achieved by [[forcing]] the existence of invertible infinitesimal elements. The result is the refined topos denoted $\mathcal{B}$ at [[Models for Smooth Infinitesimal Analysis]].


## In a well-pointed topos

The category [[Set]] is a very special sort of topos.  A generally useful principle in formulating categorical properties of [[Set]] is that "external" and "internal" notions should coincide.  A general default understanding across the nLab is that $Set$ is a [[well-pointed topos]] whose terminal object $1$ is projective and [[indecomposable object|indecomposable]].  These latter properties of the terminal object hold for any well-pointed topos if the metalogic is [[classical logic|classical]]; for purposes of [[constructive mathematics]], we usually agree to add them in.

As remarked above, projectivity of $1$ easily makes internal and external inhabitedness agree.  We also present a constructive/intuitionistic proof of the following result about *emptiness*.

+-- {: .num_prop} 
###### Proposition 
In a well-pointed topos, an object $X$ which is _not_ internally inhabited is empty (is an initial object). 
=-- 

Note that the negation "not" in this statement is an *external* one, which is what makes it nontrivial.  If an object is *internally* "not inhabited", then it is empty essentially by definition.

+-- {: .proof} 
###### Proof 
Let $X \to U \hookrightarrow 1$ be the epi-mono factorization of the unique map $X \to 1$. Here $m: U \hookrightarrow 1$ is monic but not epic if $X \to 1$ is not epic, and we use this to prove $U \cong 0$. In that case, we have a map $X \to 0$, whence $X \cong 0$ since in a topos initial objects are strict. (For given $X \to 0$, the projection $\pi_1: X \times 0 \to X$ has a section, and it follows that $X \cong 0$ since $X \times 0 \cong 0$ and retracts of initial objects are initial. This also implies that for any $V$ the map $i: 0 \to V$ is monic: for it is obviously true that for any pair of maps $h, k: A \to 0$ we have that $i h = i k$ implies $h = k$, as $A$ is initial by strictness and this makes $h = k$ automatic.) 

Let $f: U \to \Omega$ be the classifying map of the mono $1_U: U \to U$, and let $g: U \to \Omega$ be the classifying map of the mono $0 \to U$. There is no map $1 \to U$, else $m: U \to 1$ would retract it and hence be epic. Hence it is vacuously true that $f x = g x$ for all $x: 1 \to U$, and so $f = g$ by well-pointedness. Hence the subobjects $1_U$ and $0$ coincide, forcing $U \cong 0$.   (In other words, the presence of a [[subobject classifier]] causes any [[generator]] to be a [[strong generator]].)
=-- 


## Discussion##

While writing this page, we had the following discussion about whether or not "$X$ is inhabited" in a topos should be interpreted internally or externally, before deciding that we should mention both.

+--{.query}

_[[Mike Shulman|Mike]]_: I strongly disagree that "inhabited" means "has a global element" in a topos.  Intuitionistically, "$X$ is inhabited" means "there exists an $x\in X$" which when interpreted in the internal logic of a topos means that $X$ is well-supported.  By contrast, the property of having a global element is not expressible in the internal language at all.  "Inhabited" is also universally used in the topos-theoretic literature to mean well-supported.

_Toby_: Then what is the term for what I have called 'inhabited'? [At least one reference](http://www.dcs.kcl.ac.uk/technical-reports/papers/tr97-04.ps.gz) uses the term that way; I see (through Google) that it\'s used in the Elephant, but it\'s not in the index and I haven\'t managed to tell what the definition is. Certainly I\'m not in the position to make a good literature search.

_Mike_: On p618 of the Elephant he uses "inhabited" to mean "there exists an $x\in X$" in the internal language.  What do you think about the change I made above?

_Toby_: I certainly can\'t disagree with any of the statements there.

I would like us to be a bit bolder with the terminology if it\'s safe and useful (neither of which condition has been established, of course). The Elephant has its share of terminological changes (like 'cartesian category' and 'cartesian morphism', which I remember got a lot of complaints on the categories mailing list), so I\'d want to check its references (which I can do later).

The wiki saved a previous version of your comments; since you changed it, I won\'t hold you to it. But having read it does inspire me to say that the terminology that comes naturally to me is indeed 'inhabited' for having a global element and 'internally inhabited' for being well supported; the latter seems at least as well justified as 'internal axiom of choice' (as used in, say, Mac Lane \& Moerdijk). That\'s just me, of course.

_Mike_: Yeah, I wasn't sure if it would (there seems to be a certain timeout within which multiple edits by the same person overwrite each other?).  I also wasn't sure if it was kosher to remove/change my comment; perhaps I shouldn't have.  The reason I changed it was that "inhabited" and "internally inhabited" did start to make a little sense.  My current feeling is that "inhabited" is a set-theoretic term, and as such should only be used in set-theoretic-like situations.  This includes (1) constructive set theory, (2) IHOL and hence the internal language of a topos, and (3) a well-pointed topos. If we are talking about an arbitrary topos, and it is not clear that our statements are to be interpreted in the internal logic, I would rather use "has a global element" and "is well-supported" since they are both unambiguous.

You are certainly right about the Elephant and terminology.  "Cartesian category," "prone morphism," and "effective regular category" are the ones that come to mind that seem to have been rejected by much of the categorical community.

_Mike_: Another thought: one could argue that just as a "ring" in a topos means a model of the theory of rings, and likewise for many other concepts, so should an "inhabited object" mean a model of the theory of inhabited objects, which is the same as a well-supported object.  Of course this fails for "projective object," but I don't think there is a "theory of projective objects," at least not one interpetable in the usual internal logic of a topos.  And I suppose maybe it fails for "choice object" too, although that probably depends on whether you formulate the theory of choice objects to be equipped with a choice function or merely assert that one exists.  Perhaps the literature is not very consistent in its use of "internally" or lack thereof.

_Toby_: I see 'inhabited' as just a convenient abbreviation of 'that has an element' (convenient enough that 'is inhabited' is still nicer than 'has an element'). So an inhabited object should naturally be an object with an element (a global element, that is; every object has a generalised element, and we must at least reproduce the situation in $\Set$). And after all, 'inhabited' is hardly more of a set-theoretic term than 'axiom of choice'! (^_^)

Maybe life would be simpler if we always internalised using the internal language, but there\'s a lot of precedent that we don\'t, probably because it\'s a lot easier not to. And anyway, that\'s what the word 'internalised' is for!

As for the timeout, I think that it\'s an hour, although I haven\'t timed it carefully. (It definitely exists.) I think that it\'s fine to remove or change old comments, certainly if they haven\'t been replied to, but one should be aware that they can still be read. (And if you\'re not sure if they can still be read, try 'See changes' or 'Back in time' below.)

_Mike_: Well, I think that I will continue using "has a global element" myself for clarity, but you've convinced me that it's not entirely unreasonable to use "is inhabited" to mean the same thing.  Though I reserve the right to reopen the discussion if we discover precendent to the contrary.  (-:

A different question, as you mentioned earlier, is whether it is useful.  How often do we want to talk about objects that have a global element?  We may frequently care about _pointed_ objects, which are _equipped_ with a global element, but there isn't any dispute about what to call those.

_Toby_: You\'ve got a good point there. Probably 'pointed object' and 'well-supported object' are the only really useful notions. Actually, I think that a lot of constructivists (the ones that are really think that mathematics should talk about *constructions*, like Bishop and Coquand) would say that an inhabited set and a pointed set are really the same thing. We can distinguish them, of course, by their morphisms (or even isomorphisms), but that doesn\'t mean that we need two words (just as we don\'t use two different words for metric spaces with, say, continuous maps between them and uniformly continuous maps bewteen them). So as you move towards my position, I move towards yours ....

_Mike_: Does that mean you might be satisfied with the way it's written now?  (I added a note about pointed objects.)

_Toby_: Yes, I\'m happy now for now.

=--

## Related concepts

* [[inhabited set]]


[[!redirects well-supported object]]
[[!redirects well-supported objects]]

[[!redirects inhabited]]