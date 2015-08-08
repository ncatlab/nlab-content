
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

**Skeletal geometric morphisms** are those [[geometric morphisms]] that preserve [[double negation]] $\neg\neg$ and therefore play a role in characterizations of classes of toposes like e.g. [[Boolean topos|Boolean]] or [[De Morgan toposes]] in whose definitions the negation participates.

The notion of a skeletal geometric morphism can be viewed as a common generalization of the notions of [[dominant geometric morphism|dominant]] and [[open geometric morphisms]].

## Definition

A [[geometric morphism]] $f :  \mathcal{F} \to \mathcal{E}$ is called _skeletal_ if the following equivalent conditions hold:

* $f$ restricts to a geometric morphism $Sh_{\neg\neg}(\mathcal{F}) \to Sh_{\neg\neg}(\mathcal{E})$ .

* The [[inverse image]] $f^\ast$ preserves $\neg\neg$-dense monomorphisms.

* For any subobject $A'\rightarrowtail A$ in $\mathcal{E}$: $\neg\neg f^\ast(A')=\neg f^\ast(\neg A')$ in $Sub_\mathcal{F}(f^\ast(A))$.

## Example

* Inverse images of [[open geometric morphism|open geometric morphisms]] are [[Heyting functors]], hence commute with $\neg$ and, therefore, are skeletal.

* [[dense subtopos|Dense subtoposes]] $i:Sh_j(\mathcal{E})\hookrightarrow \mathcal{E}$ are characterized by $Sh_{\neg\neg}(Sh_j((\mathcal{E}))=Sh_{\neg\neg}(\mathcal{E})$ (cf. [this proposition](dense+subtopos#negdense)) and, therefore are skeletal.

## Properties

The following two propositions characterize skeletal [[geometric embedding|inclusions]] (cf. Johnstone ([2002, p.1007](#J02))):

+-- {: .num_prop}
###### Proposition
An inclusion $i:Sh_j(\mathcal{E})\hookrightarrow \mathcal{E}$ is skeletal iff $ext(j)$ , the $j$-closure of $0\rightarrowtail 1$ , is a $\neg\neg$-closed [[subterminal object]] of $\mathcal{E}$.
=--

+-- {: .num_prop}
###### Proposition
The class $\Sigma$ of skeletal [[geometric embedding|inclusions]] is the smallest class $\Gamma$ of geometric morphisms such that:

* $\Gamma$ contains [[open subtopos|open inclusions]] and,

* $\Gamma$ is closed under precomposition with [[dense subtopos|dense inclusions]]: from $g$ dense and $f\in\Gamma$ follows $fg\in\Gamma$.
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
* [[De Morgan topos]]

## References

* {#Johnstone80}[[Peter Johnstone]], _The Gleason Cover of a Topos I_ , JPAA **19** (1980) pp.171-192. 

* {#Johnstone81}[[Peter Johnstone]], _The Gleason Cover of a Topos II_ , JPAA **22** (1981) pp.229-247. 

* {#J02}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol.II_ , Oxford UP 2002. (section D4.6, pp.1006-1010)

* {#J06}[[Peter Johnstone]], _Complemented sublocales and open maps_ , Annals of Pure and Applied Logic **137** (2006) pp.240&#8211;255.

[[!redirects skeletal geometric morphisms]]
[[!redirects skeletal morphism]]