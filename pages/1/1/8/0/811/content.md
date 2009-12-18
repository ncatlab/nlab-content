#Contents#
* automatic table of contents goes here
{:toc}


## Idea 

An **$n$-fibration** is the version of a [[Grothendieck fibration]] appropriate for $n$-[[n-category|categories]].

The idea is that a functor $p:E\to B$ between $n$-categories is an $n$-fibration if the assignation $x\mapsto E_x = p^{-1}(x)$ of an object $x\in B$ to its fiber can be made into a (contravariant) functor from $B$ to the $(n+1)$-category $n Cat$.


## Definition 

(This definition is schematic, and needs to be adapted to be made precise for any particular definition of $n$-category.)

Let $p:E\to B$ be a functor between $n$-categories.

+--{: .num_defn}
###### Definition
A morphism $\phi:b\to a$ in $E$ is **cartesian** (relative to $p$) if for any $c\in E$, the following square:
$$\array{E(c,b) & \overset{\phi\circ -}{\to} & E(c,a)\\
  ^p \downarrow && \downarrow ^p\\
  B(p c, p b) & \underset{p\phi\circ -}{\to} & B(p c, p a)}$$
(which commutes by functoriality of $p$) is a [[pullback]] of $(n-1)$-categories.
=--

+--{: .num_defn}
###### Definition
We say that $p:E\to B$ is an **$n$-fibration** (or just a **fibration**) if
1. For any object $a\in E$ and morphism $f:x\to p a$ in $B$, there exists a cartesian $\phi:b\to a$ and an [[equivalence]] $p\phi \simeq f$ in the [[over category|slice]] $n$-category $B/p a$.
1. For any objects $a,b\in E$, the functor $p:E(b,a) \to B(p b, p a)$ is an $(n-1)$-fibration.
1. For any $a,b,c\in E$ and $\psi:c\to b$, the square
$$\array{E(b,a) &\overset{-\circ \psi}{\to} & E(c,a)\\
  ^p\downarrow && \downarrow^p\\
  B(p b, p a) & \underset{-\circ p\psi}{\to} & B(p c, p a)}$$
is a morphism of $(n-1)$-fibrations.
=--

+--{: .num_defn}
###### Definition
If $p_1:E_1\to B_1$ and $p_2:E_2\to B_2$ are $n$-fibrations, a commutative square
$$\array{E_1 & \overset{h}{\to} & E_2\\
  p_1 \downarrow && \downarrow p_2\\
  B_1 & \underset{g}{\to} & B_2}$$
is a **morphism of $n$-fibrations** if
1. Whenever $\phi$ is cartesian for $p_1$, $h(\phi)$ is cartesian for $p_2$, and
1. For any $a,b\in E_1$, the square
$$\array{E_1(b,a) & \overset{h}{\to} & E_2(h b, h a)\\
  p_1 \downarrow && \downarrow p_2\\
  B_1(p_1 b, p_1 a)& \underset{g}{\to} & B_2(g p_1 b, g p_1 a)}$$
is a morphism of $(n-1)$-fibrations.
=--


## Remarks

* The definition is recursive in $n$, but if we unravel it, it makes perfect sense for $n=\omega$.

* When $n=1$, this reduces to Street's weakened version of a [[Grothendieck fibration]].  We recover Grothendieck's original notion by requiring that for any $a\in E$ and $f:x\to p a$ in $B$, there exists a cartesian $\phi:b\to a$ such that $p\phi$ and $f$ are _equal_ (an [[evil]] condition).

  +--{+ .query}
  Zoran: Where did Street define this weaker notion of fibered category ? Which examples you know of such weakened version which do not fit into Grothendieck definition ? The geometric examples appearing in real nature (say inverse image of qcoh sheaves in algebraic geometry etc.) correspond to Grothendieck's definition. If he had seen real examples of more general notion, I do not believe Grothendieck would fail to deliver the definition in appropriate generality. The universality property is a universality property in its own right and it is internal so I am not convinced on the basis of "counterevil" philosophy. Finally, am I wrong in thinking that it is a theorem that Grothendieck's fibered categories are exactly those categories over categories which are in essential image of Grothendieck's construction for pseudofunctors with values in Cat ?

  [[Mike Shulman|Mike]]: In "Fibrations in bicategories."  I do not know any examples in nature (of ordinary functors between ordinary categories) which do not fit Grothendieck's definition, nor am I claiming that Grothendieck's definition is not an appropriate level of generality in most cases.  I believe that sometimes evil is good, although that doesn't make it any less evil.  (Make sense of that, moral philosophers!) The point is that when you are working in a _weak_ 2-category, (the internalization of) Grothendieck's definition doesn't really even make sense.  For instance, if you are working in a weak 2-category of categories and [[anafunctor]]s, you certainly want to use Street's weaker version.

  You are correct that Grothendieck's fibrations are precisely the functors arising from the Grothendieck construction for pseudofunctors with values in $Cat$ --- where "precisely" means "up to isomorphism."  Street's fibrations are precisely the same thing, where now "precisely" means "up to equivalence."  In particular, every Street fibration in $Cat$ is equivalent to a Grothendieck fibration---which can be seen as one "reason" why Grothendieck fibrations are good enough in $Cat$.

  By the way, universality and internalization are completely orthogonal concerns to evil.  The internal version of Grothendieck fibrations has a _strict_ universal property, while the internal version of Street fibrations has a _weak_ universal property.  This is just like "strict [[2-limit]]s" versus "bilimits:" the weak version is the "correct" notion, but in many cases it is equivalent to a strict notion, and when it is, we tend to use the strict notion because it is easier to work with.
  =--

* Likewise, when $n=2$ this is a weakened version of Hermida's definition of 2-fibration.


## From fibrations to functors

If $p:E\to B$ is an $n$-fibration, we define a functor (or '$n$-pseudofunctor') from $B$ to $n Cat$ as follows.  (Like the above definition, this is only a schematic sketch.)

* Send $x\in B$ to the [[essential fiber]] $E_x$, whose objects are objects $a\in E$ equipped with a equivalence $p a \simeq x$.

* For a morphism $f:y\to x$ in $B$, define $f^*:E_x\to E_y$ by choosing, for each $a\in E_x$, a cartesian $\phi:b\to a$ over $f$ and defining $f^*(a)=b$.  The universal property of cartesian arrows makes $f^*$ a functor.

* For a 2-cell $\alpha:f\to g:y\to x$ in $B$, define a transformation $\alpha^*:g^*\to f^*$ as follows.  Given $a\in E_x$, we have a cartesian arrow $\phi:g^*a\to a$ over $f$.  Now choose a cartesian 2-cell $\mu:\psi\to \phi$ over $\alpha$ in $E(g^*a,a)$.  Since $p \psi = f$, $\psi$ factors essentially uniquely through the cartesian arrow $\chi:f^*a\to a$, giving a morphism $g^*a \to f^*a$; we define this to be the component of the transformation $\alpha^*$ at $a$.

* and so on...

Note that the functor we obtain is "totally contravariant:" it is contravariant on $k$-cells for all $1\le k\le n$.

One expects that in this way, the $(n+1)$-category of fibered $n$-categories over $B$ is equivalent to the $(n+1)$-category of functors $B\to n Cat$.  The inverse should be a generalization of the [[Grothendieck construction]], which is known only for $n=2$.

## Related concepts

A notion of fibration of [[(∞,1)-category|(∞,1)-categories]] exists in terms of [[Cartesian fibration]]s of [[simplicial set]]s.


## References 

[Claudio Hermida](http://maggie.cs.queensu.ca/chermida) introduced 2-fibrations in:

* Claudio Hermida, "Some properties of Fib as a fibred 2-category," J. Pure Appl. Algebra 134 (1), 83--109, 1999; [preprint version ps.gz](http://maggie.cs.queensu.ca/chermida/papers/jpaa.ps.gz)

In fact they also appeared earlier, in some form, in [[Gray-adjointness-for-2-categories|Gray's book]]. 

A definition for strict $n$-categories due to Hermida is unpublished, but it is used and presented in another joint work with [Marta Bunge](http://www.math.mcgill.ca/bunge), presented at CATS07 at Calais:

* Marta Bunge, "Intrinsic $n$-stack completions over a topos," slides [here](http://saxo.univ-littoral.fr/CT08/slides/Bunge.pdf)

 $n$-pseudofunctors may be viewed (and defined) as [[anafunctor]]s.  For $n$-groupoids such an approach to $n$-pseudofunctors has been studied in

* [D. Bourn](http://www-lmpa.univ-littoral.fr/~bourn), 
Pseudo functors and non abelian weak equivalences, in "Categorical algebra and its applications", Springer LNM 1348 (1988), 55--70.

## Discussion 

This was at [[fibered n category]]:

+--{+ .query}
[[Zoran Skoda]]: I like the expansion (by Mike I guess) which is now in the entry n-fibration, it is instructive and a strong novelty of the nlab (is there more to read on the weak case somewhere?). However, I would prefer that for the case of STRICT n-categories, for which I intended the fibered n category entry when I created it; that we keep the original name and original definition (thus talking about n-cartesian
cells, regardless that it is evil, and one should expand on that). Grothendieck, Gabriel and Gray discovered fibered (strict) 1- and 2- categories and called them fibered 1- or 2-categories; Hermida generalized to strict n and Bunge is following , also under the same name: so let us keep the explicit version for the strict n-categories under the name fibered n category and with "evil" definition (which is very useful in my practice, at least for n=2); and lets us keep homotopically-biased title n-fibration for the weak n-category version. Of course, no hurry, in due time...And also having an entry fibered 2-category for the case of strict 2-categories where hermida has two different but equivalent definitions. Does that make sense to you ? Mike, Toby, Urs ?

[[Toby Bartels]]:  If these are useful to you, then we should certainly have an article on them.  But can we put it at [[strict fibered n-category]]? (or [[fibered strict n-category]] if you don\'t want to imply that there\'s anything strict about how the strict $n$-category is fibred).  Besides the hyphen (which is a technicality), one of the biases of the $n$-Lab is that the default notion of $n$-category is weak.  Of course, people who work with strict $n$-categories don\'t share that bias, so we won\'t quite match their language.

[[Mike Shulman|Mike]]: I'm with Toby.  When we mean strict, we should say strict.  I don't think '$n$-fibration' is 'homotopically biased' either; plenty of people say 'fibration' rather than 'fibered category.'

The level of strictness in Hermida's definition is a bit puzzling to me.  A 2-fibration $E\to B$ in his sense corresponds to an (appropriately contravariant) functor $B\to 2Cat$, but neither to a fully strict 3-functor nor a fully weak one.  (This has nothing to do with the evilness of requiring on-the-nose cartesian lifts rather than up-to-iso ones, that is rather about strictness of the equivalence between fibrations and pseudofunctors.)  But if you think it is important, we should certainly have a page on it.

[[Zoran Skoda]]: I am not really a conformer to the nlab conventions, I always say weak when I mean weak in my own work; but I am happy with conforming in the nlab entry (i just did not think of weak case when writing the oroiginal entry). I also agree iwth the hyphen, I noticed that afvter submitting v1. As far as "plenty of people say 'fibration' rather than 'fibered category.'" Yes, people doing homotopy/topology, not a single algebraic geometer, 
who are the main consumers of
Grothendieck's definition, and have direct and inverse image functors all over the place. Thus the terminology is homotopically biased, at least in social sense. I am a bit puzzled about the statement of semi-strictness you say; I used this definition in a number of examples of mine and it was always working' maybe my perception of what should be a 2-pseudofunctor is not good as well. But one should also compare with Gray's universal property in the formal/adjointness book. I think fibered strict n-category is better than strict fibered n-category. The thing is that sometimes in expositions people use fibered category actually for pseudofunctor, then one would think that strict
in the sense of functor. There is also a curiousity (used by Thomason) that Grothendieck construction works for lax functors in fact. Gorghendieck construction for n=2 has been studied by hermida (though he has just few words on it) so I doubt he woudl not have the correspondence with teh coprrect generality of 2-pseduofunctors. Igor and I were doing some ground work on the 2-Groth constr but we did not do complete equivalence of 2-categories, just some other aspects, so i can not claim myself. 

_Mike_: I don't always use the nLab terminology in my own work either; I tend to be more Australian and say "2-category" for the strict notion.  But I've been convinced that it is valuable for the nLab to have a consistent terminological convention, and for $n\gt 2$ the weak notions are (most of us believe) so much more important than the strict ones that they deserve the unadorned name.

And I agree that "fibered strict $n$-category" is better than "strict fibered $n$-category," although perhaps "strictly fibered strict $n$-category" would be even better in view of the relative strictness of Hermida's definition.  If I am remembering correctly, I think that Hermida's 2-fibrations over a 2-category $B$ correspond to pseudofunctors from $B^{coop}$ into $Str2Cat$, the 2-category of strict 2-categories, strict 2-functors, and strict 2-natural transformations.  A fully weak version would of course land in the 3-category of 2-categories, (weak) 2-functors, (pseudo) natural transformations, and modifications.

I disagree that algebraic geometers are the main consumers of fibrations.  They are used plenty by category theorists as well, and people working in related fields such as categorical topology.  (And they _should_ be used by more topologists, an oversight I am working to correct.)

Yes, actually the category of elements (aka lax colimit, aka one of Grothendieck's constructions) works for lax functors landing in $Prof$ and not just in $Cat$, and that way it recaptures all functors, not just fibrations.  Probably there is a similar version of this in the $n$-case.

[[Zoran Skoda]] Yes, Hermida has pseudofunctors into 2Cat;
the target is strict but the pseudo- is in the weakest 3-categorical sense. I think "strict fibration of strict n-categories" is unnecessarily precise: you see if one wants to consider strict categories as non-strict then one can just say that; I think that fibration of strict n-categories is enough; one can always in concrete case say fibration of n-categories where the domain and target happen to be 
strict. For an example, look at the category of internal categories (taken as descent data in the spirit of MacLane-Pare article) in an indexed category is a 2-fibered strict 2-category. There is a reason more, that I woudl not like "strict fibered strict n-catgeory"; usually one starts 
developing theory by saying what a category over category is; so here what a strict 2-category over a strict 2-category is; prefix fibered is just about modifying this
to a sub-2-category of such. So really starting with strict 2-categories viewed as nonstrict, means that we modify nonstrict (2-category over 2-category); but if you are strongly inclined it is OK, at least for the lexicon. 

[[Mike Shulman|Mike]]: I am skeptical that the pseudo- is in the weakest 3-categorical sense; what reference are you looking at?

I wasn't really serious about "strictly fibered strict $n$-category;" I think [[fibered strict n-category]] would be fine.

[[Zoran Skoda]]: In my memory, Igor checked that the Gordon-Power-Street style of a weak 3 functor when the codomain is 2Cat as a strict 3 category, and domain is a strict 2-category in the case of invertible coherences corresponds to what is the input for Grothendieck construction for Hermida case. I did not check his calculation (whose outcome was partly even typed). We did not check if the Grothendieck construction gives an equivalence of 2- or 3- categories of such objects; it would be more work. 
=--


[[!redirects fibered n category]]
[[!redirects fibered n-category]]
[[!redirects strict fibered n-category]]
[[!redirects fibered strict n-category]]