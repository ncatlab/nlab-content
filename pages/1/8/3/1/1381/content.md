<div class="rightHandSide toc">
[[!include higher category theory - contents]]

***

[[!include higher algebra - contents]]

</div>


#Idea#

A _symmetric monoidal $(\infty,1)$-category_ is 

* an [[(infinity,1)-category]]

* which is "$\infty$-[[k-tuply monoidal n-category|tuply monoidal]]", or "stably monoidal".

This means that it is

* a [[monoidal (infinity,1)-category]];

* for which the [[tensor product]] is commutative up to infinite coherent homotopy.


#Definition#

## in terms of quasi-categories ##

Recall that in terms of [[quasi-category|quasi-categories]] a general [[monoidal (infinity,1)-category]] is conceived as a coCartesian fibration $C^\otimes \to N(\Delta)^{op}$ of [[simplicial set]]s over the ([[opposite category|opposite]] of) the [[nerve]]  $N(\Delta)^{op}$ of the [[simplex category]] satisfying a certain property. 

The fiber of this fibration over the 1-[[simplex]] $[1]$ is the [[monoidal (infinity,1)-category]] $C$ itself, its value over a map $[n] \to [1]$ encodes the tensor product of $n$ factors of $C$ with itself.

The following definition encodes the _commutativity_ of all these operations by replacing $\Delta$ with the category $FinSet_*$ of pointed finite sets.

+-- {: .un_defn}
###### Definition
A **symmetric monoidal $(\infty,1)$-category** is a coCartesian fibration of [[simplicial set]]s 

$$
  p : C^\otimes \to N(FinSet_*)
$$

such that

* for each $n \geq 0$  the associated functors $C^\otimes_{[n]} \to C^\otimes_{[1]}$ determine an equivalence of $(\infty,1)$-categories $C^\otimes_{[n]} \stackrel{\simeq}{\to} C_{[1]}^n$.

=--

+-- {: .un_prop}
###### Proposition

  The [[homotopy category of an (infinity,1)-category|homotopy category]] of a symmetric monoidal $(\infty,1)$-category is an ordinary [[symmetric monoidal category]].

=--


###Remarks###

* There is a functor $\varphi : \Delta^{op} \to FinSet_*$ such that the [[monoidal (infinity,1)-category]] _underlying_ a symmetric monoidal $(\infty,1)$-category $p : C^\otimes \to N(FinSet_*)$ is the [[(infinity,1)-pullback]] of $p$ along $\varphi$.

#Examples#

* [[stable (infinity,1)-category of spectra]]

* [[symmetric monoidal (infinity,1)-category of presentable (infinity,1)-categories]]

#References#

The defintion of symmetric monoidal quasi-category is definition 1.2 in 

* [[Jacob Lurie]], [[higher algebra|Commutative algebra]]

[[!redirects symmetric monoidal (infinity,1)-categories]]
[[!redirects symmetric monoidal (∞,1)-category]]
[[!redirects symmetric monoidal (∞,1)-categories]]