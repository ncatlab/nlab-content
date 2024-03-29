
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of  _lax natural transformation_ is a generalization of the notion of [[natural transformation]] from [[category theory]] to [[higher category theory]].

As a natural transformation is a [[morphism]] between two [[functor]]s between [[categories]], a lax natural transformation is a morphism between [[2-functors]] between [[2-categories]]:

Where a natural transformation has a [[commutative square|commuting]] naturality square, a lax natural transformation has a [[2-morphism]] filling that square.  If that 2-morphism is required to be invertible, one speaks of a [[pseudonatural transformation]], and if it is required to be an identity (which implies that the square commutes), then one speaks of a [[strict 2-natural transformation]] (this latter notion only really makes sense for [[strict 2-functors]] between [[strict 2-categories]]).

In the general terminology of [[higher category theory]], a lax natural transformation may equivalently be called a (lax) [[k-transfor|1-transfor]].


## Definitions ##

Given (possibly weak) [[2-categories]] $C,D$ and (possibly [[lax functor|lax]] or oplax) [[2-functors]]
$F, G : C\to D$, a __lax natural transformation__ $\alpha:F\Rightarrow G$
is given by

* for each $A\in C$ a [[1-morphism]] $\alpha_A:F(A)\to G(A)$ in $D$,
as usual

* for each $f:A\to B$ in $C$ a [[2-morphism]] $\alpha_f: G(f) \circ
\alpha_A \Rightarrow \alpha_B \circ F(f)$:

\begin{tikzcd}
F A \ar[r,"F(f)"] \ar[d,"\alpha_A"']\ar[dr,phantom,"\Rightarrow"] & F B \ar[d,"\alpha_B"]\\
G A \ar[r,"G(f)"'] & G B
\end{tikzcd}

such that

* for each $A,B$, the $\alpha_f$ are the components of a
(strict) [[natural transformation]] $\alpha_{A,B}:
(\alpha_A)^* \circ G_{A,B} \dot{\to} (\alpha_B)_* \circ
F_{A,B}$

* the assignment $f\mapsto \alpha_f$ behaves sensibly with
respect to identities and composition (see the
references for details).

An __oplax natural transformation__ is as above, only with the $2$-cells $\alpha_f$ reversed.  This distinction is not entirely consistent in the literature; see the discussion of terminology below.

An (op)lax natural transformation $\alpha$ is a __[[pseudonatural transformation]]__ if each $\alpha_f$ is [[isomorphism|invertible]], and a __strict natural transformation__ or __[[strict 2-natural transformation]]__ if each is an [[identity morphism|identity]].  

In all of these cases, the word 'natural' is often dropped for brevity.


## Categories and $n$-categories of lax transformations ##

Lax transformations from $F$ to $G$ and [[modification]]s between them form a [[category]] $Lax(F,G)$; likewise we have $Ps(F,G)$ and $Oplax(F,G)$ consisting of pseudo-natural and oplax transformations, respectively.

Pushing it up a notch, for 2-categories $C$ and $D$ we have hom-2-categories $2Cat_{lax}(C,D)$, $2Cat_{ps}(C,D)$, and $2Cat_{oplax}(C,D)$ whose objects are 2-functors (generally taken to be strong or strict), whose morphisms are lax, pseudo, or oplax transformations respectively, and whose 2-cells are modifications.  These hom-2-categories are the [[internal homs]] for the various version of the [[Gray tensor product]] on $2Cat$.

Finally, there is a [[3-category]] consisting of 2-categories, (strong or strict) 2-functors, pseudo-natural transformations, and modifications.  No laxness is possible at this level (without "laxifying" the notion of 3-category).


## "Lax" versus "oplax" ##

The choice of which direction to call "lax" and which to call "oplax" is not made consistently in the literature.  The convention used above is Benabou's original choice, as well as that of Leinster, Borceaux, and the majority of Australian writing on category theory.  However, some references, such as the [[Elephant]], make the opposite choice.  One or two references use "left lax" and "right lax" instead.

It is arguably the case that the direction we call "oplax" occurs more commonly in practice.  For instance, [[icons]] are a special sort of oplax transformations (although if "lax" and "oplax" were switched, then the acronymic derivation of the word "icon" would no longer work).  Likewise, when monoidal categories are viewed as one-object 2-categories, [[monoidal natural transformation]]s are special oplax transformations (in fact, they are precisely the icons).

On the other hand, the convention used above (besides having a little more weight of tradition) has the advantage that there is a [[2-monad]] whose algebras are 2-functors, and for which [[lax morphism|lax and oplax algebra morphisms]] are precisely lax and oplax transformations, respectively, under this convention.  Thus, for instance, theorems such as [[doctrinal adjunction]] can be applied to lax and oplax transformations without needing to switch back and forth between two different meanings of "lax."

+-- {: .query}
How consistent are different authors in this convention?  Should we include a warning ---or for that matter, a reassurance?  ---Toby

[[Finn Lawler|Finn]]:  I don't know myself, but back in [May](http://ncatlab.org/nlab/show/2009+May+changes) (see end of page) Jonas Frey said 'Johnstone in the elephant and Gurski in his PhD-thesis for example use an other orientation than Leinster and Borceux in their books'.  The one above is Leinster's.  I haven't seen any of the other references.

_Toby_:  OK, I just checked the Elephant, and it is reverse.

_Todd_: My own impression is that Leinster and Borceux are in the minority here, and that a bigger warning may be warranted. I think for instance that Johnstone is on the side of most Australians, who after all have done the most work in this area.

My own convention is that of Street: the arrow orientations in a product of [[parity complex]]es is to follow the usual sign conventions for chain complexes. For example, if I write $\alpha \otimes f$ instead of $\alpha_f$, and $\partial^-$ for 'source' and $\partial^+$ for 'target', and interpreting '+' as union, then for $\varepsilon \in \{-1, 1\}$ we would have 

$$\partial^{\varepsilon}(\alpha \otimes f) = \partial^{\varepsilon}(\alpha) \otimes f + \alpha \otimes (-1)^{dim(\alpha)} \partial^\varepsilon f$$ 

so accordingly, since $dim(\alpha) = 1$, the set of source cells of $\alpha \otimes f$ would be $\{F \otimes f, \alpha \otimes G\}$, if you follow my drift. Street's rule of thumb then is that 'lax' would follow this "normal" order, and 'colax' the opposite. 

_Toby_:  I didn\'t want to say anything before, but my own intuition follows Todd\'s logic.

[[Mike Shulman]]: Actually, my impression is that Leinster and Borceaux (specifically, the convention $\alpha_f: G(f) \circ
\alpha_A \Rightarrow \alpha_B \circ F(f)$) are on the side of the Australians.  See for instance p189 of Kelly, "On Clubs and Doctrines" in the Sydney Category Seminar reports.  It's also the one originally used by Benabou.  And the acronymic derivation of the word [[icon]] depends on using this convention.

I also think there is a very good reason to use that convention. Namely, given a small 2-category $C$, there is a [[2-monad]], say $T$, on $Cat^{ob(C)}$, whose algebras are functors $C\to Cat$ and such that a lax $T$-morphism, in the general sense of 2-monad theory, is a lax natural transformation with this convention.  Ideally there would be a general rule which we could apply in any given situation to decide which direction should be called "lax" and which "oplax;" this doesn't quite seem to be the case, but 2-monad theory covers the vast majority of cases, so I think we should stick to it whenever possible.

This isn't just for consistency and predictability, but so that we can apply _theorems_ of 2-monad theory without having to worry about the words being swapped around on us.  For example, [[doctrinal adjunction]] says that given a 2-monad $T$ on a 2-category $K$, two $T$-algebras $A$ and $B$, and an adjunction $f:A\leftrightarrows B:g$ in $K$, to give the left adjoint $f$ the structure of a colax $T$-morphism is the equivalent to giving the right adjoint $g$ the structure of a lax $T$-morphism.  This is one of those insufficiently-well-known facts that is frequently rediscovered in special cases.  For instance, given an adjunction between monoidal categories, to make the left adjoint a colax monoidal functor is the same as to make the right adjoint a lax monoidal functor.  And if I have a lax natural transformation $\alpha:F\to G$ such that each component $\alpha_A$ has a left adjoint, then those left adjoints automatically form an oplax natural transformation.  I think this would be unutterably confusing if "lax natural transformations" were the _oplax_ $T$-morphisms. 

[[Todd Trimble]]: I got around finally to consulting Ross Street about this, and Steve Lack also entered the discussion. I think you may be right (Mike) and I wrong about which is more common in Australia; certainly Kelly for example goes along with B&#233;nabou. 

However, the feelings about that in Australia may be slightly less sanguine then yours. Ross says he has at times felt this was the wrong direction (see for example Coherence for Tricategories, where the direction goes the other way). For example, the direction for monoidal natural transformations is the reverse of B&#233;nabou's. When Ross asked Steve if his opinion on this were strong or lax, he replied: 

"I don't think I'd say I have a strong opinion.

"I agree that the 'other' direction (what has in Australia been called oplax, and which Todd recalls below) seems to be more important (e.g. prevalence of oplax limits/colimits, fact that they generalize monoidal transformations). I also feel that there is probably no perfect system - just as there no perfect system out which things are op and which are co.

"My 'limits for lax morphisms' suggests that there is a mismatch: 2-categories of lax morphisms have oplax limits, but again I think that if this were fixed something else would pop out elsewhere. For instance you can describe oplax naturals as being oplax morphisms somewhere or other.

"If oplax naturals were no longer called oplax naturals then the name icon would become odd (or should that be even odder) but part of the point of naming it was to get away these issues, so I don't think that is too serious." (End of Steve's email)

(Incidentally, I don't know or have forgotten this 'icon' business. What does it stand for, again?) 

Ross summarized his feelings by emphasizing the wisdom of being flexible in these matters. Both directions arise and are important. 

Ross also mentioned that the lax terminology began with the paper "Two constructions on lax functors", where the transformations in B&#233;nabou's direction were dubbed "left lax", and the ones in the other "right lax". Perhaps we could use this terminology ourselves to avoid confusion, and cite this paper as reference. Your thoughts? 

[[Mike Shulman]]: I don't really understand the point of view that "the more important" direction should be called lax and "the less important" direction oplax.  Are limits called "limits" rather than "colimits" because they're "more important"?  I wouldn't say so---it's just that we need to have some convention about which one gets the prefix.  As Ross said, both directions arise and are important, but that doesn't mean we should be inconsistent in naming them.  (Maybe inconsistency isn't what he means by "being flexible," but then I don't know what he means.)  Wouldn't it be confusing if the word "limit" meant either (what we now call) "limit" or "colimit" depending on which one a particular author cared more about at the moment?  And there are so many other *really* poor choices of terminology in mathematics, that I'm surprised people choose to fight a battle about the positioning of an "op."

Speaking for myself, "left lax" and "right lax" would confuse me more.  How do I remember which is which?  Neither one looks particularly "left" or "right" to me. 

_Todd_: Well, it's not that I really care to argue about it that much. As a matter of historical record we _do_ have different conventions appearing in the literature, and you seemed to be plumping for one of those conventions earlier. Now I can't tell: it looks as though you're now saying that the convention is arbitrary, but we should stick with the original (which is Benabou's). 

Linguistically, 'oplax' would be considered as a term derived from 'lax', so I think a natural tendency for people is to apply the primary term to whatever situation they feel is the more dominant. I think that's what Ross must have meant when he said that he's sometimes felt Benabou's direction is the "wrong" one. (I'm not sure if that applies to limit/colimit; in one sense, colimits could be considered secondary because their definition in the enriched context can be seen as based on hom functors hom(-, c) taking them to ordinary limits in the base of enrichment.) 

Perhaps I shouldn't speak for Ross, but I know him a bit, and I think by 'flexible' he means not being too doctrinaire about these things -- his tendency would be to state at the outset of a paper "by lax transformation we mean..." and specify the direction clearly. He's bounced back and forth; apparently he feels the convention is not so strongly established yet that he needs to fix it once and for all, the important thing is to maintain consistency throughout a paper (or talk). But maybe you should ask him next time you see him, if you feel strongly about this. 

So I'm guessing that Ross and Steve are tolerant and non-fussed about this particular issue, and they in particular are not the ones who battle over things like 'co' and 'op'. 

Anyway, this whole discussion started only to sound a warning to the reader that conventions do differ in the literature. Note that I never said we should change the entry, and the arguments put forth for my own preference were not to start an argument. There are good arguments on both sides.

[[Mike Shulman]]: I'm sorry if I sounded too argumentative; I didn't mean to.  What I meant was that I'm surprised people have tried to change Benabou's original terminology at all.  I believe it was Jaap van Oosten who wrote that "the only thing worse than bad terminology is continually changing terminology."  Benabou did use some terminology quite worthy of being changed, like "morphism" and "homomorphism" for "lax 2-functor" and "strong 2-functor" respectively, but switching the meanings of "lax" and "oplax" seems like engendering a lot of confusion for very little gain, when the only argument in favor of it is that oplax ones are (maybe) more common.  On top of this, the argument about 2-monads is a positive reason to prefer Benabou's choice.

Anyway, in terms of productive work, I expanded the entry somewhat to include a warning to the reader about the different choices that exist and a summary of the reasons for making either choice.  Feel free to improve it.

_Todd_: I think you've certainly made a good start. Thanks for writing this up. 
=--


## The Yoneda Lemma ##

Given a bicategory $C$, a lax functor $F:C^{op}\to Cat$ and a $0$-cell $A\in C$, there
are [[adjoint functor]]s

$$ I : Lax(y A,F) \stackrel{\to}{\leftarrow} F(A) : J $$

such that $J \dashv I$.  Here $y A:C \to Cat^{C^{op}}$ is the image of $A$ under the
bicategorical [[Yoneda embedding]].

+-- {: .proof}
###### Proof (sketch)

For $a\in F(A)$, let $J(a):y A\Rightarrow F$ be the lax transformation defined by $J(a)_B(f) = (F f)(a)$.  The components

$$  J(a)_g : F(g) \circ J(a)_X \dot{\to} J(a)_Y \circ g_* $$

for $g:X\to Y$ in $C$ are given by $F$'s comparison map $(F_{g,-})_a$.  The coherence conditions follow from those on $F$ wrt the associator and left unitor of $C$.  For $x:a\to b$ in $F(A)$, $J(x)$ is a modification because $F_{g,f}$ is a natural transformation (i.e. 2-cell in $Cat$).

Let $I(\alpha) = \alpha_A(1_A)$ as usual.  For $m:\alpha\ddot{\to}\beta$ a modification, $I(m)=(m_A)(1_A)$.

The unit $\eta: F A \dot{\to} I J$ at $a\in F A$ is the component $(F_A)_a$ of $F$'s comparison map, which is natural in $a$ by definition.  The counit $\epsilon_\alpha$ is obtained via the usual 1-chasing, and is given in components by

\[ (\epsilon_\alpha)_B(f) = \alpha_B(r_f) \circ (\alpha_f)(1_A) \]

where $r$ is the right unitor of $C$.  Some diagram-chasing confirms that this is indeed natural in everything, and so $\epsilon: J I \dot{\to} Lax(y A,F)$.

The triangle identities may be proved by expanding the definitions above and using the coherence conditions on lax functors and transformations and coherence of $C$.

See Gray for the case [[strict 2-categories]] and strict 2-functors.
=--

+-- {: .query}
[[Finn Lawler|Finn]]:  I don't know how natural this is in $F$ and $A$, but I'll try to figure it out.

Also, if you reverse the definitions of lax and oplax transformations, then you should do the same for functors, and I think in that case $I\dashv J$.

[[Mike Shulman]]: Please don't try to reverse the definitions of lax and oplax functors!  As far as I know everyone is consistent about those, regardless of the choices they make about lax and oplax transformations, so let's not create _additional_ confusion.  Lax functors have comparison maps that go $F g \circ F f\to F(g\circ f)$.
=--

## Related concepts

* [[homotopy]]

* [[transfor]]

  * [[natural transformation]]

    * [[extranatural transformation]], [[dinatural transformation]]

  * [[pseudonatural transformation]]

    * [[pseudo-extranatural transformation]]

  * **lax natural transformation**

  * [[2-dinatural transformation]]

  * [[lax F-natural transformation]]



## References ##

See the references at [[2-category]]. For instance (note slightly outdated terminology)

* Gray, _[[Gray-adjointness-for-2-categories|Adjointness For
2-Categories]]_

The definition is spelled out explicitly in the following, where they are called *lax transformations*:

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

In the following **oplax natural transformations** are defined, but called, simply, "transformations":

* [[Tom Leinster]], _Basic bicategories_,
[arXiv:math/9810017](http://arxiv.org/abs/math/9810017).

* [[Ross Street]], _Two constructions on lax functors_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Volume 13 (1972) no. 3 , p. 217-264 [numdam](http://www.numdam.org/item?id=CTGDC_1972__13_3_217_0)

[[!redirects lax natural transformations]]
[[!redirects lax transformation]]
[[!redirects lax transformations]]
[[!redirects oplax natural transformation]]
[[!redirects oplax natural transformations]]
[[!redirects oplax transformation]]
[[!redirects oplax transformations]]

[[!redirects lax 2-natural transformation]]
[[!redirects lax 2-natural transformations]]
[[!redirects oplax 2-natural transformation]]
[[!redirects oplax 2-natural transformations]]
