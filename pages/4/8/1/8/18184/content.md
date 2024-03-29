
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

<div style="float:right;margin:0 10px 10px 0;"><img src="http://ncatlab.org/nlab/files/AttachingSpace.jpg" width="400"></div>

In [[topology]], the result of a _space attachment_ (sometimes called an _attaching space_ or _adjunction space_) is a [[topological space]], denoted $X \cup_{f} Y$, which is constructed by "attaching" or "gluing" two topological spaces $X$ and $Y$ along a [[topological subspace]] $A \subset X$ by means of a [[continuous function]] $f \colon A \to Y$. The function $f$ is then called the _attaching map_. 

> (graphics taken from [AGP08, §3.1](#AGP08))

More [[category theory|abstractly]], space attachments are [[pushouts]] along [[monomorphisms]] in the [[category]] [[Top]] of all [[topological spaces]]. The [[formal dual|formally dual]] concept is that of [[fiber]] spaces or more generally of [[fiber products]] of topological spaces.

## Definition

Let $X,Y \in Top$ be [[topological spaces]], let $A \subset X$ be a [[topological subspace]] and let $f \colon A \to Y$ be a [[continuous function]].
 
Then the _attaching space_ $X \cup_f Y \in Top$ may be realized as the [[quotient topological space]] of the [[disjoint union space]] $X \sqcup Y$ by the [[equivalence relation]] which identifies a point $x \in A \subset X$ with its [[image]] $f(x) \in Y$:


$$
  X \cup_f Y
  \;\simeq\;
  \left(
    X \sqcup Y
  \right)/\sim
  \,.
$$

More [[category theory|category theoretically]], the attaching space is the [[pushout]] in the [[category]] [[Top]] of [[topological spaces]] of the subspace inclusion $i \colon A \hookrightarrow X$ along $f$, i.e. the topological space which is [[universal property|universal]] with the property that it makes the following [[commuting square|square commute]]:

$$
  \array{
    A &\overset{\phantom{A}i\phantom{A}}{\hookrightarrow}& X
    \\
    {}^{\mathllap{f}}\downarrow &(po)& \downarrow
    \\
    Y &\longrightarrow& X \cup_f Y
  }
  \,.
$$

For more on this see at _[Top -- Universal constructions](Top#UniversalConstructions)_.

## Examples

* In forming topological [[cell complexes]] such as [[CW-complexes]], one consecutively forms space attachments along [[n-sphere|(n-1)-sphere]] inclusions as [[boundaries]] of [[n-disks]]. These are called _cell attachments_.




## Related concepts

[[!include universal constructions of topological spaces -- table]]

* [[Whitehead product]]

## References

* {#AGP08} [[Marcelo Aguilar]], [[Samuel Gitler]], [[Carlos Prieto]], §3.1 in: *Algebraic topology from a homotopical viewpoint*, Springer (2008) &lbrack;[doi:10.1007/b97586](https://link.springer.com/book/10.1007/b97586)&rbrack;

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Chapter 17, p. 217 of:  _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics **82**, Springer (1982) &lbrack;[doi:10.1007/978-1-4757-3951-0](https://link.springer.com/book/10.1007/978-1-4757-3951-0)&rbrack;

See also

* Wikipedia, _[Adjunction space](https://en.wikipedia.org/wiki/Adjunction_space)_

[[!redirects space attachments]]

[[!redirects attaching space]]
[[!redirects attaching spaces]]

[[!redirects attaching map]]
[[!redirects attaching maps]]

[[!redirects adjunction space]]
[[!redirects adjunction spaces]]

[[!redirects cell attachment]]
[[!redirects cell attachments]]

[[!redirects attachment space]]
[[!redirects attachment spaces]]
