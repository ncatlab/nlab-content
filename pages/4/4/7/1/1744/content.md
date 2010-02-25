#Contents#
* automatic table of contents goes here
{:toc}




## Definition


For $\Delta$ the [[simplex category]] write $\Delta_{\leq n}$ for its [[full subcategory]] on the objects $[0], [1], \cdots, [n]$. The inclusion $\Delta|_{\leq n} \hookrightarrow \Delta$ induces a truncation functor

$$
  tr_n : sSet = [\Delta^{op}, Set] \to [\Delta_{\leq n},Set]
$$ 

that takes a [[simplicial set]] and restricts it to its degrees $\leq n$.


This functor has a [[left adjoint]], given by left [[Kan extension]]

$$
  sk_n : [\Delta_{\leq n},Set] \to SSet
$$

called the $n$-**skeleton**

and a [[right adjoint]], given by right [[Kan extension]]

$$
  cosk_n : [\Delta_{\leq n},Set] \to SSet
$$

called the $n$-**coskeleton**.

The $n$-skeleton produces a simplicial set that is freely filled with degenerate simplices above degree $n$.

By slight abuse of notation one also writes

$$
  cosk_n : sSet \to sSet
$$

for the composite $sSet \stackrel{tr_n}{\to} [\Delta_{\leq n}] \stackrel{cosk_n}{\to} sSet$.

The $k$-coskeleton of a simplicial set $X$ is given by the formula

$$
  cosk_k X : [n] \mapsto Hom_{sSet}(sk_k \Delta^n, X)
  \,.
$$



Simplicial sets isomorphic to objects in the image of $cosk_n$ are called **coskeletal** simplicial sets.


## Properties

For $X \in $ [[sSet]], the following are equivalent:

* $X$ is $n$-coskeletal; 

* on $X$ the unit  $X \to cosk_n(X)$ of the adjunction is an [[isomorphism]];

* the map

  $$
   X_k = Hom(\Delta[k], X) \stackrel{tr_n}{\to} Hom(tr_n(\Delta[k]), tr_n(X))
  $$

  is a bijection for all $k \gt n$

* for $k \gt n$ and every morphism $\partial\Delta[k] \to X$ from the [[boundary of a simplex|boundary]] of the $k$-[[simplex]] there exists a _unique_ filler $\Delta[k] \to X$

  $$
    \array{
       \partial \Delta[k] &\to& X
       \\
       \downarrow & \nearrow
       \\
       \Delta[k]
    }
  $$

## References

* P. G. Goerss and J. F. Jardine, 1999, _Simplicial Homotopy Theory_, number 174 in Progress in Mathematics, Birkhauser. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

[[!redirects coskeletal]]
[[!redirects coskeleton]]
[[!redirects simplicial coskeleton]]