\tableofcontents

\section{Idea}

The counterpart to [[function extensionality]] but for [[products]]/[[pairs]] of [[elements]] $(a, b)$. Product extensionality characterizes the equality of elements in [[cartesian products]] in [[set theory]] and [[product types]] in [[type theory]]. 

\section{Definition}

\subsection{In set theory}

Product extensionality states that for all elements $a \in A$, $a' \in A$, $b \in B$, and $b' \in B$, $a = a'$ and $b = b'$ if and only if $(a, b) = (a', b')$. Product extensionality is sometimes assumed as an axiom in [[material set theory]] to make the [[pairing structure]] into an [[ordered pairing structure]] $(a, b)$. 

\subsection{In type theory}

In [[intensional type theory]], [[equality]] is represented by the [[identity type]], and furthermore, there might be more than one element of the identity type in [[intensional type theory]], so a naive translation of product extensionality into intensional type theory doesn't result in the right statement. 

Instead, we have the following:

For every type $A$ and $B$ and elements $a:A$, $a':A$ and $b:A$, $b':A$, there is a canonical function 
$$\mathrm{idstoproductid}(a, a', b, b'):(a =_A a') \times (b =_B b') \to ((a, b) =_{A \times B} (a', b'))$$
inductively defined by 
$$\mathrm{idstoproductid}(a, a, b, b)(\mathrm{refl}_{A}(a), \mathrm{refl}_{B}(b)) \equiv \mathrm{refl}_{A \times B}((a, b)):\Omega(A \times B, (a, b))$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

Product extensionality is the statement that the function $\mathrm{idstoproductid}(a, a', b, b')$ is an [[equivalence of types]] for all elements $a:A$, $a':A$ and $b:A$, $b':A$:
$$\mathrm{prodext}(a, a', b, b'):\mathrm{isEquiv}(\mathrm{idtoprojectionids}(a, a', b, b'))$$

\subsection{Judgmental product extensionality}

One could replace the equivalence of types above with a [[judgmental equality]] of types, resulting in judgmental product extensionality, that for all types $A$ and $B$ and elements $a:A$, $a':A$, $b:B$, and $b':B$, 
$$(a, b) =_{A \times B} (a', b') \equiv (a =_A a') \times (b =_B b')$$

Judgmental product extensionality holds in [[cubical type theory]] and [[higher observational type theory]]. 

\subsection{Relation to dependent product extensionality}

Product extensionality is equivalent to dependent product extensionality for dependent products indexed by the [[two-valued type]] $\mathbb{2}$. Indeed, given types $A$ and $B$, we can define a type family $C$ indexed by $\mathbb{2}$ as $C(0) \coloneqq A$ and $C(1) \coloneqq B$. Then $A \times B$ is the same as $\prod_{x:\mathbb{2}} C(x)$. 

We define $c:\prod_{x:\mathbb{2}} C(x)$ and $c':\prod_{x:\mathbb{2}} C(x)$ by $c(0) \coloneqq a$, $c(1) \coloneqq b$, $c'(0) \coloneqq a'$, $c'(1) \coloneqq b'$. 

There is a canonical function
$$\mathrm{idstodepprodid}(c, c'):(c(0) =_{C(0)} c'(0)) \times (c(1) =_{C(1)} c'(1)) \to (c =_{\prod_{x:\mathbb{2}} C(x)} c')$$
inductively defined by 
$$\mathrm{idstodepprodid}(c, c)(\mathrm{refl}_{C(0)}(c(0)), \mathrm{refl}_{C(1)}(c(1))) \equiv \mathrm{refl}_{\prod_{x:\mathbb{2}} C(x)}(c):\Omega(\prod_{x:\mathbb{2}} C(x), c)$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

We could also make $(c(0) =_{C(0)} c'(0)) \times (c(1) =_{C(1)} c'(1))$ into a dependent product as well, as $\left(\prod_{x:\mathbb{2}} (c(x) =_{C(x)} c'(x))\right)$, making the above function

$$\mathrm{idstodepprodid}(c, c'):\left(\prod_{x:\mathbb{2}} (c(x) =_{C(x)} c'(x))\right) \to (c =_{\prod_{x:\mathbb{2}} C(x)} c')$$

Product extensionality is the statement that the function $\mathrm{idstodepprodid}(c, c')$ is an [[equivalence of types]] for all elements $c:\prod_{x:\mathbb{2}} C(x)$ and $c':\prod_{x:\mathbb{2}} C(x)$:
$$\mathrm{prodext}(c, c'):\mathrm{isEquiv}(\mathrm{idstodepprodid}(c, c'))$$

\section{See also}

* [[extensionality]]

\section{References}

For judgmental product extensionality in higher observational type theory, see

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

For a proof that the given function above between identity types is a [[quasi-inverse function]] in [[intensional type theory]], see section 2.6:

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))