
This entry is about the article


* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_, Advances in Mathematics __164__, 144&#8211;176 (2001) ([arXiv:math/0007070](http://arxiv.org/abs/math/0007070))

  **Abstract** _Given a small category $C$, we show that there is a universal way of expanding $C$ into a model category, essentially by formally adjoining homotopy colimits. The technique of localization becomes a method for imposing "relations" into these universal gadgets. The paper develops this formalism and discusses various applications, for instance to the study of homotopy colimits, the Dwyer-Kan theory of framings, and to the homotopy theory of schemes._


The article discusses the _projective_ global and local [[model structure on simplicial presheaves]]. 

The general discussion is in parts is based on the unfinished but useful notes

* Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))



In particular this 

* shows that and how the projective model structure on simplicial presheaves on $C$ is something like the free completion of $C$ under [[homotopy colimit]]s. This is the model-category theoretic analog of the fact that the [[(∞,1)-category of (∞,1)-presheaves]] on $C$ is the  
  [[free (∞,1)-cocompletion]] of $C$;


* announces the statement of **[Dugger's theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem)** which states that every [[combinatorial model category]] arises as the [[Bousfield localization of model categories|left Bousfield localization]] of the projective [[global model structure on simplicial presheaves]]. The full proof of this is in the companion article

  * Daniel Dugger, _[[Combinatorial model categories have presentations]]_ 

* discusses [cofibrant replacement in the projective model structures](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#FibAndCofibObjects) (necessarily both for the global as well as for the local structure)

* discusses _geometric realization_ of $\infty$-stacks on [[Diff]] essentially by using the geometric homotopy $\infty$-groupoid functor as disscussed at [[homotopy groups in an (∞,1)-topos]].


## Free $(\infty,1)$-cocompletion

The main theorem of the article is the following. For more details see [[(∞,1)-category of (∞,1)-presheaves]].

+-- {: .un_def}
###### Definition

Let $A$ and $B$ be [[model categories]], $D$ a plain [[category]] and

$$
  \array{
    D &\stackrel{r}{\to}& A
    \\
    & \searrow_\gamma 
    \\
    && B
  }
$$

two plain [[functor]]s. Say that a **model-category theoretic factorization** of $\gamma$ through $A$ is 

1. a [[Quillen adjunction]] $(L \dashv R) : A \stackrel{\overset{L}{\to}}{\underset{R}{\leftarrow}} B$

1. a [[natural transformation|natural]] weak equivalence $\eta  : L \circ r \to \gamma$

   $$
     \array{
       D &&\stackrel{r}{\to}&& A
       \\
       & \searrow_\gamma &{}^\eta\swArrow& \swarrow_{L}
       \\
       && B
     }
     \,.
   $$

Let the [[category]] of such factorizations have morphisms $((L \dashv R), \eta ) \to ((L' \dashv R'), \eta' )$ given by [[natural transformation]]s $L \to L'$ such that for all all objects $d \in D$ the diagrams

$$
  \array{
     L\circ r(d) &&\to&& L'\circ r(d)
     \\
     & {}_{\eta_{d}}\searrow && \swarrow_{\eta'_{d}}
     \\
     &&
     \gamma()
  }
$$

commutes.

=--

Notice that the [[(∞,1)-category]] presented by a [[model category]] -- at least by a [[combinatorial model category]] -- has all [[limit in a quasi-category|(∞,1)-categorical colimits]], and that the Quillen left adjoint functor $L$ presents, via its [[derived functor]], a left [[adjoint (∞,1)-functor]] that preserves $(\infty,1)$-categorical colimits. So the notion of factorization as above is really about factorizations through colimit-preserving $(\infty,1)$-functors into $(\infty,1)$-categories that have all colimits.

+-- {: .un_theorem}
###### Theorem
**(model category presentation of free $(\infty,1)$-cocompletion)**

For $C$ a [[small category]], the projective global [[model structure on simplicial presheaves]] $[C^{op}, sSet]_{proj}$ on $C$ is universal with respect to such factorizations of functors out of $C$:

every functor $C \to B$ to any [[model category]] $B$ has a factorization through $[C^{op}, sSet]_{proj}$ as above, and the category of such factorizations is [[contractible]].

=--

+-- {: .proof}
###### Proof

This is theorem 1.1 in the article.

=--




category: reference

[[!redirects Universal homotopy theories]]