
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[formal logic]], a *logical connective* is a [[type formation]] rule which from given ([[sets]] and) [[propositions]] forms new [[propositions]].

For example, the logical connective "AND" combines a [[pair]] of propositions $P_1$, $P_2$ to a new proposition $P_1 \wedge P_2$.

To the extent that propositions are regarded as [[functions]] from [[sets]]/[[types]] $S$ (whose [[elements]]/[[terms]] they are propositions about) to the [[set]]/[[type]] of [[truth values]] (the [[type of propositions]])

$$
  \frac{
    \Gamma
    ,\;\;
    s \colon S 
    \;\;\;
    \vdash
    \;\;\;
    P(s) \colon Prop
  }{
    \Gamma
    \;\;\;
    \vdash
    \;\;\;
    P \,\colon\, S \to Prop
  }
$$

one may regard logical connectives as forming the resulting functions. This is what is expressed by the notorious *truth tables* of classical logic.


## Examples

[[!include logic symbols -- table]]

## Related concepts

* *the [intuitionistic interpretation of connectives](intuitionistic+logic#ConstructiveInterpretationOfConnectives)




[[!redirects logical connective]]
[[!redirects logical connectives]]
[[!redirects connectives]]
