+-- {: .standout}
Every wiki needs a sandbox! Just test between the horizontal rules below (`***` in the source) and don't worry about messing things up.
=--

***

<p>Here is an ordered list:</p>
<ol><li>Here is the first item.</li>
<li>Here is the second item.</li></ol>
<p>The difference between the previous items and the following ones is so remarkable that I want to take a break for a moment and remark upon it.</p>
<ol start="3"><li>OK, now here is the third item.</li>
<li>Item (4) obviates the need for item (5).</li>
<li value="6">And therefore we go on to item (6).</li>
<li>This is now item (7), automatically.</li></ol>
<p>And that's the whole list!</p>

Testing ... $\int_{0}^{1} \sin(3t) t^2 \mathrm{dt}$.

{:l: style="float:left;width:4em; font-style:normal;"}

* *1*{:l} list
* *1.1*{:l} in
* *2*{:l} order
* *3.1*{:l} is
* *3.2*{:l} markdown's
* *3.3*{:l} way

{:d: style="float:left; font-style:normal;"}

*1*{:d}
: list


*1.1*{:d}
: in

*2*{:d}
: order

*3.1*{:d}
: is

*3.2*{:d}
: markdown's

*3.3*{:d}
: way


### Preparation 

Let $\mathbb{P}$ be the groupoid of finite cardinals with bijections as morphisms. Since $\mathbb{P}$ is the core groupoid of the category $Fin$ of finite cardinals and functions between them, the coproduct on $Fin$ restricts to a symmetric monoidal product called the cardinal sum on $\mathbb{P}$. 

+-- {: .un_remark}
###### Remark
Under this symmetric monoidal structure, $\mathbb{P}$ may be characterized as the free symmetric strict monoidal category on one generator.
=--

The cardinal sum on $\mathbb{P}$ extends along the Yoneda embedding to a symmetric monoidal product $F \otimes G$ on the presheaf category $Psh(\mathbb{P}):=[\mathbb{P}^{op},Set]$. This is an instance of the [[Day convolution]]. 

+-- {: .un_note}
###### Warning
By abuse of notation, we will also denote the presheaf category $Psh(\mathbb{P})$ equipped with the monoidal structure induced by the cardinal sum by $Psh(\mathbb{P})$.
=--

Since $Psh(\mathbb{P})$ is a [[presheaf]] category, it is cocomplete, and since the Day convolution is cocontinuous in each of its separate arguments we say that $Psh(\mathbb{P})$ is **symmetric monoidally cocomplete**. 

+-- {: .un_note}
###### Note
In addition to the standard coend formula, the Day convolution product on the $Psh(\mathbb{P})$ may be described by the rule:

$$(F \otimes G)[S] = \sum_{S = T + U} F[T] \times G[U],$$ 

summing over all partitions of $S$ into two parts (each possibly empty). 
=--

According to the yoga of presheaf categories and Day convolution, given a symmetric monoidally cocomplete category $D$, a symmetric monoidal functor 

$$X: \mathbb{P} \to D$$

extends uniquely up to isomorphism to a symmetric monoidal _cocontinuous_ functor 

$$\hat{X}: Psh(\mathbb{P}) \to D,$$ 

taking a presheaf $W: \mathbb{P}^{op} \to Set$ to the [[limit|weighted colimit]] $W \cdot X$.  

+-- {: .un_remark}
###### Remark
It follows from the earlier remark and the above that we may describe $Psh(\mathbb{P})$ universally up to equivalence as the free symmetric monoidally cocomplete category on a single generator.
=--

+-- {: .un_note}
###### Digression
Recall that we can describe $W \cdot_{\mathbb{P}} X$ as follows: First note that the functor 

$$\Lambda:=Hom_D(X(\cdot),\cdot):\mathbb{P}^{op}\times D\to Set,$$ 

so $\Lambda$ also gives a functor $\bar{X}: D\to [\mathbb{P}^{op},Set]$ by restriction to the second coordinate. 

+--{.query}
I know what is trying to be said by those last five words, but it's not a clean use of language. Actually, there's a technical word for it: "[[currying]]" (after Haskell Curry). That could link to another page. 

Also, the functor gotten from $\Lambda$ got turned around a little -- I fixed it.
=--

Then we define $W \cdot_{\mathbb{P}} X$ to be the object representing the functor 

$$\Lambda_W:=Hom_Psh(\mathbb{P})(W,\bar{X}(\cdot)):D\to Set$$ 

whenever $\Lambda_W$ is representable.   

In general, weighted colimits may be described explicitly by coend formulas; here 

$$W \cdot_{\mathbb{P}} X = \int^{k: \mathbb{P}} F(k) \cdot X(k)$$ 

where $S \cdot d$ denotes the tensoring of a set $S$ with an object $d$, that is the coproduct of an $S$-indexed set of copies of $d$. The coend here indicates a coequalizer.

$$\sum_k W(k) \cdot S_k \cdot X(k) \rightrightarrows \sum_k W(k) \cdot X(k) \to \int^k W(k) \cdot X(k)$$ 

where one of the parallel arrows involves right actions of symmetric groups $S_k$ on the $F(k)$, and the other involves left actions of $S_k$ on objects $X$. In other words, the coend in this instance may be described as a sum of tensor products: 

$$W \cdot_{\mathbb{P}} X = \sum_k W(k) \otimes_{S_k} X(k).$$
=--

The aforementioned universal property of $Psh(\mathbb{P})$ with its convolution product may be more explicitly described as follows: given a symmetric monoidally cocomplete category $D$ and an object $d$ therein, there exists up to isomorphism a _unique_ symmetric monoidal cocontinuous functor $Psh(\mathbb{P}) \to D$ which sends the presheaf represented by the cardinal $1$, $h_1$, to $d$. 

This functor takes a presheaf $F: \mathbb{P}^{op} \to Set$ to the following object of $D$: 

$$\sum_k F(k) \otimes_{S_k} d^{\otimes k}.$$

+-- {: .un_example}
######Example
When $D$ is the symmetric monoidally cocomplete category $(Set, \times)$ and $x$ is a set, this formula 

$$\hat{F}(x) = \sum_n F(k) \otimes_{S_k} x^k$$ 

is the value at $x$ of what Joyal calls the _analytic functor_ $\hat{F}: Set \to Set$ associated to a species $F$, which has been proposed as the categorification of the theory of exponential generating functions. The fact that $F \mapsto \hat{F}(x)$ is symmetric monoidal (cocontinuous) means that there is a canonical isomorphism

$$\widehat{(F \otimes_{Day} G)}(x) \cong \hat{F}(x) \times \hat{G}(x)$$ 

In other words, $F \mapsto \hat{F}$ behaves like a categorified version of Fourier transform, taking convolution products to ordinary (pointwise) products. 
=--

* For symmetric monoidally cocomplete categories $C, D$, let $\underline{Hom}(C, D)$ denote the category of symmetric monoidal cocontinuous functors $C \to D$. The universal property of $Psh(\mathbb{P})$ means that we have an equivalence $\underline{Hom}(Psh(\mathbb{P}), D) \simeq D$. Consequently, we have an equivalence $\underline{Hom}(Psh(\mathbb{P}), Psh(\mathbb{P})) \simeq Psh(\mathbb{P})$. Since symmetric monoidal cocontinuous functors compose, the category on the left carries a monoidal product given by endofunctor composition. Transferring endofunctor composition across the equivalence produces a monoidal product on $Psh(\mathbb{P})$ called _substitution product_ of species. The substitution product of species $F, G$ is denoted $F \circ G$. 

In detail: a species $G: \mathbb{P}^{op} \to Set$ induces a symmetric monoidal cocontinuous functor 

$$Psh(\mathbb{P}) \to Psh(\mathbb{P}): F \mapsto F \circ G = \sum_k F(k) \otimes_{S_k} G^{\otimes_{Day} k}$$ 

The $k$-fold Day tensor power of $G$ is given (in the language of species) by the formula 

$$G^{\otimes k}[S] = \sum_{S = T_1 + \ldots + T_k} G[T_1] \times G[T_2] \times \ldots \times G[T_k]$$ 

where we sum over all ways of breaking up a finite set $S$ into $k$ blocks, some possibly empty. Thus we have an explicit description of the substitution product, 

$$(F \circ G)[n] = \sum_k F[k] \otimes_{S_k} (\sum_{[n] = T_1 + \ldots + T_k} G[|T_1|] \times \ldots \times G [|T_k|]),$$ 

and it is clear from our discussion above that substitution is a monoidal product. 

### Definition as monoid 

We are at last ready for the one-sentence **definition**: 

A ($Set$-based) **operad** is a [[monoid]] in the [[monoidal category]] $(Psh(\mathbb{P}), \circ)$. 
***

category: meta

[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects שנה טובה]]