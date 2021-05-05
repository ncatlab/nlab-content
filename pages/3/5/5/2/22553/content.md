
#Contents#
* table of contents
{:toc}

## Idea

In [[coding theory]], an *error correcting code* is a means to encode data in a way that is robust against errors ([[noise]]).

Very broadly, for $L$ a [[finite set]] playing the role of a [[space of states]] that is to be saved/communicated/analyzed, an error correcting code for $L$ is an [[injection]] $L \overset{\;\;\;}{\hookrightarrow} P$ into a larger set. The idea is that noise/errors move the image of $L$ within $P$, but if $P$ is large enough and the embedding chosen well enough, then a sufficiently small number of errors stays within a small neighbourhood of $L$ in $P$ that allows to [[retraction|retract]] back to $L$.

The simplest example is the *repetition code*, where the inclusion is the [[diagonal]] on the $n$-fold [[Cartesian product]] 

$$
  \array{
  L 
  &
    \overset{diag}{\hookrightarrow}
  & 
  P \coloneqq \underset{n \; factors}{\underbrace{L \times \cdots \times L}}
  \\
  \ell &\mapsto& (\ell, \cdots, \ell)
  }
  \,.
$$

This code "protects against $n/2-1$ errors" in an evident sense.

More concretely, much attention in [[coding theory]] is on the special lass of *[[linear codes]]*, where $L$ and $P$ carry the structure of [[vector spaces]] (necessarily over a [[finite field]] if they are [[finite sets]] or relevance in practice) and where the inclsion $L \hookrightarrow P$ is a [[linear map]].

## Examples

* [[linear code]]

  * [[Hamming code]]
  
  * [[binary linear code]]

    * [[binary Golay code]]

* [[quantum error correcting code]]

  * [[HaPPY code]]

  * [[Majorana dimer code]]

## References

See at *[[coding theory]]* and *[[linear code]]*.

[[!redirects error correcting codes]]
[[!redirects error-correcting code]]
[[!redirects error-correcting codes]]

[[!redirects error correction]]
[[!redirects error corrections]]
[[!redirects error-correction]]
[[!redirects error-corrections]]
