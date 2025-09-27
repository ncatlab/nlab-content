
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

A [[subcategory]] $D$ of a [[strict category]] $C$ is called __replete__ if it respects [[isomorphism]] of morphisms in the [[arrow category]] of $C$.  It is a subcategory for which the property of (strictly) belonging to it respects the [[principle of equivalence]] of categories.


## Definition

A [[subcategory]] $D$ of $C$ is __replete__ if for any [[object]] $x$ in $D$ and any [[isomorphism]] $f\colon x\cong y$ in $C$, both $y$ and $f$ are also in $D$.  Equivalent ways to state this include:

* If $f \in D$ and $f \cong g$ in the [[arrow category]] $Arr(C)$, then $g \in D$.

* The inclusion $D\hookrightarrow C$ is an [[isofibration]].


## Repletion and replete images
 {#RepletionAndRepleteImages}

Since repleteness is a "closure condition," the [[intersection]] of any collection of replete subcategories is again replete.  Therefore, any subcategory is contained in a smallest replete subcategory, called its **repletion**.  We can construct the repletion $repl(D)$ of $D\subset C$ explicitly as follows:

* its objects are those objects of $C$ which admit an isomorphism to some object of $D$, and
* its morphisms are those morphisms of $C$ which can be written as a composite of morphisms in $D$ and isomorphisms in $C$.

Repleteness and repletions are most often applied to [[full subcategories]], in which case the repletion is simply the full subcategory of $C$ determined by those objects which are isomorphic to some object of $D$.  In particular, in this case, the repletion is [[equivalence of categories|equivalent]] to $D$.  More generally, we can say:

+-- {: .un_prop}
###### Proposition
The inclusion $D\hookrightarrow repl(D)$ is an equivalence if and only if the inclusion $D\hookrightarrow C$ is [[pseudomonic functor|pseudomonic]].
=--
+-- {: .proof}
###### Proof
The inclusion of a replete subcategory is always pseudomonic, so if $D\hookrightarrow repl(D)$ is an equivalence, and in particular full and faithful, then $D\hookrightarrow C$ must also be pseudomonic.

Conversely, if $D\hookrightarrow C$ is pseudomonic, then every morphism of $repl(D)$ can be written as $g f h^{-1}$ for some morphism $f$ in $D$ and isomorphisms $g$ and $h$ in $C$.  If the domain and codomain are in $D$, then since $D\hookrightarrow C$ is pseudomonic, both $g$ and $h$ must also be in $D$, hence such a morphism is itself necessarily in $D$.  Thus the inclusion $D\hookrightarrow repl(D)$ is full.  It is clearly faithful and essentially surjective, so it is an equivalence.
=--

The **replete image** of a functor is the repletion of its image.  The **replete full image** of a functor is the repletion of its [[full image]], i.e. the full subcategory of its target determined by those objects isomorphic to some object in its image.  See also [[essential image]].


## Higher-categorical versions

More generally, for $n\geq 0$, a subcategory $D$ of an $n$-[[n-category|category]] $C$ is replete if all [[equivalence]]s in $C$ whose either source or target is in $D$ are themselves in $D$. In particular, all $k$-cells equivalent in $C$ to some $k$-cell in $D$ are themselves in $D$ (because they are sources of some equivalence in $D$).  Then replete subcategories of $1$-[[1-category|categories]] are those which are replete in this sense.

Here we are using the weakest notion of equivalence; one could also talk about $k$-replete $n$-subcategories if every $k$-equivalences in $C$ belongs to $D$ if either its source or target does.  Then using the usual definition of 'category' as a model for $1$-categories, replete subcategories are already those which are $0$-replete (indeed, $0$-equivalence is isomorphism in this model); but using a model of $1$-categories in which [[hom-sets]] are [[setoid]]s (as is common, for example, in [[type theory|type-theoretic]] [[foundations]]), we must insist on $1$-repleteness.

Note that a subcategory $D$ of an $n$-category $C$ is $(k-1)$-replete if and only if:

*  for every $(n-k)$-cell in $D$ all $(n-k)$-cells $(k-1)$-equivalent to an $(n-k)$-cell in $D$ are themselves in $C$, and
*  for any two $(n-k)$-cells $x,y$ the hom $k$-category $hom(x,y)$ is $(k-2)$-replete.



[[!redirects replete]]
[[!redirects replete subcategory]]
[[!redirects replete subcategories]]
[[!redirects replete image]]
[[!redirects replete images]]
[[!redirects full replete image]]
[[!redirects full replete images]]
[[!redirects repletion]]
