

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

The notion of "superconvex spaces" generalizes the idea of *[[convex spaces]]* by replacing [[finite set|finite]] affine [[sums]] with [[countable set|countable]] affine sums.

Let $\mathcal{G}(\mathbb{N})$ denote the set of all [[probability measures]] on the set of [[natural numbers]], hence every $\mathbf{p}$ can be represented as $\mathbf{p} = \sum_{i \in \mathbb{N}} p_i \delta_i$ where $\sum_{i \in \mathbb{N}} p_i=1$ with each $p_i \in [0,1]$.  Here $\mathcal{G}$ is the [[Giry monad]], but because we want to forget the $\sigma$-algebra associated with that measurable space we often write $\Delta_{\mathbb{N}}$ to denote the underlying set  of $\mathcal{G}(\mathbb{N})$. That set is the [[countable set|countably]] [[infinite]]-[[dimension|dimensional]] [[simplex]]. The set $\mathcal{G}(\mathbb{N})$ (= $\Delta_{\mathbb{N}}$) is the prototype space from which the axioms are abstracted.


## Definition 

 Given any set $A$, a sequence $\mathbf{a}: \mathbb{N} \rightarrow A$, and any $\mathbf{p} \in \mathcal{G}(\mathbb{N})$, we refer to the formal expression $\sum_{i \in \mathbb{N}} p_i  a_i$  as a countably affine sum of elements of $A$, and for brevity we use the notation $\sum_{i\in \mathbb{N}} p_i a_i$  to refer to a countably affine sum dropping the explicit reference to the condition that the limit of partial sums $\sum_{i=0}^N p_i$ converges to one.  An alternative notation to the countable affine sum notation is to use the integral notation
 \begin{equation} 
  \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p} := \sum_{i \in \mathbb{N}} p_i a_i.
 \end{equation}

We say a set $A$ has the structure of a superconvex space  if it comes equipped with a function
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
Note the second axiom alone is sufficient because by choosing the constant sequence $\mathbf{Q}: \mathbb{N} \rightarrow \mathcal{G}\mathbb{N}$ with value $\delta_j$ it follows that the second axiom implies the first axiom.


A morphism of superconvex spaces, called a countably affine map, is a set function $m: A \rightarrow B$ such that
\begin{equation} 
m\big( \int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p}\big) = \int_{\mathbb{N}} (m \circ \mathbf{a}) \, d\mathbf{p},
\end{equation}
where the composite  $m \circ \mathbf{a}$ gives the sequence in $B$  with component $m(a_i)$.
Composition of countably affine maps is the set-theoretical composition.
Superconvex spaces with morphisms the countably affine maps form a category denoted $\mathbf{SCvx}$. 
 

## Probability Amplitudes

In physics, superconvex spaces have been referred to as *strong convex spaces*, and since [[probability amplitudes]] are employed there one makes use of the $\ell_2$-norm instead of the tradition ''$\ell_1$-norm'' which is used above. By using
 \begin{equation}
\mathcal{G}(\mathbb{N}) = \{  \mathbf{p}: \mathbb{N} \rightarrow  \mathbf{D}_2  |  \lim_{N \rightarrow \infty} \{ \sum_{i=1}^N p_i p_i^{\star} \}= 1 \}
 \end{equation}
where $\mathbf{D}_2 = \{r e^{\imath \theta} \in \mathbb{C} \, | r \in [0,1],  and  \theta \in [0,2 \pi) \}$ and $p_i^{\star}$ is the complex conjugate of $p_i$, 
applied to the above axioms one obtains superconvex spaces useful for physics. 


## Properties
The most basic property of superconvex spaces,  is
\begin{lemma} For $A$  any superconvex space  every countably affine map $m \in \SCvx(\Delta_{\mathbb{N}}, A)$ is uniquely specified by a sequence in $A$, hence we have $\SCvx(\Delta_{\mathbb{N}}, A) \cong  \Set(\mathbb{N},A)$.
\end{lemma}
\begin{proof}
Every element $\mathbf{p} \in \Delta_{\mathbb{N}}$ has a unique representation as a countable affine sum $\mathbf{p} = \sum_{i \in \mathbb{N}} p_i \delta_i$, and hence a countably affine map $m:\Delta_{\mathbb{N}} \rightarrow A$ is uniquely determined by where it maps each Dirac measure $\delta_i$.  Thus  $i \mapsto m(\delta_i)$  specifies a sequence in $A$.  
\end{proof}
We denote the bijective correspondence $\SCvx(\Delta_{\mathbb{N}}, A) \cong  \Set(\mathbb{N},A)$ by 
 $\langle \mathbf{a} \rangle \leftrightarrow \mathbf{a}$, where $\mathbf{a}: \mathbb{N} \rightarrow A$ specifies a sequence in $A$. 

\begin{lemma} A function $f: \mathbb{N} \rightarrow \mathbb{N}$ is a countably affine map if and only if $f$ is monotone, $i \lt j$ implies $f(i) \le f(j)$.
\end{lemma}
\begin{proof}
Necessary condition.  Suppose that $f: \mathbb{N} \rightarrow \mathbb{N}$ is a countably affine map.  Let $i \lt j$. By the superconvex space structure on $\mathbb{N}$ it follows, for all $\alpha \in (0,1)$, that  $\alpha i + (1-\alpha) j = i$ .  If $f$ is not monotone then there exist a pair of elements $i,j \in \mathbb{N}$ such that $i \lt j$ with $f(j) \lt f(i)$.  This implies, for all $\alpha \in (0,1)$, that $f(j)= \alpha f(i) + (1-\alpha) f(j) \lt   f(\alpha i + (1-\alpha) j ) =f(i)$, which contradicts our hypothesis that $f$ is a countably affine map.
 
Sufficient condition. Suppose $f$ is a monotone function, and
 that we are given an arbitrary countably affine sum $\sum_{i \in \mathbb{N}} p_i i = n$ in $\mathbb{N}$, so that for all $i=0,1,\ldots,n-1$ we have $p_i=0$.  Since the condition defining the superconvex structure is conditioned on the property $p_i \ne 0$, the countably affine sum is not changed  by removing any number of terms $i$ in the countable sum whose coefficient $p_i=0$.  Hence 
for all $j$ such that $n\lt j$ it follows that $f(n) \le f(j)$ so that
\begin{equation}
f( \sum_{i=0}^{\infty} p_i \, i) = f(n) = \sum_{i=n}^{\infty} p_i f(i) 
\end{equation}
where the last equality follows from the definition of the superconvex space structure on $\mathbb{N}$.
\end{proof}


The category $\mathbf{SCvx}$ has all limits and colimits.  Furthermore it is a symmetric monoidal closed category under the tensor product. The proof of the latter condition follows the proof by Meng, replacing finite sums with countable sums.

The full subcategory consisting of the single object $\Delta_{\mathbb{N}}$ is dense in $\mathbf{SCvx}$, and hence we can employ the restricted Yoneda embedding to view superconvex spaces as the functors $\widehat{A}=\mathbf{SCvx}(\cdot,A) \in \mathbf{Set}^{\Delta_{\mathbb{N}}^{op}}$, where $\Delta_{\mathbb{N}}$ is viewed as a [[monoid]].  


  An ideal in a superconvex space $A$ is a subset $\mathcal{I}$ such that whenever $a_0 \in \mathcal{I}$ and $\sum_{i \in \mathbb{N}}p_i a_i$ is a countable affine sum with the coefficient of $a_0$ nonzero then $\sum_{i \in \mathbb{N}}p_i a_i \in \mathcal{I}$.   Ideals are useful for defining functors to or from $\mathbf{SCvx}$.

## Examples
\begin{example}
A fundamental superconvex space is the set $\mathbb{N}$ with the superconvex space structure defined, for every sequence $\mathbf{s}: \mathbb{N} \rightarrow \mathbb{N}$  by 
\begin{equation}
\int_{\mathbb{N}} \mathbf{s} d\mathbf{p} = \inf_i \{\mathbf{s}_i \, | \, p_i \gt 0 \}
\end{equation}
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
The one point compactification of the real line $\mathbb{R}_{\infty}$, with one point adjoined, denoted $\infty$, which satisfies the property that any countably affine sum $\sum_{i \in \mathbb{N}} p_i r_i = \infty$ if either (1) $r_j = \infty$ and $p_j \gt 0$ for any index $j$, or (2) the sequence of partial sums does not converge, is a superconvex space.  The real line $\mathbb{R}$ is not a super convexspace since we could take $p_i = \frac{1}{2^i}$ and $r_i = 2^{i+1}$ and the limit of the sequence does not exist in $\mathbb{R}$.  Thus while $\mathbb{R}$ is a convex space it is not a superconvex space.  

 The only nonconstant countably affine map $j: \mathbb{R}_{\infty} \rightarrow \mathbb{2}$ is given by $j(u)=1$ for all $u \in \mathbb{R}$ and $j(\infty)=0$ (for the superconvex space structure on $\mathbf{2}$ determined by $\frac{1}{2} \underline{0} + \frac{1}{2} \underline{1} = \underline{0}$).  
\end{example}

\begin{example} A pathological space, useful for counterexamples, is given by the closed unit interval with the superconvex space structure defined by the infimum function, $\sum_{i \in \mathbb{N}} p_i u_i := inf_i \{ u_i | p_i \gt 0\}$.
\end{example}
 

\begin{example}  Consider the probability monad on compact Hausdorff spaces, where the algebras are precisely the compact convex sets $K$ in locally convex topological vector spaces together with the barycenter maps $\beta_K:\mathcal{P}K\rightarrow K$.  

Given such a space $K$ we can endow it with a superconvex space structure by defining, for all $\mathbf{p} \in \mathcal{G}\mathbb{N}$, countable affine sums by  $\sum_{i \in \mathbb{N}} p_i k_i := \beta_K( \sum_{i \in \mathbb{N}} p_i \delta_{k_i})$ which, along with the pointwise superconvex space structure on $\mathcal{P}K$ makes the barycenter map $\beta_K$ a countably affine map.  

To prove this endows $K$ with a superconvex space structure note that $\beta_K(\delta_{k_i})= k_i$ for all $k_i \in K$ to obtain
$$
\sum_{i \in \mathbb{N}} p_i \beta_K(\delta_{k_i}) = \sum_{i \in \mathbb{N}} p_i k_i := \beta_K(\sum_{i \in \mathbb{N}} p_i \delta_{k_i}).
$$
To prove $\beta_K$ is countably affine on $\mathcal{P}K$ use the property that $\beta_K \circ \mu_K = \beta_K \circ \mathcal{P}\beta_K$.

The method employed in this example is not restricted to locally convex compact Hausdorff spaces. It shows that the algebras of a probability monad are a superconvex space.
That implication is the motivation for the next example.
\end{example}

\begin{example}
 The standard *free space* construction can be applied to superconvex spaces to obtain  an adjoint pair $\mathcal{F}:\mathbf{Set} \leftrightarrows \mathbf{SCvx}: \mathcal{U}$
where $\mathcal{F}(A)$ consists of all formal countable affine sums, $\int_{\mathbb{N}} \mathbf{a} \, d\mathbf{p} := \sum_{i \in \mathbb{N}}p_i a_i$ for $\mathbf{p} \in \mathcal{G}{\mathbb{N}}$ and $\mathbf{a} \in \mathbf{Set}(\mathbb{N},A)$,
modulo the relations 
\begin{equation}
\int_{j \in \mathbb{N}} \big( \int_{i \in \mathbb{N}} \mathbf{a} \, d\mathbf{Q}^i \big) \, d\mathbf{p} \cong  \int_{j \in \mathbb{N}} \mathbf{a} \, d\big( \int_{i \in \mathbb{N}} \mathbf{Q}^{\bullet} \,   d\mathbf{p} \big)  \quad \forall \, \mathbf{Q} \in \mathbf{Set}( \mathbb{N},  \mathcal{G}{\mathbb{N}})
\end{equation}
 so that the sole necessary axiom of a superconvex space is satisfied. 

One important aspect of the free space adjunction is that it implies

*Lemma* Let $X$ be an arbitrary set and $\mathcal{F}X$ the free superconvex space on $X$.  Let the quotient map $\widehat{q}: \mathcal{F}{X} \rightarrow A$ be the coequalizer of  the parallel pair $\mathbf{1}_{\mathcal{F}{X}}, k: \mathcal{F}{X} \rightarrow \mathcal{F}{X}$.     Then the quotient of the free space is the free space of the quotient, $\mathcal{F}X / \widehat{q} \cong \mathcal{F}(X/q)$

\begin{centre} 
\begin{tikzpicture}
    \node  (X)   at   (0,0)   {$X$};
    \node  (Xq)  at  (0, -1.5)  {$X/q$};
    \node  (UFX) at  (3,0)    {$\mathcal{U}(\mathcal{F}(X))$};
    \node  (UA)  at  (3, -1.5)  {$\mathcal{U}(A)$};
    \node  (c)   at  (.5, -2.5)   {in $\mathbf{Set}$};
    \draw[->, above] (X) to node {$\eta_X$} (UFX);
    \draw[->>,left] (X) to node [xshift=-3pt,yshift=-3pt]{$q$} (UA);
    \draw[->>,right] (UFX) to node {$\mathcal{U}(\widehat{q})$} (UA);
    
    \node  (FX)  at  (5.5,0)  {$\mathcal{F}{X}$};
    \node  (A)    at  (5.5, -1.5)  {$A \cong \mathcal{F}{X}/\widehat{q}$};
    \node   (d)   at   (5.5, -2.5)  {in $\mathbf{SCvx}$};
    \draw[->>,right] (FX) to node {$\widehat{q}$} (A);
    
    \draw[->>,left,dashed] (X) to node {$\pi$} (Xq);
    \draw[>->>,below,dashed] (Xq) to node {$\widetilde{q}$} (UA);
    
\end{tikzpicture}
\end{centre}
*Proof*
The quotient map $\widehat{q}:\mathcal{F}X \rightarrow A$  is, up to isomorphism, just $\widehat{q}:\mathcal{F}X \rightarrow \mathcal{F}X/\widehat{q}$.  Because the quotient map is countably affine it  is completely specified by where it sends the elements $1 x \in \mathcal{F}X$.  Because $q(x) = \widehat{q}(\eta_X(x)) = \widehat{q}(1x) = [1 x]_{\widehat{q}}=[k (1 x)]_{\widehat{q}}$ we have
\begin{equation}
\hat{q}(\sum_{i \in \mathbb{N}} p_i x_i)=\sum_{i \in \mathbb{N}} p_i 
 [1 x_i]_{\hat{q}} = \sum_{i \in \mathbb{N}} p_i q(x_i).  
\end{equation}
The function $q$ specifies an equivalence relation on $X$, yielding the set $X/q$. Because $q$ is surjective we can thus endow the set $X/q$ with the superconvex space structure of $A$ using the bijective map of sets $\widetilde{q}: X/q \rightarrow \mathcal{U}(A)$.  Hence the above equation extends (trivially) on the right  by  $\sum_{i \in \mathbb{N}} p_i q(x_i) = \sum_{i \in \mathbb{N}} p_i \, \widetilde{q}([x_i]_q) =  \widetilde{q}(\sum_{i \in \mathbb{N}} p_i [x_i]_q )$.  
The map $\mathcal{F}X / \hat{q} \rightarrow \mathcal{F}( \mathcal{U}(A))$ specified by $\sum_{i \in \mathbb{N}}p_i [1 x_i]_{\widehat{q}} \mapsto \sum_{i \in \mathbb{N}}p_i \widetilde{q}( [x_i]_q )$ specifies  a $\mathbf{SCvx}$-isomorphism.  By the isomorphism $\widetilde{q}$ we can write this as $\mathcal{F}{X}/\widehat{q} \cong \mathcal{F}(X/q)$.  That completes the proof.
    
 Now let $X$ denote a standard measurable space, so $\mathcal{G}{X}$ is standard also. Forgetting the measurable structure on $\mathcal{G}{X}$ we can take the free space of that set, $\mathcal{F}( \mathcal{U}( \mathcal{G}{X}))$ which consist of all countable affine sums $\int_{\mathbb{N}} \mathbf{P} \, d\mathbf{p}$ for all $\mathbf{P} \in \mathbf{Set}(\mathbb{N}, \mathcal{U}(\mathcal{G}{X}))$ and all $\mathbf{p} \in \mathcal{G}{\mathbb{N}}$.  These countable affine sums are  defined pointwise $(\int_{\mathbb{N}} \mathbf{P} \, d\mathbf{p})U := \sum_{i \in \mathbb{N}} p_i P_i(U)$ for all $U \in \Sigma_X$. 
  
 We observe that the free space $\mathcal{F}(\mathcal{U}(\mathcal{G}{X}))$ can also be viewed as the image of the functor $\mathcal{P}: \mathbf{Meas} \rightarrow \mathbf{SCvx}$ on $X$, where $\mathcal{P}$  is the Giry monad (functor) viewed as a functor into $\mathbf{SCvx}$.  

 We would like to extend the free space adjunction $\mathcal{F} \dashv \mathcal{U}$ with an adjunction $\mathcal{P}: \mathbf{Std} \leftrightarrows \mathbf{SCvx}: \mathbf{\Sigma}$
such that the composite is the Giry monad on $\mathbf{Std}$. The category $\mathbf{SCvx}_{\star}$ denotes some subcategory of $\mathbf{SCvx}$ so that the adjunction can be constructed.  If such an adjunction exists the counit of the adjunction says every space $A$  is the quotient of a free space, i.e., $A$ is the coequalizer of a parallel pair of maps into a free space.    To illustrate this consider the following elementary example.
 
 The coequalizer of the pair of points $\frac{1}{3}: \mathbf{1} \rightarrow [0,1]$ and $\frac{2}{3}: \mathbf{1} \rightarrow [0,1]$, where $[0,1] \cong \mathbf{P}{\mathbf{2}}$.  The coequalizer of those pair of points is the discrete space  $A=\{0,u,1\}$ with the structure defined by $p u + (1-p) 0 = u$ for all $p \in (0,1]$, $p u + (1-p) 1 = u$ for all $p \in (0,1]$, and $p 0 + (1-p) 1 = u$ for all $p \in (0,1)$.  

If the functor $\mathbf{\Sigma}: \mathbf{SCvx}_{\star} \rightarrow \mathbf{Std}$ exists  it should recognize that that superconvex space arises as a quotient space of $\mathcal{P}{\mathbf{2}}$, and hence should have the barycenter map $\epsilon_A: \mathcal{P}{\mathbf{2}} \rightarrow A$ given by
the mapping $\delta_0 \mapsto 0$, $\delta_1 \mapsto 1$, and $r \delta_0 + (1-r) \delta_1 \mapsto u$ for all $r \in (0,1)$.

Let $\mathbf{\Omega}$ denote the full subcategory of $\mathbf{SCvx}$ consisting of the two objects $\mathbb{N}$ and $\Delta_{\mathbb{N}}$, and let $\iota:\mathbf{\Omega} \rightarrow \mathbf{SCvx}$ be the inclusion functor.  

If we look at the category $A \downarrow \iota$ there are two countably affine maps, 
\begin{equation}
\begin{array}{lcccc}
\phi_{0,u} &:& A & \rightarrow & \mathbb{N} \\
&:& a & \mapsto & \left\{ \begin{array}{ll} 0 & for \, a \in \{0,u\} \\ 1 & for \, a=1 \end{array} \right.
\end{array}
\end{equation}
and 
\begin{equation}
\begin{array}{lcccc}
\phi_{1,u} &:& A & \rightarrow & \mathbb{N} \\
&:& a & \mapsto & \left\{ \begin{array}{ll} 0 & for \, a \in \{1,u\} \\ 1 & for \, a=0 \end{array} \right.
\end{array},
\end{equation}
from which every other countably affine map  $A \rightarrow \mathbb{N}$ can be obtained by composing either $\phi_{0,u}$ or $\phi_{1,u}$
 with a monotonic function $\phi: \mathbb{N} \rightarrow \mathbb{N}$.  Because $A$ is discrete there are no non-constant countably affine maps $A \rightarrow \Delta_{\mathbb{N}}$.
  
 The coequalizer of those two maps yields the discrete space $\mathbf{2}$ for which $\mathcal{P}{\mathbf{2}}$ is the space we are trying to find - it is the smallest free space such that there is a countably affine map  $\mathcal{P}{\mathbf{2}} \rightarrow A$.
 
 Whether probing a space $A$ with arrows to objects and products of objects  in $\mathbf{\Omega}$  is sufficient is unknown but a clue is given in the fact that every standard space is $\mathbf{Std}$-isomorphic to either $[0,1]$ or a countable discrete space. Hence $\mathbf{SCvx}_{\star}$ should intuitively consists of quotients of $\prod_{i \in \mathbb{N}} \Delta_{\mathbb{N}}$ (and smaller) - the countability condition being the critical condition. That condition rules out spaces such as $\prod_{i \in [0,1]}\Delta_{\mathbb{N}}$ and the pathological space of Example 5.4.

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

The fact that  the functor $\mathbf{\Sigma}: \mathbf{\Omega} \rightarrow \mathbf{Std}_2$ is a codense functor can be found  in

* {#Sturtz22} [[Kirk Sturtz]], _Giry algebras for standard measurable spaces_ $[$[arXiv:2202:10819](https://arxiv.org/abs/2202.10819)$]$

although several aspects, such as the construction with the right-Kan is incorrect. 

For purposes of constructing models of complex systems using superconvex spaces the construction given in Example 6.1 of the following article applies equally well to superconvex spaces.

* [[Tobias Fritz]], Convex spaces I: definition and examples. 
[arXiv/0903.5522](http://arxiv.org/abs/0903.5522)

The term strong convex spaces was employed in the text

* [[George Mackey]], _The Mathematical Foundations of Quantum Mechanics_ A Lecture-note Volume, ser. The mathematical physics monograph series. Princeton university, 1963


[[!redirects superconvex spaces]]

[[!redirects strong convex space]]
[[!redirects strong convex spaces]]

[[!redirects super convex space]]
[[!redirects super convex spaces]]

[[!redirects Super convex space]]
[[!redirects Super convex spaces]]


