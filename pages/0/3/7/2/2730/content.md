This is a page similar to other "Journal Club" pages where we attempt to understand some concept. In this case it is the category [[M-Set]]. Other Journal Club pages include:

* [[An Exercise in Kantization]]
* [[geometric infinity-function theory|Geometric ∞-Function Theory]]

One paper, in particular, we would like to look at is

>[**The category of M-sets**](http://cat.inist.fr/?aModele=afficheN&cpsidt=13517583)<br>
>EBRAHIMI M. Mehdi and MAHMOUDI M.

>**Abstract**<br>
>A topos is a category which looks and behaves very much like the category of sets, and so it may be thought of as a universe for mathematical discourses. One of the very useful topoi in many branches of mathematics as well as in computer sciences is the topos MSet, of sets with an action of a monoid M on them. It is well known that MSet, being isomorphic to the functor category SetM, is a topos. Here, we explicitly give the ingredients of a topos in MSet and investigate their properties for the working scientists and computer scientists. Among other things, we give some equivalent conditions, such as the left Ore condition, to &#937;, the subobject classifier of MSet, being a Stone algera. Also the free and the cofree objects, as well as, limits and colimits are discussed in MSet.

Here are some initial questions we hope to better understand:

* What exactly is $M$-$Set$?
* How is it isomorphic to $Set^M$? (Is the '$M$' here the same as the '$M$' in $M$-$Set$? If not, how are the two senses of $M$ related?) 
* How does one calculate finite products in $M$-$Set$/$Set^M$?

As [[Todd Trimble]] said

>We can go on from there to discuss general limits and colimits in $M-Set$, cartesian closure, the subobject classifier, and so on. This could be fun and a very good learning experience, and there are people right here who know this material rather well.

So let's do it! 

[[Todd Trimble]]: Okay! 

Off the bat, I'm not seeing a clear connection between $M$-sets and multisets. It sounds like you were hoping that (locally finite) multisets were in some way connected with $\mathbb{N}$-sets, so let's talk a little about the latter. As stated in the abstract, an $\mathbb{N}$-set is a set equipped with an action by the monoid $\mathbb{N}$ (natural numbers $0, 1, 2, \ldots$ with the monoid multiplication taken to be ordinary addition). 

A first thing to do is get a very clear picture of what $\mathbb{N}$-sets are like; there are other suggestive words that can be used to describe them. Any ideas? 

[[Eric]]: So the [[monoid]] $\mathbb{N}$ has one object $\bullet$, an identity morphism labeled "+0" and a morphism labeled "+1" that generates all the other morphisms, e.g. $+2 = (+1)\circ(+1)$? So we need to understand the [[functor category]] $Set^\mathbb{N}$. Hmm...

So $F(\bullet)$ is one set $X$ and we need to understand what is the function $F(+1)$ on that set. Hmm...

I guess it doesn't really matter what $F(+1)$ is. It can be any function $f:X\to X$. We simply have $F(+n) = f^n$ with $f^0 = Id$. Ok! 

_Todd_: Right! Very good. So an $\mathbb{N}$-set is tantamount to a set $X$ equipped with an endofunction $f: X \to X$. You could think of $f$ as giving a discrete-time dynamics on $X$. 

And you've sort of answered as well the question about the two senses of $M$. One sense is that $M$ as monoid is a set equipped with a monoid multiplication; the other is to think of $M$ as a one-object category. Here in the nLab we often use $B M$ for the latter, to keep the two senses distinguished. So, to be pedantic, we really ought to say: 

$$M-Set \simeq Set^{B M}$$ 

although I think I'll just elide over the $B$ and let the context dictate the appropriate sense. 

If you'd like to stay focused on multisets and shelve the project of doing some topos theory here, that would be fine. I'll leave it up to you. Of course, now that you've started it, other people might wander by and want to continue this discussion... 

If you did want to continue, then I think we could use $\mathbb{N}$-sets as a running example, since a lot (not all, but a lot) of the general phenomena associated with $M$-sets are already illustrated in this case, and we have clear mental pictures for this case. We could go on for instance to understand finite products (pretty easy), and then more general limits and colimits, and move on from there. 
