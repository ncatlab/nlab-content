#Contents#
* table of contents
{:toc}

## Remark

This is a small subcollection of my (Tom Mainiero's) personal notes on some functorial aspects of the [[Gelfand-Naimark-Segal construction]] (GNS construction) that have been sitting around for a while. Please feel free to contribute! The ideas here underlie some of the constructs of [Homtools](#Mainiero2019).


## Baby's first GNS functor
For the purposes of this section, $R$ is a fixed a unital ring and $A$ is a unital $R$-algebra.

\begin{definition}
Let ${}_{A}\mathbf{Mod}^{\bullet}$ denote the category with:

* objects given by *pointed left $A$-modules*: pairs $(M,m)$ of a left $A$-module $M$ and an element $m \in M$

* morphisms given by point preserving intertwiners.

${}_{A}\mathbf{Mod}^{\odot}$ is the full subcategory of ${}_{A}\mathbf{Mod}^{\bullet}$ whose objects are *cyclic* pointed modules: $(M,m)$ such that $A m = M$.
\end{definition}

\begin{remark}
For those that find the notion of a pointed module somewhat awkward, note that: ${}_{A}\mathbf{Mod}^{\bullet}$ is equivalent to the overcategory ${}_{A}{A}/{}_{A}\mathbf{Mod}$, where ${}_{A}\mathbf{Mod}$ is the category of left $A$-modules.
\end{remark}

For any left $A$-module $M$, we denote the annihilator of a point $m \in M$ as:
\[
	\mathrm{Ann}_{A}(m) \coloneqq \{ a \in A : a \cdot m = 0 \}.
\]

The following lemma establishes the fact that the hom-set ${}_{A}\mathbf{Mod}^{\bullet}((M,m), (N,n))$ is either the empty set or a point when $(M,m)$ is a cyclic pointed module. 

\begin{lemma}
	Let $(M,m)$ and $(N,n)$ be pointed $A$-modules and suppose $(M,m)$ is cyclic. Then there exists a morphism from $(M,m)$ to $(N,n)$ if and only if $\mathrm{Ann}_{A}(m) \subseteq \mathrm{Ann}_{A}(n)$.
	Moreover, this morphism is unique when it exists.
\end{lemma}
\begin{proof}
	This follows quickly from the fact that a morphism $f: (M,m) \rightarrow (N,n)$ must satisfy $f(a m) =a n$ for all $a \in A$.
\end{proof}

There is an immediate corollary of this Lemma: ${}_{A}\mathbf{Mod}^{\odot}$ is equivalent to the poset of left-ideals of $A$ (thought of as a category).
This equivalence of categories is actually part of the restriction of a larger adjunction.
We now spell out the details of this claim.

\begin{definition}
$\mathbf{L}(A)$ is the [[thin category]] given by the poset of left ideals of $A$: 

* objects are left ideals of $A$, and 

* there is a unique morphism $I \to J$ if and only if $I \subseteq J$.

\end{definition}

Note that the process of taking annihilators of distinguished points of left $A$-modules defines a functor:
\[
  \mathsf{Ann}_{A} \colon \mathbf{Mod}_{A}^{\bullet} \longrightarrow \mathbf{L}(A).
\]
Explicitly: it acts on objects by:
\[
   \mathsf{Ann}_{A} \colon (M,m) \mapsto \mathrm{Ann}_{A}(m) \coloneqq \{ a \in A : a \cdot m = 0 \}
\]
and its action on morphisms is deduced from the following straightforward remark.

\begin{remark}
 If $f \colon (M,m) \to (N,n)$ is a morphism of pointed modules, then $a \cdot n = a \cdot f(m) = f(a \cdot m)$; so we must have $\mathrm{Ann}_{A}(m) \subseteq \mathrm{Ann}_{A}(n)$
\end{remark}

Thus, for $f \colon (M,m) \to (N,n)$ a $\mathbf{Mod}^{\bullet}_{A}$-morphism, we can define $\mathsf{Ann}_{A}(f) \colon \mathsf{Ann}_{A}(m) \to \mathsf{Ann}_{A}(n)$ as the unique $\mathbf{L}(A)$-morphism given by the inclusion of ideals $\mathrm{Ann}_{A}(m) \subseteq \mathrm{Ann}_{A}(n)$.

\begin{proposition}
There is an adjunction:
\begin{center}
  \begin{tikzcd}
    \mathbf{L}(A)
     \arrow[r, shift right=6pt, "\mathsf{Quot}_{A}"', "\bot"]
    & 
    {}_{A}\mathbf{Mod}^{\bullet}
     \arrow[l, shift right=6pt, "\mathsf{Ann}_{A}"']
  \end{tikzcd}
\end{center}
restricting to an equivalence
\begin{center}
  \begin{tikzcd}
    \mathbf{L}(A)
     \arrow[r, shift right=6pt, "\mathsf{Quot}_{A}"']
    & 
    {}_{A}\mathbf{Mod}^{\odot}
     \arrow[l, shift right=6pt, "\mathsf{Ann}_{A}"']
  \end{tikzcd}
\end{center}
\end{proposition}

### Connection to the GNS construction
The above observations are simple shadows of the functorality of the GNS construction for [[C-star-algebra|C*-algebras]] and [[von Neumann algebra|W*-algebras]].
The *opposite* of the category of ideals $\mathbf{L}(A)$ can be thought of as a stand-in for the category of states (to every $C^\ast$-algebraic state $\rho \colon E \to \mathbb{C}$ on a $C^{\ast}$-algebra $E$ we can associate its "left kernel" $\{e: \rho(e^{*} e) = 0 \}$).
The quotient functor $\mathsf{Quot}$ is a toy-model of the GNS construction.

## Notation/Terminology
In the following the letters $E, F$ and $G$ will denote $C^\ast$-algebras that are not necessarily $\W^\ast$-algebras and $A, B, C$ will denote $W^\ast$-algebras.

The term (normal) state will be taken to mean *(normal) positive linear functional*
Note that this is at odds with some definitions in the physics literature, where "state" typically means "normalized" positive linear functional (if $f(1_{E}) = 1$ for $f: E \to \mathbb{C}$ a positive linear functional).
Using the definition of "state" here, the zero map $0: E \to \mathbb{C}$ is a perfectly valid state.


# The GNS construction as a functor on a fixed C$^\ast$-algebra

With an appropriate notion of a "category of states", one can explore functorial properties of the GNS construction as in Arthur Parzygnat's work (see [Parzygnat2016](#Parzygnat2016) and [Parzygnat2018](#Parzygnat2018)).

The construction here is from a slightly different perspective, using a mildly richer category of states based on the natural poset structure on the collection of (normal) states on a fixed $W^\ast$ or $C^\ast$-algebra.
The posetal relation is intimately related to the notion of a Radon-Nikodym derivative.

## The category of (normal) states over a fixed (W$^\ast$) C$^\ast$-algebra.

Begin by recalling a well-known posetal relation on the set of states $\text{State(E)}$ on a $C^\ast$-algebra $E$:
\begin{definition}
For any $f, g \in \text{State}(E)$, define the relation $\leq$ by $f \leq g$ if $f - g$ is a state, where $-$ denotes pointwise subtraction; equivalently: $f \leq g$ if $f(e^\ast e) \leq g(e^\ast e)$ for all $e \in E$
\end{definition}

It is a straightforward exercise to show this relation is posetal.

The story for normal states in the $W^\ast$-algebra world is nearly identical: let $\text{NState(A)}$ denote the set of normal states on a $W^\ast$-algebra $A$ (a subset of $\text{State}(A)$); for any $f, g \in \text{NState(A)}$ we can define a relation $\leq_{\text{norm}}$ by: $f \leq_{\text{norm}} g$ if $f - g$ is a normal state.
Because the space of linear functionals splits as an orthogonal sum into normal and singular parts, it follows immediately that $f \leq_{\text{norm}} g$ for normal linear functionals $f$ and $g$ if and only if $f \leq g$.
As a result we can simply write $\leq$ when discussing states on $C^\ast$-algebras or normal states on $W^\ast$-algebras without any issues if we forget down from the category of $W^\ast$-algebras to the category of $C^\ast$-algebras.


\begin{remark}
We can easily define weaker versions of the relation $\leq$ that may also be of interest: for $f$ and $g$ positive linear functionals on a $C^\ast$ algebra $E$, we can define relations $\ll$ and $\lesssim$ in the following manner:

* $f \ll g$ if there is an inclusion of $\ker^{L}(g) \subseteq \ker^{L}(f)$, where, for any positive linear functional h on E, the "left kernel" or "vanishing ideal" is defined by:
\[
\ker^{L}(h) \coloneqq \{e: h(e^\ast e ) = 0 \}.
\]
		
* $f \lesssim g$ if there exists an $M$ such that $f(a^\ast a) \leq M g(a^\ast a)$ for every $a \in A$.  
		
We have the following immediate properties:

* $f \leq g \Rightarrow f \lesssim g \Rightarrow f \ll g$.
		
* $\leq$ is a partial order as it is antisymmetric: $f \leq g$ and $g \leq f$ if and only if $f = g$.

However, the weaker preorders $\ll$ and $\lesssim$ do not satisfy antisymmetry: e.g. $2 f \lesssim f$ and $f \lesssim 2f$.
		
Moreover, while $\lesssim$ is only a mild weakening of $\leq$, the weakest preorder $\ll$ is vastly different. 
In particular, we will show there is a unique Radon-Nikodym derivative associated to every pair of functionals related by the preorders $\leq$ and $\lesssim$; the result can be weakened for $\ll$, but the Radon-Nikodym derivative will be an unbounded (densely defined) operator. 
See [Gudder](#Gudder).
\end{remark}


\begin{definition}
Let $E$ be a $C^\ast$-algebra.
The category $\mathbf{State}(E)$ is the opposite of the thin category determined by the preorder $\leq$, i.e. it is the category whose objects are all states (positive linear functionals) on $E$, and whose morphism sets are given by
\[
  \mathbf{State}(E)(\omega, \nu) = 
  \left\{
    \begin{array}{ll}
       \{\star\}, & \nu \leq \omega\\    
       \emptyset, & \text{otherwise}    
    \end{array}
\right.
\]
where $\{\star\}$ denotes the one point set.
\end{definition}

\begin{definition}
For $E$ a $C^\ast$-algebra, the category $\mathbf{Rep}^{\bullet}(E)$ is the category with: 
* objects given by pointed $\ast$-representations of $E$: triples $(\mathcal{H}, v, \pi: E \to \mathrm{B} \mathcal{H})$ of a Hilbert space $\mathcal{H}$ a vector $v \in \mathcal{H}$ and a $\ast$-representation $\pi$;
* morphisms given by contractive linear point-preserving intertwiners: a morphism from $(\mathcal{H}_{1}, v_{1}, \pi_1)$ to $(\mathcal{H}_2, v_2, \pi_2)$ is a linear map $f: \mathcal{H}_{1} \to \mathcal{H}_{2}$ such that $\|f\| \leq 1$ with respect to the operator norm, $f v_{1} = v_{2}$, and
\[
  f \circ \pi_{1}(e) =  \pi_{2}(e) \circ f	
\]
for all $e \in E$.
$\mathbf{Rep}^{\odot}(E)$ is the full subcategory of $\mathbf{Rep}^{\bullet}(E)$ whose objects are *cyclic* representations: $(\mathcal{H}, v, \pi: E \to \mathrm{B} \mathcal{H})$ such that the subspace $E v = \{e v : e \in E \}$ is dense in $\mathcal{H}$.  
\end{definition}

We also define normal versions of the above.
\begin{definition}
Similarly, for $A$ a $W^\ast$-algebra, the category $\mathbf{NRep}^{\odot}(A)$ is the category whose objects are pointed normal $\ast$-representations of $A$, and morphisms are contractive linear intertwiners.
$\mathbf{NRep}^{\odot}(A)$ is the full subcategory of cyclic representations.
\end{definition}

The following are a few straightforward observations about the subcategories $\mathbf{(N)Rep}^{\odot}(\ldots)$ generated by cyclic objects.
\begin{remark}
These subcategories are thin: there is at most one morphism between two objects, every morphism is uniquely determined by where distinguished point is sent.
\end{remark}
\begin{remark}
 The subcategories $\mathbf{(N)Rep}^{\bullet}(\ldots)$ generated by cyclic objects are reflective subcategories.
\end{remark}

The observations in the above remark are shadows of an adjunction:
\begin{center}
  \begin{tikzcd}
    \mathbf{State}(E)
     \arrow[r, shift right=6pt, "\mathsf{GNS}"', "\bot"]
    & 
    \mathbf{Rep}^{\bullet}(E)
     \arrow[l, shift right=6pt, "\mathsf{Fnl}"']
  \end{tikzcd}
\end{center}
which restricts to an equivalence of categories:
\begin{center}
  \begin{tikzcd}
    \mathbf{State}(E)
     \arrow[r, shift right=6pt, "\mathsf{GNS}"']
    & 
    \mathbf{Rep}^{\odot}(E)
     \arrow[l, shift right=6pt, "\mathsf{Fnl}"']
  \end{tikzcd}
\end{center}
The analogous statements hold for normal states/pointed representations.
Our next step is to unravel the functors $\mathsf{GNS}$ and $\mathsf{Fnl}$

# The GNS construction *without* fixing an algebra

*...To be continued*.

# References

* {#Mainiero2019} [[Tom Mainiero]], _Homological Tools for the Quantum Mechanic_, ([arXiv:1901.02011](https://arxiv.org/abs/1901.02011))

* {#Parzygnat2016} [[Arthur Parzygnat]], _From observables and states to Hilbert space and back: a 2-categorical adjunction_, ([arXiv:1609.08975](https://arxiv.org/abs/1609.08975))

* {#Parzygnat2018} [[Arthur Parzygnat]], _Stinespring's construction as an adjunction_ ([arXiv:1807.02533](https://arxiv.org/abs/1807.02533))

* {#MO247626}  _MathOverflow: In which sense the GNS construction is a functor?_ ([link](https://mathoverflow.net/questions/247626/in-which-sense-the-gns-construction-is-a-functor))

* {#Gudder} [[Stanley Gudder]], _A Radon-Nikodym Theorem for $\ast$-Algebras_ ([link](https://projecteuclid.org/download/pdf_1/euclid.pjm/1102785959))


[[!redirects Functorial Aspects of the GNS Representation]]
[[!redirects Functorial Aspects of the GNS Representation]]
[[!redirects functorial aspects of the gns representation]]

