
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

> This entry is about the notion of (co)skeleta of simplicial sets. For the notion of skeleton of a category see [[skeleton]].

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

$$
  ( sk_n \dashv tr_n \dashv cosk_n) \;\;
   :
   \;\;
   sSet_{\leq n}
   \stackrel{\overset{sk_n}{\to}}{\stackrel{\overset{tr_n}{\leftarrow}}{\underset{cosk_n}{\to}}}
   sSet
  \,.
$$


The $n$-skeleton produces a simplicial set that is freely filled with degenerate simplices above degree $n$.



Write

$$
  \mathbf{sk}_n := sk_n \circ tr_n: sSet \to sSet
$$

and

$$
  \mathbf{cosk}_n := cosk_n \circ tr_n: sSet \to sSet
$$

for the composite functors. Often by slight abuse of notation we suppress the boldface and just write $sk_n : sSet \to sSet$ and $cosk_n : sSet \to sSet$.

these in turn form an [[adjunction]]

$$
  ( \mathbf{sk}_n \dashv \mathbf{cosk}_n)
  \;\;
  :
  \;\;
  sSet
  \stackrel{\leftarrow}{\to}
  sSet
  \,.
$$

So the $k$-coskeleton of a simplicial set $X$ is given by the formula

$$
  \mathbf{cosk}_k X : [n] \mapsto Hom_{sSet}(\mathbf{sk}_k \Delta[n], X)
  \,.
$$


Simplicial sets isomorphic to objects in the image of $cosk_n$ are called **coskeletal** simplicial sets.


## Properties {#Properties}

### General

+-- {: .un_prop}
###### Proposition


For $X \in $ [[sSet]], the following are equivalent:

* $X$ is $n$-coskeletal; 

* on $X$ the unit  $X \to \mathbf{cosk}_n(X)$ of the adjunction is an [[isomorphism]];

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

=--

+-- {: .un_remark}
###### Remark

So in particular if $X$ is an $n$-coskeletal [[Kan complex]], all its [[simplicial homotopy group]]s above degree $(n-1)$ are trivial.

=--





### Truncation and Postnikov towers {#Truncation}

+-- {: .un_prop}
###### Proposition

For each $n \in \mathbb{N}$, the unit of the adjunction

$$
  X \to \mathbf{cosk}_n(X)
$$

induces an [[isomorphism]] on all [[simplicial homotopy group]]s in degree $\lt n$.

=--


It follows from the above that for $X$ a [[Kan complex]], the sequence

$$
  X = \lim_n cosk_n X \to \cdots \to cosk_{n+1} X \to cosk_{n} X \to \cdots \to *
$$

is a [[Postnikov tower]] for $X$.

See also the discussion on [p. 140, 141](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf#page=3) of [DwKan1984](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf). 

For the interpretation of this in terms of  [[(n,1)-topos]]es inside the [[(∞,1)-topos]] [[∞Grpd]] see [[n-truncated object in an (∞,1)-category]], example <a href="http://ncatlab.org/nlab/show/n-truncated+object+of+an+(infinity%2C1)-category#InInfGrpd">In ∞Grpd and Top</a>.


## Examples

* The [[nerve]] of a [[category]] is a 2-coskeletal simplicial set.

* A [[Kan complex]] that is $(n+1)$-coskeletal is equivalent to (the [[nerve]] of) an [[n-groupoid]].

* A 0-coskeletal simplicial set $X$ is (-1)-[[truncated]] and hence either empty or a [[contractible]] [[Kan complex]] , $X \stackrel{\simeq}{\to} *$ that is the [[nerve]] $X = N(C)$ of a [[groupoid]] $C$ that has a [[equivalence of categories]] $C \simeq *$.






## References

A standard textbook reference is

* P. G. Goerss and J. F. Jardine, 1999, _Simplicial Homotopy Theory_, number 174 in Progress in Mathematics, Birkh&#228;user. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

A classical article that amplifies the connection of the coskeleton operation to [[Postnikov tower]]s is

* [[William Dwyer]], [[Dan Kan]], _An obstruction theory for diagrams of simplicial sets_ ([pdf](http://www.nd.edu/~wgd/Dvi/ObstructionTheoryForDiagrams.pdf))


[[!redirects coskeletal]]
[[!redirects coskeleton]]
[[!redirects simplicial coskeleton]]