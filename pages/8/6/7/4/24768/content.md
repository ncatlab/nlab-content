\tableofcontents

\section{Idea}

The counterpart to [[function extensionality]] but for [[products]]/[[pairs]] of [[elements]] $(a, b)$. Product extensionality characterizes the equality of elements in [[cartesian products]] in [[set theory]] and [[product types]] in [[type theory]]. 

\section{Definition}

\subsection{In set theory}

Product extensionality states that for all elements $a \in A$, $a' \in A$, $b \in B$, and $b' \in B$, $a = a'$ and $b = b'$ if and only if $(a, b) = (a', b')$. Product extensionality is sometimes assumed as an axiom in [[material set theory]] to make the [[pairing structure]] into an [[ordered pairing structure]] $(a, b)$. 

\subsection{In type theory}

In [[intensional type theory]], [[equality]] is represented by the [[identity type]], and furthermore, there might be more than one element of the identity type in [[intensional type theory]], so a naive translation of product extensionality into intensional type theory doesn't result in the right statement. 

Instead, product extensionality is the statement that given types $A$ and $B$, the [[binary function application to identities]] $\mathrm{apbinary}_{(-,-)}(a, a', b, b')$ of the function $a:A, b:B \vdash (a, b):A \times B$ defined in the [[introduction rule]] for the [[product type]] is an [[equivalence of types]] for all elements $a:A$, $a':A$ and $b:A$, $b':A$:
$$\mathrm{prodext}(a, a', b, b'):\mathrm{isEquiv}(\mathrm{apbinary}_{(-,-)}(a, a', b, b'))$$

\subsection{Rules for product extensionality}

Formation rules for the identity type of negative product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash x:A \times B \quad \Gamma \vdash y:A \times B}{\Gamma \vdash \mathrm{Id}_{A \times B}(x, y) \; \mathrm{type}}$$

Introduction rules for the identity type of negative product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash a:A  \quad \Gamma \vdash a':A \quad \Gamma \vdash b:B \quad \Gamma \vdash b':B}{\Gamma \vdash \mathrm{apbinary}_{(-,-)}(a, a', b, b'):\mathrm{Id}_{A}(a, a) \times \mathrm{Id}_{B}(b, b') \to \mathrm{Id}_{A \times B}((a, b), (a', b'))}$$

Elimination rules for the identity type of negative product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash x:A \times B \quad \Gamma \vdash y:A \times B}{\Gamma \vdash \mathrm{ap}_{\pi_1}(x, y):\mathrm{Id}_{A \times B}(x, y) \to \mathrm{Id}_{A}(\pi_1(x), \pi_1(y))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash x:A \times B \quad \Gamma \vdash y:A \times B}{\Gamma \vdash \mathrm{ap}_{\pi_2}(x, y):\mathrm{Id}_{A \times B}(x, y) \to \mathrm{Id}_{B}(\pi_2(x), \pi_2(y))}$$

Computation rules for the identity type of negative product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash x:A \times B \quad \Gamma \vdash y:A \times B}{\Gamma, p:\mathrm{Id}_{A}(\pi_1(x), \pi_1(y)), q:\mathrm{Id}_{B}(\pi_2(x), \pi_2(y)) \vdash \mathrm{ap}_{\pi_1}(\mathrm{apbinary}_{(-,-)}(\pi_1(x), \pi_2(x), \pi_1(y), \pi_2(y))(p, q)) \equiv p:\mathrm{Id}_{A}(\pi_1(x), \pi_1(y))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash x:A \times B \quad \Gamma \vdash y:A \times B}{\Gamma, p:\mathrm{Id}_{A}(\pi_1(x), \pi_1(y)), q:\mathrm{Id}_{B}(\pi_2(x), \pi_2(y)) \vdash \mathrm{ap}_{\pi_2}(\mathrm{apbinary}_{(-,-)}(\pi_1(x), \pi_2(x), \pi_1(y), \pi_2(y))(p, q)) \equiv q:\mathrm{Id}_{A}(\pi_2(x), \pi_2(y))}$$

Uniqueness rules for the identity type of negative product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash a:A  \quad \Gamma \vdash a':A \quad \Gamma \vdash b:B \quad \Gamma \vdash b':B}{\Gamma, r:\mathrm{Id}_{A \times B}((a, b), (a', b')) \vdash \mathrm{apbinary}_{(-,-)}(a, a', b, b')(\mathrm{ap}_{\pi_1}(r), \mathrm{ap}_{\pi_2}(r)) \equiv r:\mathrm{Id}_{A \times B}((a, b), (a', b'))}$$

These rules ensure that $\mathrm{apbinary}_{(-,-)}$ is a judgmental equivalence of types. 

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
* [[tuple extensionality]]

\section{References}

For judgmental product extensionality in higher observational type theory, see

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

For a proof that the given function above between identity types is a [[quasi-inverse function]] in [[intensional type theory]], see section 2.6:

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))