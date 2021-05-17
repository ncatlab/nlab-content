## Contents
* table of contents
{: toc}

## Idea
_Automatic differentiation_ (AD) is a technique for computing ([[transpose matrix|transposed]]) [[derivative|derivatives]] of functions implemented by computer programs, essentially by applying the chain-rule across program code.
It is typically the method of choice for computing derivatives in machine learning and scientific computing because of its efficiency and numerical stability.

## Forward and reverse automatic differentiation
AD works by calculating the (transposed) derivative of a composite program in terms of the (transposed) derivatives of the parts, by using the chain-rule. The distinction between derivatives and transposed derivatives leads to the main distinction in automatic differentiation modes:


* _forward mode AD_: this implements the [[tangent bundle]] functor $T$ and calculates derivatives by a forward pass to calculate function values (primals), followed by another forward pass to calculate derivative values (tangents); these two forward passes can be interleaved into a single forward pass for efficiency.

* _reverse mode AD_: this implements the [[cotangent bundle]] functor $T^*$ and calculates transposed derivatives by a forward pass to calculate function values (primals), followed by a _reverse_ pass (inverting the control flow of the original program) to calculate transposed derivative values (cotangents); these two passes cannot easily be interleaved due to their differing direction.

When calculating a derivative of a program that implements a function $f:R^n\to R^m$, reverse mode tends to be the more efficient algorithm if $n \gg m$ and forward mode tends to be more efficient if $n\ll m$.
Seeing that many tasks in machine learning and statistics require the calculation of derivatives (for use in gradient-based optimization or Monte-Carlo sampling) of functions $f:R^n\to R$ (e.g. probability density functions) for $n$ very large, reverse mode AD tends to be the most popular algorithm.

## Combinatory Homomorphic Automatic Differentiation (CHAD) - a categorical take on AD

Let us fix some class of categories with [[stuff]] $S$. We will call its members $S$-categories. For example, for our purposes, $S$ might include [[property|properties]] like

* closure under finite [[products]] (aka tuples, in programming-speak);
* [[cartesian closed category|Cartesian closure]] (aka higher-order functions);
* closure under finite [[coproducts]] (aka sum or variant types);

and [[structure]] like 

* designated objects like $R$ and $Z$ (which we think of as real numbers and integers)
* designated morphisms like $sin:R\to R$, $cos: R\to R$, $(+): R\times R\to R$, $(*):R\times R\to R$ (which we think of as the corresponding mathematical operations). 


The idea behind CHAD will be to view forward and reverse AD as the unique structure (stuff) preserving functor (homomorphism of $S$-categories) from the initial $S$-category $Syn$ to two suitably chosen $S$-categories $\Sigma_{CSyn}LSyn$ and $\Sigma_{CSyn}LSyn^{op}$.

### The source language
Consider the initial $S$-category $Syn$ (put differently, the S-properties category that is freely generated from $S$-structure).
We can think of this category as a programming language: its objects are types and its morphisms are programs modulo [[beta-equivalence]] and [[eta-equivalence]].
In fact, for a wide class of programming languages, we can find a suitable choice of stuff $S$, such that the programming language arises as the initial $S$-category.
We will refer to this category as the _source language_ of our AD transformation: its morphisms are the programs we want to differentiate.

For example, if we choose the property part of $S$ to consist of Cartesian closure and the structure part of $S$ consists of designated objects $R$ and $Z$ and morphisms $sin$, $cos$, $(+)$, and $(*)$, then $Syn$ is the simply typed [[lambda-calculus]] with base types $R$ and $Z$ and the primitive operations $sin$, $cos$, $(+)$, and $(*)$.

### The target language and deriving AD
Given a strictly [[indexed category]] $L:C^{op}\to Cat$, we can form its [[Grothendieck construction]] $\Sigma_C L$, which is a [[split fibration]] over $C$.
Similarly, we can take the [[opposite category]] $L^{op}:C^{op}\to Cat$ of $L$ and form $\Sigma_C L^{op}$ from that.

For most natural choices of stuff $S$, we can find elegant sufficient conditions on $C$ and $L$ that guarantee that $\Sigma_C L$ and $\Sigma_C L^{op}$ are both $S$-categories.
Let us call a strictly indexed category $L:C^{op}\to Cat$ satisfying these conditions a $S'$-category (where we think of $S'$ again as [[stuff]]).
We give the corresponding $S'$ for some examples for different choices of $S$:

* for the property of closure under finite products, we demand that $C$ has finite products and $L$ has finite ([[indexed]]) [[biproducts]] (or, equivalently, that $L$ has finite products and is enriched over [[commutative monoids]]); (this can be extended with conditions to guarantee Cartesian closure; see the CHAD paper below;)
* for the property of closure under finite coproducts, we demand that $C$ has finite coproducts and that $L$ is [[extensive]], in the sense that the canonical functors $L(0)\to 1$ and $L(A+B)\to L(A)\times L(B)$ are isomorphisms of categories;
* for structure like distinguished objects $R$, we need to have chosen distinguished objects $R'$ of $C$, $TR'$ (which we think of as the tangent bundle of $R'$)  of $L(R')$ and $T^* R'$ (the cotangent bundle of $R'$) of $L(R')$;
* for structure like distinguished morphisms $(*):R\times R\to R$, we need to have chosen distinguished morphisms $(*)'$ in $C(R'\times R', R')$ (the primal computation of $(*)$), $T(*)'$ in $L(R'\times R')(TR'\times TR', TR')$ (the derivative of $(*)$) and $T^*(*)'$ in $L(R'\times R')(TR', TR'\times TR')$ (the transposed derivative of $(*)$).

Let us write $LSyn:CSyn^{op}\to Cat$ for the initial $S'$-category. 
We think of this category as the _target language_ of automatic differentiation, in the sense that the forward/reverse derivatives of programs (morphisms) in the source language $Syn$ with consist of an associated primal program that is a morphism in $CSyn$ and an associated tangent/cotangent program that is a morphism in $LSyn$/$LSyn^{op}$.
As a programming language, $LSyn$ is a [[linear dependent type theory]] over the Cartesian type theory $CSyn$.
 

Indeed, as for any $S'$-category $L:C^{op}\to Cat$, $\Sigma_C L$ and $\Sigma_C L^{op}$ are $S$-categories, it follows that $\Sigma_{CSyn} LSyn$ and $\Sigma_{CSyn} LSyn^{op}$ are, in particular, $S$-categories.
Seeing that $Syn$ is the initial $S$-category, we obtain unique morphisms of $S$-categories:

* forward AD: $Df:Syn\to \Sigma_{CSyn} LSyn$;
* reverse AD: $Dr:Syn\to \Sigma_{CSyn} LSyn^{op}$.

### Semantics of the source and target languages
The category $Set$ of [[sets]] and functions gives another example of an $S$-category, for a lot of choices of $S$ (if we choose the sets $[[R]]$ and functions $[[op]]$ that we would like to denote with the types $R$ and operations $op$ in the structure part of $S$).
Moreover, the strictly indexed category $Fam(CMon):Set^{op}\to Cat$ of [[families]] of [[commutative monoids]] tends to give an example of an $S'$-category.
By initiality of $Syn$ and $LSyn:CSyn^{op}\to Cat$, we obtain

* the semantics of the source language: the unique $S$-functor $[[-]]:Syn\to Set$;
* the semantics of the target language: the unique $S'$-functor $[[-]]:(CSyn,LSyn)\to (Set,Fam(CMon))$ (with a slight abuse of notation).

In particular, we see that source language programs $t\in Syn(A, B)$ get interpreted as a function $[[t]]\in Set([[A]], [[B]])$.
Similarly, programs  $t\in CSyn(A, B)$ in the target language with _Cartesian_ type get interpreted as a function $[[t]]\in Set([[A]], [[B]])$.
Finally, programs $t\in LSyn(A)(B,C)$ in the target language with _linear_ type get interpreted as a function $[[t]] \in Fam(CMon)([[A]])([[B]],[[C]])$:
families of monoid homomorphisms.

### Correctness of CHAD
We say that CHAD calculates the correct derivative (resp. transposed derivative) of a program $s$ if
the [[semantics]] $[[Df(s)]]$ of the program $Df(s)$ (resp. $Dr(s)$) equals the pair of the semantics $[[s]]$ of $s$ and the derivative $T[[s]]$ (resp. transposed derivative $T^*[[s]]$) of the semantics $[[s]]$ of $s$.
CHAD is correct in the sense that it calculates the correct (transposed) derivative of any composite (possibly higher-order) program between first-order types  (meaning: types built using only [[positive type]] formers), provided that it calculates the correct (transposed) derivatives of all primitive operations like $(*)$ that we used to generate the source language.
That is, CHAD is a valid way for compositionally calculating (transposed) derivatives of composite computer programs, as long as we correctly implement the derivatives for all primitive operations (basic mathematical functions like multiplication, addition, sine, cosine) in the language.

We can prove this by a standard [[logical relations]] argument, relating smooth curves to their primal and (co)tangent curves.
Viewed more abstractly, the proof follows automatically because the [[Artin gluing]] along a representable functor (like the hom out of the real numbers) of an $S$-category is itself again an $S$-category, for common most choices of $S$.

## Related concepts 

* [[differential programming]]
* [[backpropagation]]

## References

Forward mode automatic differentiation was introduced by Robert Edwin Wengert in 

* [[Robert Edwin Wengert]], A simple automatic derivative evaluation program. Communications of the ACM 7.8. 1964.

An early description of reverse mode automatic differentiation can be found in 

* [[Bert Speelpenning]], Compiling fast partial derivatives of functions given by algorithms. Illinois Univ., Urbana (USA). Dept. of Computer Science. Technical report. 1980.

but it was already described earlier by others such as Seppo Linnainmaa:

* [[Seppo Linnainmaa]], The representation of the cumulative rounding error of an algorithm as a Taylor expansion of the local rounding errors. Master's Thesis (in Finnish), Univ. Helsinki. 1970.

A categorical analysis of (non-interleaved) forward and reverse AD is given by 

* [[Matthijs Vákár]], CHAD: Combinatory Homomorphic Automatic Differentiation. 2021. [arXiv preprint 2103.15776](https://arxiv.org/abs/2103.15776) [Haskell implementation](https://github.com/VMatthijs/CHAD)

A categorical analysis of (interleaved) forward mode AD for calculating higher order derivatives is given by 

* [[Mathieu Huot]], [[Sam Staton]], [[Matthijs Vákár]], Higher Order AD of Higher Order Functions. 2021. [arXiv preprint 2101.06757](https://arxiv.org/abs/2101.06757)