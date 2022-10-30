$\Lambda$ is the ring of [[symmetric function]]s in countably many variables. A **$\Lambda$-ring** is a [[P-ring]] for $P = \Lambda$.

$\Lambda$-rings are also called $\lambda$-rings. 


##Idea##

In many situations, we can take [[direct sum]]s of [[representation]]s of some algebraic gadget.  So, decategorifying, the set of isomorphism classes of representations becomes a [[commutative monoid]]. But nobody likes commutative monoids.  So, we throw in formal negatives and get an [[abelian group]] &#8212; the so-called [[Grothendieck group]].

In many situations, we can also take [[tensor product]]s of representations.  Then our Grothendieck group becomes something better than an abelian group.  It becomes a [[ring]]: the [[representation ring]]. But, we're not done!  In many situations we can also take [[exterior power|exterior]] and [[symmetric power|symmetric]] powers of representations.  Indeed, we can often apply any [[Young diagram]] to a representation and get a new representation! Then our representation ring becomes something better than a ring.  It becomes a $\Lambda$-ring!

More generally, the Grothendieck group of a [[monoidal category|monoidal]] [[abelian category]] is always a ring, but if we start with a [[symmetric monoidal category|symmetric monoidal]] abelian category, we get a $\Lambda$-ring. So, $\Lambda$-rings are all about getting the most for your money when you decategorify a symmetric monoidal abelian category -- for example the category of representations of a group, or the category of [[vector bundle]]s on a space.


##Connection to arithmetic##

The abstract of [$\Lambda$-rings and the field with one element](http://arxiv.org/abs/0906.3146) by James Borger

>The theory of $\Lambda$-rings, in the sense of Grothendieck's Riemann--Roch theory, is an enrichment of the theory of commutative rings. In the same way, we can enrich usual [[algebraic geometry]] over the ring $\mathbf{Z}$ of integers to produce $\Lambda$-algebraic geometry. We show that $\Lambda$-algebraic geometry is in a precise sense an algebraic geometry over a deeper base than $\mathbf{Z}$ and that it has many properties predicted for algebraic geometry over the mythical [[field with one element]]. Moreover, it does this is a way that is both formally robust and closely related to active areas in arithmetic algebraic geometry. 


## Two points of view ##

On the [n-Caf&#233;](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025615), James Borger explained two ways that $\Lambda$-rings arise in nature, which he called the 'orthodox' and 'heterodox' approaches.  
He wrote:

>A few words on the orthodox/heterodox approaches to $\Lambda$-rings...

>By the orthodox approach I mean everything involving symmetric functions, including symmetric groups, decategorifying linear tensor categories, K-theory, and so on. Everything mentioned above or pretty much anywhere takes this point of view. Indeed Grothendieck invented $\Lambda$-rings to understand the extra structure on the Grothendieck group inherited from tensor operations (exterior powers etc) on tensor categories.

>By the heterodox point of view, I mean everything involving Frobenius lifts. A Frobenius lift at a prime $p$ on a commutative ring $A$ is an endomorphism which reduces to the $p$-th power 'Frobenius' map $x\mapsto x^p$ on the quotient ring $A/pA$.  If the orthodox point of view is closely related to $K$-theory, the heterodox point of view is closely related to cohomology (e.g crystalline cohomology).

>The connection between the two is as follows. Given any $\Lambda$-ring structure in the orthodox sense, the $p$-th Adams operation $\psi_p$ is a Frobenius lift, and the $\psi_p$ for different primes $p$ all commute with each other. (You can see the split forming already: the Adams operations don't exist on tensor categories until you decategorify.)  Wilkerson's theorem gives the converse, at least in the absence of torsion. It says this: Let $A$ be a commutative ring which is torsion free (in the additive sense), and let $\psi_p$ be a family of commuting Frobenius lifts on $A$ indexed by the prime numbers $p$. Then there is a unique $\lambda$-ring structure on $A$ whose Adams operations are the given Frobenius lifts $\psi_p$. The proof is an unenlightening (IMHO) exercise in composition of symmetric functions. Further, a ring map between two torsion-free $\lambda$-rings is a map of $\lambda$-rings if and only if it commutes with the Adams operations. Thus we have an explicit equivalence between the category of torsion-free $\lambda$-rings and the category of torsion-free commutative rings equipped with commuting Frobenius lifts.

>[In fact, we can get around the torsion-free restriction with a dash of category theory. The category of $\lambda$-rings is both monadic and comonadic over the category of rings (commutative, which I will now stop writing). The point is that that the comonad (and hence the monad) is determined by what happens in the torsion-free setting, where it can be described in terms of Frobenius lifts. How does this work? The category of torsion-free $\lambda$-rings is also comonadic over the category of torsion-free rings. You can show this from either orthodox point of view or the heterodox point of view (where your definition of torsion-free $\lambda$-ring would be the one involving Frobenius lifts). Let $W'$ be this comonad, on the category of torsion-free rings. Now let $W$ be the left Kan extension of this functor (or more precisely the composition of $W'$ with the embedding of torsion-free rings into all rings) to the category of all rings. Then $W$ is a comonad on the category of all rings, and the category of its coalgebras is equivalent to the category of $\lambda$-rings, torsion free or not. By the way, this comonad is precisely the 'big' Witt vector functor.]

>The odd thing is that pretty much no one cares that the two approaches are equivalent, including me. Everything most people want to do is on the orthodox side, and everything I want to do is on the heterodox side. The deeper meaning of connection between the two is completely unclear to me. It could be that it should be viewed as an accident. Indeed the heterodox point of view generalizes to families of Frobenius lifts on other Dedekind domains with finite residue fields in a way that perhaps the orthodox point of view doesn't.  For instance over $F_p[x]$ (instead of $\mathbf{Z}$), we would look at families of $\psi$-operators indexed by the irreducible monic polynomials $f(x)$, and each $\psi_{f(x)}$ would have to be congruent to the $q$-th power map modulo $f(x)$, where $q$ is the size of $F_p[x]/(f(x))$. What is the analogue of such a structure in the world of symmetric functions? Is there a function-field version of symmetric functions? A number field version? It would be great if the answer to these were Yes. But the fact that such analogues are (apparently) unknown suggests that there is something to the split between the two points of view.


##References##

* John Baez, [comment](http://golem.ph.utexas.edu/category/2007/12/this_weeks_finds_in_mathematic_19.html#c013821)
* Donald Knutson, $\lambda$-Rings and the Representation Theory of the Symmetric Group, Lecture Notes in Mathematics, Vol. 308, Springer, Berlin, 1973.


[[!redirects lambda-ring]]
[[!redirects ∞-ring]]
[[!redirects ∞-ring]]
[[!redirects Lambda-rings]]
[[!redirects lambda-rings]]
[[!redirects ∞-rings]]
[[!redirects ∞-rings]]