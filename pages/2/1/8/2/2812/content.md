

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The collectoin $[S^\bullet,R]$ of $R$-valued functions on a [[simplicial set]] $S^\bullet$ is a commutative [[cosimplicial algebra]]. Under the [[monoidal DoldKan correspondence]] it maps to its [[Moore complex|Moore cochain complex]] $C^\bullet([S^\bullet,R])$ which is a [[dg-algebra]] under the [[cup product]]: this is the **cochain complex of the simplicial set**.

Notably, this cochain complex is an $E_\infty$-[[E-infinity-algebra|algebra]] (an [[algebra over an operad|algebra]] over the [[E-infinity operad|E-∞ operad]]). In [[chain homology and cohomology|cohomology]] it becomes a [[graded-commutative algebra]].

## Definition

Let $R$ be commutative [[ring]]. 

For $S$ a set, write 

$$
  [S,R] = R^S
$$

for the $R$-valued functions on $S$: the set of maps from $S$ to $R$ (using either [[internal hom]] notation or [[exponential object]] notation). 

This is in particular naturally 

* a  [[group]] (using the addition in $R$);

* and even an $R$-[[module]] 

* and even an $R$-[[algebra]]. 

* and even a commutative $R$ algebra (since $R$ is assumed to be commutative ring).

Similarly, for $S = (S_\bullet) : \Delta^{op} \to Set$ a [[simplicial set]] write $[S_\bullet,R] $
for the [[cosimplicial algebra]] obtained by taking $R$-valued functions in each degree. This is naturally

* a [[simplicial group|cosimplicial group]]

* and even a cosimplicial $R$-module

* and even a [[cosimplicial algebra]] over $R$ .

Equivalently, if we write $R [S_\bullet]$ for the [[simplicial object|simplicial]] $R$-module which is in degree $n$ the free $R$-module on the set $S_n$, we have a canonical [[isomorphism]]

$$
  [S_\bullet,R] 
    \simeq
  Hom_{R Mod}(R[S_\bullet], R)
  \,.
$$

This latter point of view is often preferred in the literature when $R[S_\bullet]$ is regarded as the collectoin of _chains_ on $S$ and $[S_\bullet,R]$ as that of _cochains_ .

More precisely, we should speak of chains and cochains after applying the [[Moore complex]] functor. Write

$$
  C^\bullet(S,R) := C^\bullet([S_\buller,R])
$$

for the [[Moore complex|Moore cochain complex]] obtained from the [[simplicial group|cosimplicial group]] $[S_\bullet,R]$. This is the **cochain complex** of the simplicial set $S$. Using the [[cup product]], this is even a [[dg-algebra]]. 


## Properties


+-- {: .un_prop}
###### Proposition


The functor 

$$
  [-,R] : SSet \to [\Delta^\op,R Mod]
$$

is a [[symmetric monoidal functor|symmetric]] [[lax monoidal functor]].

=--

+-- {: .proof}
###### Proof

For instance Prop 3.8 in _May03_ .

=--

...

### Homotopy commutativity {#homotopycommutativity}


The [[dg-algebra]] of cochains $C^\bullet(S,R)$ is not, in general, (graded) commutative. But it is homotopy commutative in that it is an [[algebra over an operad]] for an [[E-infinity operad|E-∞ operad]].


+-- {: .un_theorem}
###### Theorem


The cochain functor 

$$
  C^\bullet[-,R] : SSet \to dgAlg
$$ 

naturally factors through [[algebra over an operad|algebras over]] an [[E-infinity operad|E-∞ operad]], notably the [[EilenbergZilber operad]] as well as the [[Barratt-Eccles operad]]. 

In both these cases the complex of binary operations in these operads has a 0-cycle whose action $C^\bullet(S,R) \otimes C^\bullet(S,R) \to C^\bullet(S,R)$ is the usual [[cup product]].

=--

+-- {: .proof}
###### Proof

The statement for the Eilenberg--Zilber operad goes back to _HinSch87_ . A good review is in _May03_ . The statement for the Barrat--Eccles operad is in _BerFre01_ .

=--




## Examples

* For $X$ a [[topological space]] and $\Delta_{Top} : \Delta \to Top$ the canonical topological simplices, the simplicial set $X^{\Delta^\bullet_{Top}}$ is the [[singular simplicial complex]] of $X$. It cochain dg-algebra is the one that computes the [[singular cohomology]] of $X$. 



## References

An explicit description of the cochains that express the homotopy symmetry of the cup product is discussoin from page 30 on of the old

* N. Steenrod, [[SteenrodOnCohomologyOperations.pdf:file]], Colloquium lectures (1957)

The modern operad theoretic statement that for $S \in$ [[SSet]] a [[simplicial set]], the cochain complex  $C^\bullet([S,R])$ is an $E_\infty$-[[E-infinity algebra|algebra]] apparently goes back to 

* _HinSch87_ -- V. Hinich and V. Schechtman, _On homotopy limits of homotopy algebras_, in _K-theory, arithmetic and geometry_, Lecture notes Vol. 1289, Berlin 1987 pp. 240--264 

A particularly clear exposition is in

* M. Mandell, _Cochain multiplication_, Amer. J. Math.  124 (2002)

This in turn is nicely reviewed and spelled out in section 3 of 

* _May03_ -- [[Peter May]], _Operads and sheaf cohomology_ (2003) (unpublished private notes -- but maybe we get permission to upload them here?)

These describe actions of the [[EilenbergZilber operad]] on $C^\bullet([S^\bullet,R])$. 

An action of instead the [[Barratt-Eccles operad]] is described in 

* _BerFre01_ -- [[Clemens Berger]], [[Benoit Fresse]] _Combinatorial operad actions on cochains_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0109158v2))



