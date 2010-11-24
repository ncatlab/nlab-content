
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The **bar construction** takes a [[monad]] $(T, \mu, \epsilon)$ equipped with an algebra-over-a-monad $(A, \rho)$ to the (augmented) [[simplicial object]]

$$
  \mathrm{B}(T,A)
  :=
  \left(
    \cdots
    \stackrel{\to}{\stackrel{\to}{\to}}
    T T A
    \stackrel{\stackrel{\mu \cdot Id_A}{\to}}{\stackrel{T \cdot \rho}{\to}}
    T A \stackrel{\rho}{\to} A
  \right)
    \,.
$$

This simplicial object is a [[resolution]] of $A$.


## Properties

+-- {: .un_prop}
###### Propositioon

Regard $A$ as a constant simplicial object. The canonical morphism 

$$
  \mathrm{B}(T,A) \to A
$$

is a [[resolution]] of $A$.

In fact, the bar construction is the _universal_ resolution in the sense of 

(...)

=--

## Special cases

### For modules over an algebra

Let $A$ be a commutative [[associative algebra]]s over some [[ring]] $k$. Write $A Mod$ for the category of [[connective]] [[chain complex]]esof [[module]]s over $A$.

For $N$ a right module, also $N \otimes_k A$ is canonically a module. This construction extends to a functor

$$
  A \otimes_k (-) : 
    A Mod 
      \to 
    A Mod 
  \,.
$$

The [[monoid]]-structure on $A$ makes this a [[monad]] in [[Cat]]: the monad product and unit are given by the product and unit in $A$.

For $N$ a module its right action $\rho N \otimes A \to A$ makes the module an [[algebra over a monad|algebra over this monad]].

The bar construction $\mathrm{B}(A,N)$ is then the simplicial module

$$
  \cdots
  \stackrel{\to}{\stackrel{\to}{\to}}
  N \otimes_k A \otimes_k A \stackrel{\overset{Id \otimes \mu}{\to}}{\underset{\rho \otimes Id}{\to}} N \otimes_k A
  \,.
$$

Under the [[Moore complex]] functor of the [[Dold-Kan correspondence]] this is identified with a [[chain complex]] whose [[differential]] is given by the alternating sums of the face maps indicated above. 

This chain complex is what originally was called the **bar complex** in [[homological algebra]]. Because the first authors denoted its elements using a notation involving vertical bars ([Ginzburg](#Ginzburg))!!

This chain complex provides a resolution that computes the [[Tor]]

$$
  Tor(N, A \times A)
  \,.
$$

This gives the [[Hochschild homology]] of $A$. See there for more details.

### For differential graded (Hopf) algebras

See [[bar and cobar construction]].


## References

A general discussion of bar construction for monads is at

* [[Todd Trimble]], _On the Bar Construction_ ([blog](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html))
{#Trimble}

The bar complex of a bimodule is reviewed for instance in 

* [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603))
{#Ginzburg}

around page 16.

[[!redirects bar constructions]]

[[!redirects bar complex]]