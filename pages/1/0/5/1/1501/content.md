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

A _rigid (monoidal) category_, also called an _autonomous (monoidal) category_ is a kind of [[category with duals]]. In particular, a rigid monoidal category is a category in which every object $A$ has a dual object $A^*$. Depending on whether these duals exist on the right or the left we call the category left or right rigid. Sometimes _rigid_ refers to categories with duals on both sides.

It is important to note that every right/left rigid category can be fully embedded into a category with duals on both sides, by repeatedly applying the double dual functor and taking a colimit (see e.g. [Selinger](#Selinger2011), Proposition 4.7).


## Definition

A [[monoidal category]] is **right rigid** (or right autonomous) if every [[object]] has a right [[dualizable object|dual]]. Similarly, a monoidal category is **left rigid** (or left autonomous) if every object has a left dual. A monoidal category is autonomous (sometimes called rigid) if duals exist on both sides.

Conventions differ regarding which type of duals are which. One convention is as follows: a _right dual_ of an object $A$ in a monoidal category $\mathscr{C}$ is an object $A^*$ equipped with evaluation/co-evaluation maps

$$\text{ev}_{A}:A\otimes A^*\to 1,\,\, \text{coev}_{A}:1\to A^*\otimes A$$

where $1$ is the tensor unit, subject to the [[triangle identities]] (snake diagrams)

$$(\text{ev}_A\otimes \text{id}_A)\circ (\text{id}_A\otimes \text{coev}_{A})=\text{id}_{A},$$

$$(\text{id}_{A^*}\otimes \text{ev}_{A})\circ ( \text{coev}_{A}\otimes \text{id}_{A^*})=\text{id}_{A^*}.$$

A left dual is an object $A^*$ paired with morphisms $\text{ev}_A:A^*\otimes A\to 1$ and $\text{coev}_A:1\to A\otimes A^*$ satisfying the dual conditions.

## Examples

The canonical example of a rigid category is the category $\text{Vec}_k$ of finite dimensional [[vector space |vector spaces]] over a field $k$. Namely, given a vector space $V$ the standard dual $V^*=\text{Hom}_k(V,k)$ serves as a categorical dual for $V$. Explicitly we have the following:

\begin{proposition} Let $k$ be a field. For every vector space $V\in \text{Vec}_k$, define the maps


$$\text{ev}_V: V\otimes V^*\to k $$
$$(v,\varphi)\mapsto \varphi(v)$$

and

$$\text{coev}_V: k\to V^*\otimes V$$
$$x\mapsto x\cdot \sum_{i\in I}\varphi_i\otimes v_i$$

where $\{v_i\}_{i\in I}$ is a basis for $V$, and $\varphi_i$ is a dual basis. That is, $\varphi_i$ is defined by

$$\varphi_i(v_j)=
\begin{cases}
1 & i=j\\
0 & \text{otherwise}.
\end{cases}$$

These formulas give well defined $\text{Vec}_k$-morphisms. Moreover, the satisfy the snake identities and hence give $\text{Vec}_k$ the structure of a (right) rigid category.
\end{proposition}

\begin{proof} To begin, we verify that the definition of $\text{coev}$ is independent of basis. Suppose $\{\tilde{v}_i\}_{i\in I}$ is a different choice of basis. There is a change of basis matrix $c=(c_{i,j})_{(i,j)\in I\times I}$ between them. It is straightforward to see that the dual bases are related by the change of basis matrix $c^{-1}$. Expanding, we thus find that


$$\sum_{i}\tilde{v}_i\otimes \tilde{\varphi}_i=\sum_{i}\left(\sum_{j}c_{i,j}\cdot v_i\right)\otimes \left(\sum_{k}(c^{-1})_{k,i}\cdot \varphi_i\right)$$

$$=\sum_{j,k} \left(\sum_{i}c_{i,j}(c^{-1})_{k,i}\right)\cdot v_i\otimes \varphi_i.$$

The definition of the inverse matrix says that $\sum_{i}c_{i,j}(c^{-1})_{k,i}=\begin{cases}1 & j=k \\ 0 &\text{otherwise}\end{cases}$. Hence, we conclude that

$$\sum_{i}\tilde{v}_i\otimes \tilde{\varphi}_i=\sum_{i}v_i\otimes \varphi_i,$$

so $\coev_{V}$ is well defined as desired. We now show that the rigidity diagrams commute. Going around the square, we find that this is equivalent to the condition that $1\otimes w=\sum_{i}\varphi_i(w)\otimes v_i$ for all $w\in V$. This follows from choosing a basis such that $v_i=w$ for some $i$. Then, $\varphi_i(w)\otimes v_i=w$ and all the other terms are zero, making the equality obvious.
\end{proof}

Another key example is that of endofunctor categories. Given any category $\mathscr{C}$, the hom-space of functors $\text{Fun}(\mathscr{C},\mathscr{C})$ is a monoidal category, with the monoidal structure coming from composition. Duals correspond to [[adjoint functor]] as can be stated formally below:

\begin{proposition} Let $\mathscr{C}$ be a category, and let $F\in \text{Fun}(\mathscr{C},\mathscr{C})$ be an endofunctor. Let $F^*$ be the right adjoint of $F$. $F^*$ is a right dual for $F$, under the natural transformations

$$\text{ev}_{F}:F\otimes F^*\to \text{id}_{\mathscr{C}}$$

$$F(F^*(A))\xrightarrow{\text{id}_{F^*(A)}} A,\,\, A\in \mathscr{C}$$

where we here make the implicit identification

$$\text{Hom}_{\mathscr{C}}(F(F^*(A)),A)\cong\text{Hom}_{\mathscr{C}}(F^*(A),F^*(A))$$

using adjointness, and

$$\text{coev}_{F}:\text{id}_{\mathscr{C}}\to F\otimes F^*$$

$$A\xrightarrow{\text{id}_{F(A)}} F^*(F(A)),\,\, A\in \mathscr{C}$$

where we here make the implicit identification

$$\text{Hom}_{\mathscr{C}}(A,F^*(F(A)))\cong\text{Hom}_{\mathscr{C}}(F(A),F(A))$$

using adjointness. Conversely, if $F^*$ is a right dual for an endofunctor $F$ then $F^*$ is a right adjoint for $F$.
\end{proposition}
\begin{proof} Verifying the details is straightforward.
\end{proof}

## Graphical language

Rigid categories are best expressed using the language of [[string diagrams]]. That is, we can write the rigidity axioms as

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

Rigidity is thus graphically the statement that string diagrams can be "straightened out". This approach is taken, for example, in [Selinger](#Selinger2011).


## Remarks

Note that this definition only asserts the existence of the dual objects. It does _not_ assert that specific duals have been chosen. However, the choice of duals is unique up to unique isomorphism, justifying reference to '[[the]]' dual of an object; in fact, this extends to a [[contravariant functor|contravariant]] [[anafunctor]] ${}^*\colon M \to M$.  (Using the [[axiom of choice]] to pick duals for every object at once, we can make this into a [[strict functor]].) This functor is defined explicitly by the formula

$$f^*:A^*\xrightarrow{\text{coev}_B\otimes \text{id}_{A^*}} B^*\otimes B\otimes A^*\xrightarrow{\text{id}_{B^*}\otimes f\otimes \id_{A^*}} B^*\otimes A\otimes A^* \xrightarrow{\text{id}_{B^*}\otimes \text{ev}_A} B^*$$

This formula is clearer when written graphically:

\begin{imagefromfile}
"file_name": "duals-graphical.png",
"width": 150,
"unit": "px"
\end{imagefromfile}


Additionally, this definition does not assert that the right dual of an object is isomorphic to its left dual: this need not be the case in general, though it is true in a [[braided monoidal category]], and thus automatically also in a [[symmetric monoidal category]] (this last fact can be considered an algebraic form of the "Whitney trick" for knots; see this [MO discussion](http://mathoverflow.net/questions/162677/why-is-a-braided-left-autonomous-category-also-right-autonomous/162693#162693)). Left duals and right duals are also isomorphic in a [[semisimple category]]. Note that a rigid monoidal category which is also symmetric is sometimes called [[compact closed category|compact closed]], or simply "compact".

In practice, algebraic geometers are the most frequent users of the term 'rigid', and they focus on the symmetric monoidal case, so they ignore the difference between right and left duals.

## Properties

### Tannaka duality 

The statement of [[Tannaka duality]] for associative algebras says that rigid monoidal categories equipped with a [[fiber functor]] are [[categories of modules]] over a [[Hopf algebra]].

[[!include structure on algebras and their module categories - table]]


### Free rigid monoidal categories

The inclusion of the 2-category of monoidal categories into the 2-category
of rigid monoidal categories admits a left [[2-adjoint functor]] $L$.

Furthermore, the unit of the adjunction is a strong monoidal [[fully faithful functor]], i.e., any monoidal category $C$ admits
a fully faithful strong monoidal functor $C\to L(C)$,
where $L(C)$ is a rigid monoidal category.

See Theorems 1 and 2 in [Delpeuch](#Delpeuch).

## References

* N. Saavedra Rivano, "Cat&#233;gories Tannakiennes." _Bulletin de la Soci&#233;t&#233; Math&#233;matique de France_ 100 (1972): 417-430. [EuDML](https://eudml.org/doc/87193)

* {#Delpeuch} [[Antonin Delpeuch]], _Autonomization of monoidal categories_, [arXiv](https://arxiv.org/abs/1411.3827), [doi](https://dx.doi.org/10.4204/EPTCS.323.3).

* {#Selinger2011} [[Peter Selinger]], _A survey of graphical languages for monoidal categories_, New structures for physics, [arXiv](https://arxiv.org/abs/0908.3347)

## Related concepts

* [[star-autonomous category]]

* [[(∞,n)-category with duals]]

* [[linguistics|natural language syntax]]

* [[pregroup grammar]]

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
