
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A (left/right) _dual_ to an [[object]] in a [[monoidal category]] $\mathcal{C}$ is a [[left adjoint|left]]/[[right adjoint|right]] [[adjoint]] to the object regarded as a [[morphism]] in the [[delooping]] [[2-category]] $\mathbf{B}\mathcal{C}$. If a dual exists, the object is called _dualizable_.


Being *dualizable* may often be thought of as a [[category theory|category-theoretic]] notion of *finiteness* for [[objects]] in a [[monoidal category]].  For instance, a [[vector space]] is dualizable in [[Vect]] with its standard [[tensor product]] precisely if it is a [[finite-dimensional vector space]]; and a [[spectrum]] is dualizable in the [[stable homotopy category]] with its [[smash product]] precisely if it is a [[finite spectrum]].

A more precise intuition is that an object is dualizable if its "size" is no larger than the "additivity" of the monoidal category.  Since [[Vect]] and the [[stable homotopy category]] are finitely [[additive category|additive]], but not infinitely so, dualizability there is a notion of finiteness.  This is the case for many monoidal categories in which one considers dualizability.  However, in a monoidal category which is not additive at all, such as [[Set]] (or any cartesian monoidal category), only the terminal object is dualizable---whereas in an "infinitely additive" monoidal category such as [[Rel]] or [[SupLat]], many "infinite" objects are dualizable.  (In $Rel$, *all* objects are dualizable.) 

+-- {: .num_remark}
###### Remark

Beware that there are other notions of "dual object", distinct from this one. See for example _[[dual object in a closed category]]_, and also the discussion at _[[category with duals]]_.

=--


## In a monoidal category

### Definition

+-- {: .num_defn #DualizableObject}
###### Definition

An object $A$ in a [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ is **dualizable** if it has an [[adjunction|adjoint]] when regarded as a [[morphism]] in the one-object [[delooping]] [[bicategory]] $\mathbf{B}\mathcal{C}$ corresponding to $\mathcal{C}$.  Its adjoint in $\mathbf{B}\mathcal{C}$ is called its **dual** in $C$ and often written as $A^*$.

If $C$ is [[braided monoidal category|braided]] then left and right adjoints in $\mathbf{B}C$ are equivalent; otherwise one speaks of $A$ being **left dualizable** or **right dualizable**.  

Explicitly this means the following:

A right **[[duality]]** between objects $A, A^\ast \in (\mathcal{C}, \otimes, 1)$

consists of

1. a [[morphism]] of the form

   $$
     ev_A\;\colon\;A^\ast \otimes A \longrightarrow 1
   $$

   called the _counit_ of the duality, or the _[[evaluation]] map_;

1. a [[morphism]] of the form

   $$
     i_A \;\colon\; 1 \longrightarrow A \otimes A^\ast
   $$

   called the _unit_ or _coevaluation map_

such that

* ([[triangle identity]]) the following [[commuting diagram|diagrams commute]]

  $$
    \array{
       A^\ast \otimes (A \otimes A^\ast)
         &\overset{id_{A^\ast} \otimes i_A}{\longleftarrow}&
       A^\ast \otimes 1
       \\
       {}^{\mathllap{\alpha^{-1}_{A^\ast,A, A^\ast}}}_{\mathllap{\simeq}}\downarrow
       &&
       \downarrow^{\mathrlap{\ell^{-1}_{A^\ast} \circ r_{A^\ast}}}_{\mathrlap{\simeq}}
       \\
       (A^\ast \otimes A) \otimes A^\ast
         &\underset{ev_A \otimes id_{A^\ast}}{\longrightarrow}&
       1 \otimes A^\ast
    }
  $$

  and

  $$
    \array{
       (A \otimes A^\ast)  \otimes A
         &\overset{i_A \otimes id_A}{\longleftarrow}&
       1 \otimes A
       \\
       {}^{\mathllap{\alpha_{A,A^\ast, A}}}_{\mathllap{\simeq}}\downarrow
       &&
       \downarrow^{\mathrlap{r_A^{-1}\circ \ell_A}}_{\mathrlap{\simeq}}
       \\
       A \otimes (A^\ast \otimes A)
         &\underset{id_A \otimes ev_A}{\longrightarrow}&
       A \otimes 1
    }
  $$

  where $\alpha$ denotes the [[associator]] of the [[monoidal category]] $\mathcal{C}$, and $\ell$ and $r$ denote the left and right [[unitors]], respectively.

=--


+-- {: .num_remark}
###### Remark

Unfortunately, conventions on left and right vary and sometimes contradict their use for adjoints.  A common convention is that a *right dual* of $A$ is an object $A^*$ equipped with a **[[unit of an adjunction|unit]]** (or *[[coevaluation]]*)
$$i: I \to A \otimes A^* $$
and **counit** (or *[[evaluation]]*)
$$e : A^* \otimes A \to I $$
satisfying the '[[triangle identities]]' familiar from the concept of [[adjunction]].  With this convention, if $\otimes$ in $C$ is interpreted as composition in $\mathbf{B} C$ in [[diagrammatic order]], then right duals in $C$ are the same as right adjoints in $\mathbf{B}C$ --- whereas if $\otimes$ in $C$ is interpreted as composition in $\mathbf{B} C$ in classical 'Leibnizian' order, then right duals in $C$ are the same as *left* adjoints in $\mathbf{B} C$.

Of course, in a [[symmetric monoidal category]], there is no difference between left and right duals.

=--

+-- {: .num_remark}
###### Remark
There are various equivalent definitions of dualizability, some of which are apparently weaker than the explicit definition in terms of both unit and counit, or which assume only one of them together with a universal property for it.  However, in a few references one can find a claim that $A$ is dualizable as soon as the functor $(A\otimes -)$ has a right adjoint of the form $(A^* \otimes -)$, and this does not seem to be true; one also needs that the adjunction between these functors is preserved by tensoring with $A$.
=--

+-- {: .num_defn #InvertibleObject}
###### Definition

A dualizable object $A$, def. \ref{DualizableObject}, for which the structure unit/counit maps between $A \otimes A^\ast$ and the [[unit object]] are [[isomorphisms]] is called an _[[invertible object]]_.


=--

+-- {: .num_defn #RigidAndCompactClosed}
###### Definition

If every object of $C$ has a left and right dual, then $C$ is called a [[rigid monoidal category]] or an [[autonomous monoidal category]].  If moreover it is [[symmetric monoidal category|symmetric]], it is called a [[compact closed category]].  

=--

See [[category with duals]] for more discussion.

+-- {: .num_defn}
###### Definition

Given a [[morphism]] $f \colon X \to Y$ between two dualizable objects in a [[symmetric monoidal category]], the corresponding [[dual morphism]] 

$$
  f^\ast \colon Y^\ast \to X^\ast
$$

is the one obtained by $f$ by composing the duality unit, the counit and the [[braiding]]...


=--

### Examples
 {#Examples}

\begin{definition}
**([[finite-dimensional vector spaces]])**
\linebreak
Let $V$ be a [[finite-dimensional vector space]] over a [[field]] $k$, and let $V^* = Hom(V,k)$ be its usual [[dual vector space]].  We can define $\varepsilon\colon V^* \otimes V \to k$ to be the obvious pairing.  If we also choose a finite basis $\{v_i\}$ of $V$, and let $\{v_i^*\}$ be the [[dual basis]] of $V^*$, then we can define $\eta\colon k \to V\otimes V^*$ by sending $1$ to $\sum_i v_i \otimes v_i^*$.  It is easy to check the [[triangle identities]], so $V^*$ is a dual of $V$ in $Vect_k$.
\end{definition}


\begin{example}
**([[dualizable modules]])**
\linebreak
More generally, in the [[symmetric monoidal category]] of [[modules]] over a [[commutative ring]], dualizable objects are precisely [[finitely generated module|finitely generated]] [[projective modules]].
See at *[[dualizable module]]* for more.
\end{example}

\begin{example}
**([[Spanier-Whitehead duality]])**
\linebreak
Let $M$ be a finite-dimensional [[smooth manifold]], [[Whitney embedding theorem|choose]] an [[embedding of smooth manifolds|embedding]] $M\hookrightarrow \mathbb{R}^n$ for some $n$, and let $Th(N X)$ be the [[Thom spectrum]] of the [[normal bundle]] of this embedding.  Then the [[Thom collapse]] map defines an $\eta$ which exhibits $Th(N X)$ as a dual of $\Sigma_+^\infty M$ in the [[stable homotopy category]].  This is a version of *[[Spanier-Whitehead duality]].*
\end{example}


\begin{definition}
\label{AdjointEndofunctors}
**([[adjoint functor|adjoint]] [[endofunctors]])**
\linebreak
Given any [[category]] $\mathscr{C}$, the [[endofunctor|endo]]-[[functor category]] $End(\mathcal{C}) \,\coloneqq\, \text{Fun}(\mathscr{C},\mathscr{C})$  canonically becomes a [[monoidal category]], with [[tensor product]] given by [[composition]] of [[functors]] and [[horizontal composition]] of [[natural transformations]] (*[[whiskering]]*).

Under this identification, an object in $End(\mathcal{C})$ is dualizable iff it is an [[adjoint functor]], with [[evaluation]] and [[co-evaluation]] given by the [[counit of the adjunction]] and the [[unit of the adjunction]], respectively.
\end{definition}


\begin{example}
**([[Poincaré duality algebras]])**
\linebreak
A [[C*-algebra]] is a *[[Poincaré duality algebra]]*
if it is a dualizable object in the  [[symmetric monoidal category]] [[KK-theory|KK]] with dual its [[opposite algebra]]. 

See at _[KK-theory -- Poincare duality](KK-theory#PoincareDualityAndThomIsomorphism)_.
\end{example}

\begin{example}
For $E$ an [[E-∞ ring]], then in the [[(∞,1)-category of (∞,1)-modules]] $E Mod$ the dualizable objects coincide with the [[compact objects]] and the [[perfect objects]].

See at _[(∞,1)-category of (∞,1)-modules -- Compact generation](%28?%2C1%29-category+of+%28?%2C1%29-modules#CompactGeneration)_ for more.
\end{example}


### Properties

#### Trace

Dualizable objects support a good abstract notion of [[trace]]. (...)

#### Relation to cobordism hypothesis

Dualizable objects in an [[symmetric monoidal (∞,1)-category]] are already [[fully dualizable objects]]. The [[cobordism hypothesis]] implies that there is a canonical $O(1) \simeq \mathbb{Z}/2\mathbb{Z}$-action on the [[∞-groupoid]] of dualizable objects, and this is just the dualizing operation. See at _[cobordism hypothesis -- Framed version -- Implications: Canonical O(n)-action](cobordism+hypothesis#TheCanonicalOnAction)_.


## In a closed category

In a [[closed category]] $(\mathcal{C}, [-,-], 1)$ the dual to an object $X \in \mathcal{C}$ is defined to be the [[internal hom]] into the [[unit object]]

$$
  \mathbb{D}X \coloneqq [X,1]
  \,.
$$

## In a closed monoidal category

In a [[closed monoidal category]] $\mathbb{D}X$ is also called the _weak dual_ of $X$ (e.g. [Becker-Gottlieb, p. 5](#BeckerGottlieb)), to contrast with the monoidal dual as above, which would then be called the _strong dual_ . If the induced morphism $X \to \mathbb{D}\mathbb{D}X$ is an [[equivalence]] this weak dual is called a _reflexive weak dual_.

If $\mathcal{C}$ is a [[compact closed category]], def. \ref{RigidAndCompactClosed}, then the weak dual $\mathbb{D}X$ is also [[generalized the|the]] strong dual object $X^\ast$ to $X$ in the above monoidal sense. Here dualization exhibits $\mathcal{C}$ as a [[star-autonomous category]] ($\mathbb{D}(-) = (-)^\ast$ is the star-operation).

The property of $X$ being dualizable can be expressed as a property of the weak dual, namely that the induced map $\mathbb{D}X \otimes X \to [X,X]$ is an isomorphsim.


## In a symmetric monoidal $(\infty,n)$-category

+-- {: .num_defn}
###### Definition

An [[object]] in a [[symmetric monoidal (∞,n)-category]] $C$ is called **dualizable** if it is so as an object in the ordinary [[symmetric monoidal category|symmetric monoidal]] [[homotopy category]] $Ho(C)$.

=--

This appears as ([Lurie, def. 2.3.5](#Lurie)).


+-- {: .num_remark}
###### Remark

This means that an object in $C$ is dualizable if there exists unit and counit 1-morphism that satisfy the [[triangle identity]] up to [[homotopy]]. The definition does not demand that this homotopy is [[coherent]] (that it satisfies itself higher order relations up to higher order [[k-morphism]]s).

If the structure morphisms of the adjunction of a dualizable object _have_ themselves all adjoints, then the object is called a [[fully dualizable object]].

=--


+-- {: .num_remark}
###### Remark

As before, we may equivalently state this after [[delooping]] the monoidal structure and passing to the $(\infty,n+1)$-category $\mathbf{B}C$. Then $C$ has duals for objects precisely if $\mathbf{B}C$ has all adjoints.

=--

## In a linearly distributive category

In a [[linearly distributive category]], duality is naturally defined by mixing the two tensors $(\otimes,\top)$ and $(\parr,\bot)$: the unit is $i : \top \to A \parr A^* $ and the counit is $ev:A^* \otimes A \to \bot$.  The triangle identities make sense by inserting the linear distributivities; they assert that the following composites are identities:

$$ A \cong \top \otimes A \xrightarrow{i} (A \parr A^*) \otimes A \xrightarrow{\delta} A \parr (A^* \otimes A) \xrightarrow{ev} A \parr \bot \cong A $$

$$ A^* \cong A^* \otimes \top \xrightarrow{i} A^* \otimes (A \parr A^*) \xrightarrow{\delta} (A^* \otimes A) \parr A^* \xrightarrow{ev} \bot \parr A^* \cong A^*. $$

A symmetric linearly distributive category is (symmetric) [[star-autonomous category|star-autonomous]] if and only if all objects have duals in this sense.  The same is true in the non-symmetric case if we require both left and right duals.

This notion of duality generalizes to that of [[linear adjoints]] in a [[linear bicategory]], and also to dual objects in a [[polycategory]].


## Related concepts

* [[dualizable module]]

* [[dualizing object]]

* [[self-dual object]]

* [[fully dualizable object]]

* [[rigid monoidal category]],

* [[star-autonomous category]]

[[!include finite objects -- table]]


## References

Original articles:

* [[Harald Lindner]], _Adjunctions in monoidal categories_, manuscripta mathematica 26.1-2 (1978): 123-139. ([doi:10.1007/BF01167969](https://doi.org/10.1007/BF01167969))

* [[Pierre Deligne]], [[James Milne]]: §1 of: *Tannakian categories*,  in: *Hodge Cycles, Motives, and Shimura Varieties*, Lecture Notes in Mathematics **900**, Springer (1982) &lbrack;[doi:10.1007/978-3-540-38955-2_4](https://doi.org/10.1007/978-3-540-38955-2_4), [webpage](http://www.jmilne.org/math/xnotes/tc.html)&rbrack;

* [[Albrecht Dold]], [[Dieter Puppe]], §1 of: *Duality, Trace and Transfer*, Proceedings of the Steklov Institute of Mathematics, **154** (1984) 85–103 &lbrack;[mathnet:tm2435](http://mi.mathnet.ru/tm2435), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/doldpup2.pdf)&rbrack;

Early history with an eye towards formulating [[Becker-Gottlieb transfer]]:

* {#BeckerGottlieb} [[James Becker]], [[Daniel Gottlieb]], from p. 5. in _A History of Duality in Algebraic Topology_ &lbrack;[pdf](http://www.math.purdue.edu/~gottlieb/Bibliography/53.pdf), [[BeckerGottlieb-DualityHistory.pdf:file]]&rbrack; 

Further developments:

* [[Mark Hovey]], [[John Palmieri]], [[Neil Strickland]]: Def. 1.1.2 and Thm. 2.1.3 in: *Axiomatic stable homotopy theory*, Memoirs Amer. Math. Soc. **610** (1997) &lbrack;[ISBN:978-1-4704-0195-5](https://bookstore.ams.org/memo-128-610), [pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/axiomatic.pdf)&rbrack;

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], [[Mark Steinberger]] (with contributions by [[James McClure|J.E. McClure]]): §III.1 in: *Equivariant stable homotopy theory*, Springer Lecture Notes in Mathematics  **1213** (1986) &lbrack;[pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf), [doi:10.1007/BFb0075778](https://link.springer.com/book/10.1007/BFb0075778)&rbrack;

Review:

* [[Peter May]], §2 in: *Picard Groups, Grothendieck Rings, and Burnside Rings of Categories*, Advances in Mathematics **163** 1 (2001) 1-16 &lbrack;[pdf](http://math.uchicago.edu/~may/PAPERS/PicJan01.pdf), [doi:10.1006/aima.2001.1996](https://doi.org/10.1006/aima.2001.1996)&rbrack;
 
Further examples:

* [[Kate Ponto]] and [[Mike Shulman]], _Traces in symmetric monoidal categories_, ([arXiv:1107.6032](http://arxiv.org/abs/1107.6032))

On [[self-dual objects]] and the corresponding [[inner products]] and [[dagger-category|dagger-structure]]:

* {#Selinger12} [[Peter Selinger]], _Autonomous categories in which $A \simeq A^\ast$_, talk at QPL 2012 ([[SelingerSelfDual.pdf:file]])
 

Monoidal categories with freely adjoint duals:

*  Kevin Coulembier, [[Ross Street]], Michel van den Bergh, _Freely adjoining monoidal duals_  &lbrack;[arXiv:2004.09697](https://arxiv.org/abs/2004.09697)&rbrack;

The notion of duals in a [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-category]]:

* {#Lurie} [[Jacob Lurie]], Section 2.3  _[[On the Classification of Topological Field Theories]]_
 


[[!redirects dual object]]
[[!redirects dual objects]]

[[!redirects left dual object]]
[[!redirects left dual objects]]
[[!redirects left dual]]
[[!redirects left duals]]
[[!redirects right dual object]]
[[!redirects right dual objects]]
[[!redirects right dual]]
[[!redirects right duals]]

[[!redirects dualizable objects]]
[[!redirects dualisable object]]
[[!redirects dualisable objects]]

[[!redirects weak dual]]
[[!redirects weak duals]]

[[!redirects strong dual]]
[[!redirects strong duals]]

[[!redirects weak dual object]]
[[!redirects weak dual objects]]

[[!redirects strong dual object]]
[[!redirects strong dual object]]

[[!redirects weakly dual object]]
[[!redirects weakly dual objects]]

[[!redirects strongly dual object]]
[[!redirects strongly dual object]]

[[!redirects dual object]]
[[!redirects dual objects]]

[[!redirects dual type]]
[[!redirects dual types]]

[[!redirects dual pair]]
[[!redirects dual pairs]]
