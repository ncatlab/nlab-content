+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[mathematical structure]] is _essentially algebraic_ if its definition involves [[functional relation|partially defined operations]] satisfying equational laws, where the [[domain]] of any given operation is a subset where various other operations happen to be equal.  An actual [[algebraic theory]] is one where all operations are total [[function]]s.

The most familiar example may be the ([[strict category|strict]]) notion of [[category]]: a [[small category]] consists of a set $C_0$ of objects, a set $C_1$ of morphisms, source and target maps $s,t : C_1 \to C_0$ and so on, but composition is only defined for pairs of morphisms where the source of one happens to equal the target of the other.

Essentially algebraic theories can be understood through [[category theory]] at least when they are finitary, so that all operations have only finitely many arguments.  This gives a generalisation of [[Lawvere theory|Lawvere theories]], which describe finitary [[algebraic theory|algebraic theories]].

As the domains of the operations are given by the solutions to equations, they may be understood using the notion of [[equalizer]].  So, just as a Lawvere theory is defined using a category with finite [[product]]s, a finitary essentially algebraic theory is defined using a category with [[finite limits]] &#8212; or in other words, finite products and also equalizers (from which all other finite limits, including [[pullback]]s, may be derived).


## Definition

As alluded to above, the most concise and elegant definition is through category theory.  The traditional definition is this:

+-- {: .un_def}
######Definition 
An **essentially algebraic theory** or **finite limits theory** is a category that is [[finitely complete category|finitely complete]], i.e., has all finite limits.  A **model** of an essentially algebraic theory $T$ is a [[functor]]  

$$F: T \to Set$$ 

that is [[left exact]], i.e., preserves all finite limits.  A **homomorphism** of models is a natural transformation

$$ \alpha : F \to F'$$

between left exact functors $F, F' : T \to Set$.  Models of an essentially algebraic theory $T$ and the homomorphisms between them form a category $Mod(T) = Lex(T, Set)$.  

More generally, for any category with finite limits $X$, we can define the category of **models of $T$ in $X$**, $Lex(T, X)$, which has left exact functors $F: T \to X$ as objects and natural transformations between these as morphisms.
=--

However, the finiteness restriction on the limits above is not part of the core concept of an 'essentially algebraic' structure, so one may prefer to call a category with finite limits a **finitary** essentially algebraic theory.  We do this in what follows.

A more traditional syntactic definition (following Ad&#225;mek--Rosicky; see the references below) is as follows: 

+-- {: .un_def}
######Definition
An __essentially algebraic theory__ is a quadruple 

$$\Gamma = (\Sigma, E, \Sigma_t, Def)$$ 

where $\Sigma$ is a many-sorted [[signature (in logic)|signature]] consisting only of operation symbols, $E$ is a set of $\Sigma$-equations, $\Sigma_t \subseteq \Sigma$ is a set of operation symbols called "total", and $Def$ is a function which assigns, to each operation $\sigma \in \Sigma - \Sigma_t$ of type $\prod_{i \in I} s_i \to s$, a set $Def(\sigma)$ of $\Sigma_t$-equations involving only variables $x_i \in Var(s_i)$. 

A (set-theoretic) **model** $M$ of a theory $\Gamma$ assigns to each sort $s$ a set $M(s)$, to each operation symbol $\sigma: \prod_{i \in I} s_i \to s$ of $\Sigma$ a _partial_ function 
$$M(\sigma): \prod_{i \in I} M(s_i) \to M(s)$$
such that 

* For each $\sigma \in \Sigma_t$ the function $M(\sigma)$ is a total function; 

* For each $\sigma \in \Sigma - \Sigma_t$ of type $\prod_{i \in I} s_i \to s$, and each $I$-tuple 
$$a = \langle a_i \rangle_{i \in I} \in \prod_{i \in I} M(s_i),$$
$M(\sigma)(a)$ is defined if and only if all the equations in $Def(\sigma)$ are satisfied at the argument $a$. 

* All the equations of $E$ are satisfied (i.e., are interpreted as equations between partial functions). 
=--

Homomorphisms of models $\theta: M \to M'$ are defined in the standard way: a collection of functions $\theta(s): M(s) \to M'(s)$ for each sort of the signature $\Sigma$ which are compatible with the $M(\sigma), M'(\sigma)$ in the evident way. 


## Properties

The point is that (in the finitary case) either notion of theory may be used to specify the same category of models, and that 

+-- {: .standout}

Categories of models of finitary essentially algebraic theories are precisely equivalent to [[locally presentable category|locally finitely presentable categories]]. These are equivalent to categories of models of finite limit [[sketch]]es. 

=--

A [[duality]] between essentially algebraic theories and their categories of models is given by [[Gabriel-Ulmer duality]]. 

## Examples

* A (multisorted) [[Lawvere theory]] $T$ is the same thing (has the same models) as a finitary essentially algebraic theory in which all operations are total. If $C_T$ is the opposite of the category of finitely presented $T$-algebras, then the category of models is equivalent to $Lex(C_T, Set)$. 

* As mentioned above, categories are models of a finitary essentially algebraic theory. 

* An equational [[Horn theory]] is essentially algebraic, but not all essentially algebraic theories are equational Horn theories. Perhaps surprisingly, $Cat$ is not the category of models of any equational Horn theory, nor is even the category $Pos$ of posets. See [this paper](ftp://132.206.150.195/pub/barr/pdffiles/horn.pdf) by Barr for a proof. Essentially algebraic theories are equivalent to *partial* Horn theories ([Palmgren, Vickers](#PalmgrenVickers)).

* An equivalent formulation is as a _cartesian theory_, a [[geometric theory]] in which disjunction $\bigvee$ is not used, and each use of existential quantification $\exists$ must be accompanied by a proof that existence is unique. See [[Elephant]].

## Related concepts

* [[algebraic theory]] / [[Lawvere theory]] / **essentially algebraic theory** 

  * [[2-Lawvere theory]]  

  *  [[algebraic (∞,1)-theory]] / [[essentially algebraic (∞,1)-theory]]

* [[cartesian logic]]

* [[monad]] / [[(∞,1)-monad]]

* [[operad]] / [[(∞,1)-operad]]

* [[generalized algebraic theory]]

[[!include categories and logic - table]]

## References
 {#References}

Freyd first introduced essentially algebraic theories here:

* [[Peter Freyd]], _Aspects of Topoi_, Bull. Austr. Math. Soc. 7, pp. 1--76, 467--80. 1972 ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/B65FB15DCD85C816F31D9C87D355AD24/S0004972700044828a.pdf/aspects-of-topoi.pdf))

* [[Jiří Adámek]],  M. H&#233;bert,  [[Jiří Rosický]], _On essentially algebraic theories and their generalizations_, Algebra Universalis, August 1999, Volume 41, Issue 3, pp 213-227

* {#AdamekRosicky} [[Jiří Adámek]], [[Jiří Rosický]], section 3.D of _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)

A nice equivalent formulation can be found in

* {#PalmgrenVickers}[[Erik Palmgren]], [[Steve Vickers]] Partial Horn logic and cartesian categories. Annals of Pure and Applied Logic, 145(2007), 314-355. ([pdf](http://www2.math.uu.se/~palmgren/partialalgebras_pre.pdf))

Cartesian theories were introduced under different names in the early seventies by [[John Isbell]], [[Peter Freyd]] and [[Michel Coste]] (cf. [Johnstone 1979](#Johnstone79)). A standard source is Johnstone ([2002](#Johnstone02)).

* {#Freyd02}[[Peter Freyd]], _Cartesian Logic_ , Theor. Comp. Sci. **278** (2002) pp.3-21.

* {#Johnstone79}[[Peter Johnstone]], _A Syntactic Approach to Diers' Localizable Categories_ , pp.466-478 in Springer LNM **753** Heidelberg 1979.

* {#Johnstone02}[[Peter Johnstone]], _Sketches of an [[Elephant]] II_ , Oxford UP 2002. (Around D1.3.4 p.833)

A short introductory/overview note:

* {#keml-diagrams} [[Andreas Nuyts]], _Understanding Universal Algebra Using Kleisli-Eilenberg-Moore-Lawvere Diagrams_, [note](https://anuyts.github.io/files/keml-diagrams.pdf)

[[!redirects essentially algebraic]]
[[!redirects essentially algebraic theory]]
[[!redirects essentially algebraic theories]]
[[!redirects finite limits theory]]
[[!redirects finite limits theories]]
[[!redirects finite limit theory]]
[[!redirects finite limit theories]]
[[!redirects cartesian theory]]
