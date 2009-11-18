
#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

For $n \in \mathbb{N}$ the category $\Theta_n$ -- **Joyal's disk category** -- may be thought of as the full subcategory of the category $Str n Cat$ of [[strict ∞-category|strict n-categories]] on $n$-categories that are something like free $n$-categories on pasting diagrams of $n$-[[globe]]s.

For instance $\Theta_2$ contains an object that is depicted

$$
  \array{
    & \nearrow &\Downarrow& \searrow &&
    && \nearrow && \searrow 
    \\
    a && \to && b &\to & c && \Downarrow && b
    \\
    & \searrow &\Downarrow& \nearrow &&
    && \searrow && \nearrow &&
  }
$$

Such pasting diagrams may be encoded in planar trees, the above one corresponds to the tree:

$$
  \array{
    \nwarrow \nearrow &  & & \uparrow &&& 2
    \\
    & \nwarrow & \uparrow & \nearrow &&& 1
    \\
    && {*} 
  }
  \,.
$$

Accordingly, $\Theta_n$ is the category of planar rooted trees of level $\leq n$.


In low degree we have

* $\Theta_0 = *$ is the [[point]].

* $\Theta_1 = \Delta$ is the [[simplex category]]: the $n$-[[simplex]] $[n]$ is thought of as a linear [[quiver]] and as such the pasing diagram of $n$ 1-morphisms

  $$
    0 \to 1 \to \cdots \to n
    \,.
  $$

  Dually, this is the planar rooted tree of the form

  $$
    \array{
      \nwarrow &\uparrow & \cdots \nearrow
      \\
      &{*}
    }
  $$

  with $n$-branches.




## Definition ##

...


### Examples ###

In $\Theta_0$ write $O_0$ for the unique object. Then write in $\Theta_n$ 

$$
  O_n := [1](O_{n-1})
  \,.
$$

This is the strict [[n-category]] free on a single $n$-[[globe]].

## Theta-spaces ##

A local [[model structure on simplicial presheaves]] on the Theta categories is called [[Theta space]]s and models [[(n,r)-category|(n,r)-categories]].


## References ##

The $\Theta$-categories were introduced in

* [[Andre Joyal]], _Disks, duality and Theta-categories_

An discussion with lots off pictures is in [chapter 7](http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf#page=131) of

* [[Eugenia Cheng]], [[Aaron Lauda]], _Higher-dimensional categories: an illustrated guidebook_ ([pdf](http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf))

A useful discussion is in

* [[Clemens Berger]], _Iterated wreath product of the simplex category and iterated loop spaces_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0512575))

and in section 3 of

* [[Charles Rezk]], _A cartesian presentation of weak $n$-categories_ ([arXiv](http://arxiv.org/abs/0901.3602))

there leading over to the notion of [[Theta space]].

[[!redirects ? category]]
[[!redirects ∞-category]]
[[!redirects Theta-category]]
[[!redirects ? categories]]
[[!redirects ∞-categories]]
[[!redirects Theta-categories]]
[[!redirects disk category]]
[[!redirects disk categories]]
