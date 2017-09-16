Minimal logic, introduced by I. Johansson in 1936, is [[intuitionistic logic]] without the _ex falso quodlibet_ rule $\bot \vdash A$.  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for classical logic and restricting to sequents $\Gamma\vdash\Delta$ where $\Delta$ must contain _exactly one_ formula.

Because it is not the case here that
anything follows from a contradiction, minimal logic is a
[[paraconsistent logic]].

Models of minimal logic are cartesian closed categories, optionally
with finite $n$-ary coproducts for $n\gt 1$.  Under the [Curry-Howard
correspondence](http://en.wikipedia.org/wiki/Curry-Howard_correspondence) minimal logic corresponds to [simply-typed lambda
calculus](http://en.wikipedia.org/wiki/Simply-typed_lambda_calculus), which is roughly speaking another way of saying that both are forms of the [[internal logic]] of [[cartesian closed category|cartesian closed]] categories.

+--{: .query}
Finn, I\'m unsure of what exactly is supposed to be 'minimal logic'.  Does [this unreadable reference](http://projecteuclid.org/DPubS?verb=Display&version=1.0&service=UI&handle=euclid.ndjfl/1093870451&page=record) match your understanding?  To wit: two connectives ($\Rightarrow$ and $\bot$, with $\neg{p}$ defined as $p \Rightarrow \bot$), two axiom schemes ($p \Rightarrow q \Rightarrow p$ and $(p \Rightarrow q \Rightarrow r) \Rightarrow (p \Rightarrow q) \Rightarrow p \Rightarrow r$) and modus ponens.  Note in particular no characterisation of $\bot$ whatsoever (which strikes me as a little too minimal).

I think that I thought that minimal logic did not have $\neg$ or $\bot$ at all; that seems like a more reasonable amount of minimality to me.  Also, it seems that your first paragraph fits the above reference better, while your last fits better the version with no negation at all.  But I may be missing something.  ---[[Toby Bartels]]

[[Mike Shulman|Mike]]: I've definitely seen "minimal logic" used to mean logic that has $\bot$ and $\neg$ but no rule $\bot\vdash A$.

_Toby_:  Possibly I was just thinking of the wrong thing when I created the links here; it doesn\'t seem so interesting anymore.  (^_^)  Well, no point changing it now.
=--
