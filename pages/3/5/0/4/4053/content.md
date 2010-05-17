
<div class="rightHandSide toc">
[[!include monoidal categories - contents]]
</div>


The term **twist** or **twisted** is one of the hugely overloaded terms in math. Among the various meaning it may have is

* [[twisted cohomology]]

  * [[twisted bundle]]

  * [[twisted K-theory]]

* [[twisting cochain]]

* [[twisted complex]]

* [[twisted tensor product]]

* [[twisted module of homomorphisms]]

* etc....

* This page here is about the notion of twist in a 
[[braided monoidal category]] that is part of the structure of a [[balanced monoidal category]].


***

#Twists in braided monoidal categories#
* automatic table of contents goes here
{:toc}

## Definition

A __twist__, or __balance__, in a [[braided monoidal category]] $B$ is a [[natural transformation]] from the [[identity functor]] on $B$ to itself satisfying a certain condition that links it to the [[braiding]].  A __balanced monoidal category__ is a braided monoidal category equipped with such a balance.

The condition linking the balancing to the braiding, where $\theta$ is the balance and $\beta$ is the braiding, is that $\theta_{x \otimes y}$ should be the [[composite]] of $\beta_{x,y}$, $\theta_y \otimes \theta_x$, and $\beta_{y,x}$.


## Properties

Every [[symmetric monoidal category]] is balanced in a canonical way; in fact, the [[identity natural transformation]] (on the identity functor of $B$) is a balance on $B$ if and only if $B$ is symmetric.  Thus balanced monoidal categories fall between braided monoidal categories and symmetric monoidal categories.  (They should not be confused with [[balanced categories]], which are unrelated.)


In the [[string diagram]] calculus for [[ribbon categories]], the twist is represented by a 360-degree twist in a ribbon.


## References

This definition is taken from [Jeff Egger](http://www.mscs.dal.ca/~jegger/4micah.pdf) (Appendix C), but the original definition is due to [[Andre Joyal|Joyal]] and [[Ross Street|Street]].



[[!redirects twist]]

[[!redirects balancing]]
[[!redirects balance]]

[[!redirects balanced monoidal category]]
