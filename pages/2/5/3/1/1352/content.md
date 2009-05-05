#Idea#

A _stratified simplicial set_ is a [[simplicial set]] equipped with information about which of its [[simplex|simplices]] are to be regarded as being _[[thin element|thin]]_ in that they are like identies or at least like equivalences in a [[higher category theory|higher category]].

The theory of [[simplicial weak omega-category|simplicial weak omega-categories]] is based on stratified simplicial sets.

# Definition #

A **stratification** of a [[simplicial set]] $X : \Delta^{op} \to Set$ is a subset $t X \subset \coprod_{[n]} X_n$ of its set of simplices (not in general a simplicial subset!) such that

* no 0-simplex of $X$ is in $t X$;

* every degenerate simplex in $X$ is in $t X$.

A **stratified simplicial set** is a pair $(X, t X)$ consisting of a simplicial set $X$ and a stratification $t X$ of $X$.

The elements of $t X$ are called the **thin** simplices of $X$.


For $(X, t X)$ and $(Y, t Y)$ stratified simplicial sets, a morphism $f : X \to Y$ of simplicial sets is set to be a **stratified map** if it respects thin cells in that

$$
  f(t X ) \subset t Y
  \,.
$$ 

The [[category]] of startified simplicial sets and stratified maps between them is usually denoted $Strat$.

This category is a [[quasitopos]].  Hence, in particular, it is [[cartesian closed category|cartesian closed]].




#Examples#

* Every simplicial set gives rise to a stratified simplicial set

  * using the **maximal stratification**: all simplices are regarded as thin;

  * using the **minimal stratification**: only degeneracies are thin.

  These two stratifications give [[left adjoint|left]] and [[right adjoint]]s to the [[forgetful functor]] from stratified simplicial sets to simplicial sets.

* A [[complicial set]] is a stratified simplicial set satisfying certain extra conditions. Complicial sets are precisely those simplicial sets which arise (up to isomorphism) as the [[oriental|omega-nerve]] $N(C)$ of a [[strict omega-category]] $C$, where the thin cells are the images of the identity cells of $C$.


* A [[simplicial set]] is a [[Kan complex]] precisely if its maximal stratification makes it a [[weak complicial set]].


#The category of stratified simplicial sets#

There are several [[tensor product]]s on the category $Strat$ of stratified simplicial sets that make it a [[monoidal category]].

## Strat with the Verity-Gray tensor product ##

Consider the monoidal category $(Strat, \otimes)$ where $\otimes$ is the [[Verity-Gray tensor product]]. 

(Notice that this is not [[closed monoidal category|closed]], as far as I understand.)

Using the canonical stratification of [[oriental|omega-nerves]] on [[strict omega-category|strict omega-categories]] as [[complicial set]]s, the $\omega$-nerve is a functor

$$
  N : Str \omega Cat \to Strat
  \,.
$$

+-- {: .un_prop}
###### Proposition
The functor $N : Str \omega Cat \to Strat$ has a [[left adjoint]] $F : Strat \to Str \omega Cat$ which is a [[strong monoidal functor]].
=--

Or so it is claimed on [slide 60](http://www.mat.uc.pt/~categ/ct2007/slides/verity.pdf#page=60) of 
[Ver07](http://www.mat.uc.pt/~categ/ct2007/slides/verity.pdf)


#References#

A useful quick introduction is the beginning of these slides:

* Dominic Verity, _Weak Complicial sets and internal quasi-categories_ ([pdf slides](http://www.mat.uc.pt/~categ/ct2007/slides/verity.pdf))
