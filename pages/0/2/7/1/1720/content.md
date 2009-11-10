[[!redirects right proper model category]]

In a [[model category]] fibrations and cofibrations enjoy [[pullback stability]], but weak equivalences do not necessarily.

A [[model category]] is called 

* **right proper** if weak equivalences are preserved by [[pullback]] along fibrations

* **left proper** if weak equivalence are preserved by [[pushout]] along cofibrations

* **proper** if it is both left and right proper.



So a model category is right proper if for every weak equivalence $f : A \to B$ in $W\subset Mor(C)$ and every fibration $h : C \to B$ the pullback $h^* f : A \times_B C \to C$ in

$$
  \array{
    A \times_C B &\to& A
    \\
    \;\;\downarrow^{\mathrlap{\Rightarrow h^* f \in W}} && \downarrow^{\mathrlap{f \in W}}
    \\
    C &\stackrel{h \in F}{\to}& B
  }
$$

is a weak equivalence.

#Examples#

All [[model category|model categories]] that model aspects of [[infinity-stack]]s and hence of [[cohomology]] are right proper: 

* [[model structure on simplicial presheaves]]

  for presheaves over the point this restricts to:

  * [[model structure on simplicial sets]]

  * [[model structure on topological spaces]]



* [[model structure on presheaves of spectra]] 

  for presheaves over the point this restricts to:

  * [[model structure on spectra]]


#In other homotopical contexts #

The notion of right properness makes sense in any [[homotopical category]] that is further equipped with a notion of fibrations, for instance a Brown [[category of fibrant objects]]: in every such category of fibrant objects the property is satisfied and weak equivalences are preserved under [[pullback]] along fibrations.  





For the relevance of the right properness property for these examples in the general context of [[cohomology]] see

* J. Jardine, _Cocycle categories_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0605/0605198v1.pdf))