[[!redirects comma objects]]

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

My question, I suppose, is whether these 2-universality requirements are equivalent. I know for example that Toby Bartels uses the definition I outlined here in his \href{http://arxiv.org/abs/math/0410328}{paper on 2-bundles} when defining what in that paper he calls 2-pullbacks (which I guess would be bi-iso-comma objects). Sorry if I misunderstood any of that, Toby :). 


=--