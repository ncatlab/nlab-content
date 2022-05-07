
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

The notion of a skeletal geometric morphism can be viewed as a weakening of the notion of [[open geometric morphism]].

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

**Proof**: First, notice that in general for a topology $j$ a subterminal $U$ is $j$-closed iff it is a $j$-sheaf since $1$ is always a $j$-sheaf. Hence $0$ is $\neg\neg$-closed precisely when it is a $\neg\neg$-sheaf. 

Now assume $i$ skeletal. Since $ext(j)$ is a $\neg\neg$-sheaf in $Sh_j(\mathcal{E})$ and $i$ preserves them, it is also a $\neg\neg$-sheaf in $\mathcal{E}$.

Conversely, assume $ext(j)$ is a $\neg\neg$-sheaf in $\mathcal{E}$. Since it is also a $j$-sheaf, it is contained in $Sh_j(\mathcal{E})\cap Sh_{\neg\neg}(\mathcal{E})$ but this coincides with $Sh_{\neg\neg}(Sh_j(\mathcal{E}))$ because as a subtopos of the Boolean $Sh_{\neg\neg}(\mathcal{E})$ the intersection $Sh_j(\mathcal{E})\cap Sh_{\neg\neg}(\mathcal{E})$ is Boolean and $Sh_j(\mathcal{E})\cap Sh_{\neg\neg}(\mathcal{E})$, since it contains $ext(j)$, is dense in $Sh_j(\mathcal{E})$ and there can be only one such dense Boolean subtopos. $\qed$

+-- {: .num_prop}
###### Proposition
The class $\Sigma$ of skeletal [[geometric embedding|inclusions]] is the smallest class $\Gamma$ of geometric morphisms such that:

* $\Gamma$ contains [[open subtopos|open inclusions]] and,

* $\Gamma$ is closed under precomposition with [[dense subtopos|dense inclusions]]: from $g$ dense, $f\in\Gamma$ and $f,g$ composable, follows $fg\in\Gamma$. $\qed$
=--

The following exhibits the link between skeletal morphisms and Booleanness:

+-- {: .num_prop #Boolean_skeletal}
###### Proposition
A topos $\mathcal{E}$ is Boolean iff all geometric morphisms $\mathcal{F}\to\mathcal{E}$ to $\mathcal{E}$ are skeletal. 
=--

**Proof**:
When $\mathcal{E}$ is Boolean it coincides with $Sh_{\neg\neg}(\mathcal{E})$ hence $\neg\neg$-sheaves of $\mathcal{F}$ trivially have to land there.

Conversely, assume all $\mathcal{F}\to\mathcal{E}$ are skeletal. By [[Barr's theorem]], $\mathcal{E}$ receives a surjective $f:\mathcal{B}\to\mathcal{E}$ from a Boolean topos. $f$ being skeletal and surjective implies that $im(f)=\mathcal{E}$ is Boolean. $\qed$

A pullback characterisation of [[open geometric morphisms]] from Johnstone ([2006, cor. 4.9](#J06)):

+-- {: .num_prop}
###### Proposition
A [[geometric morphism]] $f:\mathcal{F}\to\mathcal{E}$ is open iff its pullback along any [[bounded geometric morphism]] with codomain $\mathcal{E}$ is skeletal. $\qed$
=--

## Remark

Skeletal morphisms between [[frame|frames]] are studied in [Banaschewski-Pultr (1994](#Banaschewski_Pultr94),[1996](#Banaschewski_Pultr96)), called _weakly open_ there.

The equivalent concept for topological spaces appears in [Mioduszewski-Rudolf (1969)](#Mioduszewski_Rudolf69).

It is possible to define an analogous concept of _m-skeletal geometric morphism_ using the [[De Morganization|De Morgan topology]] on a topos $\mathcal{E}$ instead of $\neg\neg$.

## Related entries

* [[open geometric morphism]]

* [[dominant geometric morphism]]

* [[proper geometric morphism]]

* [[double negation]]

* [[De Morganization]]

* [[De Morgan topos]]

## References

* {#Banaschewski_Pultr94}B. Banaschewski, A. Pultr, _Variants of openness_ , Appl. Cat. Struc. **2** (1994) pp.1-21.

* {#Banaschewski_Pultr96}B. Banaschewski, A. Pultr, _Booleanization_ , Cah. Top. G&#233;om. Diff. Cat. **XXXVII** no.1 (1996) pp.41-60. ([numdam](http://numdam.mathdoc.fr/numdam-bin/fitem?id=CTGDC_1996__37_1_41_0))

* [[Peter Johnstone]], _Factorization theorems for geometric morphisms II_ , pp.216-233 in LNM **915** Springer Heidelberg 1982.

* {#J02}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol.II_ , Oxford UP 2002. (section D4.6, pp.1006-1010)

* {#J06}[[Peter Johnstone]], _Complemented sublocales and open maps_ , Annals of Pure and Applied Logic **137** (2006) pp.240&#8211;255.

* {#Johnstone13}[[Peter Johnstone]], _The Gleason Cover of a Realizability Topos_ , TAC **28** no.32 (2013) pp.1139-1152. ([abstract](http://www.tac.mta.ca/tac/volumes/28/32/28-32abs.html))

* {#Mioduszewski_Rudolf69}J. Mioduszewski, L. Rudolf, _H-closed and extremally disconnected Hausdorff spaces_ , Dissertationes Math. **66** 1969. ([toc](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.desklight-99c47193-1b38-4485-9b3f-62fc71f8f83b))

[[!redirects skeletal geometric morphisms]]
[[!redirects skeletal morphism]]