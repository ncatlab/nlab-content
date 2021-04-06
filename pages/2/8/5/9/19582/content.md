[[!redirects 12-dimensional supergravity]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

There is a sensible [[theory (physics)|theory]] of [[supergravity]] in a total of 12 [[spacetime]] [[dimensions]]. Even though this requires an exotic non-[[Lorentzian signature]] of $(10,2)$ (hence with a "2-dimensional [[time]]") it has been argued that this is a better starting point for obtaining low-dimensional [[supergravity]] theory by [[KK-compactification]], since it yields some lower-dimensional theories that are missed when starting with [[11-dimensional supergravity]], notably [[type IIB supergravity]] in 10 dimensions, hence relates to [[F-theory]] as [[11-dimensional supergravity]] relates to [[M-theory]] (e.g. [Nishino 97b](#Nishino97b), [Hewson 97](#Hewson97)). (A theory in $(9,3)$ signature has also been proposed in ([Kriz 05](#Kriz05)).)

It is an oft-repeated [[folklore]] that the highest number of [[spacetime]] [[dimensions]] for [[supergravity]] to make sense is 11, realized by [[11-dimensional supergravity]]. However, there are some assumptions that go into this conclusion. First of all, the argument goes that after [[KK-compactification]] to 4-dimensions there must not appear [[supermultiplets]] with [[mass]]-less fields of [[spin]] $\gt 2$, since another [[folklore]] argument states that [[quantum field theory]] in $3+1$ dimensions with fields of spin larger than 2 is inconsistent. 

(This in turn needs further qualification: Consistent [[quantum field theory]] with an _infinite tower_ of higher spin fields _is_ consistent, this is called _[[higher spin gauge theory]]_ arising as the vanishing [[string tension]]-[[limit of a sequence|limit]] of [[string field theory]]. Ever since this discovery, the modified [[folklore]] is that field theories with a finite number of higher spin fields is inconsistent.)

Since acting with a [[supersymmetry]] generator on elements of a [[supermultiplet]] increases spin by 1/2, this argument requires that there are at most $(2 - (-2)) \times 2 = 8$ super charges in (3+1)d, hence corresponding to [[N=8 d=4 supergravity]]. 

This, in turn, requires, by the rules of [[KK-compactification]], that 

1. there be only a single supercharge in dimension $10+1$, since the [[irreducible representation|irreducible]] [[real spin representation]] of $Spin(10,1)$ has real dimension 32, which [[branching rule|branches]] as $\mathbf{32} \mapsto 8 \cdot \mathbf{4}$ under $Spin(3,1) \hookrightarrow Spin(10,1)$;

1. there cannot be any supercharge in dimension $11+1$, since the [[irreducible representation|irreducible]] [[real spin representation]] of $Spin(11,1)$ has real dimension 64, which [[branching rule|branches]] as $\mathbf{64} \mapsto 16 \cdot \mathbf{4}$ under $Spin(3,1) \hookrightarrow Spin(11,1)$.

However, the second conclusion here is evaded by a change of [[spacetime signature]]: The [[irreducible representation|irreducible]] [[real spin representation]] of [[Spin(10,2)]] still happens to be of dimension 32 and still [[branching rule|branches]] as $\mathbf{32} \mapsto 8 \cdot \mathbf{4}$.


## Properties

### The $2+1$-brane in $10+2$ dimensions
 {#The21Brane}

There is supposed to be a consistent fundamental [[super p-brane]] on $10+2$-dimensional supergravity backgrounds, whose [[double dimensional reduction]] yields the [[M2-brane]] in [[11-dimensional supergravity]] and further the [[superstrings]] not just of [[type IIA supergravity]] but also (?) of [[type IIB supergravity]]. The [[worldvolume]] of this [[p-brane]] has 4 spacetime dimensions with signature $(2,2)$. Therefore some authors refer to this as a "2+2"-brane, even though this does not mesh well with the naming convention of $p$-branes in Lorentzian signature. Since Lorentzian $p$-branes have $(p+1)$-dimensional worldvolume, the systematic naming here would be "2+1"-brane.

See ([Blencowe-Duff 88, section 7](#BlencoweDuff88), [Hewson-Perry 96](#HewsonPerry96), [Nishino 97b](#Nishino97b))

## Related concepts

* [[D=11 supergravity]]

* [[F-theory]]

* [[D=14 supersymmetry]]

* [[bosonic M-theory]]

## References

### General

* [[Leonardo Castellani]], [[Pietro Fré]], F. Giani, K. Pilch, [[Peter van Nieuwenhuizen]], _Beyond $d=11$ Supergravity and Cartan Integrable Systems_, Phys.Rev. D26 (1982) 1481 ([spire:11999](http://inspirehep.net/record/11999))

* [[Itzhak Bars]], _Supersymmetry, p-brane duality and hidden space-time dimensions_, Phys. Rev. D54, 5203 (1996) ([arXiv: hep-th/9604139](https://arxiv.org/abs/hep-th/9604139)). 

* [[Itzhak Bars]], _S-Theory_, Phys.Rev. D55 (1997) 2373-2381 ([arXiv:hep-th/9607112](https://arxiv.org/abs/hep-th/9607112))

* {#Nishino97} [[Hitoshi Nishino]], _Supergravity in 10 + 2 Dimensions as Consistent Background for Superstring_, ([arXiv:hep-th/9703214](https://arxiv.org/abs/hep-th/9703214))

* {#Nishino97b} [[Hitoshi Nishino]], _N=2 Chiral Supergravity in (10 + 2)-Dimensions As Consistent Background for Super (2 + 2)-Brane_, Phys. Lett. B437 (1998) 303-314 ([arXiv:hep-th/9706148](https://arxiv.org/abs/hep-th/9706148))

* {#Hewson97} Stephen Hewson, _An approach to F-theory_, Nucl. Phys. B534 (1998) 513-530 ([arXiv:hep-th/9712017](https://arxiv.org/abs/hep-th/9712017))

* {#Nishino98} [[Hitoshi Nishino]], _Supergravity Theories in $D \geq 12$ Coupled to Super p-Branes_, Nucl.Phys. B542 (1999) 217-261 ([arXiv:hep-th/9807199](https://arxiv.org/abs/hep-th/9807199))


* Stephen Hewson, _On supergravity in $(10,2)$_ ([arXiv:hep-th/9908209](https://arxiv.org/abs/hep-th/9908209))

* Tatsuya Ueno, _BPS States in 10+2 Dimensions_, JHEP 0012:006, 2000 ([arXiv:hep-th/9909007](https://arxiv.org/abs/hep-th/9909007))

* [[Leonardo Castellani]], _A locally supersymmetric SO(10,2) invariant action for D=12 supergravity_, ([arXiv:1705.00638](https://arxiv.org/abs/1705.00638))

### On the $2+1$-brane in $10+2$ dimensions

* {#BlencoweDuff88} [[Miles Blencowe]], [[Mike Duff]], _Supermembranes and the Signature of Space-time_, Nucl. Phys. B310 (1988) 387-404 ([spire:262142](inspirehep.net/record/262142), <a href="https://doi.org/10.1016/0550-3213(88)90155-1">10.1016/0550-3213(88)90155-1</a>, [pdf](http://inspirehep.net/record/262142/files/cer-000099708.pdf))

* {#HewsonPerry96} S. F. Hewson, M. J. Perry, _The twelve dimensional super $(2+2)$-brane_, Nucl.Phys. B492 (1997) 249-277 ([arXiv:hep-th/9612008](https://arxiv.org/abs/hep-th/9612008))

* [Nishino 97b](#Nishino97b)

### On supergravity in $9 + 3$ dimensions

* {#Kriz05} [[Igor Kriz]], _Some remarks on fundamental physical F-theory_, ([arXiv:hep-th/0508046](https://arxiv.org/abs/hep-th/0508046))


### In bosonic M-theory

On organizing all these variants inside [[bosonic M-theory]] and [[KK-reduction]] on [[Cayley planes]] to actual [[M-theory]]:


* [[Michael Rios]], [[Alessio Marrani]], [[David Chester]], _Exceptional Super Yang-Mills in $D=27+3$ and Worldvolume M-Theory_, Phys. Lett. B, 808, (2020)
([arXiv:1906.10709](https://arxiv.org/abs/1906.10709))



[[!redirects 12d supergravity]]


