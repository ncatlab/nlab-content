
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Split essentially surjective functors
* table of contents
{: toc}

## Idea

When working with [[strict categories]] in foundations without the [[axiom of choice]], it is not true that every [[fully faithful functor|fully faithful]] and [[essentially surjective functor]] is an [[equivalence of categories]], since the mere property of being isomorphic to some object in the image is not enough to get a specific such object and isomorphism without the axiom of choice.  However, it is true if instead one uses split essentially surjective functors, where the isomorphisms are structure rather than mere property. 


## Definition

\begin{definition}
A [[functor]] $F : C \to D$ is **split essentially surjective** if there is a specified [[family]]
$$ \Big\{ (x\in C, p_y : F(x) \cong y) \Big\}_{y\in D}$$
indexed by objects $y \in D$. 
\end{definition}


## Examples

* A functor is an [[equivalence of categories]] if and only if it is fully faithful and split essentially surjective, without any use of the [[axiom of choice]].


## Properties

* Every split essentially surjective functor is [[essentially surjective]]. 

* That every essentially surjective functor is split essentially surjective is equivalent to the [[axiom of choice]].


## In homotopy type theory

In [[homotopy type theory]] (or, indeed, any dependent type theory), the definition above can be phrased for general [[precategories]] in type theoretic language: 

\begin{definition}
A [[functor]] $F : C \to D$ is **split essentially surjective** if there is a specified dependent function
$$p: \prod_{y:D} \sum_{x:C} (F(x) \cong y).$$
\end{definition}

This differs from the definition of an [[essentially surjective functor]] by the lack of [[propositional truncations]] in the definition: 

\begin{definition}
A [[functor]] $F : C \to D$ is **essentially surjective** if there is a dependent term  
$$p(y) \colon \left\Vert \sum_{x:C} (F(x) \cong y)\right\Vert$$
for all objects $y:D$. 
\end{definition}

However, for precategories, and even for [[univalent categories]], the axiom of choice is insufficient to ensure that every essentially surjective functor is split essentially surjective.  For instance, let $G$ be a nontrivial group and $BG$ the corresponding connected univalent groupoid, and $\ast$ the terminal category; then the functor $\ast \to BG$ is essentially surjective, but not split essentially surjective.


## Related concepts

* [[axiom of choice]]

[[!include properties of functors -- contents]]


## References

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)


[[!redirects split essentially surjective functor]]
[[!redirects split essentially surjective functors]]
[[!redirects split essentially surjective on objects functor]]
[[!redirects split essentially surjective on objects functors]]
[[!redirects seso functor]]
[[!redirects seso functors]]
[[!redirects split essentially surjective]]
