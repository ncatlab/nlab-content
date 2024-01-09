
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General

A _quiver gauge theory_ is a [[gauge theory]] -- usually a [[super Yang-Mills theory]] -- whose [[field (physics)|field]] content is determined by a [[quiver]] in that to each node $x_i$ of the quiver is assigned a [[gauge group]] $U(n_i)$ and to each edge a [[fermion]] field species which is charged as the [[fundamental representation]] under the gauge group of the target and the anti-fundamental representation of the domain of the quiver edge.

Such data naturally arises in [[geometric engineering of quantum field theory]] from [[D-brane]] models in [[string theory]] with D-branes located at certain [[singularities]] of a [[Calabi-Yau variety]]: the nodes $x_i$ of the quiver for a $(d+1)$-dimensional quiver gauge theory correspond to $n_i$ coincident $d$-[[D-branes]] and the edges of the quiver to [[open string]] states stretching between these branes. Under this interpretation, a [[representation]] of the quiver corresponds to giving all these fields a [[vacuum expectation value]].


### As fixed point locus

Consider a $U(N)$ [[Chan-Paton gauge field]] theory on [[D-branes]] at a $G$-[[orbifold]] [[singularity]] $\mathbb{C}^n\sslash G$ for $\Gamma$ a [[finite group]].

Then the [[fermions]] transform in $\mathbf{c} \otimes (N \mathbf[r]) \otimes (N \mathbf{r}^\ast)$, where $\mathbf{r}$ denotes the [[regular representation]] of $\Gamma$ and $\mathbf{c}$ denotes the representation which defines the [[orbifold]] [[action]]. 

Then the $\Gamma$-[[fixed point space]] inside this representation is

$$
  \big(
    \mathbf{c} \otimes (N \mathbf{r}) \otimes (N \mathbf{r}^\ast)
  \big)^\Gamma
$$

is the corresponding weighted [[McKay quiver]] matrix.

This observation is due to [Lawrence-Nekrasov-Vafa 98, Section 2.1](#LawrenceNekrasovVafa98)




## Properties

### Relation between coherent sheaves and quiver representations

The [[representation theory|representation theoretic]] aspects of the [[gauge theory]] thus obtained depend only on aspects which are already seen by the [[B-model]] [[topological string]], which in this context plays the role of a simplified version of the physical [[superstring]] itself. By the discussion at _[[TCFT]]_ this [[topological field theory]] is essentially determined by its [[derived category]] of [[B-branes]], which is a [[derived category]] of [[coherent sheaves]] on the given [[target space|target]] [[spacetime]]. Localized to suitable [[singularities]] the [[B-branes]] decompose into [[fractional branes]] which is mathematically reflected by the existence of [[exceptional collections]] of objects in the derived category. The [[endomorphism algebra]] of the [[direct sum]] of the objects in the exceptional collection turns out to be the [[path algebra]] of the corresponding [[quiver]] and under this identification the [[derived categories]] of [[coherent sheaves]] and of [[quiver representations]] are [[equivalence of categories|equivalent]] ([Bondal 90](#Bondal90)). This equivalence to quiver representations gives one of the ways of getting a concrete combinatorial handle on derived categories of [[B-branes]] and hence on properties of quiver gauge theory.

### Relation to Seiberg duality

Under [[geometric engineering of quantum field theory]] via [[D-branes]] situated at [[ADE-singularities]] in non-compact [[Calabi-Yau varieties]] as above, for instance [[Seiberg duality]] of the corresponding quiver gauge field theories may be understood in terms of [[equivalences of categories]] of derived quiver representations corresponding to [[mutations of exceptional collections]] etc. ([Robles-Llana & Rocek 04](#RoblesLlanaRocek04)).

## Related concepts

* [[McKay correspondence]]

* [[knots-quivers correspondence]]

* [[AGT correspondence]]

* [[fractional D-brane]]

## References

### General

An original article is

* {#DouglasMoore96} [[Michael Douglas]], [[Gregory Moore]], _D-branes, Quivers, and ALE Instantons_ ([arXiv:hep-th/9603167](http://arxiv.org/abs/hep-th/9603167))

The understanding of the [[McKay quiver]] as the [[fixed point space]] in the [[fermion]]-representation under [[R-symmetry]] is due to 

* {#LawrenceNekrasovVafa98} A. Lawrence, [[Nikita Nekrasov]], [[Cumrun Vafa]], _On Conformal Theories in Four Dimensions_, Nucl.Phys. B533 (1998) 199-209 ([arXiv:hep-th/9803015](https://arxiv.org/abs/hep-th/9803015))

In 

* {#Bondal90} [[Alexei Bondal]], _Helices, representations of quivers and Koszul algebras_, in Helices and vector bundles, vol. 148 of London Math. Soc. Lecture Note Ser., pp. 75&#8211;95. Cambridge Univ. Press, Cambridge, 1990.

an [[exceptional collection]] in the [[derived category]] of [[coherent sheaves]] on a suitable [[Calabi-Yau variety]] [[cone]] is used to induce a [[quiver]] and make the derived category be equivalent to that of its [[quiver representations]].


Review and discussion of further details:

* {#He04} [[Yang-Hui He]], _Lectures on D-branes, Gauge Theories and Calabi-Yau Singularities_ ([arXiv:hep-th/0408142](https://arxiv.org/abs/hep-th/0408142))

* {#He18} [[Yang-Hui He]], _Quiver Gauge Theories: Finitude and Trichotomoty_, Mathematics 2018, 6(12), 291 ([doi:10.3390/math6120291](https://doi.org/10.3390/math6120291))

* {#BergmnProudfoot04} [[Aaron Bergman]], [[Nicholas Proudfoot]], _Moduli Spaces for D-branes at the Tip of a Cone_, JHEP0603:073, 2006 ([arXiv:hep-th/0510158](http://arxiv.org/abs/hep-th/0510158))

* {#Katz04} [[Sheldon Katz]], _ADE Quiver representations and branes_ ([pdf](http://math.tecnico.ulisboa.pt/galg/WAGP04/Katz-lecture2.pdf)), lecture 2 of _ADE Geometry and dualities_  ([pdf](http://math.tecnico.ulisboa.pt/galg/WAGP04/Katz-lecture1.pdf))

* [[Taro Kimura]], *Quiver Gauge Theory*, Chapter 2 in: *Instanton Counting, Quantum Geometry and Algebra*, Mathematical Physics Studies, Springer (2021) &lbrack;[doi:10.1007/978-3-030-76190-5_4](https://doi.org/10.1007/978-3-030-76190-5_4)&rbrack;


In [[heterotic string theory]] in relation to [[Donaldson-Thomas theory]]:

* {#HeLee12} [[Yang-Hui He]], Seung-Joo Lee, _Quiver Structure of Heterotic Moduli_, J. High Energ. Phys. (2012) 2012: 119 ([arXiv:1208.3004](https://arxiv.org/abs/1208.3004))

With emphasis on [[string phenomenology]]:

* [[Angel Uranga]], _From quiver diagrams to particle physics_ ([arXiv:hep-th/0007173](https://arxiv.org/abs/hep-th/0007173))

Discussion from the point of view of [[worldsheet]] [[2d CFT]] is in 

* [[Wolfgang Lerche]], A. Lutken, [[Christoph Schweigert]], _D-Branes on ALE Spaces and the ADE Classification of Conformal Field Theories_, Nucl.Phys. B622 (2002) 269-278 ([arXiv:hep-th/0006247](http://arxiv.org/abs/hep-th/0006247))

Discussion for [[Sasakian manifolds]] includes

* [[Olaf Lechtenfeld]], Alexander Popov, [[Richard Szabo]], _Sasakian quiver gauge theories and instantons on Calabi-Yau cones_ ([arXiv:1412.4409](http://arxiv.org/abs/1412.4409))


### Seiberg duality

* David Berenstein, [[Michael Douglas]], _Seiberg Duality for Quiver Gauge Theories_ ([arXiv:hep-th/0207027](http://arxiv.org/abs/hep-th/0207027))

* Subir Mukhopadhyay, Koushik Ray, _Seiberg duality as derived equivalence for some quiver gauge theories_ ([arXiv:hep-th/0309191](http://arxiv.org/abs/hep-th/0309191))

* {#RoblesLlanaRocek04} Daniel Robles-Llana, Martin Rocek, _Quivers, Quotients, and Duality_ ([arXiv:hep-th/0405230](http://arxiv.org/abs/hep-th/0405230))

On an [[algorithm]] for constructing [[S-duality|S-dual]] [[quiver gauge theories]]:

* Chiung Hwang, [[Sara Pasquetti]], Matteo Sacchi, *Rethinking mirror symmetry as a local duality on fields*, Phys. Rev. D **106** (2022) 105014 &lbrack;[arXiv:2110.11362](https://arxiv.org/abs/2110.11362), [doi:10.1103/PhysRevD.106.105014](https://doi.org/10.1103/PhysRevD.106.105014)&rbrack;


* Riccardo Comi, Chiung Hwang, Fabio Marino, [[Sara Pasquetti]], Matteo Sacchi, *The $SL(2, \mathbb{Z})$ dualization algorithm at work* &lbrack;[arXiv:2212.10571](https://arxiv.org/abs/2212.10571)&rbrack;




[[!redirects quiver gauge theories]]
