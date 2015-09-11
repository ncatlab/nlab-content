+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[higher-order logic|higher-order]] [[intuitionistic type theory]] $\mathfrak{L}$, it is possible to construct a [[topos]] $T(\mathfrak{L})$ out of the [[syntax]] of $\mathfrak{L}$. The **free topos** $T(\mathfrak{L}_0)$ is the result of this construction when $\mathfrak{L}_0$ is 'pure' type theory i.e. the only types are 1, $N$, and $\Omega$ lacking relations beyond the bare necessities.

As $\mathfrak{L}_0$ is an [[initial object]] in the appropriate category of type theories, the free topos $T(\mathfrak{L}_0)$ is itself initial in the category of toposes and [[logical morphisms]] and is, therefore, also known as the **initial topos**[^sga4].

[^sga4]: This is not to be confounded with the gadget of the same name in [[SGA4]] (1972, p.313) i.e. the topos $sh(\emptyset)$ of sheaves on the empty topological space aka the one point category, also called the _empty topos_ there. In this context the appropriate maps are [[geometric morphisms]].

## Properties
 
The [[internal language]] of the free topos is precisely pure (intuitionistic) higher order type theory. In 1978, [[Jim Lambek]] and [[Phil Scott]] exploited this connection in order to prove properties of intuitionistic type theory by [[proof theory|proof-theoretic]] means. It was observed by [[Peter Freyd]] then that the concept of a [[Freyd cover]] permits to give conceptual proofs of their findings. The following lemma and proposition is a replication of his ideas.

+-- {: .num_lemma}
###### Lemma 
For any [[category]] $C$ with a [[terminal object]] $\mathbf{1}$, the terminal object of the [[Freyd cover]] $\widehat{C}$ is [[small-projective]], i.e., the representable $\Gamma = \widehat{C}(1, -) \colon \widehat{C} \to Set$ preserves any colimits that exist. 
=-- 

+-- {: .proof} 
###### Proof 
To check that $\Gamma^{op} \colon \widehat{C}^{op} \to Set^{op}$ preserves limits, it suffices to check that the composite 

$$\widehat{C}^{op} \stackrel{\Gamma^{op}}{\to} Set^{op} \stackrel{2^-}{\to} Set$$ 

preserves limits, because the contravariant power set functor $P = 2^-$ is monadic. But it is easily checked that this composite is the contravariant representable given by $(2, \mathbf{1}, 2 \to \Gamma(\mathbf{1}))$. 
=-- 

+-- {: .num_theorem}
###### Theorem 
The [[terminal object]] in the free topos $\mathcal{T}$ is [[connected object|connected]] and [[projective object|projective]] in the sense that $\Gamma = \hom(1, -) \colon \mathcal{T} \to Set$ preserves finite [[colimits]]. 
=-- 

+-- {: .proof} 
###### Proof 
We divide the argument into three segments: 

* The [[hom-functor]] preserves [[finite limits]], so by general properties of [[Artin gluing]], the [[Freyd cover]] $\widehat{\mathcal{T}}$ is also a topos. Observe that $\mathcal{T}$ is equivalent to the [[slice category|slice]] $\widehat{\mathcal{T}}/M$ where $M$ is the object $(\emptyset, \mathbf{1}, \emptyset \to \Gamma(\mathbf{1}))$. Since pulling back to a slice is a logical functor, we have a logical functor 
$$\pi \colon \widehat{\mathcal{T}} \to \mathcal{T}$$ 
Since $\mathcal{T}$ is initial, $\pi$ is a retraction for the unique logical functor $i \colon \mathcal{T} \to \widehat{\mathcal{T}}$. 

* We have maps $\mathcal{T}(1, -) \to \widehat{\mathcal{T}}(i 1, i-) \cong \widehat{\mathcal{T}}(1, i-)$ (the isomorphism comes from $i 1 \cong 1$, which is clear since $i$ is logical), and $\widehat{\mathcal{T}}(1, i-) \to \mathcal{T}(\pi 1, \pi i-) \cong \mathcal{T}(1, -)$ since $\pi$ is logical and retracts $i$. Their composite must be the identity on $\mathcal{T}(1, -)$, because there is only one such endomorphism, using the Yoneda lemma and terminality of $1$. 

Finally, since $\mathcal{T}(1, -)$ is a retract of a functor $\widehat{\mathcal{T}}(1, i-)$ that preserves finite colimits (by the lemma, and the fact that the logical functor $i$ preserves finite colimits), it must also preserve finite colimits. 
=--

This is important because it implies that the [[internal logic]] of the free topos satisfies the following properties:

* The *disjunction property*: if "P [[or]] Q" is provable in the empty [[context]], then either P is so provable, or Q is so provable.  (Note that this clearly fails in the presence of [[excluded middle]].)

* The *existence property*: if "there exists an $x\in A$ such that $P(x)$" is provable in the empty context, then there exists a [[global element]] $x\colon 1\to A$ such that $P(x)$ is provable in the empty context.  (Again, this is clearly a [[constructive mathematics|constructivity]] property.)

* The *negation property*: False is not provable in the empty context. 

* All numerals in the free topos are "standard", i.e., the global sections functor $\Gamma = \hom(1, -): \mathcal{T} \to Set$ preserves the [[natural numbers object]] $N$ (because $N$ can be characterized in terms of finite colimits and $1$, by a theorem of Freyd). 


### Foundations

In the [[foundations of mathematics]], [[Jim Lambek]] proposed to use the free topos as ambient world to do mathematics in; see ([Lambek 2004](#LambekWorld)). Being syntactically constructed, but universally determined, with higher-order [[intuitionistic type theory]] as [[internal language]] he saw it as a reconciliation of the three classical schools of [[philosophy of mathematics]], namely [[formalism]], [[platonism]], and [[intuitionism]]. His latest views on this variant of categorical foundations can be found in ([Lambek-Scott 2011](#LS11)).

### Remark: Two properties of the free topos

Lambek and Scott mention in their 1986 monograph ([pp.viii, 233, 250](#LambekScott86)) two further remarkable properties of the free topos $\mathcal{T}$:

* Brouwer's theorem holds in $\mathcal{T}$ i.e. all maps $R\to R$ are continuous.

* $\mathcal{T}$ has countable choice i.e. the natural numbers object $N$ is projective.

The first result is attributed to [[André Joyal]], presumably unpublished, and for the second claim they refer to an unpublished manuscript by [[Michael Makkai]] and a manuscript by Friedman and Scedrov, presumably ([1983](#FriedmanScedrov83)).

## Related entries 

* [[Freyd cover]] 

* [[Artin gluing]]

* [[syntactic category]]

* [[adjoint modality]] 

## References

The free topos was first constructed by H. Volger. A second construction appears in

* [[Jim Lambek]], _From Types to Sets_ , JPAA **36** (1980) pp.113-164.

Freyd's proof of the above properties appears first in

* [[Jim Lambek]], [[Phil Scott]], _Intutionist Type Theory and the Free Topos_ , JPAA **19** (1980) pp. 215-257. {#LambekScott80}

On the relation between the proof and the topos-theoretic techniques in the proof see

* A. Scedrov, [[Phil Scott]], _A note on the Friedman Slash and Freyd Covers_ , pp. 443-452 in _The LEJ Brouwer Centenary Symposium_ , North Holland Amsterdam 1982.

* [[Jim Lambek]], [[Phil Scott]], _New Proofs of some intuitionistic principles_ , Zeit. f&#252;r Math. Logik **29** (1983) pp. 493-504.

For textbook accounts of the free topos see

* {#LambekScott86}[[Jim Lambek]], [[Phil Scott]], _[[Introduction to Higher-Order Categorical Logic]]_ , Cambridge UP 1986. ([pdf](https://synrc.com/publications/cat/Category%20Theory/Categorical%20Logic/Lambek%20J.,%20Scott%20P.J.%20Introduction%20to%20Higher%20Order%20Categorical%20Logic.pdf))

* [[Peter Freyd|P. Freyd]], A. Scedrov, _[[Categories, Allegories]]_ , North-Holland Amsterdam 1990.  (1.(10)31, p.192)

* [[Elephant]] F3, to appear.

For dependent choice in intuitionistic type theory:

* {#FriedmanScedrov83}H. M. Friedman, A. Scedrov, _Set existence property for intuitionistic theories with dependent choice_ , APAL **25** no.2 (1983) pp.129-140.

For J. Lambek's views on the role of the free topos in [[foundations of mathematics]] see:

* J. Couture, [[Jim Lambek]], _Philosophical Reflections on the Foundations of Mathematics_ , Erkenntnis **34** (1991) pp.187-209.

* [[Jim Lambek]], _Are the traditional philosophies of mathematics really incompatible?_ , Math. Intelligencer **16**
(1994) pp.56&#8211;62.

* {#LambekWorld}[[Jim Lambek]], _What is the world of mathematics?_ , APAL **126** (2004) pp.149-158. ([draft](http://www.math.mcgill.ca/barr/lambek/pdffiles/WorldMath.pdf))

* {#LS11} [[Jim Lambek]], [[Phil Scott]], _Reflections on Categorical Foundations of Mathematics_ , pp.171-185 in  Sommaruga (ed.), _Foundational Theories of Classical and Constructive Mathematics_,  Springer New York 2011. ([draft](https://www.site.uottawa.ca/~phil/papers/LS11.final.pdf)) 

[[!redirects initial topos]]