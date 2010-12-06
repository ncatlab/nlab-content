
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc} 


## Idea

By the logic of [[space]], one may think of a [[topos]] as being (the [[category of sheaves]] on) some generalization of a [[topological space]]. The construction of the first [[fundamental group]] of a topological space happens to generalize to an arbitrary topos, even without a predefined notion of path or [[interval object]]. Instead, by the logic of [[Grothendieck's Galois theory]], the homotopy groups can be detected from the behaviour of [[locally constant sheaf|locally constant sheaves]].

### More details

> (At present the following is just lifted/adapted from another article, (see references below) and needs some editing and possibly correcting. [[Tim Porter|T.P.]])


Let $\mathbb{E}$ be a [[Grothendieck topos]] (think of $\mathbb{E}$ as the
category, $Sh(X)$, of set valued [[sheaf|sheaves]] on a space $X$).  Within
$\mathbb{E}$, we can pick out a [[subcategory]], $\mathbb{C}$, of locally finite,
[[locally constant sheaf|locally constant object]]s in $\mathbb{E}$.  (If $X$ is a space with
$\mathbb{E}= Sh(X)$, $\mathbb{C}$ corresponds to those sheaves whose
'_[[etale space|espace étalé]]_' is a finite
[[covering space]] of $X$.)  Picking a base point in $X$ generalises to picking a 
'[[fiber functor]]' $F :\mathbb{C} \to \mathbf{Sets_{fin}}$, a functor satisfying
  various conditions implying that it is [[pro-representable functor|pro-representable]]. (If $x_0 \in X$
  is a base point $\{x_0\}\to X$ induces a 'fibre functor' $ Sh(X)\to
  Sh\{x_0\} \cong \mathbf{Sets}$, by pullback.)

+--{: .query}
[[Mike Shulman|Mike]]: I presume that more generally any "point" of $\mathbb{E}$, meaning a [[geometric morphism]] $Set\to \mathbb{E}$, supplies a fibre functor (its inverse image)?  Of course, in general $\mathbb{E}$ might not have a point.  Are there other examples of fibre functors when $\mathbb{E}=Sh(X)$?
=--


If $F$ is 'pro-representable' by $P$, then $\pi_1(\mathbb{E},F)$ is defined to
be $Aut(P)$, which is a [[profinite group]].  (Usually we will simply write
$\pi_1(\mathbb{E})$, for this.)  Grothendieck proves there is an [[equivalence
of categories]] 

$$\mathbb{C} \simeq \pi_1(\mathbb{E})-\mathbf{Sets_{fin}},$$ 

the
category of finite $\pi_1(\mathbb{E})$-sets. (This is what is called [[Grothendieck's Galois theory]].) 

If $X$ is a locally nicely
behaved space such as a [[CW complex]] and $\mathbb{E} = Sh(X)$, then
$\pi_1(\mathbb{E})$ is the [[profinite completion of a group|profinite completion]] of $\pi_1(X)$.  This profinite 
completion occurs only because Grothendieck considers locally [[finite object]]s.
Without this restriction, a covering space $Y$ of $X$ would correspond to a
$\pi_1(X)$-set, $Y^\prime$, but if $Y$ is a finite covering of $X$ then the
homomorphism from $\pi_1(X)$ to the finite group of transformations of $Y$
factors through the profinite completion of $\pi_1(X)$.  


### Remarks

 This idea of using covering spaces or their analogue in
$\mathbb{E}$ raises several important points:

* these are *homotopy theoretic results, but no paths (no [[interval object]]) are used*.  The argument
involving [[sheaf and topos theory|sheaf theory]], the theory of [[pro-representable functor]]s, etc., is of 
a purely categorical nature.  This means it is applicable to spaces where the
use of paths, and other homotopies is impossible because of bad (or unknown)
local properties.  Such spaces have been studied within [[shape theory]] and
[[strong shape theory]], although not by using exactly Grothendieck's fundamental group,
nor using sheaf theory. (See below for more on this connection and such
sources as _Lisica and Marde&#353;i&#263;_, _Edwards and
Hastings_, _Cordier and Porter_, _Marde&#353;i&#263; and Segal_  for more
information on Shape and Strong Shape).


*  As no paths are used, these methods can also be applied to 'non-spaces',
e.g. [[locale|locales]] and possibly to their
non-commutative analogues, [[quantale|quantales]].  

For instance, classically one could
consider a [[field]] $k$ and an algebraic closure $K$ of $k$ and then choose
$\mathbb{C}$ to be a category of &#233;tale algebras over $k$, in such a way that 
$\pi_1(\mathbb{E}) \cong Gal(K/k)$, the Galois group of $k$.  A beautiful
treatment of this can be found in Douady and Douady, (see below), and
the link with locales (which is very strong) is explored in Joyal and Tierney.  It, in fact, leads to a classification theorem for
[[Grothendieck topos]]es.  From this viewpoint, low dimensional [[homotopy theory]] is
seen as being part of [[Galois theory]], or _vice versa_. Of course, the really interesting question is how to fit higher dimensional homotopy theory into a higher dimensional Galois theory, and, again, -vice versa-.  See A. Grothendieck, (1975?), [[Pursuing Stacks|Letter to L. Breen]].  *NOT to Quillen as is sometimes claimed.* More on that at [[homotopy group of an ∞-stack]].

* This underlines the fact that $\pi_1(X)$ classifies [[covering space]]s -- but
for $i \gt 1$, $\pi_i(X)$ does not seem to classify anything other than maps
from $S^i$ into $X$!

+--{: .query}
[[Mike Shulman|Mike]]: From a higher-categorical perspective, the reason $\pi_1(X)$ classifies covering spaces is that covering spaces are fibrations with discrete fibers, and so are classified by functors $\Pi_\infty(X)\to Set$.  But since $Set$ is a 1-category, any such functors factors through the 1-categorical reflection of $\Pi_\infty(X)$, which is the ordinary [[fundamental groupoid]] $\Pi_1(X)$.  Thus, to ask what higher homotopy groups classify, one should consider not $\pi_i(X)$ but $\Pi_i(X)$, which one might expect to classify fibrations over $X$ whose fibers are homotopy $(i-1)$-types.

Does a topos have a fundamental groupoid?  A fundamental $i$-groupoid?  A fundamental $\infty$-groupoid?

[[Tim Porter|Tim]]: I am not an expert on the 'not enough points' case, but do know that a long time ago people generalised to a fundamental groupoid. (I think it was a preprint from Montpellier in which I saw this, but I know it was also taken up by others in (?) the 1970s. More recently Marta Bunge and Eduardo Dubuc have published on this and look at at Eduardo's:

http://arxiv.org/abs/0706.1771

[[David Corfield|David]]: The paper [Higher Monodromy](http://lanl.arxiv.org/abs/math/0407507) shows what the fundamental 2-groupoid classifies.

[[Mike Shulman|Mike]]: Just looking at the abstract of _Higher Monodromy_, what I was saying above (for $i=2$) looks like the special case of their theory for locally constant stacks with values in the 2-category $Gpd$ of 1-types.  They don't seem to treat the topos case, though.

=--

## Higher categorical generalization

One may consider the [[vertical categorification]] of this situation from the notion of [[topos]] to that of [[(∞,1)-topos]]. The discussion of the construction of homotopy groups of objects in such a higher topos is at

* [[homotopy group of an ∞-stack]].


## References


The above was taken from an article: 

* [[Tim Porter]], Abstract Homotopy Theory, the interaction of category theory and homotopy theory , Cubo Matematica Educacional, 5, (2003), 115--165.

The general construction of the first geometric homotopy group of objects in a [[Grothendieck topos]] is in section 8.4 of

* [[Peter Johnstone]], _Topos theory_ 



References on [[Grothendieck's Galois theory]] include

* [[Alexander Grothendieck]], (1971), S.G.A.1 - Revetements  &#233;tales et groupe fondamental, Lecture Notes in Maths. 224, Springer-Verlag. 



On Shape and strong shape:

* D.A. Edwards and H. M. Hastings, (1976), &#268;ech and Steenrod homotopy theories with applications to geometric topology, Lecture Notes in Maths. 542, Springer-Verlag. 

* J.T. Lisica and S. Marde&#353;i&#263;, Coherent prohomotopy and strong shape theory, Glasnik Mat. 19(39) (1984) 335-399.

* J.-M. Cordier and [[Tim Porter]], (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).
* S. Marde&#353;i&#263; and J. Segal, (1982) _Shape Theory_, North Holland. 
* S. Marde&#353;i&#263;, _Strong Shape and Homology_, Springer monographs in mathematics, Springer-Verlag.

* On categorical Galois theory

  * F. Borceux and G. Janelidze, (2001), Galois Theories, Cambridge Studies in Advanced Mathematics, 72, Cambridge University Press.

* and for a more traditional approach:

  * A. Douady and R. Douady, (1977) Alg&#233;bre et Th&#233;ories Galoisiennes, Cedic / F. Nathan. 

*  For the link with [[locale] theory

   * [[Andre Joyal]] and M. Tierney, (1984), An extension of the Galois theory of Grothendieck, Mem. Amer. Math. Soc. 309.

* When we have no paths, in internal case, one may find the article of Pataraia useful (beware many typoses, but the article is dense with content):

   * D. Pataraia, Internal categories in the left exact cosimplicial category. Georgian Math. J. 4 (1997), No. 6, 533-556. (<a href="http://www.emis.de/journals/GMJ/vol4/contents.htm">link</a>)
