
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _locally monoidal $(\infty,1)$-operad_ (called a _coherent $(\infty,1)$-operad_ in ([Lurie](#Lurie))) is an [[(∞,1)-operad]] $\mathcal{O}$ whose [[∞-module over an ∞-algebra over an (∞,1)-operad|modules]] over $\mathcal{O}$-[[algebra over an (∞,1)-operad|algebras]] come equipped with a well behaved [[tensor product]]

## Definition

Given $\pi_{\mathcal{O}}\colon \mathcal{O}^{\otimes} \rightarrow N(\mathrm{Fin}_*)$ a unital [[(∞,1)-operad]], write $\mathcal{O}^{\otimes}_{\mathrm{act}} \subset \mathcal{O}^{\otimes}$ be the wide subcategory of active morphisms.
Given a composable chain of active morphisms $X_0 \xrightarrow{f_1} \cdots \xrightarrow{f_n}$ with corresponding $n$-simplex $\sigma\colon \Delta^n \rightarrow \mathcal{O}^{\otimes}_{\mathrm{act}}$ and a downward-closed subset $S \subset [n]$, the [[(∞,1)]]-category of **extensions of $\sigma$ on $S$** is the full subcategroy
$$
  \mathrm{Ext}(\sigma,S) \subset \mathrm{Fun}(\Delta^n, \mathcal{O}^{\otimes})_{\sigma/}
$$
spanned by diagrams
 \begin{tikzcd}[ampersand replacement=\&]
	{X_0} \& {X_1} \& \cdots \& {X_n} \\
	{X'_0} \& {X'_1} \& \cdots \& {X'_n}
	\arrow["{f_1}", from=1-1, to=1-2]
	\arrow["{g_0}", from=1-1, to=2-1]
	\arrow["{f_2}", from=1-2, to=1-3]
	\arrow["{g_1}", from=1-2, to=2-2]
	\arrow["{f_n}", from=1-3, to=1-4]
	\arrow["{g_n}", from=1-4, to=2-4]
	\arrow["{f'_1}", from=2-1, to=2-2]
	\arrow["{f'_2}", from=2-2, to=2-3]
	\arrow["{f'_n}", from=2-3, to=2-4]
\end{tikzcd}
satisfying the following properties:

a. If $i \notin S$, $g_i$ is an equivalence

a. If $i \in S$, then $g_i$ is semi-inert over an inclusion $\langle n_i \rangle \hookrightarrow \langle n_i + 1 \rangle$ which omits a single value $a_i$

a. If $1 \le i \in S$, then $\pi_{\mathcal{O}}(f'_i)$ carries $a_{i-1}$ to $a_i$

a. each $f'_i$ is active.

If the $\infty$-category of colors $\mathcal{O}$ is an [[∞-groupoid]], then each $\mathrm{Ext}(\sigma,S)$ is itself an [[∞-groupoid]], i.e. a space.
A locally monoidal [[(∞,1)-operad]] can loosely be defined as one whose extension spaces satisfy excision under composition.

+-- {: .num_defn}
###### Definition

An [[(∞,1)-operad]] $\mathcal{O}^\otimes$ is **locally monoidal** if

1. it is unital;

1. the underlying [[(∞,1)-category]] $\mathcal{O}$ is an [[∞-groupoid]]; and

1. given a composable pair of morphisms $X \xrightarrow{f} Y \xrightarrow{g} Z$ with corresponding $3$-simplex $\sigma$, the associated diagram of spaces

\begin{tikzcd}[ampersand replacement=\&]
	{\mathrm{Ext}(\sigma,\{0,1\})} \& {\mathrm{Ext}(\sigma|\Delta^{\{0,1,3\}},\{0,1\})} \\
	{\mathrm{Ext}(\sigma|\Delta^{\{0,2,3\}},\{0\})} \& {\mathrm{Ext}(\sigma|\Delta^{\{0,3\}},\{0\})}
	\arrow[from=1-1, to=1-2]
	\arrow[from=1-1, to=2-1]
	\arrow[from=1-2, to=2-2]
	\arrow[from=2-1, to=2-2]
\end{tikzcd}
is a (homotopy) pushout square.

=--

This is ([Lurie, def. 3.3.1.9](#Lurie)).

## The exponentiability criterion

Let $\mathrm{Ar}^{\mathrm{sInt}}(\mathcal{O}^{\otimes}) \subset \mathrm{Fun}(\Delta^1, \mathcal{O}^{\otimes})$ be the full subcategory spanned by semi-inert morphisms.
The following is ([Lurie, thm. 3.3.2.2](#Lurie)).

\begin{theorem}
  Suppose $\mathcal{O}^{\otimes}$ is a unital [[(∞,1)-operad]] whose $\infty$-category of colors $\mathcal{O}$ is an [[∞-groupoid]]. Then, $\mathcal{O}^{\otimes}$ is locally monoidal if and only if the source map $s\colon \mathrm{Ar}^{\mathrm{sInt}}(\mathcal{O}^{\otimes}) \rightarrow \mathcal{O}^{\otimes}$ is an exponentiable fibration.
\end{theorem}

## Examples

Locally monoidal $(\infty,1)$-operads include

* [[Comm]]

  ([Lurie, example 3.3.1.12](#Lurie))

* [[Assoc]]

  ([Lurie, prop. 4.1.1.16](#Lurie))

* [[little k-cubes operad|little 0-cubes operad]]

  ([Lurie, example 3.3.1.13](#Lurie))

* [[little k-cubes operad]] for all $k \in \mathbb{N}$

  ([Lurie, theorem 5.1.1.1](#Lurie))



## References

Section 3.3.1 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects coherent (infinity,1)-operad]]
[[!redirects coherent (∞,1)-operad]]

[[!redirects coherent (∞,1)-operads]]
[[!redirects coherent (infinity,1)-operads]]

[[!redirects locally monoidal (∞,1)-operad]]

[[!redirects locally monoidal (∞,1)-operads]]
[[!redirects locally monoidal (infinity,1)-operads]]
