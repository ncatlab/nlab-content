
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A *quasigroup* is a binary algebraic structure (a [[magma]]) in which one-sided multiplication is a [[bijection]] in that all [[equations]] of the form 

$$
  \begin{aligned}
    a \cdot x & = b
    \\
    x \cdot a & = b
  \end{aligned}
$$ 

have a unique solution for $x$.

The notion of _quasigroup_ is hence a generalization of the notion of _[[group]]_, in that it does not require the [[associativity]] law nor the existence of an [[identity element]].  

If a quasigroup does have a two-sided [[identity element]] then it is called a _[[loop (algebra)|loop]]_ (French _la boucle_, Russian &#1083;&#1091;&#1087;&#1072;) and a *[[Moufang loop]]* if some further relations are satisfied.

Note that, in the absence of associativity, it is not enough (even for a [[loop (algebra)|loop]]) to say that every element has an [[inverse element]] (on either side); instead, you must say that division is always possible.  This is because the definition $x/y = x y^{-1}$ won\'t work right without associativity.

Some consider the concept of quasigroup to be an example of [[centipede mathematics]], see more at [[historical notes on  quasigroups]]. 


## Definitions

The usual definition is this:
+-- {: .un_defn}
###### Definition

A __quasigroup__ is a [[set]] $G$ equipped with a binary operation $G \times G \to G$ (which we will write with concatenation) such that:

*  for all $x$ and $y$, there exist unique $l$ and $r$ such that $l x = y$ and $x r = y$.

Then $l$ is called the __left quotient__ $y / x$ ($y$ divided by $x$, $y$ over $x$) and $r$ is called the __right quotient__ $x \backslash y$ ($x$ dividing $y$, $x$ under $y$).
=--
Note that we must specify, in the definition, that $l$ and $r$ are unique; without associativity, we cannot prove this.

As with the inverse elements of a group, we can make the quotients into operations so that all axioms are equations:
+-- {: .un_defn}
###### Definition

A __quasigroup__ is a [[set]] $G$ equipped with three binary operations (product, left quotient, and right quotient) such that these equations always hold:

*  $(x / y) y = x$,
*  $x (x \backslash y) = y$,
*  $(x y) / y = x$,
*  $x \backslash (x y) = y$.

=--

Also, without the right quotient we have left quasigroups, and without the left quotient the right quasigroups.
Thus quasigroups are described by a [[Lawvere theory]] and can therefore be [[internalization|internalized]] into any [[cartesian monoidal category]]. There are weaker structures, say left and right quasigroups in which either $\backslash$ or $/$ is well defined. 

## Left and right quasigroups

The left (resp. right) quasigroups that are also [[possibly empty loop|possibly empty left (right) loops]] can be explicitly defined through the left (right) quotient operation itself, with multiplication being defined from the left (right) quotient. 

A __left quotient__ on a set $G$ is a binary operation $(-)\backslash(-):G\times G\to G$, such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=b\backslash b$
  * For all $a$ in $G$, $(a\backslash (a\backslash a))\backslash (a\backslash a)=a$

For any element $a$ in $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash (a\backslash a))\backslash b$. 

The multiplication operation is __associative__ if for all $a$, $b$, and $c$ in $G$, $(a\backslash b)\backslash c= b\backslash ((a\backslash (a\backslash a))\backslash c)$, __unital__ if there exists an element $1$ in $G$ such that for all $a$ in $G$, $a\backslash a = 1$, and __commutative__ if for all $a$ and $b$ in $G$, $(a\backslash (a\backslash a))\backslash b = (b\backslash (b\backslash b))\backslash a$. 

A __right quotient__ on a set $G$ is a binary operation $(-)/(-):G\times G\to G$ such that:

  * For all $a$ and $b$ in $G$, $a/a=b/b$
  * For all $a$ in $G$, $(a/a)/((a/a)/a)=a$

For any element $a$ in $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/((b/b)/b)$. 

The multiplication operation is __associative__ if for all $a$, $b$, and $c$ in $G$, $a/(b/c)=(a/((c/c)/c)/b$, __unital__ if there exists an element $1$ in $G$ such that for all $a$ in $G$, $a/a=1$, and __commutative__ if for all $a$ and $b$ in $G$, $a/((b/b)/b) = b/((a/a)/a)$. 

A quasigroup that is left invertible and right invertible can be defined as a set with a left and right quotient $(G,\backslash,/)$ where left and right multiplications are equal (i.e. $a/((b/b)/b) = (a\backslash (a\backslash a))\backslash b$) for all $a$ and $b$ in $G$. If additionally, there exists a element $1$ in $G$ such that $a\backslash a = 1$ and $a/a = 1$, then the quasigroup is a [[loop (algebra)|loop]]. If the comdition is relaxed to the requirements that left and right identity elements are equal (i.e. $a/a = a \backslash a$) for all $a$ in $G$ and the element $1$ is not required to be in $G$, then the loop might [[possibly empty loop|possibly be empty]]. If the associativity requirement is added to the left and right quotients of the quasigroup, then it becomes an [[associative quasigroup]], where equality of left and right identity and inverse elements can be derived. 

## Examples

*  Any group is an associative quasigroup with [[identity elements]].
* Every [[associative quasigroup]], every [[nonassociative group]], and every [[loop (algebra)|loop]] is a quasigroup. 
* Every [[invertible magma]] is a quasigroup. 
*  Any [[abelian group]] is a quasigroup in two other ways: the product switches places with one of the quotients.  (The other quotient remains a quotient.)
* [[H-space]]s are (homotopy-) loops --- this is because the [[shearing maps]] $(x,y)\mapsto (x,x y)$ and $(x,y)\mapsto (x y, y)$ are equivalences.  This generalizes the octonion examples.  Note that a [[loop space]] is always equivalent to a *group*, hence not all homotopy loops are loop spaces.  In particular ...
*  The nonzero elements of a (not necessarily associative) [[division algebra]] (such as the [[octonion]]s) form a quasigroup; this fact is basically the definition of 'division algebra'.

## Applications

There are interesting subvarieties of quasigroups (which are still not associative). Also, left [[racks]] (and quandles in particular) are precisely left distributive left quasigroups, with abundance of recent applications in the study of knots and links. Finite racks have been studied in the connection to classification of finite dimensional pointed Hopf algebras. Local augmented Lie racks appeared as integration objects in the local integration theory of [[Leibniz algebra]]s.

TS-quasigroups are related to [[Steiner triple system]]s. 

Cayley multiplication tables of finite quasigroups are [[Latin square]]s (basically the 'sudoku squares' from the quotation [[historical notes on quasigroups|here]]). 

As a sample of centipede mathematics, we have the following result on smooth quasigroups, i.e., quasigroups internal to the category of [[smooth manifolds]]: 

+-- {: .num_prop} 
###### Proposition 
The tangent bundle of a smooth quasigroup $Q$ is trivial. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose WLOG that $Q$ is inhabited by an element $x$, and let $V = T_x(Q)$ be the tangent space at $x$. Define a map 

$$\phi \colon Q \times V \to T Q: (y, v) \mapsto (d (K \circ L_y))(v)$$ 

where $L_y: Q \to Q$ is the smooth map $z \mapsto y z$ and $K: Q \to Q$ is the map $z \mapsto z/x$. The map $\phi$ commutes with the bundle projections $\pi_Q: Q \times V \to Q$, $\pi: T Q \to Q$. The map $K$ has an inverse $J: z \mapsto z x$ and each map $L_y$ has an inverse $M_y: z \mapsto y \backslash z$. We may therefore write down an inverse to $\phi$: 

$$T Q \to Q \times V: w \mapsto (\pi(w), d(M_{\pi(w)} \circ J))(w)).$$ 

This shows $T Q$ is isomorphic to the product bundle $Q \times V$. 
=--  

## Related concepts

* [[loop (algebra)]], [[Moufang loop]]

[[!include oidification - table]]

## Literature

* [[eom]]: [quasi-group](http://www.encyclopediaofmath.org/index.php/Quasi-group), [Webs, geometry of](http://www.encyclopediaofmath.org/index.php/Webs,_geometry_of), [Net (in differential geometry)](http://www.encyclopediaofmath.org/index.php/Net_%28in_differential_geometry%29)
* R.H. Bruck, _A survey of binary systems_, Springer-Verlag 1958
* [[Kenneth Kunen]], _Quasigroups, loops, and associative laws_, J. Algebra __185__ (1) (1996), pp. 194&#8211;204
* Momo Bangoura, _Big&#232;bres quasi-Lie et boucles de Lie_,  Bull. Belg. Math. Soc. Simon Stevin __16__:4 (2009), 593-616 [euclid](http://projecteuclid.org/euclid.bbms/1257776236) [arXiv:math.SG/0607662 ](http://arxiv.org/abs/math/0607662); _Quasi-big&#232;bres de Lie et cohomologie d'alg&#232;bre de Lie_, [arxiv/1006.0677](http://arxiv.org/abs/1006.0677) 
* Lev Vasil&#697;evich Sabinin, _Smooth quasigroups and loops: forty-five years of incredible growth_, Commentationes Mathematicae Universitatis Carolinae __41__ (2000), No. 2, 377--400 [cdml](http://dml.cz/dmlcz/119171) [pdf](http://dml.cz/dmlcz/119171)


[[!redirects quasigroup]]
[[!redirects quasigroups]]
