
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

Much attention in [[coding theory]] is instead on the special class of *[[linear codes]]*, where $L$ and $P$ carry the structure of [[vector spaces]] (necessarily over a [[finite field]] if they are [[finite sets]] of relevance in practice) and where the inclusion $L \hookrightarrow P$ is a [[linear map]].



## Examples

* [[linear code]]

  * [[Hamming code]]
  
  * [[binary linear code]]

    * [[binary Golay code]]

* [[quantum error correcting code]]

  * [[bit flip code]]
  
  * [[stabilizer code]]

  * [[HaPPY code]]

  * [[Majorana dimer code]]

  * [[toric code]]

## References

### General

See also the references at *[[coding theory]]* and *[[linear code]]*.

* [[Victor V. Albert]] et al.,  *[errorcorrectionzoo.org](https://errorcorrectionzoo.org)*

* [[N. J. A. Sloane]], *Error-Correcting Codes and Cryptography*, The Mathematical Gardner, D. A. Klarner (editor), Prindle, Weber & Schmidt, Boston, MA, 1981, pp. 346-382, Reprinted in ``Cryptologia'', Vol. 6 (1982), 128-153 and 258-278.

An observation on classical codes preconceiving aspects of [[holographic tensor network]] [[quantum error correcting codes]]:

* [[Beni Yoshida]], *Information storage capacity of discrete spin systems*, Annals of Physics 338, 134 (2013) ([arXiv:1111.3275](https://arxiv.org/abs/1111.3275))



### Relation to 2d CFT

Construction of chiral [[2d SCFTs]] from error-correcting codes:

* [[Davide Gaiotto]], [[Theo Johnson-Freyd]], *Holomorphic SCFTs with small index*, Canadian Journal of Mathematics , **74** 2 (2022) 573-601  &lbrack;[arXiv:1811.00589](https://arxiv.org/abs/1811.00589), [doi:10.4153/S0008414X2100002X](https://doi.org/10.4153/S0008414X2100002X)&rbrack;


On their [[elliptic genera]]

* Kohki Kawabata, Shinichiro Yahagi, *Elliptic genera from classical error-correcting codes* &lbrack;[arXiv:2308.12592](https://arxiv.org/abs/2308.12592)&rbrack;



[[!redirects error correcting codes]]

[[!redirects error-correcting code]]
[[!redirects error-correcting codes]]

[[!redirects error correction]]
[[!redirects error corrections]]

[[!redirects error-correction]]
[[!redirects error-corrections]]
