
#Contents#
* table of contents
{:toc}

## Definition

### Of the modular group

Let $n \in \mathbb{N}$ be a [[natural number]]. Write

$$
  p_n \;\colon\; SL_2(\mathbb{Z}) \to SL_2(\mathbb{Z}/n\mathbb{Z})
$$

for the [[projection]] from the [[Moebius group|Moebius]] [[special linear group]] [[SL(2,Z)|$SL(2,\mathbb{Z}$]] induced by the [[quotient]] [[projection]] $\mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$ to the [[integers modulo n]].

The _mod-$n$ congruence subgroups_ of the [[special linear group]] $SL_2(\mathbb{Z})$ (essentially the [[modular group]]) are the [[preimages]] under $p_n$ of [[subgroups]] of $SL_2(\mathbb{Z}/n\mathbb{Z})$.

Some of these have traditional names and symbols;

The **principal congruence subgroup** is the preimage of the trivial group:

$$
  \Gamma(n) \coloneqq ker(p_n) = p_n^{-1}\left(\left\{\array{ 1 & 0 \\ 0 & 1}\right\}\right)
  \,.
$$

This is the origin of the term: the elements of $\Gamma(n)$ are _congruent [[modular arithmetic|modulo]] $n$_ to the identity. 


The other two congruence subgroups having special symbols are

$$
  \Gamma_0(n) \coloneqq p_n^{-1}\left(\left\{\array{ \ast & \ast \\ 0 & \ast}\right\}\right)
$$

$$
  \Gamma_1(n) \coloneqq p_n^{-1}\left(\left\{\array{ 1 & \ast \\ 0 & \ast}\right\}\right)
$$

## Properties

### Relation to spin structures

See at _[level structure -- relation to spin structure](level%20structure%20on%20an%20elliptic%20curve#RelationToSpinStructures)_.

## Examples

* [[level n subgroup]] of the [[modular group]]

## Related concepts

* [[Torelli group]]

* [[modular curve]]

* [[modular equivariant elliptic cohomology]]

## References

* [[Andrew Putman]]: *The Torelli group and congruence subgroups of the mapping class group*, in: *Moduli Spaces of Riemann Surfaces*, IAS/Park City Mathematics Series **20** (2013) &lbrack;[arXiv:1201.3946](https://arxiv.org/abs/1201.3946), [doi:10.1090/pcms/020](https://doi.org/10.1090/pcms/020)&rbrack;

See also:

* Wikipedia, _[Congruence subgroup](https://en.wikipedia.org/wiki/Congruence_subgroup)_

A list of congruence subgroups is provided in

* [[Sebastian Pauli]], _[Congruence subgroups of PSL(2,Z)](http://www.uncg.edu/mat/faculty/pauli/congruence/)_


[[!redirects congruence subgroups]]

[[!redirects principal congruence subgroup]]
[[!redirects principal congruence subgroups]]