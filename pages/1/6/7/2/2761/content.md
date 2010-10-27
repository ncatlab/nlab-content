
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


# Contents#
* table of contents
{: toc}


## Idea

The statement of the [[Yoneda lemma]] has a straightforward generalization from [[category|categories]] to [[(∞,1)-category|(∞,1)-categories]].


## Details

+-- {: .un_theorem }
###### Theorem
**$(\infty,1)$-Yoneda embedding**

Let $C$ be an [[(∞,1)-category]] and $PSh(C) := Func(C^\op, \infty Grpd)$ be the corresponding [[(∞,1)-category of (∞,1)-presheaves]]. Then the canonical [[(∞,1)-functor]]

$$
  Y : C \to PSh(C) 
$$

is a [[full and faithful (∞,1)-functor]].

=--


+-- {: .proof}
###### Proof

In terms of [[quasi-categories]], this is proposition 5.1.3.1 in

* [[Jacob Lurie]], [[Higher Topos Theory]]

=--


+-- {: .un_theorem }
###### Theorem
**$(\infty,1)$-Yoneda theorem**

For $C$ a small $(\infty,1)$-category and $F : C^{op} \to \infty Grpd$ an $(\infty,1)$-functor, the composite

$$
  C^{op} \to PSh_{(\infty,1)}(C)^{op} \stackrel{Hom(-,F)}{\to}
  \infty Grpd
$$

is equivalent to $F$.
=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT Lemma 5.5.2.1]].

The statement is a direct consequence of the [[sSet]]-[[enriched category theory|enriched]] [[Yoneda lemma]] by using the fact that the [[(infinity,1)-category of (infinity,1)-presheaves]] $PSh_{(\infty,1)}(C)$ is modeled by the [[enriched functor category]] $[C^{op}, sSet]_{proj}$ with $C$ regarded as a [[simplicially enriched category]] and using the global [[model structure on simplicial presheaves]].

=--


## References

Published statements appear in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

as indicated above.

See also the  [discussion on MathOverflow](http://mathoverflow.net/questions/9737/the-yoneda-lemma-for-oo-1-categories).


[[!redirects Yoneda lemma for (∞,1)-categories]]
[[!redirects (infinity,1)-Yoneda lemma]]
[[!redirects (∞,1)-Yoneda lemma]]

[[!redirects Yoneda embedding for (∞,1)-categories]]
[[!redirects (∞,1)-Yoneda embedding]]
[[!redirects (infinity,1)-Yoneda embedding]]