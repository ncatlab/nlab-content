
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

[[Arne Strom|Arne Strøm]] has proven that the [[category]] [[Top]] of *all* topological spaces has a structure of a Quillen [[model category]] where 

* fibrations are [[Hurewicz fibrations]], 

* cofibrations are closed [[Hurewicz cofibrations]] 

* and the role of weak equivalences is played by (strong) [[homotopy equivalences]]. 

The theorem might have been a folklore at the time, but the actual paper has a number of subtleties.

Str&#248;m's proofs are not that well-known today and use techniques better known to the topologists of that time, and there is consequently a slight controversy among topologists now. One of these is that there are modern reproofs, but these modern techniques essentially use the [[compactly generated space|compactly generated]] [[Hausdorff spaces]], while Str&#248;m's proofs succeeded in avoiding that assumption. 


## Properties


Write $({\vert- \vert} \dashv Sing) : Top\stackrel{\overset{{|-|}}{\leftarrow}}{\underset{Sing}{\to}} $ [[sSet]] for the ordinary [[geometric realization]]/[[singular simplicial complex]] [[adjunction]] (see [[homotopy hypothesis]]).

For $S_{\bullet,\bullet} : \Delta^{op} \times \Delta^{op} \to Set$ a [[bisimplicial set]], write $d S$ for its [[diagonal]] $d X : \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{S}{\to} Set$.

+-- {: .un_prop}
###### Proposition

For $X_\bullet$ any [[simplicial topological space]], there is a [[homeomorphism]] between the [[geometric realization of simplicial topological spaces|geometric realizaton]] of the 
[[simplicial topological space]] $[n] \mapsto |Sing(X_n)|$ and the ordinary [[geometric realization]] of the [[simplicial set]] that is the diagonal of the [[bisimplicial set]] $Sing(X_\bullet)_\bullet$

$$
  \left|[n] \mapsto |Sing(X_n)|\right|  \simeq_{iso} | d Sing(X_\bullet)_\bullet | 
  \,.
$$

Moreover, the degreewise $(|-| \dashv Sing)$-[[unit of an adjunction|counit]] yields a morphism

$$
 ([n] \mapsto |Sing(X_n)|) \to X_\bullet
$$

and this is a cofibrant [[resolution]] in the [[Reedy model structure]]  $[\Delta^{op}, Top_{Strom}]_{Reedy}$ relative to the Str&#248;m model structure. 

=--

See [[geometric realization of simplicial topological spaces]] for more details.


## References



The main article is 

* [[Arne Strøm]], _The homotopy category is a homotopy category_ , Archiv der Mathematik 23 (1972)

but it depends on earlier results of several authors and mostly his own earlier papers

* Arne Str&#248;m, _Note on cofibrations_,  Math. Scand.  19  1966 11--14 [file](http://www.mscand.dk/article.php?id=1782) MR0211403 (35 #2284); _Note on cofibrations II_,  Math. Scand.  22  1968 130--142 (1969) [file](http://www.mscand.dk/article.php?id=1867) MR0243525 (39 #4846)

One modern re-proof can be found in

* [[Peter May|May]] and Sigurdsson, _Parametrized homotopy theory_

[[!redirects Strøm's model category]]
[[!redirects Strom's model category]]
[[!redirects Strøm's model category]]
[[!redirects Strom's model category]]
[[!redirects Strøm model category]]
[[!redirects Strom model category]]
[[!redirects Strøm's model structure]]
[[!redirects Strom's model structure]]
[[!redirects Strøm's model structure]]
[[!redirects Strom's model structure]]
[[!redirects Strøm model structure]]
[[!redirects Strom model structure]]
[[!redirects Hurewicz model structure]]
[[!redirects h-model structure]]