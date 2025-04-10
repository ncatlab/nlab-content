
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

The analogue of a [[Segal space]] in [[simplicial type theory]]. A *Segal type* is a type $A$ such that every [[pair of composable morphisms]] to $z:A$ is [[uniquely composable]]. 

## Definition

### Using morphisms

\begin{definition}
In [[simplicial type theory]], a **Segal type** is a type $A$ such that given elements $x:A$, $y:A$, and $z:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(y, z)$, the type

$$\sum_{h:\mathrm{hom}_A(x, z)} \sum_{k:\Delta^2 \to A} \left(
\begin{array}{c}
    (k(0, 0) = x) \times (k(0, 1) = y) \times (k(1, 1) = z) \times \\
    (k_{(0, 0), (0, 1)} = f) \times (k_{(0, 1), (1, 1)} = g) \times (k_{(0, 0), (1, 1)} = h)
\end{array}
\right)$$

is a [[contractible type]], where $\Delta^2 \coloneqq \sum_{(s, t):\mathbb{I} \times \mathbb{I}} s \leq t$ is the [[2-simplex]] type. 
\end{definition}

\begin{definition}
In [[simplicial type theory]] in the [[type theory with shapes]] formalism, a **Segal type** is a type $A$ such that given elements $x:A$, $y:A$, and $z:A$ and morphisms $f:\mathrm{hom}_A(x, y)$ and $g:\mathrm{hom}_A(y, z)$, 
$$\sum_{h:\mathrm{hom}_A(x, z)} \left\langle \Delta^2 \to A \vert_{[x, y, z, f, g, h]}^{\partial \Delta^2} \right\rangle$$

is a [[contractible type]], where $\Delta^2$ is the $2$-simplex probe shape and $\partial \Delta^2$ is its boundary. 
\end{definition}

### Using functions from shapes

In [[simplicial type theory]] where the directed interval primitive $\mathbb{I}$ is defined via axioms, let the 2-simplex type be defined as 

$$\Delta^2 \coloneqq \sum_{s:\mathbb{I}} \sum_{t:\mathbb{I}} s \leq t$$

and let the (2,1)-[[horn]] type be defined as 

$$\Lambda_1^2 \coloneqq \sum_{s:\mathbb{2}} \sum_{t:\mathbb{2}} (s =_\mathbb{I} 0) \vee (t =_\mathbb{I} 1)$$

where $P \vee Q$ is the [[disjunction]] of the types $P$ and $Q$. Since $s \leq t$ implies $(s =_{\mathbb{I}} 0) \vee (t =_{\mathbb{I}} 1)$ for all $s:\mathbb{I}$ and $t:\mathbb{I}$, we have a canonical function 

$$(\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P):\Delta^2 \to \Lambda^2_1$$

which is a tuple consisting of two copies of the [[identity function]] on $\mathbb{I}$ and a [[dependent function]] $P$ that takes the witness that $s \leq t$ to a witness that $(s =_{\mathbb{I}} 0) \vee (t =_{\mathbb{I}} 1)$. By precomposition, this leads to a function 

$$\lambda u.u \circ (\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P):(\Delta^2 \to A) \to (\Lambda^2_1 \to A)$$

for all types $A$. 

\begin{definition}
$A$ is a **Segal type** if the above function is an [[equivalence of types]]. 

$$\mathrm{isSegal}(A) \coloneqq \mathrm{isEquiv}(\lambda u.u \circ (\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P))$$
\end{definition}

## Categorical semantics

The categorical semantics of a Segal type is a [[Segal space object]] in a [[locally cartesian closed (infinity,1)-category|locally cartesian closed $(\infty,1)$-category]] $\mathbf{H}$. 

## Related concepts

* [[hom type]]
* [[discrete Segal type]]
* [[Rezk type]]
* [[isomorphism in a Segal type]]
* [[Segal space]]
* [[precategory]]
* [[skeletal Segal type]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

[[!redirects Segal type]]
[[!redirects Segal types]]