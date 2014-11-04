[[!redirects ThCartSp]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Cohesive toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A [[site]] of [[formal smooth manifold|formal]] [[Cartesian spaces]].

## Definition

+-- {: .num_defn}
###### Definition

Let $FormalCartSp$ (or $FormalCartSp$) be the [[full subcategory]] of the category of [[smooth loci]] on those of the form 

$$
  \mathbb{R}^n \times \ell W
  \,,
$$

consisting of a [[product]] of a [[Cartesian space]] with an [[infinitesimally thickened point]], i.e. a formal dual of a _Weil algebra_ .

Dually, the [[opposite category]] is the [[full subcategory]] $FormalCartSp^{op} \hookrightarrow SmoothAlg$ of [[smooth algebras]] on those of the form

$$
  C^\infty( \mathbb{R}^k \times \ell W)
  = 
  C^\infty(\mathbb{R}^k) \otimes W
  \,.
$$

=--

This appears for instance in [Kock Reyes (1)](#KockReyes).

+-- {: .num_defn}
###### Definition

Define a structure of a [[site]] on [[FormalCartSp]] by declaring a [[covering]] family to be a family of the form

$$
  \{
    U_i \times \ell W \stackrel{p_i \times Id}{\to} U \times \ell W
  \}
$$

where $\{U_i \stackrel{p_i}{\to} U\}$ is an [[open cover]] of the [[Cartesian space]] $U$ by Cartesian spaces $U_i$. 

=--

This appears as [Kock (5.1)](#Kock). 

+-- {: .num_defn}
###### Definition


The **[[Cahiers topos]]** $\mathcal{CT}$ is the [[category of sheaves]] on this site:

$$
  \mathcal{CT} := Sh(FormalCartSp)  
  \,.
$$

=--

This site of definition appears in [Kock, Reyes](#KockReyes). The original definition is due to [Dubuc](#Dubuc)

+-- {: .num_defn}
###### Definition

The [[(∞,1)-topos]] of [[(∞,1)-sheaves]] over $FormalCartSp$ is that of _[[formal smooth ∞-grouopoids]]_

$$
  FormSmooth\infty Grpd \coloneqq Sh_\infty(FormalCartSp)
  \,.
$$

=--

## References

The Cahiers topos was introduced in 

* {#Dubuc} [[Eduardo Dubuc]], _Sur les mod&#232;les de la g&#233;om&#233;trie diff&#233;rentielle synth&#233;tique_ [[Cahiers]] de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 20 no. 3 (1979), p. 231-279  ([numdam](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)).
 

and got its name from this journal publication. The definition appears in theorem 4.10 there, which asserts that it is a well-adapted model for [[synthetic differential geometry]].

A review discussion is in section 5 of

* {#Kock} [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17  ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0))
  

and with a corrected definition of the site of definition in

* {#KockReyes} [[Anders Kock]], [[Gonzalo Reyes]], _Corrigendum and addenda to: Convenient vector spaces embed into the Cahiers topos_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17 ([numdam](http://www.numdam.org/item?id=CTGDC_1987__28_2_99_0))
 

