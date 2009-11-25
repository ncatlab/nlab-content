# Terminal objects in quasi-categories
* tic
{: toc}


##Idea#

In a [[quasi-category]] the notion of [[terminal object]] in an ordinary [[category]] is relaxed in the suitable [[homotopy theory|homotopy-theoretic]] sense: instead of demanding that form any other object there is a _unique_ morphism into the terminal object, in a quasi-category there is a _contractible space_ of such morphisms, i.e. the morphism to the terminal object is unique up to homotopy.


##Definition#

Let $C$ be a [[quasi-category]] and $c \in C$ one of its [[object]]s (a vertex in the corresponding [[simplicial set]]). The object $c$ is a **terminal object** in $C$ if the following equivalent conditions hold:

* The projection from the [[over quasi-category|over category]] $C_{/c} \to C$ is a [[model structure on simplicial sets|trivial fibration of simplicial sets]].

* For every object $d$ of $C$ the right hom Kan-complex into $d$ is contractible:
$$
  Hom_C^R(d,c) \simeq pt
  \,.
$$


##References#

See [definition 1.2.12.3, p. 46](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=46) in 

*  [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects terminal objects in quasi-categories]]
[[!redirects terminal object in a quasicategory]]
[[!redirects terminal objects in quasicategories]]