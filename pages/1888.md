


The first thing to notice about (covariant) **tensorial strengths** is that they attach to a [[functor]] from a [[monoidal category]] to itself, say $T: V \to V$. (The concept doesn't make much immediate sense if $T$ is a functor between different monoidal categories.) 

One possible reason why it may be hard to grasp the notion of strength is because in the case $V = Set$, they're sort of invisible. Every functor $T: Set \to Set$ has one, in fact a canonical one! This will make more sense in a moment. 

Strengths are easier to understand by considering the case where $V$ is [[closed monoidal category|closed monoidal]]. Here $V$ is [[enriched category|enriched]] in itself, and one of the most important aspects of strengths is this: 

* A functor $T: V \to V$ with a strength is the same thing as a $V$-enrichment on $T$. 

Here's how that works. An enrichment on $T$ in $V$-[[enriched category theory]] consists of a natural family of morphisms in $V$, 

$$hom(a, b) \to hom(T(a), T(b)),$$ 

satisfying some suitable axioms. Here $hom$ denotes the enrichment of $V$ in itself -- the [[internal hom]]. Starting from a strength on $T$, you can cook up an enrichment on $T$, roughly as follows: the map above is equivalent by hom-tensor [[adjunction]] to a map 

$$hom(a, b) \otimes T(a) \to T(b)$$ 

and now the strength allows you to slide $hom(a, b)$ inside $T$, and from there you just apply $T$ to the evaluation: 

$$T(hom(a, b) \otimes a) \overset{T(eval_{a, b})}{\to} T(b)$$ 

and presto, you're done. The strength axioms ensure that this enrichment structure on $T$ satisfies the axioms you need for a functor to be enriched. 

(And going back the other way, from an enrichment to a strength, is also easy -- there you have to dualize. That is, instead of using the evaluation which is the counit of the hom-tensor adjunction, you use the coevaluation which is the unit. ) 

After some work, one can convince oneself that the notions of strength and enrichment for endofunctors on closed monoidal categories really are equivalent notions. 

And now we can understand why strengths in the case $V = Set$ are so "invisible" -- every functor $T: Set \to Set$ is $Set$-enriched; that's what we mean by an ordinary functor!  

There's rather a lot more one could say about strengths, and I may come back to more of that later, but I would like to say that strengths are kind of a trade secret. The first mathematician I know of who intuitively grasped strength was C.S. Peirce! And particularly in his Alpha graphs, the notion of strength plays an important role. 

The insight here can be related back to the enrichment = strength phenomenon. Suppose for instance we're in the theory of [[Boolean algebra]]s -- say we're studying the structure of a free Boolean algebra on a set of generators, $B[X]$. Then again we can think of this, or of any [[Heyting algebra]], as enriched in itself. Further, we have definable unary operators 

$$T: B[X] \to B[X]$$ 

in the theory, such as $T = p \wedge (-)$, or $T = p \Rightarrow (-)$, etc. The great discovery of Peirce is that any definable unary operator in the theory of Boolean algebras carries a strength, or if you prefer is enriched. That may be taken to be the essence of Peirce's iteration rule for Alpha, and it [[vertical categorification|categorifies]] right over to a similar statement for the theory of [[closed monoidal category|closed categories]], [[star-autonomous category|star-autonomous categories]], what have you: all definable unary covariant functors in such theories carry canonical strengths. 

(Peirce went a little further, and incorporated notions of contravariant strength as well.) 

