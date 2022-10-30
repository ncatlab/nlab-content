
#Contents#
* table of contents
{:toc}

## Frobenius morphism of fields

Suppose $k$ is a [[field]] of positive [[characteristic]] $p$. The **Frobenius morphism** is an [[endomorphism]] of the field $F:k\to k$ defined by $F(a)=a^p$. 

Notice that this is indeed a [[homomorphism]] of fields: the identity $(a b)^p=a^p b^p$ evidently holds for all $a,b\in k$ and the [[characteristic]] of the field is used to show $(a+b)^p=a^p+b^p$. 

### Properties

* Frobenius is always [[injective]]. Note that the Frobenius morphism of schemes (see below) is *not* always a monomorphism.

* The [[image]] of Frobenius is the set of elements of $k$ with a $p$-th root and is sometimes denoted $k^{1/p}$.

* Frobenius is [[surjective]] if and only if $k$ is [[perfect field|perfect]].

## Frobenius morphism of schemes

### In terms of schemes as locally ringed spaces

Suppose $(X,\mathcal{O}_X)$ is an $S$-[[scheme]] where $S$ is a [[scheme]] over $k$. The **absolute Frobenius** is the map $F^{ab}:(X,\mathcal{O}_X)\to (X,\mathcal{O}_X)$ which is the identity on the [[topological space]] $X$ and on the structure sheaves $F_*:\mathcal{O}_X\to \mathcal{O}_X$ is the $p$-th power map. This is not a map of $S$-schemes in general since it doesn't respect the structure of $X$ as an $S$-scheme, i.e. the diagram:

$\displaystyle \begin{matrix} X & \stackrel{F^{ab}}{\to} & X \\
\downarrow &  & \downarrow \\
S & \stackrel{F^{ab}}{\to} & S \end{matrix}$, 

so in order for the map to be an $S$-scheme morphism, $F^{ab}$ must be the identity on $S$, i.e. $S=Spec(\mathbb{F}_p)$.

Now we can form the [[fiber product]] using this square: $X^{(p)}:=X\times_{S} S$. By the universal property of [[pullback]]s there is a map $F^{rel}:X\to X^{(p)}$ so that the composition $X\to X^{(p)}\to X$ is $F^{ab}$. This is called the **relative Frobenius**. By construction the relative Frobenius is a map of $S$-schemes.

### Properties

For the purposes below $k$ will be a [[perfect field]] of [[characteristic]] $p$>$0$.

* $X$ is [[smooth scheme|smooth]] over $k$ if and only if $F$ is a [[vector bundle]], i.e. $F_*\mathcal{O}_X$ is a free $\mathcal{O}_X$-module of rank $p$. One can study singularities of $X$ by studying properties of $F_*\mathcal{O}_X$.

* If $X$ is [[smooth scheme|smooth]] and [[proper scheme| proper]] over $k$, the sequence $0\to \mathcal{O}_X\stackrel{F^{ab}}{\to} F_*\mathcal{O}_X \to d\mathcal{O}_X\to 0$ is exact and if it [[split exact sequence|splits]] then $X$ has a lifting to $W_2(k)$.

### In terms of schemes as sheaves on $C Ring ^{op}$

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

#### In terms of symmetric products

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

### Properties

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

## Frobenius morphism of $\lambda$-rings

### Examples

If $X=Sp_k A$ is a $k$-ring spectrum we have $X^{(p)}=Sp_k A^{(p)}$ and $F_X=Sp_k F_A$.

If $k=\mathbb{F}$ is a finite field we have $X^{(p)}=X$ however $F_X$ will not equal $id_X$ in general.

If $k\hookrightarrow k^\prime$ is a field extension we have $F_{X\otimes_k k^\prime}=F_X\otimes_k k^\prime$.

## Related concepts

* [[Weil conjecture]]

## References


* Michel Demazure, [[lectures on p-divisible groups]] [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

* Michiel Hazewinkel, witt vectors. part 1, [arXiv:0804.3888v1](http://arxiv.org/abs/0804.3888v1){#Hazewinkel}

* Karen Smith, *Brief Guide to Some of the Literature on F-singularities*, <a href="www.aimath.org/WWN/singularvariety/F-sings.pdf">American Institute of Mathematics</a>


* [[James Milne]], section 27 of _[[Lectures on Étale Cohomology]]_

[[!redirects Frobenius morphisms]]

[[!redirects Frobenius endomorphism]]
[[!redirects Frobenius endomorphisms]]

[[!redirects Frobenius map]]
[[!redirects Frobenius maps]]
