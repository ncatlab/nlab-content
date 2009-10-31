A [[category]] is __skeletal__ if objects that are [[isomorphism|isomorphic]] are necessarily [[equality|equal]].  (This is an irredeemably [[evil]] notion.)  A **skeleton** of a category is any skeletal [[subcategory]] whose inclusion functor exhibits it as [[equivalence of categories|equivalent]] to the original category.

If the [[axiom of choice]] holds, then every category has a skeleton: simply choose one object in each isomorphism class.  In fact, the statement that every (possibly [[small category|small]]) category has a skeleton is _equivalent_ to the axiom of choice if "subcategory" and "equivalence" have their naive ('strong') meanings.  For given a [[surjection]] $p:A\to B$, make $A$ into a category with a unique isomorphism $a\cong a'$ iff $p(a)=p(a')$; then a skeleton of $A$ supplies a splitting of $p$.

However, in the absence of choice, it is more appropriate to define a skeleton of $C$ to be *any* equivalent skeletal category, where now "equivalence" is understood in the sense of [[anafunctor]]s or [[weak equivalence]].  In the presence of choice this definition is not much different, since any strong [[equivalence of categories]] $D\to C$, where $D$ is skeletal, exhibits $D$ as isomorphic (not merely equivalent) to a skeletal subcategory of $C$.  This is no longer true for an ana-equivalence or weak equivalence.  However, even with this more general notion of equivalence, some amount of choice is required to show that every category has a skeleton (although, for instance, any [[preorder]] has a skeleton in this sense without any need for choice).

+--{: .query}
_Mike_: It would be interesting to know the precise strength of the statement "every category is (ana-)equivalent to a skeletal one."
=--

Notice that the [[axiom of choice]] fails in general when one considers [[internal category|internal categories]].  Hence not every [[internal category]] has a skeleton.

## Equivalents of choice

Define a *coskeleton* of a category $C$ to be a skeletal category $S$ with a surjective equivalence $C\to S$.  In [[Categories, Allegories]] it is shown that the following are equivalent.

1. Any two ana-equivalent categories are strongly equivalent.
   +-- {: .query}
   I removed 'non-ana', since I don\'t think that 'strongly equivalent' would ever be used in an 'ana-' sense.  ---Toby

   Addendum:  Actually, I don\'t know why I asked whether you meant weakly or strongly here, since obviously one can prove that two ana-equivalent categories are weakly equivalent!  It seems that the discussion above used the terms 'equivalence' and 'ana-equivalence' where [[equivalence of categories]] uses 'strong equivalence' and 'weak equivalence' or 'ana-equivalence'; so I just changed it.  And then I added another entry, which maybe you should remove if Freyd & Scedrov don\'t actually address it.  On the other hand, if they really talk about weak equivalence instead of ana-equivalence (although if they define it in elementary terms, it\'s hard to tell the difference), maybe there\'s no need to say 'ana-' at all on this page.
   =--
1. Any two weakly equivalent categories are strongly equivalent.
1. Every small category has a skeleton.
1. Every small category has a coskeleton.
1. Any two skeletons of a given small category are isomorphic.
1. Any two coskeletons of a given small category are isomorphic.

For convenience we add:

1. Given an inhabited family $\{S_i\}_I$ of equinumerous sets there exists $0 \in I$  and a family of isomorphisms of the permutation groups $\{Aut(S_0) \to Aut(S_i)\}_I$.
1. Given a family $\{S_i\}_I$ of inhabited equinumerous sets, there exists a family $(x_i)_I$ such that $x_i \in S_i$ for all $i \in I$.


[[!redirects skeleta]]
[[!redirects skeletons]]
[[!redirects skeletal]]
[[!redirects skeletal category]]
