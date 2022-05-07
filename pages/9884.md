
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

The relative version of the notion of [[(∞,1)-limit]].

## Definition

+-- {: .num_defn}
###### Definition

For $f \colon \mathcal{C} \to \mathcal{D}$ an [[(∞,1)-functor]] between [[(∞,1)-categories]] which is presented by an [[inner fibration]] of [[quasi-categories]] (which we denote by the same symbols), and for

$$
  \overline{p} \colon K^{\ast} \to \mathcal{C}
$$

a [[cocone]] [[diagram]] in $\mathcal{C}$ over the $K$-shaped [[diagram]]

$$
  p \coloneqq \overline{p}|K
  \,,
$$

then $\overline{p}$ is an **$(\infty,1)$-colimiting** cocone if the canonical map

$$
  \mathcal{C}_{\overline{p}/}
  \to 
  \mathcal{C}_{p/}
  \underset{\mathcal{D}_{f p /}}{\times}
  \mathcal{D}_{f\overline{p}/}
$$

(from the [[slice (∞,1)-category|co-slice quasi-category]])
is an [[acyclic Kan fibration]] of [[simplicial sets]].

=--

([Lurie, def. 4.3.1.1](#Lurie))

## Examples

 - If $\mathcal{D} = \Delta[0]$ is the terminal category and $f: \mathcal{C} \to \Delta[0]$ is the unique functor, then an $f$-colimit is the same thing as a colimit in the usual sense.

 - If $K = \Delta[0]$ is the terminal category so that $p: \Delta[0] \to \mathcal{C}$ picks out an object and $f\overline{p}: K^{\triangleright} = \Delta[1] \to \mathcal{D}$ picks out an edge, an $f$-colimit is precisely an $f$-cocartesian lift.

## References

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}


[[!redirects relative (infinity,1)-limits]]

[[!redirects relative (∞,1)-limit]]
[[!redirects relative (∞,1)-limits]]

[[!redirects relative (infinity,1)-colimit]]
[[!redirects relative (infinity,1)-colimits]]

[[!redirects relative (∞,1)-colimit]]
[[!redirects relative (∞,1)-colimits]]

