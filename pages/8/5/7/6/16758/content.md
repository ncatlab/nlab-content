
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

**Skeletal geometric morphisms** are those [[geometric morphisms]] that preserve [[double negation|double negation sheaves]] and therefore play a role in the descriptions of classes of toposes like e.g. [[Boolean topos|Boolean]] or [[De Morgan toposes]] in whose definitions the negation participates.

The notion of a skeletal geometric morphism can be viewed as a common generalization of the notions of [[dominant geometric morphism|dominant]] and [[open geometric morphisms]].

## Definition

A [[geometric morphism]] $f :  \mathcal{F} \to \mathcal{E}$ is called _skeletal_ if the following equivalent conditions hold:

* $f$ restricts to a geometric morphism $Sh_{\neg\neg}(\mathcal{F}) \to Sh_{\neg\neg}(\mathcal{E})$ .

* The [[inverse image]] $f^\ast$ preserves $\neg\neg$-dense monomorphisms.

* For any subobject $A'\rightarrowtail A$ in $\mathcal{E}$: $\neg\neg f^\ast(A')=\neg f^\ast(\neg A')$ in $Sub_\mathcal{F}(f^\ast(A))$.

## Example

* Inverse images of [[open geometric morphism|open geometric morphisms]] are [[Heyting functors]], hence commute with $\neg$ and, therefore, _open geometric morphisms are skeletal_. In particular, geometric morphisms with [[Boolean topos|Boolean]] codomain are open ([Johnstone 2002, p.612](#J02)), hence skeletal. 

* [[dense subtopos|Dense subtoposes]] $i:Sh_j(\mathcal{E})\hookrightarrow \mathcal{E}$ are precisely those subtoposes with $Sh_{\neg\neg}(Sh_j(\mathcal{E}))=Sh_{\neg\neg}(\mathcal{E})$ (cf. [this proposition](dense+subtopos#negdense)) and, therefore, are skeletal.

## Properties

The following two propositions concern skeletal [[geometric embedding|inclusions]] (cf. Johnstone ([2002, p.1007](#J02))):

+-- {: .num_prop}
###### Proposition
An inclusion $i:Sh_j(\mathcal{E})\hookrightarrow \mathcal{E}$ is skeletal iff $ext(j)$ , the $j$-closure of $0\rightarrowtail 1$ , is a $\neg\neg$-closed [[subterminal object]] of $\mathcal{E}$.
=--

+-- {: .num_prop}
###### Proposition
The class $\Sigma$ of skeletal [[geometric embedding|inclusions]] is the smallest class $\Gamma$ of geometric morphisms such that:

* $\Gamma$ contains [[open subtopos|open inclusions]] and,

* $\Gamma$ is closed under precomposition with [[dense subtopos|dense inclusions]]: from $g$ dense, $f\in\Gamma$ and $f,g$ composable, follows $fg\in\Gamma$.
=--

A pullback characterisation of [[open geometric morphisms]] from Johnstone ([2006, cor. 4.9](#J06)):

+-- {: .num_prop}
###### Proposition
A [[geometric morphism]] $f:\mathcal{F}\to\mathcal{E}$ is open iff the pullback of any [[bounded geometric morphism]] with codomain $\mathcal{E}$ is skeletal.
=--

## Related entries

* [[open geometric morphism]]

* [[dominant geometric morphism]]

* [[proper geometric morphism]]

* [[double negation]]

* [[De Morganization]]

* [[De Morgan topos]]

## References

* [[Peter Johnstone]], _Factorization theorems for geometric morphisms II_ , pp.216-233 in LNM **915** Springer Heidelberg 1982.

* {#J02}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol.II_ , Oxford UP 2002. (section D4.6, pp.1006-1010)

* {#J06}[[Peter Johnstone]], _Complemented sublocales and open maps_ , Annals of Pure and Applied Logic **137** (2006) pp.240&#8211;255.

* {#Johnstone13}[[Peter Johnstone]], _The Gleason Cover of a Realizability Topos_ , TAC **28** no.32 (2013) pp.1139-1152. ([abstract](http://www.tac.mta.ca/tac/volumes/28/32/28-32abs.html))


[[!redirects skeletal geometric morphisms]]
[[!redirects skeletal morphism]]