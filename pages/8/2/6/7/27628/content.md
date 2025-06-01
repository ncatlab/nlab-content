
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The notion of [[uniqueness quantifier|unique]] [[composition]] of a [[composable pair of morphisms]] in [[simplicial type theory]], since composition of a composible pair of morphisms isn't unique in general. 

## Definition

We work in [[simplicial type theory]] with a [[directed interval]] $\mathbb{I}$. 

### Using functions from shapes

Let the 2-simplex type be defined as 

$$\Delta^2 \coloneqq \sum_{s:\mathbb{I}} \sum_{t:\mathbb{I}} s \leq t$$

and let the (2,1)-[[horn]] type be defined as 

$$\Lambda_1^2 \coloneqq \sum_{s:\mathbb{2}} \sum_{t:\mathbb{2}} (s =_\mathbb{I} 0) \vee (t =_\mathbb{I} 1)$$

where $P \vee Q$ is the [[disjunction]] of the types $P$ and $Q$. Since $s \leq t$ implies $(s =_{\mathbb{I}} 0) \vee (t =_{\mathbb{I}} 1)$ for all $s:\mathbb{I}$ and $t:\mathbb{I}$, we have a canonical function 

$$(\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P):\Delta^2 \to \Lambda^2_1$$

which is a tuple consisting of two copies of the [[identity function]] on $\mathbb{I}$ and a [[dependent function]] $P$ that takes the witness that $s \leq t$ to a witness that $(s =_{\mathbb{I}} 0) \vee (t =_{\mathbb{I}} 1)$. By precomposition, this leads to a function 

$$\lambda u.u \circ (\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P):(\Delta^2 \to A) \to (\Lambda^2_1 \to A)$$

for all types $A$. 

\begin{definition}
A [[composable pair of morphisms]] $k:\Lambda^2_1 \to A$ is **uniquely composable** if the [[fiber type]] of $\lambda u.u \circ (\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P)$ at $k$ is a [[contractible type]]:

$$\mathrm{isUniquelyComposable}(f) \coloneqq \mathrm{isContr}\left(\sum_{h:\Delta^2 \to A} h \circ (\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P) = k \right)$$
\end{definition}

Let $h_{0,2}:\mathbb{I} \to \Delta^2$ be the [[face map]] which represents the unique morphism from $0$ to $2$ in the 2-simplex. 

\begin{definition}
Let $h:\Delta^2 \to A$ be the unique [[commutative triangle]] of the uniquely composable morphism $k:\Lambda^2_1 \to A$. The function $h \circ h_{0, 2}:\mathbb{I} \to A$ is the **unique composite** of $k$.  
\end{definition}

### Using morphisms

\begin{definition}
A composable pair of morphisms $(f, g)$ is **uniquely composable** if there exists a unique morphism $h:\mathrm{hom}_A(x, z)$ and function $k:\Delta^2 \to A$ such that $k(0, 0) = x$, $k(0, 1) = y$, $k(1, 1) = z$, $k_{(0, 0), (0, 1)} = f$, $k_{(0, 1), (1, 1)} = g$, $k_{(0, 0), (1, 1)} = h$:

$$\mathrm{isUniquelyComposable}(f, g) \coloneqq \mathrm{isContr}\left(\sum_{h:\mathrm{hom}_A(x, z)}\sum_{k:\Delta^2 \to A} \left(
\begin{array}{c}
    (k(0, 0) = x) \times (k(0, 1) = y) \times (k(1, 1) = z) \times \\
    (k_{(0, 0), (0, 1)} = f) \times (k_{(0, 1), (1, 1)} = g) \times (k_{(0, 0), (1, 1)} = h)
\end{array}
\right)\right)$$
\end{definition}

\begin{definition}
A morphism $h:\mathrm{hom}_A(x, z)$ is said to be the **unique composite** of $(f, g)$ if there exists a unique function $k:\Delta^2 \to A$ such that $k(0, 0) = x$, $k(0, 1) = y$, $k(1, 1) = z$, $k_{(0, 0), (0, 1)} = f$, $k_{(0, 1), (1, 1)} = g$, $k_{(0, 0), (1, 1)} = h$ and $(h, k)$ is the [[center of contraction]] of the dependent sum type:

$$\sum_{h:\mathrm{hom}_A(x, z)}\sum_{k:\Delta^2 \to A} \left(
\begin{array}{c}
    (k(0, 0) = x) \times (k(0, 1) = y) \times (k(1, 1) = z) \times \\
    (k_{(0, 0), (0, 1)} = f) \times (k_{(0, 1), (1, 1)} = g) \times (k_{(0, 0), (1, 1)} = h)
\end{array}
\right)$$
\end{definition}

## Properties

Identity morphisms are always uniquely composable:

* Every morphism $f:\mathrm{hom}_A(x, y)$ is uniquely composable with the [[identity morphism]] $\mathrm{id}_A(x):\mathrm{hom}_A(x, x)$, whose unique composite is the original morphism $f$ itself. 

* The [[identity morphism]] $\mathrm{id}_A(y):\mathrm{hom}_A(y, y)$ is uniquely composable with every morphism $f:\mathrm{hom}_A(x, y)$, whose unique composite is the original morphism $f$ itself. 

## Related concepts

* [[hom set]], [[hom type]]

* [[composable pair]]

* [[commutative triangle]]

* [[composite]]

* [[Segal type]]

* [[span in simplicial type theory]]

* [[cospan in simplicial type theory]]

## References

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

The phrase "unique composite" appears in:

* {#RS17} [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* [[Emily Riehl]], *[Could $\infty$-category theory be taught to undergraduates?](https://www.ams.org/journals/notices/202305/noti2692/noti2692.html?adat=May%202023&trk=2692&galt=feature&cat=feature&pdfissue=202305&pdffile=rnoti-p727.pdf)*, Notices of the AMS (May 2023) &lbrack;[published pdf](https://www.ams.org/journals/notices/202305/rnoti-p727.pdf), [arxiv:2302.07855](https://arxiv.org/abs/2302.07855)&rbrack;

[[!redirects uniquely composable]]

[[!redirects unique composite]]
[[!redirects unique composites]]

[[!redirects unique composition]]

[[!redirects unique composite of morphisms]]
[[!redirects unique composites of morphisms]]

[[!redirects unique composition of morphisms]]