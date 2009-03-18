#Idea and historical remarks#

(At present this is just lifted/adapted from another article, (see references below) and needs some editing and possibly correcting. T.P.)


Let $\mathbb{E}$ be a Grothendieck topos (think of $\mathbb{E}$ as the
category, $Sh(X)$, of set valued sheaves on a space $X$).  Within
$\mathbb{E}$, we can pick out a subcategory, $\mathbb{C}$, of locally finite,
locally constant objects in $\mathbb{E}$.  (If $X$ is a space with
$\mathbb{E}= Sh(X)$, $\mathbb{C}$ corresponds to those sheaves whose
'\emph{espace &#233;tal&#233;}' (is a finite
covering space of $X$.)  Picking a base point in $X$ generalises to picking a 
'[[fibre functor]]' $F :\mathbb{C} \to \mathbf{Sets_{fin}}$, a functor satisfying
  various conditions implying that it is [[pro-representable]]. (If $x_0 \in X$
  is a base point $\{x_0\}\to X$ induces a 'fibre functor' $ Sh(X)\to
  Sh\{x_0\} \cong \mathbf{Sets}$, by pullback.)

If $F$ is 'pro-representable' by $P$, then $\pi_1(\mathbb{E},F)$ is defined to
be $Aut(P)$, which is a profinite group.  (Usually we will simply write
$\pi_1(\mathbb{E})$, for this.)  Grothendieck proves there is an equivalence
of categories 

$$\mathbb{C} \simeq \pi_1(\mathbb{E})-\mathbf{Sets_{fin}},$$ 

the
category of finite $\pi_1(\mathbb{E})$-sets. (This is what is called [[Grothendieck's Galois theory]].) 

If $X$ is a locally nicely
behaved space such as a CW-complex and $\mathbb{E} = Sh(X)$, then
$\pi_1(\mathbb{E})$ is the profinite completion of $\pi_1(X)$.  This profinite 
completion occurs only because Grothendieck considers locally finite objects.
Without this restriction, a covering space $Y$ of $X$ would correspond to a
$\pi_1(X)$-set, $Y^\prime$, but if $Y$ is a finite covering of $X$ then the
homomorphism from $\pi_1(X)$ to the finite group of transformations of $Y$
factors through the [[profinite completion]] of $\pi_1(X)$.  

 This idea of using covering spaces or their analogue in
$\mathbb{E}$ raises several important points:

* these are *homotopy theoretic results, but no paths are used*.  The argument
involving sheaf theory, the theory of [[pro-representable]] functors, etc., is of 
a purely categorical nature.  This means it is applicable to spaces where the
use of paths, and other homotopies is impossible because of bad (or unknown)
local properties.  Such spaces have been studied within [[Shape Theory]] and
[[Strong Shape Theory]], although not by using exactly Grothendieck's fundamental group,
nor using sheaf theory. (See below for more on this connection and such
sources as _Lisica and Mardesic_, _Edwards and
Hastings_, _Cordier and Porter_, Mardesic and Segal  for more
information on Shape and Strong Shape).


*  As no paths are used, these methods can also be applied to 'non-spaces',
e.g. [[locale|locales]] and possibly to their
non-commutative analogues, [[quantale|quantales]].  

For instance, classically one could
consider a field $k$ and an algebraic closure $K$ of $k$ and then choose
$\mathbb{C}$ to be a category of &#233;tale algebras over $k$, in such a way that 
$\pi_1(\mathbb{E}) \cong Gal(K/k)$, the Galois group of $k$.  A beautiful
treatment of this can be found in Douady and Douady, (see below), and
the link with locales (which is very strong) is explored in Joyal and Tierney.  It, in fact, leads to a classification theorem for
Grothendieck toposes.  From this viewpoint, low dimensional homotopy theory is
seen as being part of Galois theory, or _vice versa_. (Of course, the really interesting question is how to fit higher dimensional homotopy theory into a higher dimensional Galois theory, and, again, -vice versa-.  See A. Grothendieck, (1975?), _Letter to L. Breen_.  *NOT to Quillen as is sometimes claimed.*)

* This underlines the fact that $\pi_1(X)$ classifies covering spaces -- but
for $i \gt 1$, $\pi_i(X)$ does not seem to classify anything other than maps
from $S^i$ into $X$!

#References# 

+-- {: .query}
[[Tim Porter|Tim]]: 
  * Can someone with diacriticals on their fonts fix 'Mardesic' and other instances, please?  I have not found out how to do the Croatian accents on my Mac!

  * Some of these references will need to be shifted to more appropriate entries perhaps, but those entries do not yet exist!
=--
* The above was taken from an article: 

  * T. Porter, Abstract Homotopy Theory, the interaction of category theory and homotopy theory , Cubo Matematica Educacional, 5, (2003), 115 &#8211; 165.

*  On Grothendieck's original approach:

  * A. Grothendieck, (1971), S.G.A.1 Revetements  &#233;tales et groupe fondamental, Lecture Notes in Maths. 224, Springer-Verlag. 



* On Shape and strong shape:

  * D.A. Edwards and H. M. Hastings, (1976), &#711;Cech and Steenrod homotopy theories with applications to geometric topology, Lecture Notes in Maths. 542, Springer-Verlag. 
  * J.T. Lisica and S. Mardesic, Coherent prohomotopy and strong shape theory, Glasnik Mat. 19(39) (1984) 335-399.
  * J.-M. Cordier and T. Porter, (1989), Shape Theory: Categorical Methods of Approximation, Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).
  * S. Marde&#711;si &#769;c and J. Segal, (1982) _Shape Theory_, North Holland. 
  * S. Marde&#711;si &#769;c, _Strong Shape and Homology_, Springer monographs in mathematics, Springer-Verlag.

* On categorical Galois theory

  * F. Borceux and G. Janelidze, (2001), Galois Theories, Cambridge Studies in Advanced Mathematics, 72, Cambridge University Press.

and for a more traditional approach:

  * A. Douady and R. Douady, (1977) Alg&#233;bre et Th&#233;ories Galoisiennes, Cedic / F. Nathan. 

*  For the link with locale theory

  * A. Joyal and M. Tierney, (1984), An extension of the Galois theory of Grothendieck, Mem. Amer. Math. Soc. 309.