+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[model category]] structure $M_1$ is a 
[[right Bousfield localization]] of a model structure $M_2$ on the same
underlying [[category]] if $M_1$ and $M_2$ have the same [[fibrations]]
and the [[weak equivalences]] of $M_1$ contain those
of $M_2$

The notion of _right Bousfield delocalization_ reverses this relation: $M_1$ is a right Bousfield delocalization of $M_2$ if $M_2$ is a right Bousfield localization of $M_1$.

Of course, the nontrivial task here
is to establish interesting existence criteria
for right Bousfield delocalizations.

## Existence theorem

+-- {: .num_theorem}
###### Theorem (Corrigan-Salter)

If $M_1$ and $M_2$ are two [[cofibrantly generated model category]]
structures on the same category with coinciding classes of fibrations,
then there is a third cofibrantly generated model structure $M_3$ with the same fibrations and whose weak equivalences are the [[intersection]] of weak equivalences in $M_1$ and $M_2$. This model structure is a right Bousfield delocalization
of both $M_1$ and $M_2$.

=--

([Corrigan-Salter 15](#CS15))

## Related entries

* [[right Bousfield localization]]

* [[colocalization]]

## References

* {#CS15} [[Bruce Corrigan-Salter]], _Right delocalization of model categories_, [arXiv:1504.04545](http://arxiv.org/abs/1504.04545).