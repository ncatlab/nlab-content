#Idea#

[[Nils Baas]] has been emphasizing for many years, in print and in private communication, the conviction that the usual  notions of [[n-category]], [[infinity-category]] [[omega-category]] in [[higher category theory]] are **not** naturally suited for describing

* [[extended cobordism]]s such as appearing in 

  * the [[generalized tangle hypothesis|tangle hypothesis]]

  * in [[FQFT|extended quantum field theory]]

* hierarchical systems such as appearing in

  * complex systems;

  * biology.


The point is essentially that the _directedness_ of morphisms and -- related to that -- the binary notion of [[source]] and [[target]] in categories and higher categories are notions alien to these contexts, which in applications have to and are essentially removed again in a second step by adding extra structure and requiring further properties, such as various monoidal structures and dualities, which allow to change the direction of morphisms, to collect objects together, etc.

In contrast to that, Baas pointed out that more naturally the above situations are thought of from the beginning in terms of hierarchies of what he calls _bonds_, where, quite generally, a bond is an oject equipped with information of how a collection of sub-bonds sits inside it, _bound by the bond_.

A sketch of a generic such a situation of hierarchical bonds is a diagram 

$$
  \array{
     \beta_2 &&=&& \beta_2
     \\
     \downarrow && && \downarrow
     \\
     b_1 &\to& B &\leftarrow& b_2
     \\
     \uparrow && \uparrow  && \uparrow
     \\
     \beta_1 && b_3 && \beta_3
  }
$$

where a bond $B$ binds sub-bonds $b_1, b2$ and $b_3$ which in turn bind sub-bonds $\beta_i$.

For instance $B$ might be an [[extended cobordism]] with three boundary components $b_1, b_2, b_3$ which in turn have pieces of boundary components $\beta_i$.

Nils Baas has made, in print and in private communication, suggestions for a formalization of such systems of hierarchical bonds and coined the term **hyperstructures** for these. One reference is

* Nils Baas, _Introducing abstract matter_ ([pdf](http://pagesperso-orange.fr/vbm-ehr/ChEh/articles/Baas%20paper.pdf))

#Remarks#

* The vague notion of replacing morphisms by _bonds_ is familiar and concretely realizes at least in a hierarchy of depth 2 in the context of [[groupoidification]] and [[geometric function theory]], where morphisms are replaced by [[span]]s. Regarding these as [[cospan]]s in the [[opposite category]] produces diagrams alike the above sketch of a generic bond system. 

* Accordingly, the notion of [[multispan]] and [[multi-cospan]] may come close to exhibiting some crucial aspects of the idea that motivated the concept of hyperstructures.

#Blog discussion#

* David Corfield, [Category Theory and Biology](http://golem.ph.utexas.edu/category/2007/11/category_theory_and_biology.html)

  * The birth of the idea of [[multispan]]s as a formalization of hyperstructures is mentioned in [this comment](http://golem.ph.utexas.edu/category/2007/11/category_theory_and_biology.html#c013165). 
Its application to the description of extended cobordisms and the [[generalized tangle hypothesis]] is topic of some thought chatted about at [this entry](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html#c021486).

