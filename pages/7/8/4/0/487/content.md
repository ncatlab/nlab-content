A category is **balanced** if every [[bimorphism]] (a morphism which is both [[monomorphism|monic]] and [[epimorphism|epic]]) is an [[isomorphism]].

Any [[topos]] (in fact, any [[pretopos]]) is balanced, as are some algebraic categories such as [[Grp|the category of groups]] and any [[abelian category]].  However, the category of rings is not balanced ($Z\hookrightarrow Q$ is monic and epic but not isic). Topological categories are rarely balanced (in $\Top$, for example, the bimorphisms are the continuous bijections), although the category of compact Hausdorff spaces is.

+--{.query}
_Todd_: If $Y$ is Hausdorff, then any $f: X \to Y$ with dense image is also epic.

_Toby_: Yeah, I used to always think so too, but eventually I realised that it was wrong. Take the inclusion $Q \hookrightarrow R$; you\'d think that it\'s epic since you know from geometry that any two curves that agree on the rationals must be equal, but that\'s only true in a Hausdorff space. If $S$ is the usual example of a non-Hasudorff manifold (where a single point is duplicated), then you can map $R \to S$ so as to put some irrational on that point, and then you get two different curves that agree on rationals.

Also argument from authority: Mac Lane gives early on in [[Categories Work]], with the examples of what epimorphisms are in several categories, that they are precisely the surjections in $\Top$. (It was only after reading that several times, and always trying to prove Mac Lane wrong, that I finally realised that he was right.)
=--