

#Definition#

The objects of the _augmented_ [[simplex category]] $\Delta_a$ can be identified with finite sets of cardinality $0$, $1$, $2$ .... The operation of addition of natural numbers extends to the structure of a [[monoidal category]] on $\Delta$. Via [[Day convolution]] this induces a monoidal structure on the category [[SSet]] of [[simplicial set]]s. The corresponding monoidal $S \otimes S'$ product is the **join** of simplicial sets


The join forms part of a *closed* monoidal structure on the category of
augmented simplicial sets, $ASS = Sets^{\Delta_a^{op}}$. The \internal hom" is given by
$$[X; Y ]n =ASS(X; Dec^{n+1}Y ),$$
where $Dec$ is the [[decalage]] functor.




The **join** of two ordinary (not augmented) [[simplicial set]]s $S$ and $S'$ is the join of their _trivial augmentation_ ($S_{-1} = S'_{-1} = pt$). This yields

$$
  (S \star S')_n := S_n \cup S'_n \cup 
   (\cup_{i+j = n-1} S_i \times S'j)
  \,.
$$



#References#

* P. J. Ehlers and [[Tim Porter]], _Joins for (Augmented) Simplicial Sets_ ([arXiv](http://arxiv.org/abs/math.CT/9904039)) and Jour. Pure Applied Algebra, 145 (2000) 37-44.

See also [definition 1.2.8.1, p. 42](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=42) of

* J. Lurie, _Higher topos theory_ ([arXiv](http://arxiv.org/abs/math.CT/0608040))


