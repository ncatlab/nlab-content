


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[higher algebra]] a _higher central extension_ of some algebraic object should be a higher analog of a [[central extension]], hence a [[higher extension]] by something in the higher analog of the [[center]]. What exactly "higher center" should mean is subject to some choices, see for instance _[[center of an ∞-group]]_.

But there is an easily identified sub-class of higher extensions that should definitely count as _higher central extensions_:

For $G$ a [[group]], an ordinary [[central extension]]

$$
  1 \to A \longrightarrow \widehat G \longrightarrow G \to 1
$$

may equivalently be thought of, via the [[homotopy theory]] of [[∞-groups]], as part of the [[long homotopy fiber sequence]]

$$
  \array{
    A &\longrightarrow& \widehat G
    \\
    && \Big\downarrow
    \\
    && G &\overset{c_2}{\longrightarrow}& B A
  }
$$

where $B A$ is the [[delooping]] [[2-group]] of $A$, and where $c_2 \;\colon\; G \longrightarrow B A$ is the [[cocycle]] which classifies the central extension.

Equivalently, under further [[delooping]] this is the [[long homotopy fiber sequence]] of the form

$$
  \array{
    B A &\longrightarrow& B \widehat G
    \\
    && \Big\downarrow
    \\
    && B G &\overset{c_2}{\longrightarrow}& B^2 A
  }
$$

which makes explicitl that $c_2$ is a _2-cocycle_.

Phrased this way it is clear that a concept of _higher central extension_ of an [[∞-group]] $G$ should subsume at least those [[long homotopy fiber sequence]] of the form

$$
  \array{
    B^{p+1} A &\longrightarrow& B \widehat G
    \\
    && \Big\downarrow
    \\
    && B G &\overset{c_{p+2}}{\longrightarrow}& B^{p+2} A
  }
$$

where now $c_{p+2}$ is the classifying $(p+2)$-cocyle.

This concept makese sense not just for [[∞-groups]] in any [[(∞,1)-topos]], but also for instance for ([[nLab:super L-∞ algebra|super]]) [[L-∞ algebras]].

## Examples

* [[higher central ∞-group extension]]

* [[L-∞ algebra extension]]

## Related concepts

* [[universal higher central extension]]

* [[infinity-Lie algebra cohomology]]

## References

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], section 4.3 of  _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal infinity-bundles - General theory]]_, Journal of Homotopy and Related Structures, Volume 10, Issue 4 (2015) ([arXiv:1207.0248](https://arxiv.org/abs/1207.0248))

[[!redirects higher central extensions]]
