
The **comma object** of two morphisms $f:A\to C$ and $g:B\to C$ in a [[2-category]] is an object $(f/g)$ equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ and a 2-cell

+--{: style="text-align:center"}
[[!include comma object/2cell]]
=--

which is universal in the sense of a [[2-limit]].

Part of this (to be explicit) is the statement that for any object $D$, 1-morphisms $p':D\to A$, $q':D\to B$ and 2-cell $\sigma:f p'\Rightarrow g q'$ there is a 1-morphism $u:D\to(f/g)$ and isomorphisms $p u\cong p'$, $q u\cong q'$ such that modulo these isomorphisms, we have $\sigma u=\alpha$.  There is also an additional "2-dimensional universality" saying that given $u:D\to (f/g)$ and $v:D\to (f/g)$ and 2-cells $\mu:p u \to p v$ and $\nu:q u \to q v$ such that $\alpha v. f \mu = g\nu . \alpha u$, there exists a unique 2-cell $\beta:u\to v$ such that $p\beta = \mu$ and $q \beta = \nu$.  Note that the 2-dimensional property implies that in the 1-dimensional property, [[generalized the|the]] 1-morphism $u$ is unique up to unique isomorphism.  A square containing a 2-cell with this property is sometimes called a **comma square**.

A **strict comma object** is analogous but has the universal property of a [[strict 2-limit]].  This means that given $p'$, $q'$, and $\sigma$ as above, there exists a _unique_ $u:D\to (f/g)$ such that $p u = p'$, $q u = q'$, and $\sigma u = \alpha$.  Note that any strict comma object is a comma object, but the converse is not in general true.

In [[Cat]], a [[comma category]] is a comma object (in fact a strict one, as normally defined); these give their name to the general notion.


+-- {: .query}

I'm not very experienced with this, so this might be a rather silly observation, but I've been looking at definitions such as this one and the on for [[2-pullback]] in nLab, and I can't help the feeling that they're not really as natural as they ought to be.

Specifically, my problem is with the uniqueness part of the definition, i.e. what you referred to as the 2-dimensional universality: if you were to ask me to guess what the "right" definition for that universality is, I'd phrase it like this: 

Given $u,v: D\to (f/g)$ and isomorphisms $p u \cong p', q u \cong q'$ and similarly for $v$ such that the appropriate identities hold for $u$ and $v$, there is a unique isomorphism $u \cong v$ such that the given isomorphism $p v \cong p'$ is obtained from $p u \cong p'$ by composing with this $u\cong v$, and similarly for $q$ instead of $p$. 

My question, I suppose, is whether these 2-universality requirements are equivalent. I know for example that Toby Bartels uses the definition I outlined here in his [paper on 2-bundles](http://arxiv.org/abs/math/0410328) when defining what in that paper he calls 2-pullbacks (which I guess would be bi-iso-comma objects). Sorry if I misunderstood any of that, Toby :).  ---[[Alexandru Chirvasitu]]

They\'re equivalent in the strong case, that is when all of the $2$-cells involved are assumed or required to be invertible (and that is the case in my paper).  If $\mu_u\colon p u \to p'$ etc (as in your definition above), then $\mu\colon p u \to p v$ etc (as in the definition in the main text) may be defined as $\mu_v^{-1} \circ \mu_u$ etc; conversely, given $\mu$ etc, $p'$ etc may be defined as $p v$ etc and then $\mu_u$ as $mu$, $\mu_v$ as $id_{p v}$, etc.  But for a pure comma object, where $\mu$ etc need not be invertible, then we also wouldn\'t want to require $\mu_u$ etc to be invertible, and then the definition in the text uses a weaker universality condition.

And that is good, since the stronger condition (the one that you gave, but using arbitrary morphisms instead of isomorphism) is not met by the motivating example of [[comma categories]].  (At least I don\'t think it is; I\'ll post this while I look for a specific counterexample).  ---[[Toby Bartels]]


First, thanks for the remarkably quick reply :). Also, thanks for the editing: I'm new here, so I had some trouble with the hyperlink to your paper. 

About the weak case you were referring to above: in my proposed definition, there would be no $\mu:pu\to pv$ to speak of. Even for the usual (i.e. not iso) comma object, I'd ask that $pu\cong p',qu\cong q'$, i.e. isomorphisms, not merely 2-cells (this is what the definition in the main text says too). The difference to the iso-comma object would lie only in the fact that for the usual comma object, the square 2-cell (denoted in Mike's definition by $\alpha$) is no longer required to be invertible. 

So my understanding is that for bilimits, the factorisation of any other "diagram" happens up to isomorphism (i.e. $pu\cong p',qu\cong q'$ in our case). On the other hand, the fact that our 2-arrow $\alpha$ is not an isomorphism in the case of a comma object as opposed to the case of an iso-comma object is another matter, specific to the limit we're looking at. 

Having said that, I believe I see now where the original definitions were coming from: the universailty of the bilimit should simply say that there has to be an equivalence of categories between the category $(D,(f/g))$ of 1-arrows from $D$ to $(f/g)$ and some other category that the limit itself determines (here, we can look at the comma object as the weighted bilimit). Mike's 2-universality part of the definition (the part following after "There is also an additional "2-dimensional universality"") is, I believe, the full faithfulness part of that equivalence of categories. And in fact, he mentioned that the 2-universality in question implies what I was talking about (uniqueness of $u$ up to unique isomorphism). 

So I think I've made my peace with the original definition; I guess it was a rather silly question :). 

Thanks for the help. What's customary? Do we delete the discussion∞---[[Alexandru Chirvasitu]]


=--


[[!redirects comma objects]]