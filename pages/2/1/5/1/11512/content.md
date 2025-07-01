

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn} 
###### Definition

The [[profinite completion of a group|profinite completion]] of the [[integers]] is the [[inverse limit]]

$$
  \widehat{\mathbb{Z}} 
    \coloneqq 
  \underset{\leftarrow}{\lim}_{n \in \mathbb{N}} (\mathbb{Z}/n\mathbb{Z})
$$

of all the [[cyclic groups]] over their canonical [[filtered diagram]].

=--

+-- {: .num_prop #AsProductOverAlsoPAdicIntegers} 
###### Proposition

This is [[isomorphism|isomorphic]] to the [[product]] of the [[p-adic integers]] for all [[prime numbers]] $p$

$$
  \widehat{\mathbb{Z}} \simeq \underset{p\; prime}{\prod} \mathbb{Z}_p
  \,.
$$

=--

+-- {: .num_remark} 
###### Remark

From this perspective the concept of the [[ring of adeles]] is natural, see there for more.

=--

## Properties

### Pontryagin duality

Under [[Pontryagin duality]], $\hat \mathbb{Z}$ maps to $\mathbb{Q}/\mathbb{Z}$, see at _[[Pontryagin duality for torsion abelian groups]]_.

$$
  \array{
     &\mathbb{Z}[p^{-1}]/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{Q}/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{R}/\mathbb{Z}
     \\
     {}^{\mathllap{hom(-,\mathbb{R}/\mathbb{Z})}}\downarrow
     \\
     &\mathbb{Z}_p
     &\leftarrow&
     \hat \mathbb{Z}
     &\leftarrow&
     \mathbb{Z}
  }
$$

### Extension of $U(1)$

There exists an [[extension]] of $U(1)$ by the profinite integers $\widehat{\mathbb{Z}}$

$$
1 \to \widehat{\mathbb{Z}} \to S^1_{\mathbb{Q}} \to U(1) \to 1,
$$

called the *universal one–dimensional solenoid* or *adelic solenoid* $S^1_{\mathbb{Q}}$, which can be thought of as the limit of the $p$-fold covers of $U(1)=S^1$.

This extension is equivalently the quotient of the [[ring of adeles|adèle group]] of the [[rational numbers]] $A_{\mathbb{Q}}$ by $\mathbb{Q}$
$$
S^1_{\mathbb{Q}} = A_{\mathbb{Q}} / \mathbb{Q}.
$$

See ([Ramakrishnan and Valenza '99](#RV99)), and ([Burgos and Verjovsky '16](#BV16)) for more.


## Related concepts

* the [[modular group]]/[[general linear group]] with profinite integer coefficients $GL_2(\widehat{\mathbb{Z}})$ appears as the symmetry group in [[modular equivariant elliptic cohomology]].

## References

* {#Lenstra} [[Hendrik Lenstra]], example 2.2 in _Profinite groups_ ([pdf](http://websites.math.leidenuniv.nl/algebra/Lenstra-Profinite.pdf))
 
* [[Groupprops]], _[Profinite completion of the integers](http://groupprops.subwiki.org/wiki/Profinite_completion_of_the_integers)_

* {#RV99} Dinakar Ramakrishnan, Robert Valenza, *Fourier Analysis on Number Fields*. Graduate Texts in Mathematics 186, Springer-Verlag, New York, (1999). ([doi](https://doi.org/10.1007/978-1-4757-3085-2)).

* {#BV16} Juan Manuel Burgos, Alberto Verjovsky. *Adelic solenoid I: Structure and topology* (2016). ([arXiv:1603.05676](https://arxiv.org/abs/1603.05676)).

In the context of [[gauge theory]]:

* [[Pavel Putrov]]: *$\mathbb{Q}/\mathbb{Z}$ symmetry* &lbrack;[arXiv:2208.12071](https://arxiv.org/abs/2208.12071)&rbrack;




[[!redirects profinite integers]]