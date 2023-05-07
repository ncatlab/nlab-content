+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _rigid (monoidal) category_, also called an _autonomous (monoidal) category_ is a kind of [[category with duals]]. In particular, a rigid monoidal category is a category in which every [[object]] $A$ has a [[dual object]] $A^*$. Depending on whether these duals exist on the right or the left we call the category left or right rigid. Sometimes _rigid_ refers to categories with duals on both sides.


## Definition

### In components

A [[monoidal category]] is **right rigid** (or *right autonomous*) if every [[object]] has a right [[dualizable object|dual]]. Similarly, a monoidal category is **left rigid** (or left autonomous) if every object has a left dual. A monoidal category is *autonomous* (sometimes called rigid) if duals exist on both sides.

Conventions differ regarding which type of duals are which. One convention is as follows: a _right dual_ of an object $A$ in a monoidal category $\mathscr{C}$ is an object $A^*$ equipped with [[evaluation]]/[[co-evaluation maps]]

$$
  \text{ev}_{A}
  \,\colon\,
  A\otimes A^*\to 1,\,\, 
 \text{coev}_{A}:1\to A^*\otimes A
$$

where $1$ is the [[tensor unit]], subject the the [[triangle identities]] (snake diagrams)

$$(\text{ev}_A\otimes \text{id}_A)\circ (\text{id}_A\otimes \text{coev}_{A})=\text{id}_{A},$$

$$(\text{id}_{A^*}\otimes \text{ev}_{A})\circ ( \text{coev}_{A}\otimes \text{id}_{A^*})=\text{id}_{A^*}.$$

A left dual is an object $A^*$ paired with morphisms $\text{ev}_A:A^*\otimes A\to 1$ and $\text{coev}_A:1\to A\otimes A^*$ satisfying the dual conditions.


### Via string diagrams
 {#DefiinitionViaStringDiagrams}

This definition are best expressed using the language of [[string diagrams]] for [[monoidal categories]], where the rigidity axioms look as follows:

\begin{imagefromfile}
"file_name": "string-naive.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

Even better, we often fix graphical notation for $\text{ev}$ and $\text{coev}$ which makes these axioms even simpler to write out:

\begin{imagefromfile}
"file_name": "string-notation-rigidity.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

We can now express rigidity as follows:

\begin{imagefromfile}
"file_name": "string-better.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

Rigidity is thus graphically the statement that [[string diagrams]] can be "straightened out". This approach is taken, for example, in [Selinger (2011)](#Selinger2011).

### Remarks

Note that this definition only asserts the existence of the [[dual objects]]. It does _not_ assert that specific duals have been chosen. However, the choice of duals is unique up to unique [[isomorphism]], justifying reference to '[[the]]' dual of an object; in fact, this extends to a [[contravariant functor|contravariant]] [[anafunctor]] ${}^*\colon M \to M$.  (Using the [[axiom of choice]] to pick duals for every object at once, we can make this into a [[strict functor]].) This functor is defined explicitly by the formula

$$
  f^*
  \,\colon\, 
  A^*\xrightarrow{\text{coev}_B\otimes \text{id}_{A^*}} B^*\otimes B\otimes A^*\xrightarrow{\text{id}_{B^*}\otimes f\otimes \id_{A^*}} B^*\otimes A\otimes A^* \xrightarrow{\text{id}_{B^*}\otimes \text{ev}_A} B^*
$$

This formula is clearer in its [[string diagram]]-form

\begin{imagefromfile}
"file_name": "duals-graphical.png",
"width": 150,
"unit": "px"
\end{imagefromfile}

Additionally, the above definition does not assert that the right dual of an object is isomorphic to its left dual: this need not be the case in general, though it is true in a [[braided monoidal category]], and thus automatically also in a [[symmetric monoidal category]] (this last fact can be considered an algebraic form of the "Whitney trick" for knots; see this [MO discussion](http://mathoverflow.net/questions/162677/why-is-a-braided-left-autonomous-category-also-right-autonomous/162693#162693)). 

Left duals and right duals are also isomorphic in a [[semisimple category]]. Note that a rigid monoidal category which is also symmetric is sometimes called [[compact closed category|compact closed]], or simply "compact".

In practice, [[algebraic geometry|algebraic geometers]] are the most frequent users of the term 'rigid', and they focus on the [[symmetric monoidal category|symmetric monoidal]] case, so they ignore the difference between right and left duals.



## Examples
 {#Examples}

### Finite-dimensional vector spaces
 {#FiniteDimensionalVectorSpaces}

The canonical example of a rigid category is the category [[FinDimVect|$FinDimVect_k$]] of [[finite dimensional vector spaces]] over a [[field]] $k$. Namely, given a [[finite-dimensional vector space]] $V$, its [[dual vector space]] inthe sense of [[linear algebra]], $V^* \coloneqq\text{Hom}_k(V,k)$, constitutes its [[dual object]] in the [[category]] [[FinDimVect]]. Explicitely we have the following:

\begin{proposition} Let $k$ be a [[field]]. For every $V\in FinDimVect_k$, define the maps


$$\text{ev}_V: V\otimes V^*\to k $$
$$(v,\varphi)\mapsto \varphi(v)$$

and

$$\text{coev}_V \colon k\to V^*\otimes V$$
$$x\mapsto x\cdot \sum_{i\in I}\varphi_i\otimes v_i$$

where $\{v_i\}_{i\in I}$ is a basis for $V$, and $\varphi_i$ is a dual basis. That is, $\varphi_i$ is defined by

$$\varphi_i(v_j)=
\begin{cases}
1 & i=j\\
0 & \text{otherwise}.
\end{cases}$$

These formulas give well defined $\text{Vec}_k$-morphisms. Moreover, the satisfy the [[triangle identities]] and hence give $\text{Vec}_k$ the structure of a (right) rigid category.
\end{proposition}

\begin{proof} To begin, we verify that the definition of $\text{coev}$ is independent of basis. Suppose $\{\tilde{v}_i\}_{i\in I}$ is a different choice of basis. There is a change of basis matrix $c=(c_{i,j})_{(i,j)\in I\times I}$ between them. It is straightforward to see that the dual bases are related by the change of basis matrix $c^{-1}$. Expanding, we thus find that


$$\sum_{i}\tilde{v}_i\otimes \tilde{\varphi}_i=\sum_{i}\left(\sum_{j}c_{i,j}\cdot v_i\right)\otimes \left(\sum_{k}(c^{-1})_{k,i}\cdot \varphi_i\right)$$

$$=\sum_{j,k} \left(\sum_{i}c_{i,j}(c^{-1})_{k,i}\right)\cdot v_i\otimes \varphi_i.$$

The definition of the inverse matrix says that $\sum_{i}c_{i,j}(c^{-1})_{k,i}=\begin{cases}1 & j=k \\ 0 &\text{otherwise}\end{cases}$. Hence, we conclude that

$$\sum_{i}\tilde{v}_i\otimes \tilde{\varphi}_i=\sum_{i}v_i\otimes \varphi_i,$$

so $\coev_{V}$ is well defined as desired. We now show that the rigidity diagrams commute. Going around the square, we find that this is equivalent to the condition that $1\otimes w=\sum_{i}\varphi_i(w)\otimes v_i$ for all $w\in V$. This follows from choosing a basis such that $v_i=w$ for some $i$. Then, $\varphi_i(w)\otimes v_i=w$ and all the other terms are zero, making the equality obvious.
\end{proof}


## Properties

### Tannaka duality 

The statement of [[Tannaka duality]] for associative algebras says that rigid monoidal categories equipped with a [[fiber functor]] are [[categories of modules]] over a [[Hopf algebra]].

[[!include structure on algebras and their module categories - table]]


### Free rigid monoidal categories
 {#FreeRigidMonoidalCategories}

The inclusion of the [[full sub-2-category]] of rigid monoidal categories into the [[2-category]] [[MonCat]] of [[monoidal categories]] a [[left adjoint|left]] [[adjoint 2-functor]] $L$, making it a [[reflective sub-2-category]] with reflector a [[free construction]] of rigid monoidal structure from any [[monoidal category]].

Furthermore, the [[unit of the adjunction]] is a [[strong monoidal functor|strong monoidal]] [[fully faithful functor]].

This means thatany [[monoidal category]] $C$ admits
a [[fully faithful functor|fully faithful]] [[strong monoidal functor]] $C\to L(C)$ into a rigid monoidal category.

This is [Delpeuch (2020), Thm. 1 & 2](#Delpeuch).


## Related concepts

* [[star-autonomous category]]

* [[(∞,n)-category with duals]]

* [[linguistics|natural language syntax]]


## References
 {#References}

* N. Saavedra Rivano, "Cat&#233;gories Tannakiennes." _Bulletin de la Soci&#233;t&#233; Math&#233;matique de France_ 100 (1972): 417-430. [EuDML](https://eudml.org/doc/87193)

* {#Selinger2011} [[Peter Selinger]], _A survey of graphical languages for monoidal categories_, New structures for physics, [arXiv](https://arxiv.org/abs/0908.3347)

* {#Delpeuch2020} [[Antonin Delpeuch]], *Autonomization of monoidal categories*, EPTCS 323 (2020) 24-43 &lbrack;[arXiv:1411.3827](https://arxiv.org/abs/1411.3827), [doi:10.4204/EPTCS.323.3](https://dx.doi.org/10.4204/EPTCS.323.3)&rbrack;




[[!redirects rigid monoidal category]]
[[!redirects rigid monoidal categories]]
[[!redirects rigid category]]
[[!redirects rigid categories]]
[[!redirects autonomous monoidal category]]
[[!redirects autonomous monoidal categories]]
[[!redirects autonomous category]]
[[!redirects autonomous categories]]
[[!redirects left autonomous monoidal category]]
[[!redirects left autonomous monoidal categories]]
[[!redirects left autonomous category]]
[[!redirects left autonomous categories]]
[[!redirects right autonomous monoidal category]]
[[!redirects right autonomous monoidal categories]]
[[!redirects right autonomous category]]
[[!redirects right autonomous categories]]
