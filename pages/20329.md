

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #CentralProduct}
###### Definition
**([[central product]])**

Given two [[groups]] $G_1$ and $G_2$ and a joint [[subgroup]] 

\[
  \label{SubgroupInclusion}
  C \xhookrightarrow{\iota_i} Z(G_i)
\]

in each of their [[centers]], then the corresponding ("external") _central product_ is the [[quotient group]]

$$
  G_1 \circ G_2
  \;\coloneqq\;
  \big( 
    G_1 \times G_2
  \big)/_{diag} C
$$

of the [[direct product group]] $G_1 \times G_2$ by the [[diagonal]] subgroup $C \xhookrightarrow{(\iota_1, \iota_2)} G_1 \times G_2$.

=--

([Gorenstein 80, p. 29](#Gorenstein80))

+-- {: .num_remark #MaterialDefinition}
###### Remark
**([[structural set theory|structural]] over [[material set theory|material]] definition)**

Beware that most texts insists on stating the choices in Def. \ref{CentralProduct} as that of 

1. two separate subgroups $C_i \xhookrightarrow{\iota_i} Z(G_i)$ 

1. an [[isomorphism]] $C_1 \xrightarrow[\simeq]{\phi} C_2$ between them

and insists that the second groups as via $(-)^{-1}\circ \phi$

These clauses matter if one thinks of the subgroup inclusions as in [[material set theory]]. But we speak [[structural set theory]], which means that a [[subgroup]] inclusion as in (eq:SubgroupInclusion) is really a choice of _[[monomorphism|monic]] [[homomorphism]]_, and this choice already absorbs the choice of $\phi$ and or of $(-)^{-1}\circ \phi$.


=--

+-- {: .num_remark}
###### Remark
**(notation)**

Beware that there is no widely accepted convention for the notation of central products, and that most notational conventions suppress the choices of central subgroups involved.  The "$\circ$"-notation is popular in [[finite group]]-theory, while in [[Riemannian geometry]] people tend to use "$\cdot$" (see [[Sp(n).Sp(1)]]) or just plain juxtaposition, with no symbol for the central product at all.

=--


## Examples

### In Riemannian geometry and spin geometry

A [[Spin^c-group]] is a central product of a [[spin group]] with the [[circle group]].

Moreover, in [[Riemannian geometry]] and [[spin geometry]] one considers the central products [[Sp(n).Sp(1)]] and [[Spin(n).Spin(m)]].



## References

* {#Gorenstein80} D. Gorenstein, p. 29 of _Finite Groups_, New York (1980)

See also

* Wikipedia, _[Central product](https://en.wikipedia.org/wiki/Central_product)_

* GroupProps, _[External central product](https://groupprops.subwiki.org/wiki/External_central_product)_


[[!redirects central products of groups]]

[[!redirects external central product of groups]]
[[!redirects external central products of groups]]

[[!redirects internal central product of groups]]
[[!redirects internal central products of groups]]

[[!redirects central product group]]
[[!redirects central product groups]]

[[!redirects external central product group]]
[[!redirects external central product groups]]

[[!redirects internal central product group]]
[[!redirects internal central product groups]]

[[!redirects central product]]
[[!redirects central products]]

[[!redirects external central product]]
[[!redirects external central products]]

[[!redirects internal central product]]
[[!redirects internal central products]]


