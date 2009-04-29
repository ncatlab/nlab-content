#Idea#

A _stratified simplicial set_ is a [[simplicial set]] equipped with information about which of its [[simplex|simplices]] are to be regarded as being _thin_ in that they are like identies or at least like equivalences in a [[higher category theory|higher category]].

The theory of [[simplicial weak omega-category|simplicial weak omega-catgeories]] is based on stratified simplicial sets.

#Definition#

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

This category is a [[quasi-topos]].




#Examples#

* Every simplicial set gives rise to a stratified simplicial set

  * using the **maximal stratification**: all simplices are regarded as thin;



* A [[complicial set]] is a stratified simplicial set satisfying certain extra conditions. Complicial sets are precisely those simplicial sets which arise as the [[oriental|omega-nerve]] $N(C)$ of a [[strict omega-category]] $C$ and whose thin cells are precisely the images of the identity cells of $C$.


* A [[simplicial set]] is a [[Kan complex]] precisely if its maximal stratification makes it a [[weak complicial set]].



#References#

A useful quick introduction is the beginning of these slides:

* Dominic Verity, _Weak Complicial sets and internal quasi-categories_ ([pdf slides](http://www.mat.uc.pt/~categ/ct2007/slides/verity.pdf))