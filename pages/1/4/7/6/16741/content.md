

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects demorganization]]
[[!redirects DeMorganization]]
[[!redirects de Morganization]]
[[!redirects De Morganisation]]
[[!redirects De Morgan topology]]
[[!redirects de Morgan topology]]
[[!redirects DeMorgan topology]]


## Idea

The **De Morganization** of a [[topos]] $\mathcal{E}$ is a universal way to turn $\mathcal{E}$ into a [[de Morgan topos]] $Sh_m(\mathcal{E})$ with the use of a certain [[Lawvere-Tierney topology]] $m$, called the **De Morgan topology** on $\mathcal{E}$.

This can be viewed as an analogue to the Booleanization $Sh_{\neg\neg}(\mathcal{E})$ of $\mathcal{E}$ with the help of the [[double negation|double negation topology]] $\neg\neg$ .

## Definition

Let $\mathcal{E}$ be a [[topos]]. The _De Morgan topology_ $m$ on $\mathcal{E}$ is defined as the smallest [[Lawvere-Tierney topology]] $j$ such that the canonical monomorphism $(\top,\bot): 1\coprod 1\rightarrowtail \Omega_{\neg\neg}$ is $j$-dense. The _De Morganization_ of $\mathcal{E}$ is the associated topos $Sh_m(\mathcal{E})$ of $m$-sheaves.

### Remark

Here $\Omega_{\neg\neg}$ denotes the [[subobject classifier]] for $Sh_{\neg\neg}(\mathcal{E})$ with $\neg\neg$ the [[double negation|double negation topology]] on $\mathcal{E}$. The De Morgan topology $m$ is well-defined due to _Joyal's lemma_ (cf. [Johnstone 1977](#Johnstone77), p.99; or [Johnstone 2002](#Johnstone), p.215). Compare its definition to this [proposition](double+negation#smallest_j-dense) about $Sh_{\neg\neg}(\mathcal{E})$ .

## Example

+--{: .num_prop}
###### Proposition
The De Morganization of the [[classifying topos]] for the theory of [[field|fields]] is the classifying topos for the geometric theory of fields of finite characteristic, in which every element is algebraic over the [[prime field]].
=--

This is proposition 2.3 in [Caramello-Johnstone (2009)](#CJ09).

## Properties

+--{: .num_prop}
###### Proposition
The De Morgan topology $m$ is the [[dense subtopos|smallest dense topology]] $j$ on $\mathcal{E}$ , i.e. $j\leq \neg\neg$ , such that $Sh_j(\mathcal{E})$ is a [[De Morgan topos]].
=--

This appears as theorem 1 in [Caramello (2009)](#Caramello09). In other words, $Sh_{m}(\mathcal{E})$ is the _largest dense De Morgan subtopos_ of $\mathcal{E}$


+--{: .num_prop #DeMorgan_mono}
###### Proposition
The De Morgan topology $m$ is the smallest [[Lawvere-Tierney topology|topology]] $j$ on $\mathcal{E}$ such that all monomorphisms of the form $\neg A\vee\neg\neg A\rightarrowtail E$ for subobjects $A\rightarrowtail E$ in $\mathcal{E}$ are $j$-dense.
=--

This appears as proposition 6.2 in [Caramello (2012a)](#Caramello12a).

+--{: .num_prop #DeMorgan_prop}
###### Proposition
Let $\mathcal{E}$ be a [[topos]] and $m$ be the De Morgan topology on it.

* $Sh_m(\mathcal{E})=\mathcal{E}$ iff $\mathcal{E}$ is a [[De Morgan topos]].

* For any [[dense subtopos|dense topology]] $j$ on $\mathcal{E}$ , $Sh_m(Sh_j(\mathcal{E}))=Sh_{m\vee j}(\mathcal{E})$.
=--

[Caramello (2009)](#Caramello09), prop.1.5. In fact, in the second statement it suffices to demand that $j$ is a [[weakly open topology]] i.e. the [[associated sheaf functor]] $a_j:\mathcal{E}\to Sh_j(\mathcal{E})$ preserves the pseudo-complementation operator in the lattices of subobjects (cf. [Caramello (2012, prop.4.5)](#Caramello12)).

Notice that $Sh_{m\vee j}(\mathcal{E})=Sh_{m}(\mathcal{E})\cap Sh_{ j}(\mathcal{E})$ and, accordingly, for a dense or, more generally a weakly open subtopos De Morganization simply amounts to intersection with $Sh_m(\mathcal{E})$.

## Geometric morphisms preserving De Morganizations

Notice that in analogy to $Sh_{\neg\neg}(\mathcal{E})$ and the class of [[skeletal geometric morphism]], the universality of the De Morganization affords to define a class of **m-skeletal geometric morphisms** as those geometric morphisms $f:\mathcal{F}\to\mathcal{E}$ that restrict to geometric morphisms $f|_m:Sh_m(\mathcal{F})\to Sh_m(\mathcal{E})$ .

Due to a result in [Johnstone (2002, p.194)](#Johnstone), this is equivalent to the preservation of $m$-dense monomorphisms by $f^\ast$.

By the [above proposition](#DeMorgan_prop), $Sh_m(Sh_{j}(\mathcal{E}))\hookrightarrow Sh_{m}(\mathcal{E})$ for $j$ dense. Accordingly, _dense inclusions_ $Sh_{j}(\mathcal{E})\hookrightarrow\mathcal{E}$ are m-skeletal !

The [characterization of Boolean toposes by skeletal morphisms](http://ncatlab.org/nlab/show/skeletal+geometric+morphism#Boolean_skeletal) carries over to m-skeletal morphisms and De Morgan toposes:

+--{: .num_prop #DeMorgan_m-skeletal}
###### Proposition
A topos $\mathcal{E}$ is De Morgan iff every geometric morphism $\mathcal{F}\to\mathcal{E}$ is m-skeletal.
=--

**Proof**:
Assume $\mathcal{E}$ is De Morgan, then it coincides with $Sh_m(\mathcal{E})$ and $m$-sheaves of $\mathcal{F}$ necessarily have to land there.

Conversely, assume all $\mathcal{F}\to\mathcal{E}$ are m-skeletal. Then the surjective morphism $f:\gamma\mathcal{E}\to\mathcal{E}$ from the [[De Morgan topos|Gleason cover]] $\gamma\mathcal{E}$ is m-skeletal. But $\gamma\mathcal{E}$ is De Morgan and, therefore, so is $im(f)=\mathcal{E}$. $\qed$


## Related entries

* [[De Morgan topos]]

* [[De Morgan Heyting algebra]]

* [[double negation]]

* [[dense subtopos]]

* [[dense topology]]

* [[skeletal geometric morphism]]

## References

* Igor Arrieta, _The DeMorganization of a Locale_ , arXiv:2406.12486 (2024). ([abstract](https://arxiv.org/abs/2406.12486))

* {#Caramello09}[[Olivia Caramello]], _De Morgan classifying toposes_ , Adv. in Math. **222** (2009) pp.2117-2144. ([arXiv:0808.1519](http://arxiv.org/abs/0808.1519))

* {#Caramello12a}[[Olivia Caramello]], _Universal models and definability_ , Math. Proc. Cam. Phil. Soc. (2012) pp.279-302. ([arXiv:0906.3061](http://arxiv.org/abs/0906.3061))

* {#Caramello12}[[Olivia Caramello]], _Topologies for intermediate logics_ , arXiv:1205.2547 (2012). ([arXiv:1205.2547](http://arxiv.org/abs/1205.2547))

* {#CJ09}[[Olivia Caramello]], [[Peter Johnstone]], _De Morgan's law and the Theory of Fields_ , Adv. in Math. **222** (2009) pp.2145-2152. ([arXiv:0808.1572](http://arxiv.org/abs/0808.1972))

* {#Johnstone77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint New York 2014)

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. I_, Oxford UP 2002.


