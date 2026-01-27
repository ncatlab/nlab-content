

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--



> (under construction)




\tableofcontents

## Idea

The [[category]] of [[small category|small]] additive [[presheaves of abelian groups]] on an [[additive category]] contains a [[subcategory]] of finitely presented (that is [[compact object|compact]]) [[objects]]. This subcategory
has a nice [[universal property]].

## Definition

### Freyd's definition

Let $C$ be an [[additive category|additive]] [[subcategory]]. An additive presheaf is *finitely presented* if it is a [[cokernel]] of a [[morphism]] of [[representables]]. The [[full subcategory]] of object parts of these cokernels is $A(C)$, the *Freyd abelianization* of $C$ ([Freyd 1966](#Freyd1966)).

Thus, an object $x$ of $A(C)$ is a presheaf such that there exist an [[exact sequence]] of presheaves of abelian groups of the form
$$
  Hom(-,a) 
    \longrightarrow 
  Hom(-,b) 
    \longrightarrow 
  x 
    \longrightarrow 
  0
  \mathrlap{\,,}
$$
where $a,b$ are objects in $C$. In the case where $C$ is abelian already, finitely presentable additive presheaves of abelian groups were studied under the name of __coherent functors__ by Auslander. They are automatically coherent objects in the functor category, namely each finitely generated subobject of a finitely presentable functor is finitely presentable as well. Moreover, for $C$ small abelian, coherent functors are also projective. 

### Verdier's definition

[Verdier 1967](#Verdier1967) has reformulated $A(C)$ without a recourse to presheaves. He considers the (additive) [[arrow category]] $Arr(C)$ of $C$ and inside it, the morphisms which he calls *negligible*.

A morphism 
$$
  (g \colon  X \to Y,\, h \colon X'\to Y')
    \colon
  (f \colon  X \to X')
    \longrightarrow
  (g \colon Y \to Y')
$$ 
is *negligible* if the [[compositions]] $h f = f' g = 0$
are [[null morphisms]]. For any [[pair]] $(f,f')$ of arrows, the negligible morphisms $f\to f'$ form a [[subgroup]].

Now, the objects of $A(C)$ are the objects of the [[arrow category]], while the morphisms are the morphisms among the arrows modulo the negligible morphisms (that is the elements of the [[quotient group]]). Therefore, $C$ embeds in $Arr(C)$ as $X\mapsto id_X$, which projects $Hom$-wise to $A(C)$. For any fixed additive category $E$, the functor $C\to A(C)$ induces a functor
$$
  Additive\big(A(C),E\big)
    \longrightarrow 
  Additive(C,E)
  \mathrlap{\,.}
$$


## Literature

* {#Freyd1966} Freyd 1966

* {#Verdier1967} Verdier 1967

* Neeman

The category of coherent functors over an abelian category was studied in

* M. Auslander, _Coherent functors_, In: Eilenberg, S., Harrison, D.K., MacLane, S., Röhrl, H. (eds) Proceedings of the Conference on Categorical Algebra, La Jolla 1965, Springer, 1966.

Finitely presented additive functors on abelian categories with values in abelian groups are the topic of Ch. 10 in 

* Mike Prest, _Purity, spectra and localization_, Enc. Math. Appl. 112 (2009)



