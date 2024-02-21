
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Balanced monoidal categories#
* automatic table of contents goes here
{:toc}

## Definition

A __twist__, or __balance__, in a [[braided monoidal category]] $\mathscr{C}$ is a [[natural transformation | natural isomorphism]] $\theta$ from the [[identity functor]] on $\mathscr{C}$ to itself satisfying the following compatibility condition with the braiding:

$$\theta_{A\otimes B}=\beta_{B,A}\circ \beta_{A,B}\circ (\theta_A\otimes \theta_B),\,\, \forall A,B\in\mathscr{C}$$

where $\beta$ is the braiding on $\mathscr{C}$. A __balanced monoidal category__ is a braided monoidal category equipped with such a balance. 
A braided [[rigid monoidal category]] is balanced if and only if it is a [[pivotal category]], but a balanced monoidal category need not be rigid.

Balanced monoidal categories should not be confused with the other unrelated notation of a [[balanced category]].

## Properties

Every [[symmetric monoidal category]] is balanced in a canonical way. In fact, the [[identity natural transformation]] on the identity functor of $\mathscr{C}$ is a balance on $\mathscr{C}$. In this way, the twist can be seen as a way of "controlling" the non-symmetric behavior of the braiding.

In the language of [[string diagrams]], the balancing is represented by a 360-degree twist:

\begin{imagefromfile}
"file_name": "graphical-twist.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

## References

This definition is taken from [Jeff Egger](http://www.mscs.dal.ca/~jegger/4micah.pdf) (Appendix C), but the original definition can be found in chapter 4 of this paper by [[Andre Joyal|Joyal]] and [[Ross Street|Street]]:

* A. Joyal, R. Street, _The geometry of tensor calculus I_,  Adv. Math.  __88__(1991),  no. 1, 55--112, [doi](http://dx.doi.org/10.1016/0001-8708%2891%2990003-P).

[[!redirects balancing]]
[[!redirects balance]]

[[!redirects balanced monoidal category]]
[[!redirects balanced monoidal categories]]
