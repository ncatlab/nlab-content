#Contents#
* table of contents
{:toc}

##Idea
Philosophers have sought a means to isolate the properly [[logic|logical]] components of a language from the remainder. A prominent idea here has been to use invariance under arbitrary permutations of the domain of objects. Some, e.g., Mautner and Tarski, have seen this as an extension of the [[Erlangen program]] of [[Felix Klein]], which looked to distinguish geometries by their invariance under different transformation groups.

Tarski's informal definition ([Ln](#Ln)) is reproduced here,
>Now suppose we continue this idea, and consider still wider classes of transformations.
>In the extreme case, we would consider the class of all one-one transformations
>of the space, or universe of discourse, or 'world', onto itself. What will be the
>science which deals with the notions invariant under this widest class of transformations?
>Here we will have very few notions, all of a very general character. I suggest that
>they are the logical notions, that we call a notion 'logical' if it is invariant under all
>possible one-one transformations of the world onto itself.

Logic is now to be seen as the maximally invariant theory.

In the propositional case, consider the [[symmetric group]], $S_n$, acting on a set, $X$, of cardinality $n$. Then it also acts on all cartesian powers, $X^k$. Subsets of $X^k$ are $k$-ary [[relations]], and those invariant under $S_n$ are unions of the [[orbits]] of its action. The idea then is that such relations are invariant if and only if they are definable using only logical constants.

Johan van Benthem proposed ([JvB](#JvB)) such a treatment for a certain [[type theory]]. [[Steve Awodey]] ([Ull](#Ull)) has argued that [[homotopy type theory]] should be seen in a similar light as expressing invariance under [[equivalence]].

##References

* John MacFarlane, _Logical Constants:Permutation invariance_, [SEP](http://plato.stanford.edu/entries/logical-constants/#PerInv)

* F. I. Mautner, _An Extension of Klein's Erlanger Program: Logic as Invariant-Theory_, American Journal of Mathematics, Vol. 68, No. 3 (Jul., 1946), pp. 345-384 (based on [[Hermann Weyl]]'s formulation of the program in _Classical Groups_, pp. 13-18)

* {#Ln} [[Alfred Tarski]], 1986, _What are Logical Notions?_, History and Philosophy of Logic, 7: 143&#8211;154. (Transcript of a 1966 talk, ed. J. Corcoran.) doi:[10.1080/01445348608837096](http://dx.doi.org/10.1080/01445348608837096)

* V. McGee, 1996, _Logical Operations_, Journal of Philosophical Logic, 25: 567&#8211;580

* Denis Bonnay, _Logicality and Invariance_, [lecture series](http://lumiere.ens.fr/~dbonnay/) (under 'Enseignement')

* Denis Bonnay, _Logicality and Invariance_, Bulletin of Symbolic Logic 14 (1):29-68 (2006), [pdf](http://lumiere.ens.fr/~dbonnay/files/Papers/bonnaylogicalityandinvariance.pdf)

* {#JvB} Johan van Benthem, _Logical constants across varying types_, Notre Dame J. Formal Logic 30 (1989), no. 3, 315--342, ([pdf](http://www.illc.uva.nl/lgc/translation/papers/LogicalConstants.pdf))

* {#Ull} Steve Awodey, _Univalence as a logical law_, talk at [conference](https://hottatbristol.wordpress.com/), Bristol 15 Sept 2016.