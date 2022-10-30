
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Galois connections
* table of contents
{: toc}

## Definition

In [[order theory]] the term *Galois connection* can mean both: "[[adjunction]] between [[posets]]" and "[[dual adjunction]] between [[posets]]"; the former notion is sometimes called "monotone Galois connection" and the latter "antitone Galois connection". In this article the term "Galois connection" shall mean "[[dual adjunction]] between [[posets]]".

More explicitly, given posets $A$ and $B$, a __Galois connection__ between $A$ and $B$ is a pair of order-reversing maps $f:A\to B$ and $g:B\to A$ such that $a\le g(f(a))$ and $b\le f(g(b))$ for all $a\in A$, $b\in B$.

A **Galois correspondence** is a Galois connection which is an [[adjoint equivalence]] (so $a = g(f(a))$ and $b = f(g(b))$ for all $a \in A$, $b \in B$). 

+-- {: .num_prop} 
###### Proposition 
Any Galois connection $f: A \to B$, $g: B \to A$ induces a Galois correspondence between $f(A)$ and $g(B)$, given by the composites $g(B) \hookrightarrow A \stackrel{f}{\to} f(A)$ and $f(A) \hookrightarrow B \stackrel{g}{\to} g(B)$. 
=-- 

+-- {: .proof} 
###### Proof 
For any $a \in A$ of the form $a = g(b)$, we have $a \leq (g \circ f)(a)$ and also $(g \circ f)(a) = g(f(g(b))) \leq g(b) = a$ where the inequality follows from $b \leq f(g(b))$ and antitonicity of $g$. Hence $(g \circ f)(a) = a$ for all $a \in g(B)$. Similarly $(f \circ g)(b) = b$ for all $b \in f(A)$. 
=-- 


## Examples

* Frequently Galois connections between collections of [[subset]]s arise where $f(a)$ is "the set of all $y$ standing in some relation to every $x\in a$" and dually $g(b)$ is "the set of all $x$ standing in some relation to every $y\in b$."  See [[orthogonality]] for one example. 

* The Galois theory normally taught in graduate-level algebra courses (and based on the work of [[Évariste Galois]]) involves a Galois connection between the intermediate [[field]]s of a [[Galois extension]] and the subgroups of the corresponding [[Galois group]].


## Properties

*Every* Galois connection between full [[power sets]], 

$$(f: P(X) \to P(Y)^{op}) \dashv (g: P(Y)^{op} \to P(X))$$

is of the form in the first example: there is some [[binary relation]] $r$ from $X$ to $Y$ such that 

$$f(S) = \{y: \forall_{x \in X} x \in S \Rightarrow r(x, y)\}, \qquad g(T) = \{x: \forall_{y \in Y} y \in T \Rightarrow r(x, y)\}$$ 

Indeed, define $r: X \times Y \to \mathbf{2}$ by stipulating that $r(x, y)$ is true if and only if $y \in f(\{x\})$. Because $f$ is a left adjoint, it takes colimits in $P(X)$ (in this case, unions) to colimits in $P(Y)^{op}$, which are intersections in $P(Y)$. Since every $S$ in $P(X)$ is a union of singletons $\{x\}$, this gives 

$$f(S) = \bigcap_{x \in S} f(\{x\}) = \{y: \forall_{x \in S} r(x, y)\}$$ 

which is another way of writing the formula for $f$ given above. We observe that 

$$T \subseteq f(S) = \{y: \forall_{x \in S} r(x, y)\}$$ 

if and only if 

$$S \times T \subseteq r$$ 

(now viewing $r$ extensionally in terms of subsets). This last symmetrical expression in $S$ and $T$ means 

$$S \subseteq g(T) := \{x: \forall_{y \in T} r(x, y)\}$$ 

which means we have a Galois connection between $f$ and $g$ under this definition; since $g$ is uniquely determined by the presence of a Galois connection with $f$, we conclude that all Galois connections between power sets arise in this way, via a relation $r$ between $X$ and $Y$. 


## Related concepts

* [[modality]]
* [[adjoint modality]]
* [[adjunction]]
* Every Galois connection is an [[idempotent adjunction]].

## References

* Wojciech Dzik, Jouni J&#228;rvinen, Michiro Kondo, _Characterising intermediate tense logics in terms of Galois connections_ ([arXiv:1401.7646](http://arxiv.org/abs/1401.7646)).

* M. Ern&#233;, E. Klossoswki, A. Melton, G. E. Strecker, _A primer in Galois connections_ , Annals New York Academy of Sciences **704** (1993) pp.103-125. ([draft](http://www.math.ksu.edu/~strecker/primer.ps))

* O. Ore, _Galois connexions_ , Trans. AMS **55** (1944) pp.493-513. ([pdf](http://www.ams.org/journals/tran/1944-055-00/S0002-9947-1944-0010555-7/S0002-9947-1944-0010555-7.pdf))

[[!redirects Galois connection]]
[[!redirects Galois connections]]
[[!redirects Galois correspondence]]
[[!redirects Galois correspondences]]