
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

**Dinatural transformations** are a generalization of ordinary [[natural transformations]] and also of [[extranatural transformations]].  The differences can be summarized thus:

* In an ordinary *natural transformation* $F\to G$, both $F$ and $G$ involved depend on some variable $x$ with the same variance (covariant or contravariant).
* In an *extranatural transformation* $F\to G$, either $F$ depends on $x$ both covariantly *and* contravariantly and $G$ does not depend on $x$ at all, or vice versa.
* In a **dinatural transformation** $F\to G$, both $F$ and $G$ can depend on $x$ both covariantly and contravariantly.

If the dependence of $F$ or $G$ on $x$ in a dinatural transformation is trivial, it reduces to an extranatural one.  Similarly, if the contravariant (or, dually, the covariant) dependence of $F$ and $G$ on $x$ are trivial, it reduces to an ordinary natural one.

Arguably, most dinatural transformations which arise in practice are ordinary or extranatural.


## Definition

Let $F, G: C^{op} \times C \to D$ be functors. A __dinatural transformation__ from $F$ to $G$, sometimes written 

$$\alpha: F \stackrel{\bullet}{\to} G,$$ 

consists of a collection of morphisms 

$$\alpha_{c}: F(c, c) \to G(c, c)$$ 

such that for every morphism $f: c \to c'$ in $C$, 

\[ \label{hexagon} G(c, f)\alpha_c F(f, c) = G(f, c')\alpha_{c'}F(c', f): F(c', c) \to G(c, c') \]

If drawn out as a commutative diagram, this becomes a "hexagon identity":

\[
\begin{array}{ccccccc}
 &  & F(c,c) & \overset{\alpha_{c}}{\to} & G(c,c)\\
 & \overset{\mathclap{F(f,c)}}{\nearrow} &  &  &  & \overset{\mathclap{G(c,f)}}{\searrow}\\
F(c',c) &  &  &  &  &  & G(c,c')\\
 & \underset{\mathclap{F(c',f)}}{\searrow} &  &  &  & \underset{\mathclap{G(f,c')}}{\nearrow}\\
 &  & F(c',c') & \underset{\alpha_{c'}}{\to} & G(c',c')
\end{array}\,.
\]
 

### Special cases

If $F$ and $G$ both factor through the projection $C^{op}\times C \to C$, then the notion reduces to an ordinary natural transformation, and similarly if they both factor through $C^{op}$.

If $F$ factors through $C$ while $G$ factors through $C^{op}$, then we obtain a notion of natural transformation from a covariant functor to a contravariant one, and dually.

If $G$ is constant, the hexagon identity reduces to the "domain" version of extranaturality, involving a commutative square of the form 

\[ \label{domain} \alpha_c F(f, c) = \alpha_{c'} F(c', f): F(c', c) \to G \]

where $G$ is constant with respect to the argument $c$.  Similarly, if $F$ is constant, it yields the "codomain" version with a commutative square of the form 

\[ \label{codomain} G(c, f) \alpha_c = G(f, c')\alpha_{c'}: F \to G(c, c') \]

when $F$ is constant with respect to the argument $c$. 


## Examples

Of course, all ordinary natural transformations, and also all [[extranatural transformations]], are also dinatural ones.  Here we will confine ourselves to examples that do not reduce to either of these.

* Perhaps the most well known example is the [[Church numerals]]: for any category $C$, we have a class of dinatural transformations from the hom-functor $hom: C^{op}\times C\to Set$

  $$\hom(x, x) \stackrel{\alpha_n}{\to} \hom(x, x)$$ 

  defined by the rule $\alpha_n(f) = f^{(n)}$.

* Not every endo-dinatural-transformation of a hom-functor is of this form; several other examples are given in [Pare-Roman](#PareRoman).  For instance, if $C=FinSet$ then the operation sending each endomorphism to its [[eventual image]] is dinatural.

* The following example of a dinatural transformation from a covariant functor to a contravariant one is found in [Dubuc-Street](#DubucStreet) and attributed to [[Mac Lane]].  Let $C$ be the category of [[inner product spaces]] and isometries, and $D$ the category of [[vector spaces]] and linear transformations (all over a fixed [[field]]).  Let $F:C\to D$ be the forgetful functor and let $G:C^{op}\to D$ be the functor sending each inner product space to its dual.  Define $\alpha_V : F(V) \to G(V)$ to send $v\in V$ to the operation $\langle v,-\rangle$; then $\alpha$ is dinatural.

By a yoneda-like argument, dinatural transformations $\alpha : F \xrightarrow{\bullet} G$ are in bijection with natural transformations $\eta_{x,y} : \hom(x, y) \to \hom(F(y,x), G(x,y))$. The corresponding
transformations are related by

* $\eta_{x,y}(f) = G(x, f) \alpha_x F(f, x) = G(f, y) \alpha_y F(x, f)$

* $\alpha_x = \eta_{x,x}(id)$

## Dinaturality versus extranaturality

Many people who encounter the notion of dinaturality through the general definition (as in equation (eq:hexagon)) have subsequent difficulty grokking it.  It is the opinion of at least one author of this article ([[Todd Trimble]]), and it was certainly the opinion of Max Kelly, that this "efficient" definition is not the most useful or intuitive one.  Rather, one may be better off grokking the separate squares (eq:domain) and (eq:codomain) -- that is, the notion of [[extranaturality]] -- and how they arise in practice. 

One could try to argue against that by pointing to dinatural transformations which do not reduce to extranatural ones.

A counterargument, however, is that *any* dinatural transformation between functors $F,G:C^{op}\times C\to D$ can be "bent" into domain extranaturality by defining

$$C^{op} \times C \stackrel{[F,G]}{\to} Set: (x, y) \mapsto D(F(y, x), G(x, y)).$$

Then a dinatural transformation $F\to G$ can be identified with an extranatural transformation from the constant $1$ (the terminal set) to $[F,G]$. Such tricks support the counterargument that the extra generality of the traditional definition is largely spurious, and not particularly helpful in terms of comprehension.

A further argument for the relative importance of extranatural transformations over dinatural ones is that extranatural transformations can be defined for any sort of [[enriched categories]], whereas dinatural ones (including the other special case of natural transformations from covariant functors to contravariant ones) only make sense when the enriching category is [[cartesian monoidal category|cartesian]].

## Composition

Dinatural transformations cannot, in general, be composed with each other, although there are certain circumstances when they can be.

* One such case is when certain squares are pushouts or pullbacks.

* Of course, ordinary natural transformations can be composed.

* In fact, there is a category whose objects consist of both covariant functors $C\to D$ and contravariant ones $C^{op}\to D$, and whose morphisms are dinatural transformations.

In general, what we can say is that for two fixed categories $C$ and $D$, the functors $C^{op}\times C \to D$ and the dinatural transformations between them form a [[paracategory]].


## Related concepts

* [[homotopy]]

* [[contravariant functor]], [[2-category with contravariance]]

* [[transfor]]

  * [[natural transformation]]

    * [[extranatural transformation]], **dinatural transformation**

  * [[pseudonatural transformation]]

  * [[lax natural transformation]]

  * [[2-dinatural transformation]]


## References

* [[Eduardo Dubuc]] and [[Ross Street]], *Dinatural transformations*, Reports of the Midwest Category Seminar IV, Lecture Notes in Math., vol. 137, Springer, Berlin (1970), pp. 126&#8211;137
 {#DubucStreet}

* [[Robert Paré]] and Leopoldo Rom&#225;n, *Dinatural numbers*, [JPAA](http://www.sciencedirect.com/science/article/pii/S0022404997000364)
 {#PareRoman}

* Guy McCusker, Alessio Santamaria, _A Calculus of Substitution for Dinatural Transformations, I_, ([arXiv:2007.07576](https://arxiv.org/abs/2007.07576))

Here is a blog post inspired by the above discussion that discusses these concepts in the context of the programming language Haskell:

* Dan Piponi, [Dinatural transformations and coends](http://blog.sigfpe.com/2009/03/dinatural-transformations-and-coends.html)



[[!redirects dinaturality]]
[[!redirects dinatural transformations]]
