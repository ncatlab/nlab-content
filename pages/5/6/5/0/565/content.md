
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--


\tableofcontents

## Idea

A _concrete category_ is a [[category]] that looks like a category of "[[sets]] equipped with [[extra structure|extra]] [[structure]]", hence like a category of [[structured sets]].


## Definition

### With a family of collection of elements

+-- {: .num_defn}
###### Definition
Given a category $C$ with a type of objects $Ob(C)$ and for every object $a:Ob(C)$ and $b:Ob(C)$ a set of morphisms $Mor_C(a, b)$, $C$ is a __concrete category__ if for every object $a:Ob(C)$ there is a set of elements $U(a)$ and for every object $a:Ob(C)$ and $b:Ob(C)$, there is an [[injection]] $i_{a,b} \colon Mor_C(a,b) \to (U(a) \to U(b))$. 
=-- 

### With one collection of elements

+-- {: .num_defn}
###### Definition
Given a category $C$ with a type of objects $Ob(C)$ and a set of morphisms $Mor(C)$ with source and target functions $s:Mor(C) \to Ob(C)$ and $t:Mor(C) \to Ob(C)$, $C$ is a __concrete category__ if there is a set of elements $U(C)$ with a function $o:U(C) \to Ob(C)$ with an [[injection]] $i:Mor(C) \to Func(Set)$ (and functions $s_{Set}:Func(Set) \to U(C)$ and $t_{Set}:Func(Set) \to U(C)$) such that for every term $f:Mor(C)$, $s(f) = o(s_{Set}(i(f)))$ and $t(f) = o(t_{Set}(i(f)))$. 
=-- 

### With a functor into Set

+-- {: .num_defn}
###### Definition

A __concrete category__ is a [[category]] $C$ equipped with a [[faithful functor]]
  
  $$
    U : C \to Set
  $$

to the [[large category]] [[Set]]. We say a category $C$ is _concretizable_ if and only if it admits a faithful functor $U: C \to Set$. 
=-- 


+-- {: .num_remark}
###### Remark 

Very often it is useful to consider the case where $U$ is [[representable functor|representable]] by some [[object]] $c_0 \in C$, in that $U \simeq C(c_0,-)$. For example, this is important for the statement of various concrete [[duality|dualities]] induced by [[dual adjunctions]]. We say in this case that $(C, U: C \to Set)$ is _representably concrete_. By definition, the object $c_0$ is then a [[separator]] of the category.

We remark that the existence of a left [[adjoint functor|adjoint]] $F$ to $U: C \to Set$ implies that $U$ is representable by $F(1)$. Conversely, if $C$ has [[coproducts]] or even just [[copowers]], then representability of $U$ implies that $U$ has a left adjoint. 
=-- 


+-- {: .num_remark}
###### Remark

One can also consider concrete categories over any base category $X$ instead of necessarily over $Set$.  This is the approach taken in [Adámek, Herrlich & Strecker 1990](#AdámekHerrlichStrecker90).  Then the (small) categories concrete over $X$ form a [[2-category]] $Cat(X)$.

=--

+-- {: .num_remark}
###### Remark

A concrete category is **univalent** if its underlying category (by forgetting the functor into $Set$) is a [[univalent category]]. 

=--



## Examples

* Any small category $C$ can be made into a concrete category by setting $U(X)$ to be the set of all arrows with codomain $X$, and $U(X \to Y)$ given by composition with $X \to Y$. This can be generalized to any locally small category with a small [[separator]].

The following furnish examples of concrete categories, with the first three representably concrete: 

* $C = Set$ itself with [[separator]] $c_0 = \{\bullet\}$ the singleton set. 

* $C = Top$ with the separator $c_0$ taken to be the one-point space. 

* Any [[monadic functor]] $U: C \to Set$ is faithful (because it preserves equalizers and reflects isomorphisms) and has a left adjoint. As special cases, we have the usual collection of examples of concrete categories: [[monoid]]s, [[group]]s, [[ring]]s, [[algebra]]s, etc. 

A category may be concretizable in more than one way: 

* Take $ C $ to be the category of [[Banach space]]s with morphisms those (everywhere-defined) linear transformations with norm bounded (above) by $ 1 $ (so $ \| T v \| \leq \| v \| $ for all $ v $ in the source).  Then there are two versions of $ U $ that one may use: one where $ U ( V ) $ (for $ V $ a Banach space) consists of *every* vector in $ V $, and one where $ U ( V ) $ consists of those vectors bounded by $ 1 $ (so the closed unit ball in $ V $).  The first may seem more obvious at first, but only the second is representable (by a $ 1 $-dimensional Banach space). 

* Insofar as categories such as $Set$, $Top$, $Vect_k$, etc. admit many [[separators]], these categories may be rendered representably concrete in a variety of ways. Indeed, the category $Vect_k$ may be _monadic_ over $Set$ in many different ways. For example, if $V$ is $n$-dimensional, the functor $\hom(V, -): Vect_k \to Set$ is monadic and realizes $Vect_k$ as equivalent to the category of [[modules]] over the matrix algebra $\hom(V, V)$. 

* Any Grothendieck topos is concretizable, but not necessarily (and typically not) representably concretizable. If $E = Sh(C, J)$ is the category of sheaves on a small site $(C, J)$, we have a familiar string of faithful functors 
$$Sh(C, J) \hookrightarrow Set^{C^{op}} \stackrel{monadic}{\to} Set/C_0 \stackrel{\Sigma_{C_0}}{\to} Set.$$ 
But if for example $E$ is the category of sheaves over $\mathbb{R}$, then no object $X$ can serve as a single separator of $E$, since it cannot detect differences between arrows $Y \stackrel{\to}{\to} Z$ whenever the support of $Y$ is strictly contained in the support of $X$. 

* A concrete category that is equipped with the structure of a [[site]] in a compatible way is a [[concrete site]]. The category of [[concrete sheaves]] on a concrete site is concrete. 

Many familiar examples of "sets with additional structure" provide examples of concrete categories where $U$ is the usual 'underlying set':

* The category $Mon$ of [[monoids]] and monoid [[homomorphisms]] is a concrete category. 

* The category $Ab$ of [[abelian groups]] and abelian group homomorphisms is a concrete category. 

* Given a commutative ring $R$, the category $R Mod$ of $R$-[[modules]] and $R$-[[linear maps]] is a concrete category. 

* Given a commutative ring $R$, the category $R Alg$ of $R$-[[algebras]] and $R$-algebra homomorphisms is a concrete category. 

* The category $CRing$ of [[commutative rings]] and commutative ring homomorphisms is a concrete category. 

* The category $Field$ of [[fields]] and field homomorphisms is a concrete category. 

* The category $HeytAlg$ of [[Heyting algebras]] and Heyting algebra homomorphisms is a concrete category. 

* The category $Frm$ of [[frames]] and frame homomorphisms is a concrete category. 

* The category $Conv$ of [[convergence spaces]] and [[continuous functions]] is a concrete category. 

* The category $Top$ of [[topological spaces]] and continuous functions is a concrete category. 

* The category $Met$ of [[metric spaces]] and [[isometries]] is a concrete category. 

* The category $StrictCat$ of [[strict categories]] and [[strict functors]] is a concrete category. 

There are other examples of concretizable categories where the objects are described as sets, but one cannot choose $U$ satisfying $U(X) = X$

* The category $Set_\bot$ of sets and [[partial functions]] is a concrete category when equipped with the functor $U(X) = X \amalg \{ * \}$ that adds a disjoint point, and sends a partial function to the total function whose undefined values are set to the point.

* The category $Rel$ of sets and [[relations]] has a separator given by the singleton set. Thus, it is a concrete category when equipped with the functor $U(X) = PowerSet(X)$, and $U(X \to Y)$ given by composition of relations (viewing a subset of $X$ as a relation on $X$). This is faithful since for any relation $\Phi \in Rel(X, Y)$ we have $(x,y) \in \Phi$ iff $y \in \Phi \circ \{x\}$.

## Non-examples ##

* The [[classical homotopy category]] [[Ho(Top)]] of [[topological spaces]] is _not_ concretizable

* The opposite category of [[commutative rings]] $CRing^{op}$ equipped with the [[prime spectrum]] functor $CRing^{op} \to Set$ is not concrete, since the prime spectrum is not faithful. This is one of the reasons for the use of [[scheme]]s in algebraic geometry.

* The category $Prefunc$ of sets and [[prefunctions]] is not a concrete category. 


## Properties 

+-- {: .num_prop} 
###### Proposition 
Every small category $C$ is concretizable (since it fully and faithfully embeds in the concrete category $Set^{C^{op}}$). 
=-- 

+-- {: .num_prop}
###### Proposition 
If $C$ is concretizable, so is $C^{op}$. 
=-- 

+-- {: .proof} 
###### Proof 
By assumption, there is a faithful functor $U^{op}: C^{op} \to Set^{op}$, and $\hom(-, \mathbf{2}): Set^{op} \to Set$ is monadic. 
=-- 

+-- {: .num_remark} 
###### Remark 
Of course, since a category $C$ may possess a separator but no [[coseparator]], it does not follow that $C^{op}$ is representably concrete if $C$ is. 
=-- 

### Morphism evaluation and extensionality

+-- {: .num_prop}
###### Proposition 
In any concrete category $(C, U:C \to Set)$, there is an [[evaluation map]] 
$$(-)((-))\colon Hom(a,b) \times U(a) \to U(b)$$ 
such that for every morphism $f \colon Hom(a,b)$ and $g \colon Mor_C(b,c)$ and every element $x:U(a)$, $(g \circ f)(x) = g(f(x))$ and $id_A(x) = x$. 
=-- 

+-- {: .proof} 
###### Proof 
Because [[Set]] is a [[cartesian closed category]], [[currying]] the injective function $f_{a,b}$ of the functor $F$ in [[Set]] means that there is an [[evaluation map]] $(-)((-))\colon Hom(a,b) \times U(a) \to U(b)$ which satisfies the above axioms. 
=-- 

+-- {: .num_prop}
###### Proposition 
In any concrete category $(C, U:C \to Set)$, the morphisms satisfy [[function extensionality]] with respect to the [[evaluation map]]: for all morphisms $f \colon Hom(A,B)$ and $g \colon Hom(A,B)$, if $f(x) = g(x)$ for all [[elements]] $x \colon El(A)$, then $f = g$. 
=-- 

+-- {: .proof} 
###### Proof 
Since [[Set]] is a [[well-pointed category]], and there is a bijection between $\mathbb{1} \to U(a)$ and $U(a)$, function extensionality follows. 
=-- 

### Relationship with well-pointedness

The category [[Set]] of sets and functions is both concrete and well-pointed. However, not every [[well-pointed category]] is an concrete category, as well-pointed categories are not required to be [[concrete categories]]: most models of [[ETCS]] aren't defined to be concrete. Moreover, not every concrete category is a [[well-pointed category]]: the category $Field$ of [[fields]] and field [[homomorphisms]] is concrete, but is not well-pointed because it doesn't have a [[terminal object]]. 

The distinction between concreteness and well-pointedness is the distinction between [[elements]] and [[global elements]] in a concrete category with a [[terminal object]], as it is not true that elements and global elements (if they exist) coincide in general. 

### Characterization

+-- {: .num_theorem}
###### Theorem

A [[finitely complete category]] is concretizable, i.e., admits a [[faithful functor]] to $Set$, if and only if it is [[well-powered category|well-powered]] with respect to [[regular monomorphism|regular]] [[subobjects]].

=--

+-- {: .proof}
###### Proof

The "only if"-part is due to [Isbell 1963](#Isbell63).  To prove it, note that if $F \colon C\to D$ is a faithful functor, then it is injective on equivalence classes of regular subobjects.  For suppose that $m\colon a \to x$ is the [[equalizer]] of $f,g\colon x\rightrightarrows y$, and $n\colon b\to x$ is the equalizer of $h,k\colon x\rightrightarrows z$.  If $F(a) \cong F(b)$ as subobjects of $F(x)$, then since $f m = g m$ and so $F(f)\circ F(m) = F(g)\circ F(m)$, we must also have  $F(f)\circ F(n) = F(g)\circ F(n)$; hence (since $F$ is faithful) $f n = g n$, so that $n$ factors through $m$.  Conversely, $n$ factors through $m$, so we have $a\cong b$ as subobjects of $x$.  Since $Set$ is regularly well-powered, it follows that any category admitting a faithful functor to $Set$ must also be so.

(Actually, Isbell proved a more general condition which applies to categories that may lack finite limits.)

"If" was proven in ([Freyd](#Freyd)).  The argument is rather more involved, passing through [[additive categories]], and is not reproduced here.

=-- 

+-- {: .num_remark} 
###### Remark 
A relatively deep application of Isbell's result is that the [[classical homotopy category]] [[Ho(Top)]] of [[topological spaces]] is _not_ concretizable, even though it is a quotient of $Top$ which _is_ concretizable. ([Freyd 70](#Freyd70))

A similar way to use Isbell's result applies to show that a really vast number of model categories can not have a concrete localization at weak equivalences: see [Di Liberti and Loregian, 2017](#DiliLore)

=-- 

## Related concepts

* [[topological concrete category]]

* [[concrete object]]

* [[amnestic functor]]  (for many usual concrete categories, the forgetful functor happens to be amnestic)

* [[function extensionality]]

* [[well-pointed category]]

* [[family of objects in a concrete category]]

* [[concrete (2,1)-category]]

* [[concrete (n,1)-category]]

* [[concrete (infinity,1)-category]]


## References

Monograph:

* {#AdámekHerrlichStrecker90} [[Jiří Adámek]], [[Horst Herrlich]], [[George Strecker]]: *[[Abstract and Concrete Categories -- The Joy of Cats]]*, Wiley (1990), reprinted as: Reprints in Theory and Applications of Categories **17** (2006) 1-507 &lbrack;[tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html), [book webpage](http://katmat.math.uni-bremen.de/acc/), [pdf](http://www.tac.mta.ca/tac/reprints/articles/17/tr17.pdf)&rbrack;

Original articles:

* {#Isbell63} [[John Isbell]]: *Two set-theoretical theorems in categories*, Fund. Math **53** 1 (1963) 43-49 &lbrack;[eudml:213746](https://eudml.org/doc/213746)&rbrack;

* {#Freyd69} [[Peter Freyd]]: *On the concreteness of certain categories*, in: Symposia Mathematica **4** (1969) 431–456

* {#Freyd} [[Peter Freyd]]: *Concreteness*, Journal of Pure and Applied Algebra **3** 2 (1973) 171-191 \[<a href="https://doi.org/10.1016/0022-4049(73)90031-5">doi:10.1016/0022-4049(73)90031-5</a>\]

On non-concreteness of the [[classical homotopy category]]:

* {#Freyd70} [[Peter Freyd]]: *Homotopy is not concrete*, in: _The Steenrod Algebra and its Applications_, Lecture Notes in Mathematics **168**, Springer (1970) &lbrack;[doi:10.1007/BFb0058516](https://doi.org/10.1007/BFb0058516)&rbrack; 

  reprinted in: Reprints in Theory and Applications of Categories **6** (2004) 1-10 &lbrack;[tac:tr6](http://www.tac.mta.ca/tac/reprints/articles/6/tr6abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/6/tr6.pdf)&rbrack;

and generalized to certain [[homotopy categories of model categories]]:

* {#DiliLore} [[Ivan di Liberti]], [[Fosco Loregian]]: *Homotopical algebra is not concrete*, Journal of Homotopy and Related Structures **13** (2018) 673–687 &lbrack;[arXiv:1704.00303](https://arxiv.org/abs/1704.00303), [doi:10.1007/s40062-018-0197-3](https://doi.org/10.1007/s40062-018-0197-3)&rbrack;


[[!redirects concrete category]]
[[!redirects concrete categories]]
[[!redirects CAT(X)]]
[[!redirects Cat(X)]]
