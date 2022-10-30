#Definition#

A __pointed set__ is a [[set]] $S$ equipped with a chosen element $s$ of $S$. (Compare [[inhabited set]], where the element is not specified.)

Since we can identify a (set-theoretic) element of $S$ with a (category-theoretic) [[global element]] (a morphism $s: 1 \to S$), we see that a pointed set is an object of the [[under category]] $\pt \downarrow \Set$, or coslice category $1/\Set$, of objects under the [[singleton]] $\{\bullet\}$.

# The category of pointed sets

The category $Set_*$ of pointed sets is this under category or coslice category.

A morphism $(S_1, s_1) \to (S_2, s_2)$ is a map between sets which maps these chosen elements to each other, i.e., commuting triangles

$$
  \array{
    && pt
    \\
    & \swarrow && \searrow
    \\
    S_1
    &&\to&&
    S_2
  }
 \,.
$$

The category $Set_*$ naturally comes with the functor $p : Set_* \to Set$ which forgets the tip of these triangles.

#Interpretation as universal Set-bundle #

The morphism $Set_* \to Set$ is an example of a 
[[generalized universal bundle]]: the _universal [[Set]]-bundle_. 
The entire structure here can be understood as arising from the (strict) pullback diagram

$$
  \array{
    Set_* &\to& pt
    \\
    \downarrow && \downarrow^{pt \mapsto pt}
    \\
    [I,Set]
    &\stackrel{d_0}{\to}& Set
    \\
    \downarrow^{d_1}
    \\
    Sets
  }
$$

in the 1-category [[Cat]], where

* $I = \{a \to b\}$ is the [[interval category]];

* $[I, Set] = Arr(Set)$ is the [[closed monoidal category|internal hom]] category which here is the [[arrow category]] of $Set$;

* $d_i := [j_i, Set]$ are the images of the two injections 
$j_i : pt \to I$ of the point to the left and the right end of the interval, respectively -- so these functors evaluate on the left and right end of the interval, respectively;

* the square is a pullback;

* the total vertical functor is the forgetful functor $p : Set_* \to Set$.

The way in which $Set_* \to Set$ is the "universal Set-bundle" is discussed pretty explicitly in

* Kathryn Hess, _[[HessLackBundCat.pdf:file]]_ .

(The discussion there becomes more manifestly one of bundles if one regards all morphisms $C \to Set$ appearing there as being the right legs of [[anafunctor]]s. )


#Interpretation as 2-subobject-classfier#

Observing that usual morphism into the [[subobject classifier]] $\Omega$ of the [[topos]] [[Set]] is the 
[[universal truth-value bundle]] 
$\{\top\} \to \TV$, and noticing that $TV = (-1)Cat$ and $Set = 0Cat$ suggests that $Set_* \to Set$ is a [[vertical categorification|categorified]] subobject classifier:
indeed, it is the subobject classifier in the [[2-topos]] [[Cat]].

For discussion of this point see

* David Corfield: _101 things to do with a 2-classifier_ ([blog](http://golem.ph.utexas.edu/category/2008/01/101_things_to_do_with_a_2class.html))

It was David Roberts who pointed out in

* David Roberts, [comment to: 101 things to do with a 2-classifier](http://golem.ph.utexas.edu/category/2008/01/101_things_to_do_with_a_2class.html#c014559)

the relation between these higher classifiers and higher [[generalized universal bundle]]s, motivated by the observations on principal universal 1- and 2-bundles in 

* David Roberts, Urs Schreiber, _The inner automorphism 3-group of a strict 2-group_, Journal of Homotopy and Related Structures, Vol. 3(2008), No. 1, pp. 193-244, ([arXiv](http://arxiv.org/abs/0708.1741v2)).