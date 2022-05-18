
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

# Contents
* table of contents
{: toc}

## Idea

A _concrete category_ is a [[category]] that looks like a category of "[[set]]s with extra [[stuff, structure, property|structure]]", that is a category of [[structured sets]].


## Definition

### With one collection of elements

+-- {: .num_defn}
###### Definition
Given a category $C$ with a type of objects $Ob(C)$ and a set of morphisms $Mor(C)$ with source and target functions $s:Mor(C) \to Ob(C)$ and $t:Mor(C) \to Ob(C)$, $C$ is a __concrete category__ if there is a set of elements $U(C)$ with a function $o:U(C) \to Ob(C)$ with a [[partial function|partial]] [[injection]] $i:Mor(C) \to (U(C) \to U(C))$ such that for every term $f:Mor(C)$, $i(s(f)) = s_{Set}(i(f))$ and $i(t(f)) = t_{Set}(i(f))$. 
=-- 

### With a family of collection of elements

+-- {: .num_defn}
###### Definition
Given a category $C$ with a type of objects $Ob(C)$ and for every object $a:Ob(C)$ and $b:Ob(C)$ a set of morphisms $Mor_C(a, b)$, $C$ is a __concrete category__ if for every object $a:Ob(C)$ there is a set of elements $U(a)$ and for every object $a:Ob(C)$ and $b:Ob(C)$, there is an [[injection]] $i_{a,b} \colon Mor_C(a,b) \to (U(a) \to U(b))$. 
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

One can also consider concrete categories over any base category $X$ instead of necessarily over $Set$.  This is the approach taken in [The Joy of Cats](#JoyOfCats).  Then the (small) categories concrete over $X$ form a [[2-category]] $Cat(X)$.

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

Other examples: 

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

* The category $Set_\bot$ of sets and [[partial functions]] is a concrete category when equipped with the functor $U(X) = X \amalg \{ * \}$ that adds a disjoint point, and sends a partial function to the total function whose undefined values are set to the point.

## Non-examples ##

* The category $Prefunc$ of sets and [[prefunctions]] is not a concrete category. 

* The category $Rel$ of sets and [[relations]] is not a concrete category, because the functor $U:Rel \to Set$ is not [[faithful functor|faithful]]. 

* For the same reason, given a concrete [[regular category]] $C$, the category $Rel(C)$ of objects of $C$ and [[internal relations]] between objects of $C$ is not concrete. 

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

A [[finitely complete category]] is concretizable, i.e., admits a [[faithful functor]] to $Set$, if and only if it is [[well-powered category|well-powered]] with respect to [[regular monomorphism|regular]] [[subobject]]s.

=--

+-- {: .proof}
###### Proof

"Only if" was proven in ([Isbell](#Isbell)).  To prove it, note that if $F: C\to D$ is a faithful functor, then it is injective on equivalence classes of regular subobjects.  For suppose that $m\colon a \to x$ is the [[equalizer]] of $f,g\colon x\rightrightarrows y$, and $n\colon b\to x$ is the equalizer of $h,k\colon x\rightrightarrows z$.  If $F(a) \cong F(b)$ as subobjects of $F(x)$, then since $f m = g m$ and so $F(f)\circ F(m) = F(g)\circ F(m)$, we must also have  $F(f)\circ F(n) = F(g)\circ F(n)$; hence (since $F$ is faithful) $f n = g n$, so that $n$ factors through $m$.  Conversely, $n$ factors through $m$, so we have $a\cong b$ as subobjects of $x$.  Since $Set$ is regularly well-powered, it follows that any category admitting a faithful functor to $Set$ must also be so.

(Actually, Isbell proved a more general condition which applies to categories that may lack finite limits.)

"If" was proven in ([Freyd](#Freyd)).  The argument is rather more involved, passing through [[additive categories]], and is not reproduced here.

=-- 

+-- {: .num_remark} 
###### Remark 
A relatively deep application of Isbell's result is that the [[classical homotopy category]] [[Ho(Top)]] of [[topological spaces]] is _not_ concretizable, even though it is a quotient of $Top$ which _is_ concretizable. ([Freyd 70](#Freyd70))

A similar way to use Isbell's result applies to show that a really vast number of model categories can not have a concrete localization at weak equivalences: see [Di Liberti and Loregian, 2017](#DiliLore)

=-- 

## Related concepts

* [[concrete object]]
* [[amnestic functor]]  (for many usual concrete categories, the forgetful functor happens to be amnestic)
* [[function extensionality]]
* [[well-pointed category]]
* [[family of objects in a concrete category]]
* [[concrete (2,1)-category]]

## References

* [[Jiří Adámek]], [[Horst Herrlich]], [[George Strecker]], *Abstract and Concrete Categories*, Wiley 1990, reprinted as: Reprints in Theory and Applications of Categories, No. 17 (2006) pp. 1-507 ([tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html))


* _[[The Joy of Cats]]_
{#JoyOfCats}

* [[John Isbell]], _Two set-theoretical theorems in categories_, Fund. Math 53 (1963)
{#Isbell}

* {#Freyd} [[Peter Freyd]], _Concreteness_, JPAA 3 (1973)

* {#Freyd70} [[Peter Freyd]], _Homotopy is not concrete_, in _The Steenrod Algebra and its Applications_, Springer Lecture Notes in Mathematics Vol. 168, Springer-Verlag, 1970, Republished in: Reprints in Theory and Applications of Categories, No. 6 (2004) pp 1-10 ([web](http://www.tac.mta.ca/tac/reprints/articles/6/tr6abs.html))

* {#DiliLore} [[Ivan di Liberti]], [[Fosco Loregian]] "Homotopical algebra is not concrete." Journal of Homotopy and Related Structures (2017): 1-15.


[[!redirects concrete category]]
[[!redirects concrete categories]]
[[!redirects CAT(X)]]
[[!redirects Cat(X)]]
