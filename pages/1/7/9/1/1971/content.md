

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--




# Symmetric functions
* table of contents
{: toc}

## Idea

A _symmetric function_ is roughly a [[polynomial]] that is invariant under [[permutation]] of its [[variables]].  However, this is only strictly correct if the number of variables is [[finite number|finite]], while symmetric functions depend on a countably infinite number of variables.   The only symmetric *polynomials* in infinitely many variables are the constants.  To fix this, one allows infinitely many terms, as long as the *degree* is finite. 

For example, there is a $1$-dimensional space of homogeneous symmetric functions of degree $1$, with basis

$$ x_1 + x_2 + \cdots = \sum_i x_i .$$

There is a $2$-dimensional space of homogeneous symmetric functions of degree $2$, with basis

$$ x_1^2 + x_2^2 + \cdots = \sum_i x_i^2 $$

and 

$$ \sum_{i \lt j} x_i x_j .$$

These basis elementa are called the _[[elementary symmetric functions]]_.

(The homogeneous symmetric functions of degree $0$ are just the constants, as usual.)

There is also a noncommutative analogue: [[noncommutative symmetric functions]].


## Definitions

Let $\Lambda_n$ be the [[ring]] consisting of [[polynomials]] in $n$ [[variables]] $x_1, \dots, x_n$ that are invariant under all [[permutations]] of the variables; these are the **symmetric functions in $n$ variables** or **symmetric polynomials** in $n$ variables.   The rings $\Lambda_n$ are [[graded ring|graded]] by degree in the usual way, and there are homomorphisms of graded rings

$$ \Lambda_{n+1} \hookrightarrow \Lambda_{n} ,$$

given by setting the $(n+1)$st variable equal to zero.  Taking the [[limit]] (in the category-theoretic sense) of these rings $\Lambda_n$ as $n \to \infty$, we get the graded ring $\Lambda_\infty$.   This is usually called $\Lambda$, or the ring of **symmetric functions in countably many variables**, or simply **symmetric functions** (or even **symmetric polynomials**, even though very few of them are really polynomials).

Alternatively, $\Lambda$ can be constructed as a [[colimit]] of rings using the homomorphisms

$$ \Lambda_{n} \hookrightarrow \Lambda_{n+1} ,$$

where we add in new terms with the new variable to make the result symmetric.

The definition depends on the [[ground field|ground]] [[field]] (or [[commutative ring]] or [[rig]]) $k$, so we may write $\Lambda(k)$ to be precise.

A query about the Hazewinkel's description of the construction of $\Lambda$ as a (co)limit is [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=3117&Focus=25812#Comment_25812). 


## Properties

Symmetric functions play a fundamental role throughout [[representation theory]], [[combinatorics]] and [[algebraic topology]].  The ring of symmetric functions, $\Lambda$, has many interesting properties.   For example, it is the free $\lambda$-[[lambda-ring|ring]] on one generator (a coincidence of notation that has not been ignored).  It is also a [[plethory]].  There are various bases of $\Lambda$ whose elements are in natural one-to-one correspondence with [[Young diagram|Young diagrams]]. 

$\Lambda$ acquires many of these properties from the fact that it is the [[Grothendieck ring]] of the category of $k$-linear [[species]].  This category is defined to be the functor category

$$ [\mathbb{P}, Vect_{k}] $$

where $\mathbb{P}$ is the groupoid of [[finite sets]] and bijections, and $Vect_k$ is the category of vector spaces over a field $k$ of characteristic zero.  The category of $k$-linear species becomes a symmetric monoidal category thanks to [[Day convolution]].   It is also a [[semisimple category|semisimple abelian category]], with a basis of objects given by irreducible [[representation|representations]] of [[symmetric groups]] --- one for each [[Young diagram]].  So, the [[Grothendieck group]] of this category becomes a commutative ring with a basis given by Young diagrams, and this is just $\Lambda$.  

$\Lambda$ is also the Grothendieck ring of a somewhat smaller 
$Schur$, whose objects are [[Schur functors]].    There are various ways to think about these, but they can be identified with $k$-linear species

$$ F: \mathbb{P} \to Vect_{k} $$

with the special property that $F(n)$ is finite-dimensional for all $n$ and $0$ for $n$ sufficiently large.   The category of Schur functors is again a [[semisimple category|semisimple abelian category]] with a basis of objects given by irreducible [[representation|representations]] of [[symmetric groups]], so its Grothendieck ring is again $\Lambda$.   For more on this, see [[Schur functor]].

\linebreak

The classification described above of irreducible $S_n$-modules over $\mathbb{C}$ also works unchanged for any algebraically closed field $k$ of characteristic zero.  It also works when $k$ has characteristic $p$ and $n$ is not divisible by $p$.   There\'s an exercise at the end of section 6.1 of Serre\'s book (page 64 of the french edition) that says that if $k$ is a field of characteristic $p \gt 0$ then the group algebra of the group $G$ is semisimple iff $p$ doesn\'t divide the order of $G$.

Apart from this, the field matters a lot.  There is a construction that gives all irreducible $k S_n$-modules for any field $k$, field, completely analogous to the Specht module construction over $\mathbb{C}$.  However, it describes each module as a quotient module of a Specht module, and in general not even the dimension of these irreducible modules is known, let alone an explicit basis, or representing matrices.



## Examples

* In the context of [[universal characteristic classes]] of [[vector bundles]], the [[splitting principle]] identifies higher [[Chern classes]] with symmetric polynomials in copies of the [[first Chern class]].

## Related concepts

* [[Witt vector]]

* [[Schur polynomial]]

* [[Schur positivity]]

## References

* [[Richard Stanley]], Section II of: *Theory and application of plane partitions 1*, Studies in Applied Math. **50** 2 (1971), 167-188 ([pdf](http://www-math.mit.edu/~rstan/pubs/pubfiles/12-1.pdf), [[StanleyPlanePartitions1.pdf:file]])


Among the best books in the subject (cf. *[[representation theory of the symmetric group]]*) are:

* [[Gordon D. James]], *The Representation Theory of the Symmetric Groups*,  Lecture Notes in Mathematics, volume 682, Springer 1978 ([doi:10.1007/BFb0067708](https://link.springer.com/book/10.1007/BFb0067708), [pdf](http://www-users.math.umn.edu/~webb/oldteaching/Year2010-11/the-representation-theory-of-the-symmetric-groups-SLN.pdf))

* Gordon James, Adalbert Kerber, _The representation theory of the symmetric group_, With a foreword by P. M. Cohn. With an intr. by G. de B. Robinson. Enc. of Math. and its Appl. __16__, Addison-Wesley 1981. xxviii+510 pp. 

* [[Gordon D. James]], Adalbert Kerber: *The Representation Theory of the Symmetric Group*, Cambridge University Press (1984) &lbrack;[doi:10.1017/CBO9781107340732](https://doi.org/10.1017/CBO9781107340732)&rbrack;


James also has a readable survey article that outlines developments in the '80's and '90's: 

* Gordon D. James, Symmetric groups and Schur algebras, in _Algebraic Groups and their Representations_, eds. R. W. Carter and J. Saxl, Kluwer Acad. Publ. Netherlands 1998.

Other textbooks:

* {#Macdonald95} [[Ian G. Macdonald]], _Symmetric functions and Hall polynomials_, Oxford Math. Monographs, 2nd enlarged ed. 1995 ([ISBN:9780198739128](https://global.oup.com/academic/product/symmetric-functions-and-hall-polynomials-9780198739128?cc=ae&lang=en&))

* {#Stanley99} [[Richard Stanley]], Section 7 of: *Enumerative combinatorics 2*, Cambridge University Press (1999, 2010) ([doi:10.1017/CBO9780511609589](https://doi.org/10.1017/CBO9780511609589), [webpage](http://www-math.mit.edu/~rstan/ec/))

Another approach is described here:

* Alexander Kleshchev, _Linear and Projective Representations of Symmetric Groups_, Cambridge University Press, Cambridge 2009.

One can study symmetric functions in any characteristic, or over any integral domain.  The power sum symmetric functions do not generate the ring of symmetric functions over $\mathbb{Z}$, and this difference matters. They appear to be of limited usefulness in the description of the modular irreducible representations of $S_n$.

The following article surveys the subject in light of the connections to [[Hopf algebras]] and also to  [[noncommutative symmetric function|noncommutative analogue]]:

* [[Michiel Hazewinkel]], _Symmetric functions, noncommutative symmetric functions and quasisymmetric functions_, [pdf](http://oai.cwi.nl/oai/asset/10344/10344B.pdf)


See also

* [[Michiel Hazewinkel]], _[[Hazewinkel, Witt vectors|Witt vectors]]_, Part 1. [arXiv/0804.3888](http://arxiv.org/abs/0804.3888)



[[!redirects symmetric function]]
[[!redirects symmetric functions]]
[[!redirects symmetric polynomial]]
[[!redirects symmetric polynomials]]
