
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>

# Accessible $(\infty,1)$-categories
* tic
{: toc}


## Idea ##

The notion of **accessible $(\infty,1)$-category** is the generalization of the notion of [[accessible category]] from [[category theory]] to [[(∞,1)-category]] theory.

It is a means to handle $(\infty,1)$-categories that are not [[essentially small (∞,1)-category|essentially small]] in terms of small data.

An _accessible_ $(\infty,1)$-category is one which may be [[large category|large]], but can entirely be _accessed_ as an $(\infty,1)$-category of "conglomerates of objects" in a small $(\infty,1)$-category -- precisely: that it is a category of $\kappa$-small [[ind-object]]s in some small $(\infty,1)$-category $C$.


## Definition ##

+-- {: .un_defn}
###### Definition

Let $\kappa$ be a [[cardinal number|regular cardinal]]. A [[quasi-category]] $C$ is **accessible** if it satisfies the following equivalent conditions

* $C$ is equivalent to the $(\infty,1)$-category  $Ind_\kappa(C^0)$ of [[ind-object in an (infinity,1)-category|ind-objects]] for a small $(\infty,1)$-category $C^0$;

* $C$ admits small $\kappa$-[[filtered colimits]] and contains an [[essentially small (∞,1)-category|essentially small]] [[sub-quasi-category|full subcategory]] which consists of $\kappa$-[[compact object in an (infinity,1)-category|compact]] objects and generates $C$ under small $\kappa$-[[filtered colimit]]s.


=--

An [[(∞,1)-functor]] between accessible $(\infty,1)$-categories that preserves $\kappa$-filtered colimits is called an **[[accessible (∞,1)-functor]]** .


## References 

The theory of accessible 1-categories is described in 

* Adamek and Rosicky, _Locally presentable and accessible categories_, Cambridge University Press (1994)

The theory of accessible $(\infty,1)$-categories is the topic of section 5.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects accessible (infinity,1)-categories]]
[[!redirects accessible (∞,1)-category]]
[[!redirects accessible (∞,1)-categories]]