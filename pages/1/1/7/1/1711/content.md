
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A **$k$-transfor** is an operation from one $n$-[[n-category|category]] $C$ to another $D$ (for some value of $n$) that takes [[object|objects]] of $C$ to $k$-[[k-morphism|morphisms]] of $D$ (and more generally $j$-morphisms in $C$ to $(j+k)$-morphisms in $D$) in a coherent way.  Equivalently, a $k$-transfor is a $k$-cell in an [[internal-hom]] $n$-category.  Transfors are a common generalisation of:

* $n$-[[n-functor|functor]]s, which are 0-transfors
* $n$-[[natural transformation]]s, which are 1-transfors
* [[modifications]], which are 2-transfors,
* perturbations, which are 3-transfors,
* and so on.

The word "transfor" was coined by Sjoerd Crans in [this paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.26.506&rep=rep1&type=pdf); it is a _portmanteau_ of "functor" and "transformation."  A collection of components which forms a transfor is said to be *transforial*, as a generalization of "functorial" and "natural."


## Terminology

Once upon a time, there were [[categories]], [[functor|functors]] between them, and natural transformations between them.  Then when $n$-categories came along, people called the arrows between them '$n$-functors' even though one could just as easily say 'functors'.  In the same vein, people said '$n$-transformations' for natural transformations (that is, 2-transfors) between $n$-categories.  At the same time, we saw that we needed modifications between $n$-transformations, and that there would have to be things between higher modifications, and so on.  However, due to the prior use of "$n$-transformation" for a 2-transfor between $n$-categories, the natural choice "$k$-transformation" is unavailable to mean a $k$-transfor.

Here are some other possible terms for a $k$-transfor between $n$-categories, which additionally notate the value of $n$ (although this is, strictly speaking, unnecessary).

* $(n,k)$-transformation
* $n$-$k$-transfor
* $n$-dimensional $k$-transfor
* $n$-categorical $k$-transfor
* $n$-natural $k$-transformation


## Definitions

We haven\'t gotten around to saying anything precise yet, but you can see something in the discussion below, or in Crans\'s paper.


## Special cases

See this [[periodic table]] of $k$-transfors between $n$-categories for common names for low values of $n$ and $k$.  On the $n$-Lab, we tend to omit the prefix $n$- whenever possible (as ironic as that may be).

<table><tr><th markdown="1">$k$&#8595;\$n$&#8594;</th><th markdown="1">$-1$</th><th markdown="1">$0$</th><th markdown="1">$1$</th><th markdown="1">$2$</th><th markdown="1">$3$</th><th>...</th></tr>
<tr><th markdown="1">$0$</th><td>[[implication]]</td><td>[[function]]</td><td>[[functor]]</td><td markdown="1">$2$-[[2-functor|functor]]</td><td markdown="1">$3$-[[n-functor|functor]]</td><td>...</td></tr>
<tr><th markdown="1">$1$</th><td>trivial</td><td>[[equality]] of functions</td><td>[[natural transformation]]</td><td markdown="1">$2$-transformation</td><td markdown="1">$3$-transformation</td><td>...</td></tr>
<tr><th markdown="1">$2$</th><td>"</td><td>trivial</td><td>equality of natural transformations</td><td>[[modification]]</td><td markdown="1">$3$-modification</td><td>...</td></tr>
<tr><th markdown="1">$3$</th><td>"</td><td>"</td><td>trivial</td><td>equality of modifications</td><td>perturbation</td><td>...</td></tr>
<tr><th markdown="1">$4$</th><td>"</td><td>"</td><td>"</td><td>trivial</td><td>equality of perturbations</td><td>...</td></tr>
<tr><th markdown="1">$5$</th><td>"</td><td>"</td><td>"</td><td>"</td><td>trivial</td><td>...</td></tr>
<tr><th>&#8942;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&#8945;</td></tr></table>

Note that the [[source]] and [[target]] of a $k$-transfor (between $n$-categories) are $(k-1)$-transfors (between the same $n$-categories).  Given two fixed source and target $(k-1)$-transfors, the $k$-transfors between them (and the $(k+1)$-transfors between those, and so on) form an $(n-k)$-category.

### For n-posets

A similar table [[periodic table]] of $k$-transfors between $n$-posets exists for common names for low values of $n$ and $k$. 

<table><tr><th markdown="1">$k$&#8595;\$n$&#8594;</th><th markdown="1">$-1$</th><th markdown="1">$0$</th><th markdown="1">$1$</th><th markdown="1">$2$</th><th markdown="1">$3$</th><th>...</th></tr>
<tr><th markdown="1">$0$</th><td>[[implication]]</td><td>[[monotonic function]]</td><td>[[functor]]</td><td markdown="1">$2$-[[2-functor|functor]]</td><td markdown="1">$3$-[[n-functor|functor]]</td><td>...</td></tr>
<tr><th markdown="1">$1$</th><td>trivial</td><td>[[partial order]] of monotonic functions</td><td>[[natural transformation]]</td><td markdown="1">$2$-transformation</td><td markdown="1">$3$-transformation</td><td>...</td></tr>
<tr><th markdown="1">$2$</th><td>"</td><td>trivial</td><td>partial order of natural transformations</td><td>[[modification]]</td><td markdown="1">$3$-modification</td><td>...</td></tr>
<tr><th markdown="1">$3$</th><td>"</td><td>"</td><td>trivial</td><td>partial order of modifications</td><td>perturbation</td><td>...</td></tr>
<tr><th markdown="1">$4$</th><td>"</td><td>"</td><td>"</td><td>trivial</td><td>partial order of perturbations</td><td>...</td></tr>
<tr><th markdown="1">$5$</th><td>"</td><td>"</td><td>"</td><td>"</td><td>trivial</td><td>...</td></tr>
<tr><th>&#8942;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&#8945;</td></tr></table>



## Related concepts

* [[homotopy]]

* functors

  * [[functor]]

  * [[2-functor]]

  * [[(∞,1)-functor]]

* transformations

  * [[natural transformation]]

  * [[pseudonatural transformation]] / [[lax natural transformation]]

  * [[(∞,1)-natural transformation]]

  * [[(∞,n)-natural transformation]]

* modifications

  * [[modification]]

## References

* [[Sjoerd Crans]]: *A Tensor Product for Gray-Categories*, Theory and Applications of Categories **5** 2 (1999) 12–69 &lbrack;[tac:5-02](http://www.tac.mta.ca/tac/volumes/1999/n2/5-02abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/1999/n2/n2.pdf)&rbrack;

* {#Crans03} [[Sjoerd Crans]]: *Localizations of Transfors*, K-Theory **28** 1 (2003) 39-105 &lbrack;[doi:10.1023/A:1024186923002](http://dx.doi.org/10.1023/A:1024186923002)&rbrack;


* [[Camell Kachour]]: *Définition algébrique des cellules non-strictes*, [[Cahiers]] de Topologie et de Géométrie Différentielle Catégorique **1** (2008) 1-68 &lbrack;[numdam:CTGDC_2008__49_1_1_0](https://www.numdam.org/item/?id=CTGDC_2008__49_1_1_0), [pdf](https://www.numdam.org/article/CTGDC_2008__49_1_1_0.pdf)&rbrack;

* [[Camell Kachour]]: *Steps toward the weak higher category of the weak higher categories in the globular setting*, Categories and General Algebraic Structures with Applications **4** 1 (2016) 9-42 &lbrack;[cgasa:11180](https://cgasa.sbu.ac.ir/article_11180.html), [pdf](https://cgasa.sbu.ac.ir/article_11180_b13cacfd9afe5780932141c269d0add6.pdf)&rbrack;



[[!redirects (n,j)-transformation]]
[[!redirects j-transformation]]
[[!redirects k-transformation]]
[[!redirects n-transformation]]
[[!redirects (n,j)-transformations]]
[[!redirects (n,k)-transformation]]
[[!redirects (n,k)-transformations]]
[[!redirects j-transformations]]
[[!redirects k-transformations]]
[[!redirects n-transformations]]
[[!redirects k-transfor]]
[[!redirects k-transfors]]
[[!redirects transfors]]

[[!redirects n-natural transformation]]
[[!redirects n-natural transformations]]
