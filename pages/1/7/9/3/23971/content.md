
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[zigzag persistence|zig-zag]] [[persistent homology]]-theory, the *diamond principle* ([Carlsson & de Silva 2010, Sec. 5.2](#CarlssonDeSilva10)) states that [[persistence diagrams]] of [[pairs]] of [[zigzag persistence modules]] are [[bijection|bijective]] if the modules coincide away from two consecutive [[edges]] where their difference forms an "exact diamond".

Applied specifically to [[persistence modules]] given by the [[homology groups]] of [[zig-zags]] of [[topological spaces]], the diamond principle is an incarnation of the [[Mayer-Vietoris sequence]] in [[algebraic topology]]. 

In this case it says that the two canonical [[zigzag persistence modules]] associated with a [[filtered topological space]] (one built from [[union]]-[[zigzags]], the other from [[intersection]]-[[zigzags]]) in fact yield the same [[persistence diagrams]].

Notice how the diamond principle is a result genuinely about persistent invariants, in that the two persistence modules forming an exact diamond do not have the same shape as [[diagrams]] and hence are *non-comparable* when regarded, say, as [[quiver representations]] (since they are [[objects]] of *distinct* [[categories]]).



## Related concepts

* [[stability of persistence diagrams]]


## References

The diamond principle originates in 

* {#CarlssonDeSilva10} [[Gunnar Carlsson]], [[Vin de Silva]], Section 5.2 of *Zigzag Persistence*, Found Comput Math **10** (2010) 367–405 $[$[arXiv:0812.0197](https://arxiv.org/abs/0812.0197), [doi:10.1007/s10208-010-9066-0](https://doi.org/10.1007/s10208-010-9066-0)$]$

Review:

* [[Sara Kališnik]], Sections 1.3-1.4 in: *Persistent homology and duality* (2013) ([pdf](http://www.matknjiz.si/doktorati/2013/Kalisnik-14521-4.pdf), [[KalisnikPersistent.pdf:file]])


[[!redirects diamond principles]]
