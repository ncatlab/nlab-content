
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

In [[number theory]], [[Galois theory]] and [[arithmetic geometry]] in [[prime number|prime]] [[characteristic]] $p$, the _Frobenius morphism_ is the [[endomorphism]] acting on [[algebras]], [[function algebras]], [[structure sheaves]] etc., which takes each [[ring]]/[[associative algebra|algebra]]-element $x$ to its $p$th power 

$$
  x^p = \underbrace{x \cdot x \cdots x}_{p \; factors}
  \;.
$$

It is precisely in [[positive characteristic]] $p$ that this operation is indeed an algebra [[homomorphism]]. 

The Frobenius map is the shadow of the [[power operations]] in [[multiplicative cohomology theory]]/[[higher algebra]] ([Lurie, remark 2.2.7](#Lurie)).

The presence of the Frobenius endomorphism in characteristic $p$ is a fundamental property in [[arithmetic geometry]] that controls many of its deep aspects. Notably [[zeta functions]] are typically expressed in terms of the [[action]] of the Frobenius endomorphisms on [[cohomology groups]] and so it features prominently for instance in the [[Weil conjectures]].

In [[Borger's absolute geometry]] lifts of Frobenius endomorphisms through [[base change]] for all primes at once -- in the sense of _[Lambda-ring structure](Lambda-ring#LambdaRingByFrobeniusLifts)_ -- is interpreted as encoding [[descent]] data from traditional [[arithmetic geometry]] over [[Spec(Z)]] down to the "absolute" geometry over "[[F1]]". See at _[Borger's absolute geometry -- Motivation](Borger%27s+absolute+geometry#Motivation)_ for more on this.
 


## Definition

> this entry may need attention

## For fields

Let $k$ be a [[field]] of positive [[characteristic]] $p$. The **Frobenius morphism** is an [[endomorphism]] of the field $F \colon k \to k$ defined by 

$$
  F(a) \coloneqq  a^p
  \,.
$$ 

Notice that this is indeed a [[homomorphism]] of fields: the identity $(a b)^p=a^p b^p$ evidently holds for all $a,b\in k$ and the [[characteristic]] of the field is used to show $(a+b)^p=a^p+b^p$. 

### Of schemes


Suppose $(X,\mathcal{O}_X)$ is an $S$-[[scheme]] where $S$ is a [[scheme]] over $k$. The **absolute Frobenius** is the map $F^{ab}:(X,\mathcal{O}_X)\to (X,\mathcal{O}_X)$ which is the identity on the [[topological space]] $X$ and on the structure sheaves $F_*:\mathcal{O}_X\to \mathcal{O}_X$ is the $p$-th power map. This is not a map of $S$-schemes in general since it doesn't respect the structure of $X$ as an $S$-scheme, i.e. the diagram:

$\displaystyle \begin{matrix} X & \stackrel{F^{ab}}{\to} & X \\
\downarrow &  & \downarrow \\
S & \stackrel{F^{ab}}{\to} & S \end{matrix}$, 

so in order for the map to be an $S$-scheme morphism, $F^{ab}$ must be the identity on $S$, i.e. $S=Spec(\mathbb{F}_p)$.

Now we can form the [[fiber product]] using this square: $X^{(p)}:=X\times_{S} S$. By the universal property of [[pullback]]s there is a map $F^{rel}:X\to X^{(p)}$ so that the composition $X\to X^{(p)}\to X$ is $F^{ab}$. This is called the **relative Frobenius**. By construction the relative Frobenius is a map of $S$-schemes.

### For sheaves on $C Ring ^{op}$

Let $p$ be a prime number, let $k$ be a field of characteristic $p$. For a $k$-ring $A$ we define

$$f_A:
\begin{cases}
A\to A
\\
x\mapsto x^p
\end{cases}$$

The $k$-ring obtained from $A$ by scalar restriction along $f_k:k\to k$ is denoted by $A_{f}$.

The $k$-ring obtained from $A$ by scalar extension along $f_k:k\to k$ is denoted by $A^{(p)}:=A\otimes_{k,f} k$.

There are $k$-ring morphisms $f_A: A\to A_f$ and $F_A:\begin{cases}
A^{(p)}\to A
\\
x\otimes \lambda\mapsto x^p \lambda
\end{cases}$. 

For a $k$-functor $X$ we define $X^{(p)}:X\otimes_{k,f_k} k$ which satisfies $X^{(p)}(R)=X(R_f)$. The _Frobenius morphism_ for $X$ is the transformation of $k$-functors defined by

$$F_X:
\begin{cases}

X\to X^{(p)}
\\
X(f_R):X(R)\to X(R_f)
\end{cases}$$

If $X$ is a $k$-scheme $X^{(p)}$ is a $k$-scheme, too.

Since the completion functor ${}^\hat\;:Sch_k\to fSch_k$ commutes with the above constructions the Frobenius morphism can be defined for [[formal scheme|formal k-schemes]], too.

### In terms of symmetric products

We give here another characterization of the [[Frobenius morphism]] in terms of symmetric products.

Let $p$ be a prime number, let $k$ be a field of [[characteristic]] $p$, let $V$ be a $k$-vector space, let $\otimes^p V$ denote the $p$-fold tensor power of $V$, let $TS^p V$ denote the subspace of symmetric tensors. Then we have the symmetrization operator

$$s_V:
\begin{cases}
\otimes^p V\to TS^p V
\\
a_1\otimes\cdots\otimes a_n\mapsto \Sigma_{\sigma\in S_p}a_{\sigma(1)}\otimes\cdots\otimes a_{\sigma(n)}
\end{cases}$$

end the linear map

$$\alpha_V:
\begin{cases}
TS^p V\to\otimes^p V
\\
a\otimes \lambda\mapsto\lambda(a\otimes\cdots\otimes a)
\end{cases}$$

then the map $V^{(p)}\stackrel{\alpha_V}{\to}TS^p V\to TS^p V/s(\otimes^p V)$ is bijective and we define $\lambda_V:TS^p V\to V^{(p)}$ by

$$\lambda_V\circ s=0$$

and

$$\lambda_V \circ \alpha_V= id$$


If $A$ is a $k$-ring we have that $TS^p A$ is a $k$-ring and $\lambda_A$ is a $k$-ring morphism.

If $X=Sp_k A$ is a ring spectrum we abbreviate $S^p X=S^p_k X:=Sp_k (TS^p A)$ and the following diagram is commutative.

$$\array{
X
&\stackrel{F_X}{\to}&
X^{(p)}
\\
\downarrow&&\downarrow
\\
X^p
&\stackrel{can}{\to}& S^p X
}$$

## Properties

### For fields

* Frobenius is always [[injective]]. Note that the Frobenius morphism of schemes (see below) is *not* always a monomorphism.

* The [[image]] of Frobenius is the set of elements of $k$ with a $p$-th root and is sometimes denoted $k^{1/p}$.

* Frobenius is [[surjective]] if and only if $k$ is [[perfect field|perfect]].

### As elements of the Galois group
 {#AsElementsOfGaloisGroup}

Some powers of the Frobenius morphism canonically induce elements in the [[Galois group]] (...) 


Review of the standard story is for instance in ([Snyder 02, section 1.5](#Snyder02)).
Further developments include  ([Dokchitser-Dokchitser 10](#DokchitserDokchitser10))

If $\mathbb{F}_{p^n}$ is a [[finite field]],then $Gal(\mathbb{F}_{p^n}/\mathbb{F}_p)$ is [[generators and relations|generated]] by the Frobenius map $x\mapsto x^p$ (e.g. [Snyder 02, lemma 1.5.10](#Snyder02)).

(..)

See also at _[[Artin L-function]]_.



### For schemes

For the purposes below $k$ will be a [[perfect field]] of [[characteristic]] $p$>$0$.

* $X$ is [[smooth scheme|smooth]] over $k$ if and only if $F$ is a [[vector bundle]], i.e. $F_*\mathcal{O}_X$ is a free $\mathcal{O}_X$-module of rank $p$. One can study singularities of $X$ by studying properties of $F_*\mathcal{O}_X$.

* If $X$ is [[smooth scheme|smooth]] and [[proper scheme| proper]] over $k$, the sequence $0\to \mathcal{O}_X\stackrel{F^{ab}}{\to} F_*\mathcal{O}_X \to d\mathcal{O}_X\to 0$ is exact and if it [[split exact sequence|splits]] then $X$ has a lifting to $W_2(k)$.


+-- {: .num_prop}
###### Proposition
Let $X$ be a $k$-formal scheme (resp. a [[locally algebraic scheme]]) then $X$ is [[etale scheme|étale]] iff the [[Frobenius morphism]] $F_X:X\to X^{(p)}$is a monomorphism (resp. an isomorphism).
=--

The Frobenius as a morphism (natural transformation) of (affine) group schemes is one operation among other (related) operations of interest:

+-- {: .num_remark}
###### Remark
For any commutative affine [[group scheme]] $G$ the Frobenius- and the [[Verschiebung morphism]] correspond by ''completed [[Cartier duality|Cartier duality]]''; i.e. we have

$$\hat D(V_G)=F_{\hat D(G)}$$
=--

For a more detailed account of the relationship of Frobenius-, [[Verschiebung morphism|Verschiebung-]] and [[homothety morphism]] see [Hazewinkel](#Hazewinkel)


## Related concepts

* [[Artin-Schreier sequence]]

* [[Weil conjecture]]

* [[restricted Lie algebra]]

* [[shtuka]]

* [[cyclotomic spectrum]]

## References

* {#Frobenius68} [[Ferdinand Georg Frobenius]], Vol 2, around p. 719 of _Gesammelte Abhandlungen_, Springer-Verlag, Berlin, 1968.

Lecture notes include

* [[Günter Tamme]], section II 4.2 of _[[Introduction to Étale Cohomology]]_

* [[James Milne]], section 27 of _[[Lectures on Étale Cohomology]]_


Further discussion of the relation to the [[Galois group]] includes

* {#Snyder02} [[Noah Snyder]], section 1.5 of _Artin L-Functions: A Historical Approach_, 2002 ([pdf](http://www.math.columbia.edu/~nsnyder/thesismain.pdf))

* {#DokchitserDokchitser10} Tim Dokchitser, Vladimir Dokchitser, _Identifying Frobenius elements in Galois groups_ ([arXiv:1009.5388](http://arxiv.org/abs/1009.5388)) 

See also

* Michel Demazure, _[[lectures on p-divisible groups]]_ [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

* [[Michiel Hazewinkel]], witt vectors. part 1, [arXiv:0804.3888v1](http://arxiv.org/abs/0804.3888v1){#Hazewinkel}

* Karen Smith, *Brief Guide to Some of the Literature on F-singularities*, <a href="www.aimath.org/WWN/singularvariety/F-sings.pdf">American Institute of Mathematics</a>


Discussion in the context of [[power operations]] on [[E-infinity rings]] is in 

* {#Lurie} [[Jacob Lurie]], _[[Rational and p-adic Homotopy Theory]]_



[[!redirects Frobenius morphisms]]

[[!redirects Frobenius homomorphism]]
[[!redirects Frobenius homomorphisms]]


[[!redirects Frobenius endomorphism]]
[[!redirects Frobenius endomorphisms]]

[[!redirects Frobenius automorphism]]
[[!redirects Frobenius automorphisms]]

[[!redirects Frobenius map]]
[[!redirects Frobenius maps]]
