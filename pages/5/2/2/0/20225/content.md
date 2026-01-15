
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


\tableofcontents



## Definition

There is some variation in the literature on what one calls a "[[quaternionic]] [[manifold]]''. The most general definition, however, encompassing all the others, is:

+-- {: .num_defn #QuaternionicManifold}
###### Definition
**(Quaternionic manifold)**

For $n \geq 2$, a **quaternionic manifold** is a real 4n-dimensional manifold M with a $\text{GL} (n,\mathbf{H})\cdot \mathbf{H} ^{\times }$-[[G-structure|structure]] which admits a [[torsion of a G-structure|torsion-free]] [[connection]] $\nabla$ (i.e. is integrable as a [[G-structure]]).

=--

When $\nabla$ does not exist $M$ is called _almost quaternionic_, and this is just a [[reduction of the structure group]] of $M$ along a [[Lie group]] inclusion $\text{GL}(n, \mathbf{H}) \hookrightarrow \text{GL}(4n, \mathbf{R})$. Note that the multiplicative group of the quaternions $\mathbf{H}^{\times}$ can be normalized, so that the second factor of $\text{GL} (n,\mathbf{H})\cdot \mathbf{H} ^{\times }$ is isomorphic to SU(2), or isomorphically again the first quaternionic unitary group Sp(1). Hence one occasionally finds the structure group reduction written $\text{GL} (n,\mathbf{H})\cdot \text{Sp}(1)$. 

+-- {: .num_defn}
###### Remark


Other definitions have been given, based on the following useful but more naïve reasoning: consider two  [[almost complex structures]] on a smooth $4n$-manifold $M$, say $\langle M, I \rangle$ and $\langle M, J \rangle$, given the relation $\{ I, J \} =0$. Then call the structure $\langle M, I, J \rangle$ "almost quaternionic", and a map $\varphi:  \langle M, I, J \rangle \rightarrow \langle N, K, F \rangle$ of almost quaternionic structures "quaternionic" if it is separately [[complex analytic]] as a map $\langle M, I \rangle \rightarrow \langle N, K \rangle$ and also as a map $\langle M, J \rangle \rightarrow \langle N, F \rangle$.

When $\mathbf{R}^4$ is given a quaternionic multiplication with anti-commuting imaginary units $i$ and $j$, this is actually equivalent to $\varphi : \mathbf{R}^4 \rightarrow \mathbf{R}^4$ satisfying the [[Cauchy-Feuter]] complex:
$$ i \frac{\partial}{\partial u_3} = \frac{\partial }{\partial u _4}, j \frac{\partial }{ \partial u_2} = \frac{\partial }{\partial u_4}$$
$$i \frac{\partial}{\partial u_1} = \frac{\partial }{\partial u_2}, j \frac{\partial }{\partial u_1 } = \frac{\partial }{\partial u_3}$$
known as a starting point for defining a notion of "quaternionic [[holomorphy]]", since the Cauchy-Feuter complex consists of two separate [[Cauchy-Riemann]] systems in the imaginary units $i, j$. Such a complex exists on $\mathbf{R}^{4n}$ for any $n$ as an extended Cauchy-Fueter complex consisting of the systems above, repeated for each set of four coordinates. Hence, $\mathbf{R}^{4n}$ as a smooth manifold can always be endowed with an almost quaternionic structure. On this account of quaternionic structure, a _quaternionic $n$-manifold_ is then an almost quaternionic structure on a smooth manifold $M$ such that $M$ has an atlas of quaternionic maps, considered with respect to the standard quaternionic structure on $\mathbf{R}^{4n}$ just described. However, such a definition has serious drawbacks, such as the fact that quaternionic projective $n$-space $\mathbf{H}P^n := \text{Sp}(n + 1)/\text{Sp}(n)\text{Sp}(1)$ is not a "quaternionic manifold" in this sense for any $n$. It is, however, a quaternionic manifold under the official definition above. 

=--

## Examples


+-- {: .num_example #QuaternionKaehlermanifoldsAreQuaternionicManifolds}
###### Example
**([[quaternion-Kähler manifolds]] are [[quaternionic manifolds]])**

By definition, a [[quaternion-Kähler manifold]] $M$ has [[holonomy group]] contained in the [[direct product group]] [[Sp(n)]]$\times$[[Spin(3)|Sp(1)]], admitting an extension of the [[Levi-Civita connection]] $\nabla$ on the holonomy bundle as torsion-free. Thus a quaternion-Kähler manifold is automatically quaternionic. 

Such extension $\nabla_\text{quat}$ of $\nabla$ however is not unique, since $\nabla_\text{quat} + \mathcal{S}$ is another Sp(n)Sp(1)-preserving connection, where $\mathcal{S}$ is a (1, 2)-tensor such that for every $p \in M$, $\mathcal{S}(p)$ takes values in the first [[prolongation]] of the [[Lie algebra]] for the [[G-structure]]. 

=--


## Properties

### Holonomy

(...)

### Twistor Space of a Quaternionic Manifold

(...)

## Related concepts

* [[biquaternionic manifold]], [[hypercomplex manifold]], 

* [[quaternionic-Kähler manifold]]

* [[Kähler manifold]], [[hyper-Kähler manifold]]

## References

Book references include:

* {#Besse}[[Arthur Besse]], _Einstein Manifolds_, Springer-Verlag 1987.

* {#Joyce} [[Dominic Joyce]], _Compact Manifolds with Special Holonomy_, Oxford University Press, 2000.

Classical references:

* Edmond Bonan, _Sur les $G$-structures de type quaternionien_,  Cahiers de Topologie et Géométrie Différentielle Catégoriques, Volume 9 (1967) no. 4, p. 389-463 ([numdam:CTGDC_1967__9_4_389_0](http://www.numdam.org/item/CTGDC_1967__9_4_389_0))
* {#Salamon} S.M. Salamon, "Differential Geometry of Quaternionic Manifolds", Annales scientifiques de l’É.N.S. 4e série, tome 19, no 1 (1986), p. 31-55.

See also

* Wikipedia, _[Quaternionic manifold](https://en.wikipedia.org/wiki/Quaternionic_manifold)_


In terms of [[G-structure]]:

* [[Dmitri V. Alekseevsky]], [[Stefano Marchiafava]]: _Quaternionic-like structures on a manifold: Note I. 1-integrability and integrability conditions_, Atti della Accademia Nazionale dei Lincei. Classe di Scienze Fisiche, Matematiche e Naturali. Rendiconti Lincei. Matematica e Applicazioni **4** 1 (1993) 43-52 &lbrack;[[AlekseevskyMarchiafava-1993a.pdf:file]]&rbrack;

* [[Dmitri V. Alekseevsky]], [[Stefano Marchiafava]]: _Quaternionic-like structures on a manifold: Note II. Automorphism groups and their interrelations_, Atti della Accademia Nazionale dei Lincei. Classe di Scienze Fisiche, Matematiche e Naturali. Rendiconti Lincei. Matematica e Applicazioni **4** 1 (1993) 53-61 &lbrack;[[AlekseevskyMarchiafava-1993b.pdf:file]]&rbrack;

* [[Dmitry V. Alekseevsky]], _Quaternionic structures on a manifold and subordinated structures_, Annali di Matematica pura ed applicata 171, 205–273 (1996) ([doi:10.1007/BF01759388](https://doi.org/10.1007/BF01759388))

    

Holonomy, connections, and twistor spaces:

* {#ivanov} Stefan Ivanov, Ivan Minchev, Simeon Zamkovoy, [Twistors of Almost Quaternionic Manifolds](https://arxiv.org/abs/math/0511525)

* {#grantscharov} Gueo Grantcharov and Yat Sun Poon, [Geometry of Hyper-Kahler Connections with Torsion](https://arxiv.org/abs/math/9908015v1)



On [[quaternionic orbifolds]]:

*  K. Galicki, [[H. Blaine Lawson]], _Quaternionic Reduction and Quaternionic Orbifolds_, Mathematische Annalen (1988) Volume: 282, Issue: 1, page 1-22 ([dml:164446](https://eudml.org/doc/164446))


[[!redirects quaternionic manifolds]]
[[!redirects quaternion manifold]]

[[!redirects quaternionic orbifold]]
[[!redirects quaternionic orbifolds]]

