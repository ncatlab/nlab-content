
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

We say a set $A$ has the structure of a super convex space $A$ if and only if the following three axioms are satisfied:


Axiom 1. For every sequence $\mathbf{a}: \mathbb{N} \rightarrow A$ and every $\mathbf{p} \in \mathcal{G}(\mathbb{N})$ it follows that 
\begin{equation} 
\int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p}  \in A.
\end{equation}


Axiom 2. For every sequence $\mathbf{a}: \mathbb{N} \rightarrow A$ and every  $j \in \mathbb{N}$ the property 
\begin{equation} 
\int_{\mathbb{N}} \mathbf{a} \, \, d\delta_j = a_j
\end{equation}
holds.  


Axiom 3. If $\mathbf{p} \in \mathcal{G}(\mathbb{N})$ and $\mathbf{Q}: \mathbb{N} \rightarrow \mathcal{G}(\mathbb{N})$ is a sequence of probability measures on $(\mathbb{N}, \powerset{\mathbb{N}})$   then 
\begin{equation} 
\int_{j \in \mathbb{N}} \big( \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{Q}^j \big) \, d\mathbf{p} = \int_{\mathbb{N}} \mathbf{a} \,  d(  \int_{j \in \mathbb{N}} \mathbf{Q}^{\bullet} \, d\mathbf{p}  \big).
\end{equation}

Need to: Add diagram to explain Axiom 3 using the natural transformation $\mu_{\mathbb{N}}: \mathcal{G}^2 \rightarrow \mathcal{G}$

The third axiom uses  the pushforward measure $\mathcal{G}(\mathbf{Q})\mathbf{p} \in \mathcal{G}^2{\mathbb{N}}$ and the natural transformation $\mu$ of the Giry monad at component $\mathbb{N}$, $\mu_{\mathbb{N}}: \mathcal{G}^2(\mathbb{N}) \rightarrow \mathcal{G}(\mathbb{N})$, which yields the probability measure on  the measurable space $(\mathbb{N}, \powerset{\mathbb{N}})$  whose value at the measurable set $\{j\}$ is given by the composite of measurable maps
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
 Viewing $\Delta_{\mathbb{N}}$ as a monoid we can model a super convex space $A$ as the subcategory of $\mathbf{Set}^{\Delta_{\mathbb{N}}^{op}}$ consisting of those  functors  $\widehat{A} \in \Set^{\Delta_{\mathbb{N}}^{op}}$ given by $\widehat{A}(\star)=\Set(\mathbb{N}, A)$ and for all $\mathbf{p} \in \mathcal{G}{\mathbb{N}}$ (hence $\mathbf{p} \in \Delta_{\mathbb{N}}$ and vice-versa)
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
In physics, super convex spaces have been referred to as strong convex spaces.  In physics, where probability amplitudes are used which make use of the $\ell_2$-norm instead of the tradition ''$\ell_1$-norm'' which is used above, the above definition can be altered by
taking 
\begin{equation}
\mathcal{G}(\mathbb{N}) = \{ \mathbf{p}: \mathbb{N} \rightarrow  \mathbf{D}_2  \,  | \,\lim_{N \rightarrow \infty} \{ \sum_{i=1}^N p_i p_i^{\star} \}= 1 \}
\end{equation}
where $\mathbf{D}_2 = \{r e^{\imath \theta} \in \mathbb{C} \, | r \in [0,1],  and  \theta \in [0,2 \pi) \}$ and $p_i^{\star}$ is the complex conjugate of $p_i$.

## Properties

The category $\mathbf{SCvx}$ has all limits and colimits.  Furthermore it is a symmetric monoidal closed category under the tensor product. The proof of the latter condition follows the proof by Meng, replacing finite sums with countable sums.

As shown by Borger and Kemmper (cite)
there are no coseparators for $\mathbf{SCvx}$.

## Examples
A fundamental super convex space is the set $\mathbb{N}$ with the super convex space structure defined, for every sequence $\mathbf{s}: \mathbb{N} \rightarrow \mathbb{N}$  by 
\begin{equation}
\int_{\mathbb{N}} \mathbf{s} d\mathbf{p} = \inf_i \{\mathbf{s}_i \, | \, p_i>0 \}
\end{equation}
 
Add example of quotient spaces...


## References

Mackey, Meng, Borger and Kemper, ...