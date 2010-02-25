
> under construction

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **model structure for left fibrations** is a [[model category]] structure on the [[overcategory]] $SSet/S$ of [[simplicial set]]s over a given simplicial set $S$, that models the [[(∞,1)-category]] of [[left fibration]]s [[fibrations of quasi-categories|of quasi-categories]] over $S$.

This is the $(\infty,1)$-analog of the $(2,1)$-category of [[fibered category|categories cofibered in groupoids]].

The extension of this from [[left fibration]]s to [[coCartesian fibration]]s is the [[model structure for coCartesian fibrations]].


## Definition

...

The model structure on $SSet/S$ is given by

A morphism $f : X \to Y$ is 

* a cofibration if the underlying morphism of simplicial sets is a cofibration in the standard [[model structure on simplicial sets]], i.e. a [[monomorphism]];

* a weak equivalence if the induced morphism

  $$
    X^{\triangleleft} \coprod_X S
    \to 
    Y^{\triangleleft} \coprod_Y S
  $$

  is a weak equivalence in the Joyal [[model structure for quasi-categories]], where $X^{\triangleleft}$ is the [[join of simplicial sets|join]] $X^{\triangleleft} := {*} \star X$.

(def. 1.2.4.5)

This is a 

* [[proper model category|proper]]

* [[simplicial model category|simplicial]]

* [[combinatorial model category]].

(prop 2.1.4.7, 2.1.4.8)


We have 

* The fibrant objects are precisely the [[left fibration]]s 
  (corollary 2.2.3.12)

* Every left anodyne morphism is an acyclic cofibration. (prop 2.1.4.9)



## References

This is the content of section 2.1.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

There the model category is called the **covariant model structure**.

[[!redirects model structure for right fibrations]]