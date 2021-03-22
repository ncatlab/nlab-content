
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An [[operad]] is a structure whose elements are _formal operations_, closed under the operation of plugging some formal operations into others. An **algebra over an operad** is a structure in which the formal operations are interpreted as actual operations on an object, via a suitable [[action]].

Accordingly, there is a notion of [[module over an algebra over an operad]].

## Definition 

Let $M$ be a [[closed monoidal category|closed symmetric monoidal category]] with monoidal unit $I$, and let $X$ be any object. There is a canonical or tautological [[operad]] $Op(X)$ whose $n^{th}$ component is the internal hom $M(X^{\otimes n}, X)$; the operad identity is the map 

$$1_X: I \to M(X, X)$$ 

and the operad multiplication is given by the composite 

$$\array{
M(X^{\otimes k}, X) \otimes M(X^{\otimes n_1}, X) \otimes \ldots \otimes M(X^{\otimes n_k}, X) & \stackrel{1 \otimes func_\otimes}{\to} & M(X^{\otimes k}, X) \otimes M(X^{\otimes n_1 + \ldots + n_k}, X^{\otimes k}) \\ 
 & \stackrel{comp}{\to} & M(X^{\otimes n_1 + \ldots + n_k}, X)
}$$

Let $O$ be any operad in $M$. An **algebra over** $O$ is an object $X$ equipped with an operad map $\xi: O \to Op(X)$. Alternatively, the data of an $O$-algebra is given by a sequence of maps 

$$O(k) \otimes X^{\otimes k} \to X$$ 

which specifies an action of $O$ via finitary operations on $X$, with compatibility conditions between the operad multiplication and the structure of plugging in $k$ finitary operations on $X$ into a $k$-ary operation (and compatibility with actions by permutations). 

An _algebra over an [[operad]]_ can equivalently be defined as a [[category over an operad]] which has a single [[object]].

If $M$ is cocomplete, then an operad in $M$ may be defined as a monoid in the symmetric monoidal category $(M^{\mathbb{P}^{op}}, \circ)$ of permutation representations in $M$, aka [[species]] in $M$, with respect to the substitution product $\circ$. There is an [[actegory]] structure 
$M^{\mathbb{P}^{op}} \times M \to M$ which arises by restriction of the monoidal product $\circ$ if we consider $M$ as fully embedded in $M^{\mathbb{P}^{op}}$: 

$$i: M \to M^{\mathbb{P}^{op}}: X \mapsto (n \mapsto \delta_{n 0} \cdot X)$$ 

(interpret $X$ as concentrated in the 0-ary or "constants" component), so that an operad $O$ induces a [[monad]] $\hat{O}$ on $M$ via the actegory structure. As a functor, the monad may be defined by a [[coend]] formula 

$$\hat{O}(X) = \int^{k \in \mathbb{P}} O(k) \otimes X^{\otimes k}$$ 

An $O$-algebra is the same thing as an algebra over the monad $\hat{O}$. 

**Remark** If $C$ is the [[symmetric monoidal category|symmetric monoidal]] [[enriched category|enriching category]], $O$ the $C$-enriched operad in question, and $A \in Obj(C)$ is the single [[hom-object]] of the [[category over an operad|O-category]] with single object, it makes sense to write $\mathbf{B}A$ for that $O$-category. Compare the discussion at [[monoid]] and [[group]], which are special cases of this.

## Examples

### Over single-coloured operads

* an [[associative algebra]] is an algebra over the [[associative operad]].

  * an [[A-infinity algebra]] is an algebra over a cofibrant [[resolution]] of $Assoc$.

* a [[commutative algebra]] is an algebra over the [[commutative operad]].

  * an [[E-infinity algebra]] is an algebra over a cofibrant [[resolution]] of the commutative operad

* etc.

### Over coloured operads

* There is a [[coloured operad]] $Mod_P$ whose algebras are pairs consisting of a $P$-algebra $A$ and a [[module]] over $A$;

* For a single-coloured operad $P$ there is a coloured operad $P^1$ whose algebras are triples consisting of two $P$ algebras and a [[morphism]] $A_1 \to A_2$ between them.

* Let $C$ be a set. There is a $C$-coloured operad whose algebras are $V$-[[enriched categories]] with $C$ as their set of objects.

## Literature

### Related $n$Lab entries

* [[algebra over a monad]]

  [[∞-algebra over an (∞,1)-monad]] 

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]

* **algebra over an operad** 

   [[∞-algebra over an (∞,1)-operad]]

   * [[model structure on algebras over an operad]]

### Generalizations

* S. N. Tronin, _Algebras over multicategories_, Russ Math. (2016) 60: 52. [doi](http://dx.doi.org/10.3103/S1066369X16020092); Rus. original: &#1057;. &#1053;. &#1058;&#1088;&#1086;&#1085;&#1080;&#1085;, _&#1054;&#1073; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;&#1093; &#1085;&#1072;&#1076; &#1084;&#1091;&#1083;&#1100;&#1090;&#1080;&#1082;&#1072;&#1090;&#1077;&#1075;&#1086;&#1088;&#1080;&#1103;&#1084;&#1080;_, &#1048;&#1079;&#1074;. &#1074;&#1091;&#1079;&#1086;&#1074;. &#1052;&#1072;&#1090;&#1077;&#1084;., 2016, &#8470; 2,  62&#8211;74

[[!redirects algebra over operad]]
[[!redirects algebra for an operad]]
[[!redirects algebra of an operad]]

[[!redirects algebras over an operad]]
[[!redirects algebras over operads]]

[[!redirects algebras over operad]]
[[!redirects algebras for an operad]]
[[!redirects algebras of an operad]]