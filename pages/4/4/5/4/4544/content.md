
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

See also _[[compact object]]_.

## Contents
* table of contents
{:toc}

## Definitions

### In algebraic geometry

See at _[[morphism of finite type]]_ for the notion in [[algebraic geometry]].  


### In Abelian categories 

An object $X$ in an [[AB5-category]] $C$ is __of finite type__ if one of the following equivalent conditions hold:

(i) any complete directed set $\{X_i\}_{i\in I}$ of [[subobject]]s of $X$ is stationary

(ii) for any complete directed set $\{Y_i\}_{i\in I}$ of subobjects of an object $Y$ the natural morphism $colim_i C(X,Y_i) \to C(X,Y)$ is an isomorphism.

An object $X$ is __finitely presented__ if it is of finite type and if for any 
epimorphism $p:Y\to X$ where $Y$ is of finite type, it follows that $ker\,p$ is also of finite type. An object $X$ in an AB5 category is __coherent__ if it is of finite type and for any morphism $f: Y\to X$ of finite type $ker\,f$ is of finite type.

For an exact sequence $0\to X'\to X\to X''\to 0$ in an AB5 category the following hold:

(a) if $X'$ and $X''$ are finitely presented, then $X$ is finitely presented;

(b) if $X$ is finitely presented and $X'$ of finite type, then $X''$ is finitely presented;

(c) if $X$ is coherent and $X'$ of finite type then $X''$ is also coherent.

For a module $M$ over a ring $R$ this is equivalent to $M$ being finitely generated
$R$-module. It is finitely presented if it is finitely presented in the usual
sense of existence of short exact sequence of the form $R^I\to R^J\to M\to 0$
where $I$ and $J$ are finite. 

### In homotopical algebra and rational homotopy theory
 {#InRationalHomotopyTheory}

A _graded object_ is often said to be of **finite type** if it is _degreewise_ of [[finite number|finite]] [[dimension]]/[[rank]], in some sense. This terminology is used specifically in [[rational homotopy theory]].

Notably a [[rational topological space]] is said to be of _finite type_ if all its rational [[homotopy groups]] are [[finite number|finite]] [[dimension|dimensional]] [[vector spaces]] over the [[rational numbers]].

Accordingly, a [[chain complex]] of vector spaces, possibly those generating a [[semifree dga]] is said to be of finite type if it is degreewise [[finite number|finite]] [[dimension|dimensional]].

Beware however that the terminology clashes somewhat with the use in [[homotopy theory]], there the concept of _[[finite homotopy type]]_ is crucially different from _[[homotopy type with finite homotopy groups]]_.

### In stable homotopy theory

A [[spectrum]] of finite type (in the sense of [[stable homotopy theory]]) is one whose cohomology is finitely generated in each degree, but could exist in infinitely many degrees.

> check

See also/instead at _[[finite spectrum]]_.

## References

* [[Nicolae Popescu]], _Abelian categories with applications to rings and modules_, London Math. Soc. Monographs 3, Academic Press 1973. xii+467 pp. [MR0340375](http://www.ams.org/mathscinet-getitem?mr=0340375)
* MathOverflow [m-oplus-n-is-of-finite-type-if-m-n-are-of-finite-type](http://mathoverflow.net/questions/46136/m-oplus-n-is-of-finite-type-if-m-n-are-of-finite-type)
