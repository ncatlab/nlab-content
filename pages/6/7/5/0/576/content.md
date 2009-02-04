#Idea#

A _dagger compact category_ is a category which is a 

* a [[compact closed category]] 

and 

* a [[dagger category]] 

in a compatible way.

#Definition#

A category $C$ which is equipped with the structure of a [[dagger category]] and of a [[compact closed category]] is **dagger compact closed** if the dagger-operation takes units of dual objects to counits in that for every object $A$ of $C$ we have
$$
  \array{
    && A \otimes A^*
    \\
    & {}^{\epsilon_A^\dagger}\nearrow
    \\
    I && \downarrow^{\sigma_{A \times A^*}}
    \\
    & {}_{\eta_A}\searrow
    \\
    && A^* \otimes A
  }
  \,.
$$

#Examples#

* For $C$ a [[cartesian monoidal category]] 
the category $Span_1(C)$ of [[span]]s in $C$ is dagger compact: the dagger operation is that of relabeling the legs of a span as source and target; every object $X$ is dual to itself with the unit and counit given by the span
$ X \stackrel{Id}{\leftarrow} X \stackrel{Id \times Id}{\to} X \times X$.
See

  * John Baez, _Spans in quantum theory_ ([web](http://math.ucr.edu/home/baez/span/), [pdf](http://math.ucr.edu/home/baez/span/span.pdf), [blog](http://golem.ph.utexas.edu/category/2007/10/spans_in_quantum_theory.html))


#References#

The concept was introduced in 

* S. Abramsky and B. Coecke, A categorical semantics of quantum protocols, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) ([arXiv](http://arxiv.org/abs/quant-ph/0402130))

See also.

* Peter Selinger, _Dagger compact closed categories and completely positive maps_ ([web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf))