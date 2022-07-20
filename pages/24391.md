
# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

Super convex spaces generalize the idea of a convex space by replacing finite affine sums with countable affine sums. 

Let $\mathcal{G}(\mathbb{N})$ denote the set of all probability measures on the set of natural numbers, hence every $\mathbf{p}$ can be represented as $\mathbf{p} = \sum_{i \in \mathbb{N}} p_i \delta_i$ where $\sum_{i \in \mathbb{N}} p_i=1$ with each $p_i \in [0,1]$.  Here $\mathcal{G}$ is the [[Giry monad]], but because we want to forget the $\sigma$-algebra associated with that measurable space we often write $\Delta_{\mathbb{N}}$ to denote the underlying set  of $\mathcal{G}(\mathbb{N})$. That set is the countably infinite-dimensional simplex. The set $\mathcal{G}(\mathbb{N})$ (= $\Delta_{\mathbb{N}}$) is the prototype space from which the axioms are abstracted.


## Definition 

 Given any set $A$, a sequence $\mathbf{a}: \mathbb{N} \rightarrow A$, and any $\mathbf{p} \in \mathcal{G}(\mathbb{N})$, we refer to the formal expression $\sum_{i \in \mathbb{N}} p_i  a_i$  as a countably affine sum of elements of $A$, and for brevity we use the notation $\sum_{i\in \mathbb{N}} p_i a_i$  to refer to a countably affine sum dropping the explicit reference to the condition that the limit of partial sums $\sum_{i=0}^N p_i$ converges to one.  An alternative notation to the countable affine sum notation is to use the integral notation
 \begin{equation} 
  \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p} := \sum_{i \in \mathbb{N}} p_i a_i.
 \end{equation}

We say a set $A$ has the structure of a super convex space  if it comes equipped with a function
\begin{equation}
\begin{array}{ccccc}
st_A&:& \mathcal{G}{(\mathbb{N})} \times \Set(\mathbb{N}, A) & \rightarrow& A \\
&:& (\mathbf{p}, \mathbf{a}) & \mapsto & \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p}
\end{array}
\end{equation}
such that the following two axioms are satisfied:


Axiom 1. For every sequence $\mathbf{a}: \mathbb{N} \rightarrow A$ and every  $j \in \mathbb{N}$ the property 
\begin{equation} 
\int_{\mathbb{N}} \mathbf{a} \, \, d\delta_j = a_j
\end{equation}
holds.  


Axiom 2. If $\mathbf{p} \in \mathcal{G}(\mathbb{N})$ and $\mathbf{Q}: \mathbb{N} \rightarrow \mathcal{G}(\mathbb{N})$ is a sequence of probability measures on $(\mathbb{N}, \mathcal{P}(\mathbb{N}))$   then 
\begin{equation} 
\int_{j \in \mathbb{N}} \big( \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{Q}^j \big) \, d\mathbf{p} = \int_{\mathbb{N}} \mathbf{a} \,  d(  \int_{j \in \mathbb{N}} \mathbf{Q}^{\bullet} \, d\mathbf{p}  \big).
\end{equation}


The second axiom uses  the pushforward measure $\mathcal{G}(\mathbf{Q})\mathbf{p} \in \mathcal{G}^2{\mathbb{N}}$ and the natural transformation $\mu$ of the Giry monad at component $\mathbb{N}$, $\mu_{\mathbb{N}}: \mathcal{G}^2(\mathbb{N}) \rightarrow \mathcal{G}(\mathbb{N})$, which yields the probability measure on  the measurable space $(\mathbb{N}, \mathcal{P}{\mathbb{N}})$  whose value at the measurable set $\{j\}$ is given by the composite of measurable maps
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

A morphism of super convex spaces, called a countably affine map, is a set function $m: A \rightarrow B$ such that
\begin{equation} 
m\big( \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p}\big) = \int_{\mathbb{N}} (m \circ \mathbf{a}) \, d\mathbf{p},
\end{equation}
where the composite  $m \circ \mathbf{a}$ gives the sequence in $B$  with component $m(a_i)$.
Composition of countably affine maps is the set-theoretical composition.
Super convex spaces with morphisms the countably affine maps form a category denoted $\SCvx$. 



## Alternative Definition 
 Viewing $\Delta_{\mathbb{N}}$ as a [[monoid]] we can model a super convex space $A$ as the subcategory of $\mathbf{Set}^{\Delta_{\mathbb{N}}^{op}}$ consisting of those  functors of the form  $\widehat{A} \in \Set^{\Delta_{\mathbb{N}}^{op}}$ given by $\widehat{A}(\star)=\Set(\mathbb{N}, A)$ and for all $\mathbf{p} \in \mathcal{G}{\mathbb{N}}$ (hence $\mathbf{p} \in \Delta_{\mathbb{N}}$ and vice-versa)
 \begin{equation} 
  \widehat{A}(\mathbf{p})(\mathbf{a}) =  \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p},
  \end{equation}
 which we identify with the constant sequence in $A$ with the value $ \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p}$.

  A natural transformation $m: \widehat{A} \Rightarrow \widehat{B}$ given at the single component is the function $m_{\star} = \mathbf{Set}(\mathbb{N}, m)$ such that the $\mathbf{Set}$-diagram

 \begin{centre}
 \begin{tikzpicture}
           \node  (A)  at  (0,0)   {$\mathbf{Set}(\mathbb{N}, A)$};
           \node   (B)  at  (3,0)   {$\mathbf{Set}(\mathbb{N}, B)$};
           \node   (a)  at  (0,-1.5)  {$\mathbf{Set}(\mathbb{N},A)$};
           \node   (b)   at  (3, -1.5)  {$\mathbf{Set}(\mathbb{N},B)$};
           \draw[->,above] (A) to node {$m_{\star}$} (B);
           \draw[->,below] (a) to node  {$m_{\star}$} (b);
           \draw[->,left] (A) to node {$\mathbf{p}$} (a);
           \draw[->,right] (B) to node {$\mathbf{p}$} (b);
           
           \node  (A2)  at  (5.8,0)   {$\mathbf{a}$};
           \node   (B2)  at  (10.6,0)   {$m \circ \mathbf{a}$};
           \node   (b3)  at  (10.6,-1.5)  {$= \int_{\mathbb{N}} (m \circ \mathbf{a}) \, d\mathbf{p}$};
           \node   (a2)  at  (5.8,-1.5)  {$\int_{\mathbb{N}}  \mathbf{a} \,  d\mathbf{p}$};
           \node   (b2)   at  (8.3, -1.5)  {$m( \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p})$};
           \draw[|->,above] (A2) to node {} (B2);
           \draw[|->,below] (a2) to node  {} (b2);
           \draw[|->,left] (A2) to node {} (a2);
           \draw[|->,right] (B2) to node {} (b3);
           
           \node  (c)  at  (12,0)  {$$};
 
 \end{tikzpicture}
 \end{centre}
commutes.

## Probability Amplitudes
In physics super convex spaces have been referred to as strong convex spaces, and since [[probability amplitudes]] are employed there one makes use of the $\ell_2$-norm instead of the tradition ''$\ell_1$-norm'' which is used above. By using
 \begin{equation}
\mathcal{G}(\mathbb{N}) = \{  \mathbf{p}: \mathbb{N} \rightarrow  \mathbf{D}_2  |  \lim_{N \rightarrow \infty} \{ \sum_{i=1}^N p_i p_i^{\star} \}= 1 \}
 \end{equation}
where $\mathbf{D}_2 = \{r e^{\imath \theta} \in \mathbb{C} \, | r \in [0,1],  and  \theta \in [0,2 \pi) \}$ and $p_i^{\star}$ is the complex conjugate of $p_i$, 
applied to the above axioms one obtains super convex spaces useful for physics. 


## Properties
The most basic property of super convex spaces is
\begin{lemma} For $A$  any super convex space  every countably affine map $m \in \SCvx(\Delta_{\mathbb{N}}, A)$ is uniquely specified by a sequence in $A$, hence we have $\SCvx(\Delta_{\mathbb{N}}, A) \cong  \Set(\mathbb{N},A)$.
\end{lemma}
\begin{proof}
Every element $\mathbf{p} \in \Delta_{\mathbb{N}}$ has a unique representation as a countable affine sum $\mathbf{p} = \sum_{i \in \mathbb{N}} p_i \delta_i$, and hence a countably affine map $m:\Delta_{\mathbb{N}} \rightarrow A$ is uniquely determined by where it maps each Dirac measure $\delta_i$.  Thus  $i \mapsto m(\delta_i)$  specifies a sequence in $A$.  
\end{proof}

\begin{lemma} \label{NS} A function $f: \mathbb{N} \rightarrow \mathbb{N}$ is a countably affine map if and only if $f$ is monotone, $i \lt j$ implies $f(i) \le f(j)$.
\end{lemma}
\begin{proof}
Necessary condition.  Suppose that $f: \mathbb{N} \rightarrow \mathbb{N}$ is a countably affine map.  Let $i \lt j$. By the super convex space structure on $\mathbb{N}$ it follows, for all $\alpha \in (0,1)$, that  $\alpha i + (1-\alpha) j = i$ .  If $f$ is not monotone then there exist a pair of elements $i,j \in \mathbb{N}$ such that $i \lt j$ with $f(j) \lt f(i)$.  This implies, for all $\alpha \in (0,1)$, that $f(j)= \alpha f(i) + (1-\alpha) f(j) \lt   f(\alpha i + (1-\alpha) j ) =f(i)$, which contradicts our hypothesis that $f$ is a countably affine map.
 
Sufficient condition. Suppose $f$ is a monotone function, and
 that we are given an arbitrary countably affine sum $\sum_{i \in \mathbb{N}} p_i i = n$ in $\mathbb{N}$, so that for all $i=0,1,\ldots,n-1$ we have $p_i=0$.  Since the condition defining the super convex structure is conditioned on the property $p_i \ne 0$, the countably affine sum is not changed  by removing any number of terms $i$ in the countable sum whose coefficient $p_i=0$.  Hence 
for all $j$ such that $n\lt j$ it follows that $f(n) \le f(j)$ so that
\begin{equation}
f( \sum_{i=0}^{\infty} p_i \, i) = f(n) = \sum_{i=n}^{\infty} p_i f(i) 
\end{equation}
where the last equality follows from the definition of the super convex space structure on $\mathbb{N}$.
\end{proof}


The category $\mathbf{SCvx}$ has all limits and colimits.  Furthermore it is a symmetric monoidal closed category under the tensor product. The proof of the latter condition follows the proof by Meng, replacing finite sums with countable sums.


  An ideal in a super convex space $A$ is a subset $\mathcal{I}$ such that whenever $a_0 \in \mathcal{I}$ and $\sum_{i \in \mathbb{N}}p_i a_i$ is a countable affine sum with the coefficient of $a_0$ nonzero then $\sum_{i \in \mathbb{N}}p_i a_i \in \mathcal{I}$.   Ideals are useful for defining functors to or from $\mathbf{SCvx}$.

## Examples
\begin{example}
A fundamental super convex space is the set $\mathbb{N}$ with the super convex space structure defined, for every sequence $\mathbf{s}: \mathbb{N} \rightarrow \mathbb{N}$  by 
\begin{equation}
\int_{\mathbb{N}} \mathbf{s} d\mathbf{p} = \inf_i \{\mathbf{s}_i \, | \, p_i \gt 0 \}
\end{equation}
\end{example}

\begin{example} 
The one point compactification of the real line $\mathbb{R}_{\infty}$, with one point adjoined, denoted $\infty$, which satisfies the property that any countably affine sum $\sum_{i \in \mathbb{N}} p_i r_i = \infty$ if either (1) $r_j = \infty$ and $p_j \gt 0$ for any index $j$, or (2) the sequence of partial sums does not converge, is a super convex space.  The real line $\mathbb{R}$ is not a super convex space since we could take $p_i = \frac{1}{2^i}$ and $r_i = 2^{i+1}$ and the limit of the sequence does not exist in $\mathbb{R}$.  Thus while $\mathbb{R}$ is a convex space it is not a super convex space.  

 The only nonconstant countably affine map $j: \mathbb{R}_{\infty} \rightarrow \mathbb{2}$ is given by $j(u)=1$ for all $u \in \mathbb{R}$ and $j(\infty)=0$ (for the super convex space structure on $\mathbf{2}$ determined by $\frac{1}{2} \underline{0} + \frac{1}{2} \underline{1} = \underline{0}$).  
\end{example}

\begin{example} A pathological space, useful for counterexamples, is given by the closed unit interval with the super convex space structure defined by the infimum function, $\sum_{i \in \mathbb{N}} p_i u_i := inf_i \{ u_i | p_i \gt 0\}$.
\end{example}

\begin{example}
The only ideals of the super convex space $\mathbb{N}$ are the principal ideals,
\begin{equation}
\{0\} \subset \{0,1\} \subset \{0,1,2\} \subset \ldots
\end{equation}
and $\mathbb{N}$ has no maximal ideals.  
\end{example}
 
\begin{example}
 Let $A=\{\underline{u}, \underline{0}, \underline{1}\}$ denote the quotient space obtained as the coequalizer of a parallel pair of distinct maps, say $\frac{1}{3}: \one \rightarrow [0,1]$ and $\frac{2}{3}: \mathbf{1} \rightarrow [0,1]$,   in $\mathbf{SCvx}$, where $[0,1]$ has the natural super convex space structure. The quotient space $A$ has the (super) convex space structure specified by $r \underline{0} + (1-r) \underline{u} = \underline{u}$ for all $r \in (0,1)$, $r \underline{1} + (1-r) \underline{u} = \underline{u}$ for all $r \in (0,1)$, and $r \underline{0} + (1-r) \underline{1} = \underline{u}$ for all $r \in (0,1)$.
 
\end{example} 


## References
The article 

* {#Borger} B&ouml;rger & Kemper, There is no cogenerator for total convex spaces, 
Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome 35 (1994) no. 4, pp. 335-338.

shows that $\mathbf{SCvx}$ has no cogenerator.

The fact that $\mathbf{SCvx}$ is a symmetric monoidal argument can be proven the same way it is for [[convex spaces]] simply by replacing the finite affine sums with countable affine sums. That proof was given by

* {#Meng} Xiao-qing Meng, _Categories of convex sets and of metric spaces with applications to stochastic programming and related areas_, PhD thesis ([[Meng.djvu|djvu:file]]) 

Many examples of super convex spaces are given in

* {#Sturtz22} [[Kirk Sturtz]], _Giry algebras for standard measurable spaces_ $[$[arXiv:2202:10819](https://arxiv.org/abs/2202.10819)$]$

For purposes of constructing models of complex systems using super convex spaces the construction given in Example 6.1 of the following article applies equally well to super convex spaces.

* [[Tobias Fritz]], Convex spaces I: definition and examples. 
[arXiv/0903.5522](http://arxiv.org/abs/0903.5522)

[[!redirects Super convex space]]
[[!redirects super convex spaces]]
[[!redirects strong convex spaces]]