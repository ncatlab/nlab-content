
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea ##

The notion of a _net of $C^*$-systems_ combines the notion of a [[C-star system]] with the notion of [[local net of observables]]. In this way, the notion of [[global gauge groups]] is introduced into the [[Haag-Kastler approach]] to [[AQFT]].

## Definition ##

Let $\mathcal{A}_I$ be a [[local net]] of [[C-star algebras]]. Let $G$ be a [[locally compact space|locally compact]] [[topological group]] and $\alpha_G$ a [[representation]] of $G$ on the quasi-local algebra $\mathcal{A}$, that is

$$
\mathcal{A} := clo_{\| \cdot \|} \bigl( \bigcup_{i \in I} \mathcal{A}_i \bigr) 
$$

so that $(\mathcal{A}, \alpha_G)$ is a [[C-star system]].

+-- {: .num_defn}
###### Definition 

The tuple $(\mathcal{A}_I, \alpha_G)$ is a **net of $C^*$-systems** if $\alpha_g(\mathcal{A}_i) \subseteq \mathcal{A}_i \; \forall g \in G$.

=--

In the context of [[Haag-Kastler nets]] the group $G$ is called the  
**[[global gauge group]]** and every [[automorphism]] $\alpha_g$ is called a **[[gauge transformation|gauge automorphism]]**.

This definition makes sense also if the net consists of [[star-algebras]] only, of course.

## Related concepts

* [[local net of observables]]

* [[field net]]

## References ##

Chapter 6 of:

* [[Hellmut Baumgärtel]], Manfred Wollenberg: _Causal nets of operator algebras._ Berlin: Akademie Verlag 1992 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0749.46038&format=complete))



[[!redirects net of C-star-systems]]
[[!redirects net of C-star systems]]
[[!redirects net of C*-systems]]

[[!redirects nets of C-star-systems]]
[[!redirects nets of C-star systems]]
[[!redirects nets of C*-systems]]
