
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Just like [[parametric right adjoint]] functors are a generalization of [[polynomial functors]], **familial** 2-monad are a generalization of [[polynomial 2-monad|polynomial 2-monads]] with applications to higher category theory ([Weber '07](#Weber07) and [Shapiro '21](#Shapiro21)).

### Definition

The following is Definition 5.2 in [Weber '07](#Weber07).

\begin{definition}
Let $T : \mathcal{A} \to \mathcal{B}$ be a 2-functor between finitely complete [[2-categories]]. Then $T$ is **familial** when it is [[parametric right adjoint|p.r.a]] and the 2-functor
$$
T_1 : \mathcal{A} \to \mathcal{B}/T1
$$
factors through $U_{T1} : \mathrm{Spl}(T1) \to \mathcal{B}/T1$, where $\mathrm{Spl}(T1)$ are [[split fibrations]] over $T1$.

A 2-monad is **familial** when its underlying 2-functor is familial, and its unit and multiplication are [[cartesian natural transformation|cartesian]].
\end{definition}

## See also

* [[operad]]
* [[parametric right adjoint]]

## References

The concept is defined in 

* {#Weber07} [[Mark Weber]], _Familial 2-functors and parametric right adjoints_, Theory Appl. Categ. 18 (2007), No. 22, 665–732, ([tac](http://www.tac.mta.ca/tac/volumes/18/22/18-22abs.html)))

As a way to encode the shape of higher categories:

* {#Shapiro21} [[Brandon Shapiro]], _Familial Monads as Higher Category Theories_ ([arXiv:2111.14796](https://arxiv.org/abs/2111.14796))