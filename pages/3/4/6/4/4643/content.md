
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Langlands correspondence
+--{: .hide}
[[!include Langlands correspondence -- contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _quantum geometric Langlands correspondence_ is a conjectured equivalence between the [[derived category]] of certain twisted [[D-module]]s on the [[moduli stack]] of $G$-[[principal bundle]]s over some complex curve for some [[reductive group]] $G$, and that of $D$-modules with a dual twist on the stack of ${}^L G$-bundles, for ${}^L G$ the [[Langlands dual group]].

In a certain limit of the twisting parameter the $D$-modules on one side of this correspondence become equivalent to just $\mathcal{O}$-modules, but on the moduli space of [[local system]]s. This limit of the quantum correspondence reproduces the statement of the (ordinary) [[geometric Langlands correspondence]].


Slightly more precisely, writing $Bun_G^\circ$ for the connected component of the moduli stack of $G$-bundles, there is a [[line bundle]] denoted $\mathcal{L}^{\otimes k}$ on $Bun_G^\circ$ and dually a line bundle $\hat \mathcal{L}^{\otimes k}$ on $Bun_{{}^L G}^\circ$ and these serve to defined sheaves $\mathcal{D}^{(k,\lambda)}$ of twisted differential operators on $Bun_{G}^\circ$ and dually sheaves $\hat \mathcal{G}^{(k,\lambda)}$ of twisted differential operators on $Bun_{{}^L G}^\circ$, where the parameters lie in

$$
  (k, \lambda) \in \mathbb{CP}^1 \times \mathbb{C}
  \,.
$$

Writing then $\mathcal{D}^{k,\lambda} Mod(Bun_{G})$ and $\hat \mathcal{D}^{k,\lambda} Mod(Bun_{{}^L G})$, respectively, for the derived categories of modules over these sheaves, the conjectured statement is:

**Quantum geometric Langlands correspondence**

There is an equivalence

$$
  \mathcal{D}^{k,\lambda} Mod(Bun_{G})
  \simeq
  \hat \mathcal{D}^{\frac{1}{k},\lambda} Mod(Bun_{{}^L G})
  \,.
$$

(In fact $k$ and $\frac{1}{k}$ here should further be shifted by the [[dual Coxeter number]] of $G$ and ${}^L G$, respectively.)


## Embedding in string theory

Where the plain [[geometric Langlands correspondence]] is meant to be a shadow of the [[6d (2,0)-superconformal field theory]], the quantum version is meant to correspondingly relate to 6d [[little string theory]] ([Aganagic-Frenkel-Okounkov 17](#AganagicFrenkelOkounkov17)) (which turns into the 6d QFT in the limit that the strings shrink to points).
 
## Examples


### Limiting cases

The twisted sheaves of differential operators $\mathcal{D}^{k,\lambda}$ have the following limits:

* For $\lambda \neq 0$ and $k \neq \infty$ this is the sheaf of differential operators acting on $\mathcal{L}^{\otimes k}$;

* for $\lambda \neq 0$ and $k = \infty$ this is the pushforward $p_*(\mathcal{O}_{Loc_G})$ of the sheaf of $\mathcal{O}$-modules along the canonical $P : Loc_G \to Bun_G$ that sends a local system to its underlying bundle;

* for $\lambda = 0$ and $k$ arbitrary this is $p_*(\mathcal{O}_{T^* Bun_G^\circ})$.

### Abelian case

In the case where $G$ is abelian, the quantum correspondence is given by a [[Fourier-Mukai transform]] and has been constructed in ([Polishuk-Rothenstein](#PolishukRothenstein))

## Related concepts

* [[S-duality]]

  * [[electro-magnetic duality]]

  * [[geometric Langlands correspondence]]

  * **quantum geometric Langlands correspondence**



## References

The statement of the quantum geometric Langlands correspondence is surveyed on [page 70-71](http://arxiv.org/PS_cache/hep-th/pdf/0512/0512172v1.pdf#page=71) of

* [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_ ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172)).

with more details in:

* [[Dennis Gaitsgory]], *Quantum Langlands Correspondence* &lbrack;[arXiv:1601.05279](https://arxiv.org/abs/1601.05279)&rbrack;


The construction of the correspondence in the abelian case, where it is given by a [[Fourier-Mukai transform]], is given in

* {#PolishukRothenstein} A. Polishchuk and M. Rothstein, _Fourier transform for D-algebras_ , DukeMath. J. 109 (2001) 123&#8211;146.


An interpretation of the quantum Langlands correspondence in terms of the [[B-model]] [[topological string]] is given in

* [[Anton Kapustin]], _A Note on Quantum Geometric Langlands Duality, Gauge Theory, and Quantization of the Moduli Space of Flat Connections_ ([arXiv:0811.3264](http://arxiv.org/abs/0811.3264))

A general quantum geometric Langlands correspondence is produced in

* {#AganagicFrenkelOkounkov17} [[Mina Aganagic]], [[Edward Frenkel]], [[Andrei Okounkov]], Trans. Moscow Math. Soc. (2018) 1-83 , _Quantum $q$-Langlands Correspondence_ &lbrack;[arXiv:1701.03146](https://arxiv.org/abs/1701.03146), [doi:10.1090/mosc/278]( https://doi.org/10.1090/mosc/278) &rbrack;

see also

* [[David Ben-Zvi]], [[Adrien Brochier]], David Jordan, *Quantum character varieties and braided module categories*,  Sel. Math. New Ser. **24** (2018) 4711–4748 &lbrack;[doi:10.1007/s00029-018-0426-y](https://doi.org/10.1007/s00029-018-0426-y), [arXiv:1606.04769](https://arxiv.org/abs/1606.04769)&rbrack;

Relation to [[semi-topological 4d Chern-Simons theory]]:

* [[Meer Ashwinkumar]], [[Meng-Chwan Tan]], _Unifying Lattice Models, Links and Quantum Geometric Langlands via Branes in String Theory_ ([arXiv:1910.01134](https://arxiv.org/abs/1910.01134))

See also

* Peter Koroteev, Daniel S. Sage, [[Anton Zeitlin]], _$(SL(N),q$)-opers, the $q$-Langlands correspondence, and quantum/classical duality_ ([arXiv:1811.09937](https://arxiv.org/abs/1811.09937))

* [[Davide Gaiotto]], [[Jörg Teschner]], *Quantum Analytic Langlands Correspondence* &lbrack;[arXiv:2402.00494](https://arxiv.org/abs/2402.00494)&rbrack;


[[!redirects quantum geometric Langlands duality]]
