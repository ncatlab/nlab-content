
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

A braided [[rigid monoidal category]] is balanced if and only if it is a [[pivotal category]], but a balanced monoidal category need not be rigid (cf. [Selinger,  Lem. 4.20](#Selinger)).

Beware of the un-related notion of *[[balanced categories]]*.


## Properties

Every [[symmetric monoidal category]] is balanced in a canonical way. In fact, the [[identity natural transformation]] on the identity functor of $\mathscr{C}$ is a balance on $\mathscr{C}$. In this way, the twist can be seen as a way of "controlling" the non-symmetric behavior of the braiding.

In the language of [[string diagrams]], the balancing is represented by a 360-degree twist:

\begin{imagefromfile}
"file_name": "graphical-twist.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

## References



The original definition:

* [[Andre Joyal]], [[Ross Street]], _The geometry of tensor calculus I_,  Adv. Math.  __88__ 1 (1991) 55--112, &lbrack;[doi](http://dx.doi.org/10.1016/0001-8708%2891%2990003-P)&rbrack;

The above follows

* Jeff Egger*, Appendix C &lbrack;[pdf](http://www.mscs.dal.ca/~jegger/4micah.pdf)&rbrack;

See also

* {#Selinger} [[Peter Selinger]], *A survey of graphical languages for monoidal categories* &lbrack;[arXiv:0908.3347](https://arxiv.org/abs/0908.3347)&rbrack;


[[!redirects balancing]]
[[!redirects balance]]

[[!redirects balanced monoidal category]]
[[!redirects balanced monoidal categories]]
