
+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***



[[compact object#CompactnessInAdditiveCategories]]

[[compact object#CompactnessInAdditiveCategories|compact object]]

[compact object](http://ncatlab.org/nlab/show/compact+object#CompactnessInAdditiveCategories)

[compact object](compact+object#CompactnessInAdditiveCategories)

***
## Limit ##

Here I'll try to reorganize the entry [[nLab:limit|limit]] according to the structure discussed in the forum entry "objects" and tools to compute them. As this page will be complete I'll move it into the Lab. Editing of this page is strongly encouraged :)


#Contents#


#Idea#

In [[nlab:category theory]] a limit of a [[nlab:diagram]] $F\colon D \to C$ in a [[nlab:category]] $C$ is an [[nlab:object]] $lim F$ of $C$ equipped with morphisms to the objects $F(d)$ for all $d \in D$, such that everything in sight commutes. Moreover, the limit $lim F$ is the _universal_ object with this property, i.e. the "most optimized solution" to the problem of finding such an object.
One can think of the category of [[nlab:cone|cones]] over $F\colon D\to C$ as the collection of all displacements of arrows stemming from a fixed "source" $C$ (the _base_ of the cone) suitably linked by morphisms. This in turn can be regarded as a functor from the diagram $[0]\star D$ to $C$ 'extending' $F$ (see the page [[over quasi-category]]); now the universal property makes $\text{lim}\; F$ a [[nlab:terminal object]] in the category of these functors. In the $(`infty,1)$-categorical setting, this suggests to define limits again in terms of terminal objects, but using the [[nLab:join of quasi-categories|joins of quasi-categories]] instead of the [[join of categories]].

#Definition#

For $K$ and $C$ two [[nlab:quasi-category|quasi-categories]] and $F : K \to C$ a morphism of [[nlab:quasi-category|quasi-categories]] (i.e. nothing more than a map of [[simplicial set|simplicial sets]]. Then the **limit** of $F$ is, if it exists, the [[nlab:terminal object in a quasi-category|quasi-categorical terminal object]] in the [[over quasi-category]] $C_{/F}$:

$$
  \varprojlim F := TerminalObj(C_{/F})
  \,,
$$
where $C_{/F}=Hom_{F}(
    [0] \star K, C )$
## Generalization to weighted limits ##

There is an evident
generalization to [[weighted limit]]s:
replace in the above the join $[0] \star K$ with the [[weighted join]]
$[0] \star_W K$
where $W$ is _any_ functor
$W : D \to Set$ -- then called the _weight_. The $W$-weighted limit of $F$, $\lim_W F$, also written $\{W,F\}$, is, if it exists, the quasicategorical terminal oject in $Hom_{F}(
    [0] \star_W K, C )$.


# To be continued...

***

category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects שנה טובה]]
[[!redirects Featured math : Quora]]
