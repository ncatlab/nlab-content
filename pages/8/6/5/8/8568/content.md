

#Contents#
* table of contents
{:toc}

##Idea

In [[algebraic geometry]] a _geometric fiber_ is a [[fiber]] of a [[bundle]] over a [[geometric point]].

For a [[bundle]] $p: E\to X$ of [[topological spaces]], the [[fibre]] over a [[point]], $x\in X$ may be thought of as the [[preimage]] $E_x = p^{-1}(x)$ equipped with its [[subspace topology]]. More abstract, this is the [[pullback]] ${x} \times_X E$ of $p$ along the map sending a singleton space $*$ to $x \in X$, the object which is [[universal property|universal]] with the property of making this [[commuting diagram|diagram commute]]:

$$
  \array{
    E_x &\to& E
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    {*} &\stackrel{x}{\to}& X
  }
  \,.
$$

Adapting this to the algebraic context we get the following definition.

## Definition

Let $X$ be a [[scheme]] over some base field $k$.  Fix an [[algebraic closure]] $\overline{k}$ of $k$ and let $\overline{\xi} : Spec(\overline{k}) \to X$ be a [[geometric point]] in $X$.

+-- {: .num_defn }
###### Definition

For a morphism, $p: E\to X$,  the **geometric fibre** over the [[geometric point]] $x$ is the [[pullback]] 

$$
  E_x \coloneqq E \times_X Spec (\overline{k})
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

In [[EGA]], the case is also considered in which the field is replaced by a [[local ring]], (see EGA p. 112), in which case the word 'geometric' is dropped. (This needs checking.)

=--

##Example and application



An important case is where $p$ is a finite [[étale cover]], and then the geometric fibre is just a [[finite set]].



##References

* [[EGA]] I 3.4.5, p. 112.



[[!redirects geometric fibrs]]
[[!redirects geometric fiber]]
[[!redirects geometric fibers]]
