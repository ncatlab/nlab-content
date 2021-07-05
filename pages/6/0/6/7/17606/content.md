
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _Platonic 2-group_ ([Epa 10](#Epa10)) is a [[2-group]] [[infinity-group extension|higher extension]] of a "Platonic group" in the [[ADE classification]], i.e. of a [[finite subgroup of SO(3)]]; or else of its [[double cover]], hence of [[finite subgroup of SU(2)]].

[[!include ADE -- table]]


## Properties

### Relation to the string 2-group
 {#RelationToTheString2Group}

+-- {: .num_prop #UniversalPlatonic2GroupIsRestrictionOfString2}
###### Proposition

The universal Platonic 2-group extensions $\mathcal{G}_{uni}[i]$ of  $G_{ADE}$ [[finite subgroups of SU(2)]] by $U(1)$ ([Epa-Ganter 16, def.2.11](#EpaGanter16)) are equivalently the restrictions of the [[string 2-group]] extension $String(SU(2)) \to SU(2)$ of $SU(2)$, hence the classifying [[cocycle]] is the restriction of the smooth [[second Chern class]]:

$$
  \array{
    \mathcal{G}_{uni}[i] 
      &\longrightarrow& 
    \mathbf{B}G_{ADE} 
      &\longrightarrow& 
    \mathbf{B}^3 \mathbb{Z}/{\vert G_{ADE}\vert}
    \\
    \big\downarrow 
      && 
    \big\downarrow 
      && 
    \big\downarrow^{\mathrlap{\mathbf{B}^3 i}}
    \\
    String(SU(2)) 
      &\longrightarrow& 
    \mathbf{B} SU(2) 
      &\underset{\mathbf{c}_2}{\longrightarrow}& 
    \mathbf{B}^3 U(1)
  }
  \,,
$$

where $i$ is the canonical inclusion of [[roots of unity]], $i: \mathbb{Z}/{|G|} \hookrightarrow U(1)$.

=--


([Epa-Ganter 16, prop. 4.1](#EpaGanter16))

See also at _[[finite subgroup of SU(2)]] -- [Discrete torsion](finite+rotation+group#DiscreteTorsion)_


## References

* {#Epa10} [[Narthana Epa]], _Platonic 2-groups_, 2010 ([[Epa_Platonic2Groups.pdf:file]])

* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, Higher Structures 1(1):122-146, 2017 ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192), [hs:30](https://journals.mq.edu.au/index.php/higher_structures/article/view/30))

[[!redirects Platonic 2-groups]]

[[!redirects platonic 2-group]]
[[!redirects platonic 2-groups]]
