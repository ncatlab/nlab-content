
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Congruences
* table of contents
{: toc}

## Idea
 {#Idea}

In [[Euclidean geometry]], by *congruence* one means the [[equivalence relation]] on the collection of [[subsets]] of a [[Euclidean space]] which regards two of these as equivalent if one is carried into the other by an [[isometry]] (of the ambient Euclidean space).

Similarly, in [[algebra]], by a *congruence* one means certain [[equivalence relations]] on elements of algebraic [[structures]], such as [[groups]] or [[rings]] (cf. e.g. the [[multiplicative group of integers modulo n]]).

Therefore, in [[category theory]] the term *congruence* is used in the broad generality of
[[equivalence relations]] on (the [[generalized elements]] of) *any object* [[internalization|internal to]] *any* [[finitely complete category]].


## Definitions

+-- {: .num_defn #Definition}
###### Definition

In a [[category]] $C$ with [[pullbacks]], a **congruence** on an [[object]] $X$ is an [[internalization|internal]] [[equivalence relation]] on $X$ (i.e.: an [[internal groupoid]] --- hence an [[internal category]] with all [[morphisms]] being [[isomorphisms]] --- but with no non-[[identity morphism|identity]] [[automorphisms]]). 

This means that it consists of a [[subobject]] 

\[
  \label{TheSubobject}
  i 
  \;\colon\;
  R\stackrel{(p_1,p_2)}\hookrightarrow X \times X
\] 

of the [[Cartesian products]] of $X$ with itself, equipped with the following [[morphisms]]: 

* internal [[reflexive relation|reflexivity]]: $r \colon X \to R$ which is a [[section]] both of $p_1$ and of $p_2$, i.e., $p_1 r = p_2 r = 1_X$;

* internal [[symmetric relation|symmetry]]: $s \colon R \to R$ which interchanges $p_1$ and $p_2$, i.e., $p_1\circ s = p_2$ and $p_2\circ s = p_1$;

* {#InternalTransitivity} internal [[transitive relation|transitivity]]: 

  $t \,\colon\, R \times_X R \to R$ 

  (where on the left we have the [[fiber product]] 
   of $R \hookrightarrow X \times X \overset{pr_2}{\to} X$
   with $R \hookrightarrow X \times X \overset{pr_1}{\to}$, i.e. the subobject of pairs of *composable* pairs in relation)

  which factors the left/right projection map $R \times_X R \to X \times X$ through $R$, i.e., the following [[commuting diagram|diagram commutes]]

  $$
    \array{
      && R 
      \\  
      & 
        {}^{\mathllap{t}}\nearrow 
      & 
      \big\downarrow 
      \\
      R \times_X R 
      & 
        \underset{(p_1 q_1,p_2 q_2)}{\longrightarrow}
      & 
      X \times X
      \mathrlap{\,,}
    }
  $$
  where $q_1$ and $q_2$ are the [[projections]] defined by the [[pullback | pullback diagram]]
  $$\array{
    R \times_X R 
    & 
      \overset{q_2}\longrightarrow 
    & 
    R
    \\
    \big\downarrow{\mathrlap{{}^{q_1}}} 
    && 
    \big\downarrow{\mathrlap{{}^{p_1}}}
    \\
    R 
    & 
      \underset{p_2}\longrightarrow 
    & 
    X
  }
  $$
=--

+-- {: .num_remark}
###### Remark

Since $i$ is a [[monomorphism]], the maps $r$, $s$, and $t$ are necessarily unique if they exist.

=--

+-- {: .num_remark}
###### Remark

Equivalently, a congruence on $X$ is an [[internal category]] with $X$ the object of [[objects]], such that the (source,target)-map is a [[monomorphism]] and such that if there is a morphism $x_1 \to x_2$ then there is also a morphism $x_2 \to x_1$ (internally).

=--

+-- {: .num_remark}
###### Remark

We can equivalently define a congruence $R$ as (a representing object of) a representable sub-presheaf of $\hom(-, X \times X)$ so that for each object $Y$, the composite of $R(Y) \hookrightarrow \hom(Y, X \times X) \cong \hom(Y, X) \times \hom(Y, X)$ exhibits $R(Y)$ as an equivalence relation on the set $\hom(Y, X)$. The upshot of this definition is that it makes sense even when $C$ is not finitely complete.

=--

+-- {: .num_defn #EffectiveCongruence}
###### Definition

A congruence which is the kernel pair of some morphism (example \ref{KernelPairIsCongruence}) is called **effective**.  

=--

+-- {: .num_defn #QuotientObject}
###### Definition

The [[coequalizer]] of a congruence is called a **[[quotient object]]**.  

The quotient of an effective congruence is called an **effective quotient**.  

=--

+-- {: .num_defn}
###### Definition

A [[regular category]] is called an [[exact category]] if every congruence is effective.

=--



## Properties

+-- {: .num_prop}
###### Proposition

An effective congruence, def. \ref{EffectiveCongruence}, is always the [[kernel pair]] of its quotient, def. \ref{QuotientObject}, if that quotient exists.

=--


## Examples

+-- {: .num_example #DiagonalMorphismIsCongruence}
###### Example

Every [[diagonal morphism]] on an object is a congruence and has a [[quotient object]] [[isomorphic]] to the original object. 

=--

+-- {: .num_example #KernelPairIsCongruence}
###### Example

Every [[kernel pair]] is a congruence.

=--


+-- {: .num_example}
###### Example

An [[equivalence relation]] is precisely a congruence in [[Set]].

=--

+-- {: .num_example}
###### Example

The eponymous example is congruence modulo $n$ (for a fixed [[natural number]] $n$), which can be considered a congruence on $\mathbb{N}$ in the category of [[rigs]], or on $\mathbb{Z}$ in the category of [[rings]].

=--

+-- {: .num_example}
###### Example

A [[quotient group]] by a  [[normal subgroup]] $K \hookrightarrow G$ is the quotient of the congruence $R = \{(x,y) : xy^{-1} \in K \}$.

Alternatively, a [[quotient group]] by a  [[normal subgroup]] $K \hookrightarrow G$ is the quotient of the congruence 
 $G \times K \stackrel{(p_1,p_2)}{\hookrightarrow} G \times G$, where $p_1$ is projection on the first factor and $p_2$ is multiplication in $G$ (these are source and target maps in the [[action groupoid]] $G \sslash K$).

A special case of this is that of a _[[quotient module]]_.

=--


## Related pages

* The notions of [[regular category]] and [[exact category]] can naturally be formulated in terms of congruences.  A "higher arity" version, corresponding to [[coherent categories]] and [[pretoposes]] is discussed at [[familial regularity and exactness]].

* A [[Mal'cev category]] is a [[finitely complete category]] in which every internal relation satisfying reflexivity is thereby actually a congruence.

* [[higher category theory|Higher-categorical]] generalizations are that of a [[2-congruence]] and of a [[groupoid object in an (∞,1)-category]]. See also [[(n,r)-congruence]].

## See also 

* [[preordered object]]

* [[internal pseudo-equivalence relation]]

* [[setoid object]]


## References

### In common mathematics

* Wikipedia, <a href="https://en.wikipedia.org/wiki/Congruence_(geometry)">Congruence (geometry)</a>

* Wikipedia, *[Congruence relation](https://en.wikipedia.org/wiki/Congruence_relation)*

### In category theory

References using terminology as above:


* [[Jiri Adamek]], [[Horst Herrlich]], [[George Strecker]], p. 195 of: *[[Abstract and Concrete Categories]]*, John Wiley and Sons, New York (1990) reprinted as: Reprints in Theory and Applications of Categories **17** (2006) 1-507 &lbrack;[tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html), [book webpage](http://katmat.math.uni-bremen.de/acc/)&rbrack;

* [[Francis Borceux]], Exp. 2.10.3.b in: *[[Handbook of Categorical Algebra]]* Vol. 1 *Basic Category Theory*,   Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;

* [[Francis Borceux]], Exps. 2.5.6 in: *[[Handbook of Categorical Algebra]]* Vol. 2 *Categories and Structures*,   Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)&rbrack;

* [[Marek A. Bednarczyk]], [[Andrzej M. Borzyszkowski]], [[Wieslaw Pawlowski]], *Generalized congruences -- epimorphisms in $\mathcal{C}at$*, Theory and Applications of Categories **5** 11 (1999) 266-280 &lbrack;[tac:5-11](http://www.tac.mta.ca/tac/volumes/1999/n11/5-11abs.html), [dml:120226](https://eudml.org/doc/120226?lang=fr&limit=5)&rbrack;


...

But, for what it's worth, a *different* use of the term "congruence" in category theory appears in Def. 3.5.1 on [p. 89](https://www.math.mcgill.ca/triples/Barr-Wells-ctcs.pdf#page=107) in:

* {#BarrWells95} [[Michael Barr]], [[Charles Wells]], *Category theory for computing science*, Prentice-Hall International Series in Computer Science (1995); reprinted in: Reprints in Theory and Applications of Categories **22** (2012) 1-538 &lbrack;[pdf](http://www.math.mcgill.ca/barr/papers/ctcs.pdf), [tac:tr22](http://www.tac.mta.ca/tac/reprints/articles/22/tr22abs.html)&rbrack;

[[!redirects congruence]]
[[!redirects congruences]]
[[!redirects congruence relation]]
[[!redirects congruence relations]]
[[!redirects internal equivalence relation]]
[[!redirects internal equivalence relations]]
[[!redirects internal congruence]]
[[!redirects internal congruences]]