#Idea#

A _stratified simplicial set_ is a [[simplicial set]] equipped with information about which of its [[simplex|simplices]] are to be regarded as being _[[thin element|thin]]_ in that they are like identies or at least like equivalences in a [[higher category theory|higher category]].

The theory of [[simplicial weak ∞-categories]] is based on stratified simplicial sets.

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

  These two stratifications give [[left adjoint|left]] and [[right adjoints]] to the [[forgetful functor]] from stratified simplicial sets to simplicial sets.

* The **standard thin** $n$-**simplex** is obtained from $\Delta[n]$ my making its only non-degenerate $n$-simplex thin.

* The $k$th **standard admissible** $n$-**simplex** $\Delta^a_k[n]$, defined for $n \geq 2$, $0 \lt k \lt n$, is obtained from $\Delta[n]$ by making all simplices $\alpha \colon [m] \to [n]$ with $k-1,k,k+1 \in$ im$(\alpha)$ thin.

* The **standard admissible** $(n-1)$-**dimensional** $k$-**horn** $\Lambda^a_k[n]$, defined for $n \geq 2$, $0 \lt k \lt n$, is the pullback of the stratified simplicial set $\Delta^a_k[n]$.

* A [[complicial set]] is a stratified simplicial set satisfying certain extra conditions. Complicial sets are precisely those simplicial sets which arise (up to isomorphism) as the [[oriental|∞-nerve]] $N(C)$ of a [[strict ∞-category]] $C$, where the thin cells are the images of the identity cells of $C$.


* A [[simplicial set]] is a [[Kan complex]] precisely if its maximal stratification makes it a [[weak complicial set]].


#The category of stratified simplicial sets#

There are several [[tensor products]] on the category $Strat$ of stratified simplicial sets that make it a [[monoidal category]].

## Strat with the Verity-Gray tensor product ##

Consider the monoidal category $(Strat, \otimes)$ where $\otimes$ is the [[Verity-Gray tensor product]]. 

(Notice that this is not [[closed monoidal category|closed]], as far as I understand.)

Using the canonical stratification of [[oriental|∞-nerves]] on [[strict ∞-categories]] as [[complicial sets]], the $\omega$-nerve is a functor

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

* [[Dominic Verity]], _Weak Complicial sets and internal quasi-categories_ ([pdf slides](http://www.mat.uc.pt/~categ/ct2007/slides/verity.pdf))

[[!redirects stratified simplicial sets]]