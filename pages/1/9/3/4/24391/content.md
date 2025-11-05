

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


\tableofcontents

## Idea

The notion of "superconvex spaces" generalizes the idea of *[[convex spaces]]* by replacing [[finite set|finite]] affine [[sums]] with [[countable set|countable]] affine sums.

The category of superconvex spaces is the category of algebras for the countable distribution monad $D$ defined on $\mathbf{Set}$ by:

For $X$ a set let $D X$ be the set whose elements are functions $p:X\to[0,1]$ such that 

* $p(x)\ne 0$ for only countably many $x$, and

* $\sum_{x\in X} p(x)=1$. (The limit of the countable sum is one.)

Note that the sum above is countable if one excludes all the zero addenda.

The elements of $D X$ are called **countable distributions** or **countably-[[support|supported]] probability measures** over $X$. 

Given a function $f:X\to Y$, one defines the **pushforward** $D f:D X\to D Y$ as follows. Given $p\in D X$, then $(D f)(p)\in D Y$ is the function
$$
y \;\mapsto\; \sum_{x\in f^{-1}(y)} p(x) .
$$
(Note that, up to zero addenda, the sum above is again countable. Moreover, once we have defined countably affine, note that the pushforward map is countably affine.)


## Definition 

Let $\mathcal{G}(\mathbb{N})$ denote the set of all [[probability measures]] on the set of [[natural numbers]], hence every $\mathbf{p}$ can be represented as $\mathbf{p} = \sum_{i \in \mathbb{N}} p_i \delta_i$ where $\sum_{i \in \mathbb{N}} p_i=1$ with each $p_i \in [0,1]$.  Here $\mathcal{G}$ is the [[Giry monad]], but because we want to forget the $\sigma$-algebra associated with the [[measurable space]] $\mathcal{G}(\mathbb{M})$ we often write $\Delta_{\mathbb{N}}$ for its [[underlying set]]. That set may be regarded as the [[countable set|countably]] [[infinite]]-[[dimension|dimensional]] [[simplex]], as such it is the prototypical example of a superconvex space.

 Given any set $A$, a [[sequence]] $\mathbf{a} \colon \mathbb{N} \rightarrow A$, and any $\mathbf{p} \in \mathcal{G}(\mathbb{N})$, we refer to the [[formal sum]] $\sum_{i \in \mathbb{N}} p_i  a_i$  as a countably affine sum of elements of $A$, and for brevity we use the notation $\sum_{i\in \mathbb{N}} p_i a_i$  to refer to a countably affine sum dropping the explicit reference to the condition that the limit of partial sums $\sum_{i=0}^N p_i$ converges to one.  An alternative notation to the countable affine sum notation is to use the integral notation
\[
  \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p} 
  \;\coloneqq\; 
  \sum_{i \in \mathbb{N}} p_i a_i.
\]


\begin{definition}
**(superconvex spaces)**
\linebreak
We say a set $A$ has the structure of a *superconvex space*  if it comes equipped with a function
\[
\begin{array}{ccccc}
  st_A
  &\colon& 
 \mathcal{G}{(\mathbb{N})} 
    \times 
  \Set(\mathbb{N}, A) & \rightarrow& A 
  \\
  && 
  (\mathbf{p}, \mathbf{a}) 
    & \mapsto & 
  \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p}
\end{array}
\]
such that the following axiom is satisfied:


* **Axiom**. If $\mathbf{p} \in \mathcal{G}(\mathbb{N})$ and $\mathbf{Q}: \mathbb{N} \rightarrow \mathcal{G}(\mathbb{N})$ is a sequence of probability measures on $(\mathbb{N}, \mathcal{P}(\mathbb{N}))$   then 

  \[
    \textstyle{\int_{j \in \mathbb{N}}}
    \big( 
       \int_{\mathbb{N}} \mathbf{a} 
       \, 
       d\mathbf{Q}^j 
    \big) \, d\mathbf{p} 
    \;=\; 
    \textstyle{\int_{\mathbb{N}}} \mathbf{a} \,  
    d\big(  
      \textstyle{\int_{j \in \mathbb{N}}} 
      \mathbf{Q}^{\bullet} \, d\mathbf{p}  
    \big)
    \,.
  \]

\end{definition}

\begin{remark}
The axiom uses  the pushforward measure $\mathcal{G}(\mathbf{Q})\mathbf{p} \in \mathcal{G}^2{\mathbb{N}}$ and the natural transformation $\mu$ of the Giry monad at component $\mathbb{N}$, $\mu_{\mathbb{N}}: \mathcal{G}^2(\mathbb{N}) \rightarrow \mathcal{G}(\mathbb{N})$, which yields the probability measure on  the measurable space $(\mathbb{N}, \mathcal{P}{\mathbb{N}})$  whose value at the measurable set $\{j\}$ is given by the composite of measurable maps
\begin{centre}
\begin{tikzpicture}
      \node   (1)  at  (0,0)  {$1$};
      \node   (GN) at  (-3,1.5)  {$\mathcal{G}{\mathbb{N}}$};
      \node   (G2N) at  (0, 1.5)  {$\mathcal{G}^2{\mathbb{N}}$};
      \node   (GN2)  at   (2.5,1.5)  {$\mathcal{G}{\mathbb{N}}$};
      \node    (01)   at   (5,1.5)   {$[0,1]$};
      \draw[->,above] (GN2) to node {$ev_{\{j\}}$} (01);
      \draw[->,above] (G2N) to node {$\mu_{\mathbb{N}}$} (GN2);
      \draw[->,left] (1) to node [xshift=-2pt,yshift=-2pt]{$\mathbf{p}$} (GN);
      \draw[->,above] (GN) to node {$\mathcal{G}{\mathbf{Q}}$} (G2N);
      \draw[->,left] (1) to node [xshift=-2pt,yshift=3pt]{\small{$ \int_{j \in \mathbb{N}} \mathbf{Q}^{j} \, d \mathbf{p}$}} (GN2);
      \draw[->,right] (1) to node [xshift=0pt,yshift=-17pt]{$\begin{array}{lcl}
\mu_{\mathbb{N}}\big( \mathcal{G}(\mathbf{Q})\mathbf{p}\big)(\{j\}) &=& \int_{\{j\} }d\big(\mathcal{G}(\mathbf{Q})\mathbf{p}\big)  \\
&=& \int_{ \mathbb{N}} \mathbf{Q}^j \, d\mathbf{p} \\
&=& \sum_{i \in \mathbb{N}} p_i Q^j_i 
\end{array}$} (01);
\end{tikzpicture}
\end{centre}

\end{remark}

\begin{definition}
**(category of superconvex spaces)**
\linebreak
A *[[morphism]]* of superconvex spaces, called a *countably affine map*, is a set function $m: A \rightarrow B$ such that
\[ 
  m
  \big( 
    \textstyle{\int_{\mathbb{N}}} \mathbf{a} 
    \, d\mathbf{p}
  \big) 
  \;=\; 
  \textstyle{\int_{\mathbb{N}}} 
  (m \circ \mathbf{a}) \, d\mathbf{p}
  \,,
\]
where the composite  $m \circ \mathbf{a}$ gives the sequence in $B$  with component $m(a_i)$.
Composition of countably affine maps is the set-theoretical composition.

Superconvex spaces with morphisms the countably affine maps thus form a [[category]] denoted $\mathbf{SCvx}$.
\end{definition}
 

## Probability Amplitudes

In [[physics]], superconvex spaces have been referred to as *strong convex spaces*, and since [[probability amplitudes]] are employed there one makes use of the $\ell_2$-norm instead of the tradition ''$\ell_1$-norm'' which is used above. By using
\[
  \mathcal{G}(\mathbb{N}) 
   \;=\; 
  \Big\{  
    \mathbf{p} \colon \mathbb{N} \rightarrow  \mathbf{D}_2  
  \Big\vert  
    \lim_{N \rightarrow \infty} 
    \big( 
      \textstyle{\sum_{i=1}^N} p_i p_i^{\star} 
    \big)
    \,=\, 
    1 
  \Big\}
  \,,
\]
where 
$$
  \mathbf{D}_2 
  \;\coloneqq\; 
  \big\{
     r e^{\imath \theta} \in \mathbb{C} 
     \,\big\vert\, 
     r \in [0,1],  \text{and}  \theta \in [0,2 \pi) 
  \big\}
$$ 

and $p_i^{\star}$ is the [[complex conjugate]] of $p_i$, 
applied to the above axioms one obtains superconvex spaces useful for physics. 


## Properties

\begin{lemma}  For every sequence $\mathbf{a} \colon \mathbb{N} \rightarrow A$ and every  $j \in \mathbb{N}$ the property 

  \[
    \textstyle{\int_{\mathbb{N}}} \mathbf{a} \, \, d\delta_j 
    \;=\; 
    a_j
  \]

  holds.  
\end{lemma}
\begin{proof}
Choose the constant sequence $\mathbf{Q}: \mathbb{N} \rightarrow \mathcal{G}\mathbb{N}$ with value $\delta_j$ applied to the axiom yields the result.
\end{proof}
This lemma is often taken as a separate axiom.

The most basic property of superconvex spaces,  is

\begin{lemma} 
For $A$  any superconvex space  every countably affine map $m \in \SCvx(\Delta_{\mathbb{N}}, A)$ is uniquely specified by a sequence in $A$, hence we have $\SCvx(\Delta_{\mathbb{N}}, A) \cong  \Set(\mathbb{N},A)$.
\end{lemma}
\begin{proof}
Every element $\mathbf{p} \in \Delta_{\mathbb{N}}$ has a unique representation as a countable affine sum $\mathbf{p} = \sum_{i \in \mathbb{N}} p_i \delta_i$, and hence a countably affine map $m:\Delta_{\mathbb{N}} \rightarrow A$ is uniquely determined by where it maps each Dirac measure $\delta_i$.  Thus  $i \mapsto m(\delta_i)$  specifies a sequence in $A$.  
\end{proof}
We denote the bijective correspondence $\SCvx(\Delta_{\mathbb{N}}, A) \cong  \Set(\mathbb{N},A)$ by 
 $\langle \mathbf{a} \rangle \leftrightarrow \mathbf{a}$, where $\mathbf{a}: \mathbb{N} \rightarrow A$ specifies a sequence in $A$. 

\begin{lemma} A function $f \colon \mathbb{N} \rightarrow \mathbb{N}$ is a countably affine map if and only if $f$ is monotone, $i \lt j$ implies $f(i) \le f(j)$.
\end{lemma}
\begin{proof}
Necessary condition.  Suppose that $f: \mathbb{N} \rightarrow \mathbb{N}$ is a countably affine map.  Let $i \lt j$. By the superconvex space structure on $\mathbb{N}$ it follows, for all $\alpha \in (0,1)$, that  $\alpha i + (1-\alpha) j = i$ .  If $f$ is not monotone then there exist a pair of elements $i,j \in \mathbb{N}$ such that $i \lt j$ with $f(j) \lt f(i)$.  This implies, for all $\alpha \in (0,1)$, that 
$$
f(j)= \alpha f(i) + (1-\alpha) f(j) \lt   f(\alpha i + (1-\alpha) j ) =f(i),
$$
which contradicts our hypothesis that $f$ is a countably affine map.
 
Sufficient condition. Suppose $f$ is a monotone function, and
 that we are given an arbitrary countably affine sum $\sum_{i \in \mathbb{N}} p_i i = n$ in $\mathbb{N}$, so that for all $i=0,1,\ldots,n-1$ we have $p_i=0$.  Since the condition defining the superconvex structure is conditioned on the property $p_i \ne 0$, the countably affine sum is not changed  by removing any number of terms $i$ in the countable sum whose coefficient $p_i=0$.  Hence 
for all $j$ such that $n\lt j$ it follows that $f(n) \le f(j)$ so that
\[
  f\big( 
    \textstyle{\sum_{i=0}^{\infty}} 
     p_i \, i
  \big) 
  \,=\, 
  f(n) 
  \,=\, 
  \textstyle{\sum_{i=n}^{\infty}} p_i f(i) 
  \,,
\]
where the last equality follows from the definition of the superconvex space structure on $\mathbb{N}$.
\end{proof}

\begin{lemma}
 The standard *free space* construction can be applied to superconvex spaces to obtain  an adjoint pair $\mathcal{F}:\mathbf{Set} \leftrightarrows \mathbf{SCvx}: \mathcal{U}$
where $\mathcal{F}(A)$ consists of all formal countable affine sums, $\int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p} := \sum_{i \in \mathbb{N}}p_i a_i$ for $\mathbf{p} \in \mathcal{G}{\mathbb{N}}$ and $\mathbf{a} \in \mathbf{Set}(\mathbb{N},A)$,
modulo the relations 
\[
  \textstyle{\int_{j \in \mathbb{N}}} 
  \big( 
    \textstyle{\int_{i \in \mathbb{N}}} 
    \mathbf{a} \, d\mathbf{Q}^i 
  \big) 
   \, d\mathbf{p} 
  \;\cong\;  
  \textstyle{\int_{j \in \mathbb{N}}} \mathbf{a} 
  \, d
  \big( 
    \textstyle{\int_{i \in \mathbb{N}}} 
    \mathbf{Q}^{\bullet} 
    \, d\mathbf{p} 
  \big) 
  \quad\quad\quad 
  \forall \, \mathbf{Q} \in \mathbf{Set}( \mathbb{N},  \mathcal{G}{\mathbb{N}})
  \,,
\]
so that the sole necessary axiom of a superconvex space is satisfied.   

The monad arising from this adjunction, with the usual unit and counit maps (for the free and forgetful functors), is the countable distribution monad defined in the Idea section, and the category of algebras of that monad is superconvex spaces.
\end{lemma}
\begin{proof}
Note that the finite [[distribution monad]] also arises from the free functor and forgetful functor adjunction. (The verification that the finite and countable distributions arise from the free functor and forgetful functor is straight forward.)
  
 A direct method to prove that the category of algebras of $D$, $Alg(D)$, is equivalent to the category of superconvex spaces is to show that the *comparison functor* $\Phi: \mathbf{SCvx} \rightarrow Alg(D)$ has a two-sided inverse $\Psi: Alg(D) \rightarrow \mathbf{SCvx}$.  This functor is defined on objects by taking $\Psi( \alpha:D X \rightarrow X )$ as the set $X$ with the superconvex structure defined by $\sum_{i \in \mathbb{N}} p_i x_i = \alpha(\sum_{i \in \mathbb{N}} p_i x_i)$ where the countable sum on the right hand side is a formal countable sum, which is an element of $D X$.  Given any map of algebras $f: (X,h) \rightarrow (Y,k)$ it follows, as shown by the (only) proof given on the  [[Giry monad]] page is that the function $f$, which we now view in $\mathbf{Set}$, is necessarily a countably affine map. (Simply replace the terms $\sum_{i \in \mathbb{N}}p_i \delta_{x_i}$ with the term $\sum_{i \in \mathbb{N}}p_i x_i$ which is an element in $D X$.) 
\end{proof}

The category $\mathbf{SCvx}$ has all limits and colimits.  Furthermore it is a symmetric monoidal closed category under the tensor product. The proof of the latter condition follows the proof by Meng, replacing finite sums with countable sums.

The full subcategory consisting of the single object $\Delta_{\mathbb{N}}$ is dense in $\mathbf{SCvx}$, and hence we can employ the restricted Yoneda embedding to view superconvex spaces as the functors $\widehat{A}=\mathbf{SCvx}(\cdot,A) \in \mathbf{Set}^{\Delta_{\mathbb{N}}^{op}}$, where $\Delta_{\mathbb{N}}$ is viewed as a [[monoid]].  


  An ideal in a superconvex space $A$ is a subset $\mathcal{I}$ such that whenever $a_0 \in \mathcal{I}$ and $\sum_{i \in \mathbb{N}}p_i a_i$ is a countable affine sum with the coefficient of $a_0$ nonzero then $\sum_{i \in \mathbb{N}}p_i a_i \in \mathcal{I}$.   Ideals are useful for defining functors to or from $\mathbf{SCvx}$.

## Examples
\begin{example}
A fundamental superconvex space is the set $\mathbb{N}$ with the superconvex space structure defined, for every sequence $\mathbf{s}: \mathbb{N} \rightarrow \mathbb{N}$  by 
\[
  \textstyle{\int_{\mathbb{N}}} \mathbf{s} d\mathbf{p} 
  \;=\; 
  \inf_i \{\mathbf{s}_i \, | \, p_i \gt 0 \}
  \,.
\]
That structure on $\mathbb{N}$ shows that the function $\epsilon: \mathcal{G}(\mathbb{N}) \rightarrow \mathbb{N}$ defined by $\sum_{i \in \mathbb{N}} p_i \delta_i \mapsto \inf_i \{i | p_i\gt 0\}$ is a countably affine map.
\end{example}

\begin{example}
As an example of the utility of ideals in a superconvex space we note that for $\mathcal{G}$ the [[Giry monad]] the measurable space $\mathcal{G}(X)$, with the smallest $\sigma$-algebra such that the evaluation maps $ev_U: \mathcal{G}(X) \rightarrow [0,1]$ are measurable for every measurable set $U$ in $X$, has a superconvex space structure 
defined on it pointwise.

Note that if  $X$ is any [[measurable space]]  the maximal proper ideals of $\mathcal{G}{X}$ are of the form $ev_{U}^{-1}( (0,1])$ or $ev_U^{-1}([0,1))$ for $U\ne X$ a nonempty measurable set in $X$. 

To prove this, note that  both $(0,1]$ and $[0,1)$ are ideals in the superconvex space $[0,1]$, with the natural superconvex space structure, and it follows that $ev_{U}^{-1}( [0,1))$ and $ev_U^{-1}((0,1])$ are ideals in $\mathcal{G}{X}$. (The preimage of an ideal under a countably affine map is an ideal in the domain space. The proof is the standard argument for ideals in any category.)  Consider the ideal $ev_U^{-1}( [0,1))$.  To show that this is a maximal proper ideal suppose that $\mathcal{I}$ is another ideal of $\mathcal{G}{X}$ such that $ev_U^{-1}( [0,1)) \varsubsetneqq  \mathcal{I}$.  Every element $P \in \mathcal{I}$ which is not in $ev_U^{-1}([0,1))$ has the defining  property that $P(U^c)=1$.    Now let $Q \in \mathcal{G}{X}$.  If  $Q \notin \mathcal{J}$ and $Q \notin ev_U^{-1}([0,1))$ then $Q(U^c) \ne 1$ which implies  $Q \in ev_U^{-1}( [0,1)) \varsubsetneqq J$ which is self-contradictory.  Thus $\mathcal{J}$ must be all of $\mathcal{G}{X}$ which shows $ev_U^{-1}([0,1))$ is a maximal (proper) ideal.
The argument that the ideal $ev_U^{-1}( (0,1])$ is a maximal ideal is similiar except we replace the condition $P(U^c)=1$ in the above proof with $P(U)=0$.

If we restrict to the category of standard measurable spaces then every object has a countable generating basis and it is then clear that every ideal in $\mathcal{G}(X)$ is a  countable intersection of maximal ideals, and hence measurable.  This implies, for example, that every countably affine map $k: \mathcal{G}(X) \rightarrow \mathbb{N}$ is also a  measurable function with $\mathbb{N}$ having the powerset $\sigma$-algebra. (The only ideals of $\mathbb{N}$ are the principal ideals $\downarrow \! 0 \subset \downarrow \! 1 \subset \ldots$.)
\end{example}

\begin{example} 
The one point Alexandroff compactification of the interval $[0,\infty)$, denoted $[0,\infty]$, is a superconvex space.  On the other hand, the one point compactification of the real line $\mathbb{R}=(-\infty,\infty)$ is not a superconvex space since we could take $p_i = \frac{1}{2^i}$  and $r_i=(-1)^i 2^i$ for which the sequence of partial sums alternates between $-1$ and $0$.   Likewise $\mathbb{R}$ itself is not a superconvex space even though it is a  convex space.  

\end{example}

\begin{example} A pathological space, useful for counterexamples, is given by the closed unit interval with the superconvex space structure defined by the infimum function, $\sum_{i \in \mathbb{N}} p_i u_i := inf_i \{ u_i | p_i \gt 0\}$.
\end{example}
 

\begin{example}  Consider the probability monad on compact Hausdorff spaces, where the algebras are precisely the compact convex sets $K$ in locally convex topological vector spaces together with the barycenter maps $\beta_K:\mathcal{P}K\rightarrow K$.  

Given such a space $K$ we can endow it with a superconvex space structure by defining, for all $\mathbf{p} \in \mathcal{G}\mathbb{N}$, countable affine sums by  $\sum_{i \in \mathbb{N}} p_i k_i := \beta_K( \sum_{i \in \mathbb{N}} p_i \delta_{k_i})$ which, along with the pointwise superconvex space structure on $\mathcal{P}K$ makes the barycenter map $\beta_K$ a countably affine map.  

To prove that this endows $K$ with a superconvex space structure note that $\beta_K(\delta_{k_i})= k_i$ for all $k_i \in K$ to obtain
$$
  \textstyle{\sum_{i \in \mathbb{N}}} 
  p_i \beta_K(\delta_{k_i}) 
  \;=\; 
  \textstyle{\sum_{i \in \mathbb{N}}} 
  p_i k_i 
  \,\coloneqq\, 
  \beta_K\big(
    \textstyle{\sum_{i \in \mathbb{N}}} 
    p_i \delta_{k_i}
  \big)
  \,.
$$
To prove that $\beta_K$ is countably affine on $\mathcal{P}K$ use the property that $\beta_K \circ \mu_K = \beta_K \circ \mathcal{P}\beta_K$.

The method employed in this example is not restricted to locally convex compact Hausdorff spaces. It shows that the algebras of a probability monad are a superconvex space.
That implication is the motivation for the next example.
\end{example}


## Related concepts

* [[totally convex space]]

* [[convex space]]

## References

The notion of superconvex spaces originates with:

* [[Dieter Pumplün]], *Banach spaces and superconvex modules*, in *Symposia Gaussiana -- Conference A: Mathematics and Theoretical Physics*, De Gruyter (1995) &lbrack;[doi:10.1515/9783110886726.323](https://doi.org/10.1515/9783110886726.323)&rbrack;

The proof that $\mathbf{SCvx}$ has no cogenerator is due to:

* {#BörgerKemper94a} [[Reinhard Börger]], [[Ralf Kemper]], *There is no cogenerator for total convex spaces*, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome **35** 4 (1994) 335-338 &lbrack;[numdam:CTGDC_1994__35_4_335_0](http://www.numdam.org/item/CTGDC_1994__35_4_335_0)&rbrack;


The fact that $\mathbf{SCvx}$ is a symmetric monoidal argument can be proven the same way it is for [[convex spaces]] simply by replacing the finite affine sums with countable affine sums. That proof was given by

* {#Meng} Xiao-qing Meng, _Categories of convex sets and of metric spaces with applications to stochastic programming and related areas_, PhD thesis ([[Meng.djvu|djvu:file]]) 

Proposition 1.2 in 

* {#BörgerKemper94b} [[Reinhard Börger]], [[Ralf Kemper]], *Cogenerators for convex spaces*, Applied Categorical Structures **2** (1994) 1-11 &lbrack;[doi:10.1007/BF00878499](https://doi.org/10.1007/BF00878499)&rbrack;

is particularly useful for viewing superconvex spaces as positively convex spaces which are somewhat easier to work with because the condition $\sum_{i \in \mathbb{N}}p_i=1$  is replaced by the inequality $\le 1$.

Superconvex spaces play a role in obtaining a factorization of the [[Giry monad]] yielding $G$-algebras as shown in the article

* [[Kirk Sturtz]], _Deriving the Giry algebras on standard Borel spaces using $\mathbb{R}_{\infty}$-generalized points_,  $[$[arXiv:2409.14861](https://arxiv.org/abs/2409.14861)$]$

For purposes of constructing models of complex systems using superconvex spaces the construction given in Example 6.1 of the following article applies equally well to superconvex spaces.

* [[Tobias Fritz]], *Convex spaces I: definition and examples* &lbrack;[arXiv/0903.5522](http://arxiv.org/abs/0903.5522)&rbrack;

The term *strong convex space* was employed in:

* [[George Mackey]], p. 68 of: *The Mathematical Foundations of Quantum Mechanics: a Lecture-note Volume*, Mathematical physics monograph series, Benjamin (1963), Dover (2004) &lbrack;[google books](https://books.google.de/books?id=qlpb2mWYmfYC&printsec=frontcover&hl=de&source=gbs_ge_summary_r&cad=0#v=onepage&q&f=false)&rbrack;


[[!redirects superconvex spaces]]

[[!redirects strong convex space]]
[[!redirects strong convex spaces]]

[[!redirects super convex space]]
[[!redirects super convex spaces]]

[[!redirects Super convex space]]
[[!redirects Super convex spaces]]


