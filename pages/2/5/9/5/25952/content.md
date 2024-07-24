
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The notion of **strong dinatural transformation** is a notion of [[natural transformation]] between [[pairs]] of [[functors]] $C^{op}\times C\to D$ that is stronger than that of *[[dinatural transformations]]*.

Unlike dinatural transformations, strong dinatural transformations can always be [[composition|composed]]. They have close connections to [[parametricity]] in [[computer science]].

## Definition

Let $F,G:C^{op}\times C\to D$ be functors.  A **strong dinatural transformation** $\alpha :F\to G$ consists of, for each $c\in C$, a component $\alpha_c : F(c,c) \to G(c,c)$, such that for any morphism $f:c\to c'$ in $C$ and any [[span]] $F(c',c') \leftarrow W \to F(c,c)$ in $D$, if the square on the left commutes, then the outer hexagon also commutes:

\[
\begin{array}{ccccccc}
 &  & F(c,c) & \overset{\alpha_{c}}{\to} & G(c,c)\\
 & \nearrow & & \overset{\mathclap{F(c,f)}}{\searrow}  &  & \overset{\mathclap{G(c,f)}}{\searrow}\\
W &  &  &  & F(c,c') &  & G(c,c')\\
& \searrow & & \underset{\mathclap{F(f,c')}}{\nearrow} &  & \underset{\mathclap{G(f,c')}}{\nearrow}\\
 &  & F(c',c') & \underset{\alpha_{c'}}{\to} & G(c',c')
\end{array}\,.
\]

If the pullback $F(c,c) \times_{F(c,c')} F(c',c')$ exists in $D$, it suffices to assert this when the square on the left is the defining one of that pullback.  On the other hand, if $D$ has a [[separator]] (such as $1\in Set$), it suffices to assert this when $W$ is the separator.

By comparison, a [[dinatural transformation]] asserts this condition *only* when $W = F(c',c)$ with the span consisting of $F(c',f)$ and $F(f,c)$.

## References

Originally introduced (as "strong dinatural transformations") in Definition 2.7 of:

* [[Philip S. Mulry]], *Strong Monads, Algebras and Fixed Points*, in: _Applications of Categories in Computer Science_, London Mathematical Society Lecture Note Series **177** (1991) 202–216 &lbrack;[doi:10.1017/CBO9780511525902.012](https://doi.org/10.1017/CBO9780511525902.012)&rbrack;

Further developments:

* Philip S Mulry. *Strong monads, algebras and fixed points*. Applications of Categories in Computer Science 177 (1992), 202–216

* Robert Paré and Leopoldo Román. *Dinatural numbers*.  Journal of Pure and Applied Algebra 128, 1 (1998), 33–92

* A. Eppendahl, *Parametricity and Mulry's Strong Dinaturality*, <https://qmro.qmul.ac.uk/xmlui/bitstream/handle/123456789/4501/768_Eppendahl_12-1999.pdf?sequence=1>

* Varmo Vene. *Parametricity and Strong Dinaturality.* (2006). <https://www.ioc.ee/~tarmo/tday-voore/vene-slides.pdf>

* Jennifer Hackett and Graham Hutton. *Programs for cheap!*. In 2015 30th Annual ACM/IEEE Symposium on Logic in
Computer Science. IEEE, 115–126.

* Tarmo Uustalu. *Strong dinaturality and initial algebras.* 12th Nordic Wksh. on Programming Theory, NWPT 2 (2000).

* Tarmo Uustalu. *A Note on Strong Dinaturality, Initial Algebras and Uniform Parameterized Fixpoint Operators*. In
FICS. 77–82.

Strong dinatural transformations are called **paranatural transformations** in:

* [[Jacob Neumann]], *Paranatural Category Theory*, 2023, [arxiv:2307.09289](https://arxiv.org/abs/2307.09289)

[[!redirects strong dinatural transformations]]

[[!redirects paranatural transformation]]
[[!redirects paranatural transformations]]
[[!redirects paranatural]]
[[!redirects paranaturality]]
[[!redirects strong dinaturality]]


