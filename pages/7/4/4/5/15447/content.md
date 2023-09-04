
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[vector space]] is _finite-dimensional_ if it admits a [[finite set|finite]] [[basis]]: if there exists a [[natural number]] $n$ such that the vector space admits a [[linear isomorphism]] to the [[direct sum]] of $n$ copies of the [[underlying]] vector space of the [[ground field]]. 

The category [[FinDimVect]] of finite-dimensional vector spaces is of course the [[full subcategory]] of [[Vect]] whose objects are finite-dimensional. 

## Properties

### Compact closure
 {#CompactClosure}

+-- {: .num_prop}
###### Proposition

A vector space $V$ is finite-dimensional precisely if the [[hom-functor]] $\hom(V, -): Vect \to Set$ [[preserved colimit|preserves]] [[filtered colimits]]. 

=--

+-- {: .proof}
###### Proof

Every vector space $W$ is the  [[filtered colimit]] of the [[diagram]] of finite-dimensional subspaces $W' \subseteq W$ and inclusions between them; applying this to $W = V$, the condition that $\hom(V,-)$ preserves filtered colimits implies that the canonical comparison map 

$$colim_{fd\; V' \subseteq V} \hom(V, V') \to \hom(V, V)$$ 

is an [[isomorphism]], so some element $[f]$ in the colimit represented by $f: V \to V'$ gets mapped to $1_V$, i.e., $i \circ f = 1_V$ for some inclusion $i: V' \hookrightarrow V$. This implies $i$ is an isomorphism, so that $V$ is finite-dimensional. 

In the converse direction, observe that $\hom(V, -)$ has a [[right adjoint]] (and in particular preserves filtered colimits) if $V$ is finite-dimensional. 

To see this, first notice that the [[dual vector space]] $V^\ast$ of [[functionals]] $f: V \to k$ to the [[ground field]] is a [[dual object]] to $V$ in the [[monoidal category]] sense, so that there is a [[counit of an adjunction|counit]] $eva \colon V^\ast \otimes V \to k$ taking $f \otimes v \mapsto f(v)$. The [[unit of an adjunction|unit]] is uniquely determined from this counit and can be described using any basis $e_i$ of $V$ and dual basis $f_j$ as the map 

$$k \to V \otimes V^\ast$$ 

taking $1 \mapsto \sum_i e_i \otimes f_i$. We thus have an adjunction $(- \otimes_k V) \; \dashv (- \otimes V^\ast)$, which is [[mate|mated]] to an [[adjunction]] $\hom(V, -) \dashv \hom(V^\ast, -)$ by familiar hom-tensor adjunctions; thus $\hom(V, -)$ has a right adjoint. 

=--

This means that

+-- {: .num_prop}
###### Proposition

Finite-dimensional vector spaces are exactly the [[compact objects]] of [[Vect]] in the sense of [[locally presentable categories]], but also the compact = [[dualizable objects]] in the sense of [[monoidal category]] theory. In particular the category [[FinDimVect]] is a [[compact closed category]]. 

=--

## Related concepts

* [[finite-dimensional Hilbert space]]

* [[finite abelian category]]

* [[Schur functor]]

* [[finite quantum mechanics in terms of dagger-compact categories]]

## References

Discussion of finite-dimensional vector spaces as [[categorical semantics]] for [[linear logic]]/[[linear type theory]]:

* [[Benoît Valiron]], [[Steve Zdancewic]], *Finite Vector Spaces as Model of Simply-Typed Lambda-Calculi*, in: *Proc. of ICTAC'14*, Lecture Notes in Computer Science **8687**, Springer (2014) 442-459 &lbrack;[arXiv:1406.1310](https://arxiv.org/abs/1406.1310), [doi:10.1007/978-3-319-10882-7_26](https://doi.org/10.1007/978-3-319-10882-7_26), slides:[pdf](https://www.cs.bham.ac.uk/~drg/bll/steve.pdf), [[Zdancewic-LinearLogicAlgebra.pdf:file]]&rbrack;

  > (focus on [[finite field|finite]] [[ground fields]])

* {#Murfet14} [[Daniel Murfet]], *Logic and linear algebra: an introduction* &lbrack;[arXiv:1407.2650](http://arxiv.org/abs/1407.2650)&rbrack;



[[!redirects finite-dimensional vector space]]
[[!redirects finite-dimensional vector spaces]]
[[!redirects finite dimensional vector space]]
[[!redirects finite dimensional vector spaces]]
