
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _$\dagger$-compact category_ is a category which is a 

* [[compact closed category]] 

and a

* [[symmetric monoidal †-category]] 

in a compatible way.  So, notably, it is a [[monoidal category]] in which

* every object has a dual;

* every morphism has an $\dagger$-adjoint.

(Hence a $\dagger$-compact category is similar in flavor to an $(\infty,2)$-category with all adjoints in the sense of _[[On the Classification of Topological Field Theories]]_ .)


## Definition

A category $C$ that is equipped with the structure of a [[symmetric monoidal †-category]] and is [[compact closed category|compact closed]] is **$\dagger$-compact** if the dagger-operation takes [[units]] of [[dual objects]] to [[counits]] in that for every object $A$ of $C$ we have

$$
  \array{
    && A \otimes A^*
    \\
    & {}^{\epsilon_A^\dagger}\nearrow
    \\
    I && \downarrow^{\mathrlap{\sigma_{A \times A^*}}}
    \\
    & {}_{\eta_A}\searrow
    \\
    && A^* \otimes A
  }
  \,.
$$


## Examples

* For $C$ a category with [[finite limits]]  the category $Span_1(C)$ whose morphisms are [[span|spans]] in $C$ is $\dagger$-compact.  The $\dagger$ operation is that of relabeling the legs of a span as source and target.  The tensor product is defined using the cartesian product in $C$.   Every object $X$ is dual to itself with the unit and counit given by the span
$ X \stackrel{Id}{\leftarrow} X \stackrel{Id \times Id}{\to} X \times X$.
See

  * John Baez, _Spans in quantum theory_ ([web](http://math.ucr.edu/home/baez/span/), [pdf](http://math.ucr.edu/home/baez/span/span.pdf), [blog](http://golem.ph.utexas.edu/category/2007/10/spans_in_quantum_theory.html))


## Finite quantum mechanics in terms of $\dagger$-compact categories

The finite parts of [[quantum mechanics]] and [[quantum computation]] are naturally formulated as the theory of $\dagger$-compact categories.

For more on this see at _[[finite quantum mechanics in terms of †-compact categories]]_.


## Relation to Hilbert spaces

The category of [[Hilbert spaces]] (over the [[complex numbers]]) with [[finite number|finite]] [[dimension]] is a standard example of a $\dagger$-compact category.  This example is [[completeness theorem|complete]] for [[equation]]s in the language of $\dagger$-compact categories; see [Selinger 2012](#Selinger2012).


## References

The concept was introduced in 

* [[Samson Abramsky]], [[Bob Coecke]], _A categorical semantics of quantum protocols_, in _Proceedings of the 19th IEEE conference on Logic in Computer Science_ (LiCS'04), IEEE Computer Science Press, 2004. ([arXiv](http://arxiv.org/abs/quant-ph/0402130))
 {#AbramskyCoecke04}

See also:

* [[Peter Selinger]] (2007), Dagger compact closed categories and completely positive maps, in _Proceedings of the 3rd International Workshop on Quantum Programming Languages_ (QPL 2005), ENTCS 170 (2007), 139--163. 
([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))

For completeness of finite-dimensional Hilbert spaces:

*  [[Peter Selinger]] (2012), Finite dimensional Hilbert spaces are complete for dagger compact closed categories, [arXiv](http://arxiv.org/abs/1207.6972).
   {#Selinger2012}


[[!redirects dagger compact category]]
[[!redirects dagger compact categories]]
[[!redirects dagger-compact category]]
[[!redirects dagger-compact categories]]
[[!redirects † compact category]]
[[!redirects † compact categories]]
[[!redirects †-compact category]]
[[!redirects †-compact categories]]

[[!redirects dagger compact closed category]]
[[!redirects dagger compact closed categories]]
[[!redirects dagger-compact closed category]]
[[!redirects dagger-compact closed categories]]
[[!redirects † compact closed category]]
[[!redirects † compact closed categories]]
[[!redirects †-compact closed category]]
[[!redirects †-compact closed categories]]
