

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[quantum computing]] and [[quantum information theory]], the notion of *quantum random access memory* (QRAM, due to [Giovanettiy, Lloyd & Maccone 2008](#GiovanettiyLloydMaccone08)) is meant to be the [[quantum physics|quantum]]-analog of the [[classical physics|classical]] notion of [[random access memory]]; the key point being that QRAM may be addressed by *[[quantum superpositions]]* of address values and then reads/writes the corresponding [[quantum superposition]] of quantum data ([GLM08, (1)](#GiovanettiyLloydMaccone08)).

The (original and followup) references on QRAM are somewhat vague on the precise intended operational definition. But recall that a classical random access memory of [[data type]] $Mem$ is modeled (in terms of [[monads in computer science]]) by the [[state monad]] induced from the *[[cartesian monoidal category|cartesian]]* [[internal hom]]-[[adjoint functor|adjunction]] 

* [[product]]$\;$ $Mem \times (-) \;\;\dashv\;\; Maps(Mem, -)$ $\;$[[function set]]

namely:

$$
  RAM(Mem,A)
  \;\coloneqq\;
  Maps
  \big(
    Mem
    ,\,
    Mem 
    \times 
    A
  \big)
  \,.
$$

(Notice that in concrete applications people often insist that  $Mem =$ [[Bool]]${}^{\times^n}$, but the conceptual nature of RAM is indifferent to this choice.)

Now, with classical data types (such as [[bits]]) replaced by quantum data types (such as [[qbits]]), namely by *[[linear types]]*, the analogous [[internal hom]]-[[adjoint functor|adjunction]] is 

* [[tensor product]]$\;$ $ QMem \otimes (-) \;\;\dashv\;\; LinMaps(QMem, - )$ $\;$[[linear space]]-of-[[linear maps]]

and the corresponding [[monad]] is

$$
  QRAM(Mem,A)
  \;\coloneqq\;
  LinMaps
  \big(
    QMem
    ,\,
    QMem 
    \otimes
    A
  \big)
$$

and it seems clear that this does correspond to the intended behaviour of QRAM (where we are free to set $QMem \coloneqq $ [[QBit]]${}^{\otimes^n}$, if desired, which is typically the case in the literature).

In particular, the intended equivalence between the "QRAM model" and the "[[quantum circuit]]-model" of [[quantum computation]] is just the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the linear [[internal hom]]-[[adjunction]]

$$
  \Big\{
  In 
  \longrightarrow
  LinMaps
  \big(
    QMem
    ,\,
    QMem 
    \otimes
    Out
  \big)
  \Big\}
  \;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;  
  \Big\{
  In \otimes QMem
  \longrightarrow
  Out \otimes QMem
  \Big\}
  \,.
$$

## References

The terminology "quantum random access memory" is due to

* {#GiovanettiyLloydMaccone08} [[Vittorio Giovannetti]], [[Seth Lloyd]], [[Lorenzo Maccone]], *Quantum random access memory*, Phys. Rev. Lett. **100** 160501 (2008) &lbrack;[doi:10.1103/PhysRevLett.100.160501](https://doi.org/10.1103/PhysRevLett.100.160501), [arXiv:0708.1879](https://arxiv.org/abs/0708.1879)&rbrack;

but it could be argued (?) that the notion is implicit already in [Knill (1996)](quantum+programming+language#Knill96).

Further development:

* {#GiovanettiyLloydMaccone08b} [[Vittorio Giovannetti]], [[Seth Lloyd]], [[Lorenzo Maccone]], *Architectures for a quantum random access memory*, Phys. Rev. A **78** 052310 (2008) &lbrack;[doi:10.1103/PhysRevA.78.052310](https://doi.org/10.1103/PhysRevA.78.052310)&rbrack;

[[!redirects QRAMs]]

[[!redirects quantum RAM]]
[[!redirects quantum RAMs]]

[[!redirects quantum random access memory]]
[[!redirects quantum random access memories]]

[[!redirects quantum memory]]

