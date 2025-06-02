
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a (typically [[algebraically closed field|algebraically closed]]) field $k$, an __algebraic $k$-group__ is a [[group object]] in the category of $k$-[[algebraic variety|varieties]]. 



## Linear algebraic groups and abelian varieties

There are two important classes of algebraic groups whose intersection is trivial (the identity group): Linear algebraic groups and [[abelian variety|abelian varieties]].

Any algebraic group contains a unique normal linear algebraic subgroup $H$ such that their quotient $G/H$ is an abelian variety.

### Linear algebraic group

An algebraic $k$-group is [[linear algebraic group|linear]] if it is a [[Zariski topology|Zariski]]-closed subgroup of the [[general linear group]] $GL(n,k)$ for some $n$.

An algebraic group is linear iff it is affine.

An algebraic group scheme is *affine* if the underlying scheme is [[affine scheme|affine]].

The category of affine group schemes is the [[opposite category|opposite]] of the category of commutative [[Hopf algebras]].

### Abelian variety

Another important class are connected algebraic $k$-groups whose underlying variety is [[projective variety|projective]]; these are automatically commutative so they are called *abelian varieties*.  In dimension $1$ these are precisely the [[elliptic curve]]s. If $k$ is a [[perfect field]] and $G$ an algebraic $k$-group, the theorem of Chevalley says that there is a unique linear subgroup $H\subset G$ such that $G/H$ is an abelian variety.

#### Elliptic curve

An abelian variety of dimension $1$ is called an *[[elliptic curve]]*.

## Other prominent classes of algebraic groups

Some of the definitions of the following classes exist more generally for [[group schemes]].

### Jacobian

(...)

### Unipotent algebraic groups

(See also more generally [[unipotent group scheme]].)

+-- {: .num_defn}
###### Definition
An element $x$ of an affine algebraic group is called *unipotent* if its associated right translation operator $r_x$ on the affine [[coordinate ring]] $A[G]$ of $G$ is locally unipotent as an element of the ring of linear endomorphism of $A[G]$ where ''locally unipotent'' means that its restriction to any finite dimensional stable subspace of $A[G]$ is unipotent as a ring object.
=--

+-- {: .num_theorem}
###### Theorem
([[Jordan-Chevalley decomposition]])
Any commutative linear algebraic group over a perfect field is the  product of a unipotent and a [[semisimple object|semisimple algebraic group]].
=--

## Properties

The group objects in the category of [[algebraic schemes]] and [[formal scheme]]s are called (algebraic) [[group schemes]] and [[formal groups]], respectively. 

Among group schemes are 'the infinite-dimensional algebraic groups' of Shafarevich. 



Algebraic analogues of [[loop group]]s are in the category of [[ind-scheme]]s. All linear algebraic $k$-groups are affine.





## Examples

The [[affine line]] $\mathbb{A}^1$ comes canonically with the structure of a group under addition: the [[additive group]] $\mathbb{G}_a$.

The affine line without its origin, $\mathbb{A}^1 - \{0\}$ comes canonically with the structure of a group under multiplication: the [[multiplicative group]] $\mathbb{G}_m$.

## Generalizations

* [[group scheme]]

## Related concepts

* [[isogeny]]

* [[form of an algebraic group]]

## References

On [[algebraic schemes]] and algebraic groups via [[functorial geometry]]:

* [[Michel Demazure]], [[Pierre Gabriel]], _Groupes algebriques_, tome 1,  avec un appendice _Corps de classes local_ par [[Michiel Hazewinkel|Hazewinkel M]], Mason and Cie, Paris (1970) 
  > (later volumes never appeared)

English translation:

* [[Michel Demazure]], [[Peter Gabriel]], *Introduction to algebraic geometry and algebraic groups*, North-Holland mathematics studies **39** (1980) &lbrack;[ISBN:9780080871509](https://shop.elsevier.com/books/introduction-to-algebraic-geometry-and-algebraic-groups/demazure/978-0-444-85443-8)&rbrack;

See also:

* [[Gerhard P. Hochschild]], *Basic Theory of Algebraic Groups and Lie Algebras*, Graduate Texts in Mathematics **75**, Springer (1981) &lbrack;[doi:10.1007/978-1-4613-8114-3_16](https://doi.org/10.1007/978-1-4613-8114-3_16)&rbrack; 


* M. Artin, J. E. Bertin, M. Demazure, P. Gabriel, A. Grothendieck, M. Raynaud, J.-P. Serre, _Schemas en groupes_, [[SGA3]] 

* {#Milne17} [[James Milne]], *Algebraic Groups -- The theory of group schemes of finite type over a field*, Cambridge University Press (2017)  &lbrack;[doi:10.1017/9781316711736](https://doi.org/10.1017/9781316711736), [webpage](http://www.jmilne.org/math/Books/iag.html), [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf)&rbrack;


* [[Armand Borel]], _Linear algebraic groups_, Springer (2nd edition much expanded)

* W. Waterhouse, _Introduction to affine group schemes_, GTM 66, Springer 1979. 

* [[Serge Lang]], _Abelian varieties_, Springer 1983.

* [[David Mumford]], _Abelian varieties_, 1970, 1985.

* J. C. Jantzen, _Representations of algebraic groups_, Acad. Press 1987 (Pure and Appl. Math. vol 131); 2nd edition AMS Math. Surveys and Monog. 107 (2003; reprinted 2007)

* T. Springer, _Linear algebraic groups_, Progress in Mathematics 9, Birkh&#228;user Boston (2nd ed. 1998, reprinted 2008)

* Roe Goodman, Nolan R. Wallach,  Symmetry, representations, and invariants. Graduate Texts in Mathematics, 255. Springer, Dordrecht, 2009.

* J. Milne, _Algebraic groups, Lie Groups, and their arithmetic subgroups_, [pdf](http://www.jmilne.org/math/CourseNotes/ALA.pdf)

* [[!redirects algebraic groups]]
