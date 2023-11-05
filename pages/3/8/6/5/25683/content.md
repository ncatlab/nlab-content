

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theories]] with more than one layer of type, dependent extension types are types which behave like [[dependent product types]] except the index type is the outer layer of type rather than the normal layer of type. Thus, dependent extension types can be defined in [[simplicial type theory]] and [[cubical type theory]]. 

## Definition

### In type theory with shapes

In [[type theory with shapes]], there are three different layers - there are the cube layer and the tope layer, which is [[logic over type theory]] where the cubes are the types and the topes are the propositions in the logic over type theory, and finally there is the type layer, which is a [[dependent type theory]]. 

Shapes are formed in the usual set-builder notation in [[set theory]]: given a cube $I$ and a predicate tope $t:I \vdash \phi$, one could construct the shape $\{t:I \vert \phi\}$. A cofibration in a type theory with shapes is an inclusion of shapes, which means shapes $\{t:I \vert \phi\}$ and $\{t:I \vert \psi\}$ with a predicate $t:I \vert \phi \vdash \psi$. 

Formation rules for dependent extension types:
$$\frac{
\begin{array}{l}
\{t:I \vdash \phi\} \; \mathrm{shape} \quad \{t:I \vdash \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \\
\Xi \vert \Phi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash a:A
\end{array}
}{\Xi \vert \Phi \vert \Gamma \vdash \langle \prod_{t:I \vert \psi} A \vert_a^\phi \rangle \; \mathrm{type}}$$

Introduction rules for dependent extension types:
$$\frac{
\begin{array}{l}
\{t:I \vdash \phi\} \; \mathrm{shape} \quad \{t:I \vdash \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \\
\Xi \vert \Phi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash a:A \\
\Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash b:A \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash b \equiv a \\
\end{array}
}{\Xi \vert \Phi \vert \Gamma \vdash \lambda t^{I\vert \phi}.b:\langle \prod_{t:I \vert \psi} A \vert_a^\phi \rangle}$$

Elimination rules for dependent extension types

$$\frac{
\begin{array}{l}
\{t:I \vdash \phi\} \; \mathrm{shape} \quad \{t:I \vdash \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \\
\Xi \vert \Phi \vert \Gamma \vdash f:\langle \prod_{t:I \vert \psi} A \vert_a^\phi \rangle \quad \Xi \vdash s:I \quad \Xi \vert \Phi \vdash \psi(s)
\end{array}
}{\Xi \vert \Phi \vert \Gamma \vdash f(s):A}$$

$$\frac{
\begin{array}{l}
\{t:I \vdash \phi\} \; \mathrm{shape} \quad \{t:I \vdash \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \\
\Xi \vert \Phi \vert \Gamma \vdash f:\langle \prod_{t:I \vert \psi} A \vert_a^\phi \rangle \quad \Xi \vdash s:I \quad \Xi \vert \Phi \vdash \phi(s)
\end{array}
}{\Xi \vert \Phi \vert \Gamma \vdash f(s) \equiv a(s)}$$

Computation rules for dependent extension types

$$\frac{
\begin{array}{l}
\{t:I \vdash \phi\} \; \mathrm{shape} \quad \{t:I \vdash \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \\
\Xi \vert \Phi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash a:A \\
\Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash b:A \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash b \equiv a \\
\Xi \vdash s:I \quad \Xi \vert \Phi \vdash \phi(s)
\end{array}
}{\Xi \vert \Phi \vert \Gamma \vdash (\lambda t^{I\vert \phi}.b)(s) \equiv b(s)}$$

Uniqueness rules for dependent extension types

$$\frac{
\begin{array}{l}
\{t:I \vdash \phi\} \; \mathrm{shape} \quad \{t:I \vdash \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \\
\Xi \vert \Phi \vert \Gamma \vdash f:\langle \prod_{t:I \vert \psi} A \vert_a^\phi \rangle \quad \Xi \vdash s:I \quad \Xi \vert \Phi \vdash \phi(s)
\end{array}
}{\Xi \vert \Phi \vert \Gamma \vdash f \equiv \lambda t^{I \vert \psi}.f(t)}$$

### In two-level type theory

In [[two-level type theory]], there are two different layers of types - there is the pretype or non-fibrant layer and there is the type or fibrant layer. A cofibration in two-level type theory is an inclusion of pretypes, which means pretypes $A$ and $B$ and an [[embedding]] $i:A \hookrightarrow B$. The rules for dependent extension types are then given as follows:

Formation rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{pretype} \quad \Xi \vdash B \; \mathrm{pretype} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, y:B \vert \Gamma \vdash C(y) \; \mathrm{type} \quad \Xi, x:A \vert \Gamma \vdash c(x):C(x)
\end{array}
}{\Xi \vert \Gamma \vdash \langle \prod_{y:B} C(y) \vert_c^A \rangle \; \mathrm{type}}$$

Introduction rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{pretype} \quad \Xi \vdash B \; \mathrm{pretype} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, y:B \vert \Gamma \vdash C(y) \; \mathrm{type} \quad \Xi, x:A \vert \Gamma \vdash c(x):C(x) \\
\Xi, y:B \vert \Gamma \vdash d(y):C(y) \quad \Xi, x:A \vert \Gamma \vdash d(i(x)) \equiv c(x):C(x) \\
\end{array}
}{\Xi \vert \Gamma \vdash \lambda y^B.d(y):\langle \prod_{y:B} C(y) \vert_c^A \rangle}$$

Elimination rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{pretype} \quad \Xi \vdash B \; \mathrm{pretype} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vert \Gamma \vdash f:\langle \prod_{y:B} C(y) \vert_c^A \rangle \quad \Xi \vdash b:B
\end{array}
}{\Xi \vert \Gamma \vdash f(b):C(b)}$$

$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{pretype} \quad \Xi \vdash B \; \mathrm{pretype} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vert \Gamma \vdash f:\langle \prod_{y:B} C(y) \vert_c^A \rangle \quad \Xi \vdash a:A
\end{array}
}{\Xi \vert \Gamma \vdash f(i(a)) \equiv c(a):C(a)}$$

Computation rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{pretype} \quad \Xi \vdash B \; \mathrm{pretype} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, y:B \vert \Gamma \vdash C(y) \; \mathrm{type} \quad \Xi, x:A \vert \Gamma \vdash c(x):C(x) \\
\Xi, y:B \vert \Gamma \vdash d(y):C(y) \quad \Xi, x:A \vert \Gamma \vdash d(i(x)) \equiv c(x):C(x) \quad \Xi \vert b:B\\
\end{array}
}{\Xi \vert \Gamma \vdash (\lambda y^B.d(y))(b) \equiv d(b):C(b)}$$

Uniqueness rules for dependent extension types

$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{pretype} \quad \Xi \vdash B \; \mathrm{pretype} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vert \Gamma \vdash f:\langle \prod_{y:B} C(y) \vert_c^A \rangle
\end{array}
}{\Xi \vert \Gamma \vdash f \equiv \lambda y^B.f(y):\langle \prod_{y:B} C(y) \vert_c^A \rangle}$$

Now, if the pretype layer has a [[Tarski universe|Tarski]] [[type of all propositions]] $(\Omega, \mathrm{El}_\Omega)$, then given a pretype $I$ and predicates $t:I \vdash \phi(t):\Omega$, $t:I \vdash \psi(t):\Omega$, one could construct the shapes defined in the above section via the [[dependent sum type]] in the pretype layer:

$$A \coloneqq \sum_{t:I} \mathrm{El}_\Omega(\phi(t)) \qquad B \coloneqq \sum_{t:I} \mathrm{El}_\Omega(\psi(t))$$

The additional requirement above that $t:I, \phi(t):\Omega \vdash \psi(t):\Omega$ implies that $A$ is a [[subtype]] of $B$ with an embedding $i:A \hookrightarrow B$ in the pretype layer. 

## Related concepts

* [[extension type]]
* [[dependent function type]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

[[!redirects dependent extension type]]
[[!redirects dependent extension types]]