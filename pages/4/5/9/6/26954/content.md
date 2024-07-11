
# Contents
* this block creates the table of contents, leave as is
{: toc}



## Idea

The notion of _regular directed complex_, introduced by [[Amar Hadzihasanovic]], is a notion of [[pasting diagram]] shape. There, a pasting diagram is encoded as a kind of "directed [[cell complex]]", that is, a cell complex together with an orientation on each cell, which divides its boundary into two halves: an *input* half and an *output* half.



## Definition 

In this framework, a pasting diagram will be encoded as an _oriented graded poset_ (Def. \ref{ogpos}), which is a poset, whose [[covering relation|covering diagram]] is graded, and each edge possess an orientation. To see this consider the following pasting diagram (referred in this page as the **running pasting diagram**)
\begin{tikzcd}
                                                                        &  & {}                             &  &                   &  &   \\
    x \arrow[rrrr, "f"', bend right=60] \arrow[rrrr, "g", bend left=60] &  &                                &  & y \arrow[rr, "h"] &  & z \\
                                                                        &  & {} \arrow[uu, "s", Rightarrow] &  &                   &  &  
\end{tikzcd}
and the covering diagram associated to it
\begin{tikzcd}
    s \arrow[d, "-" description, no head] \arrow[rd, "+" description, no head]              &                                                                                          &                                       \\
    f \arrow[rd, "+" description, no head, shift right] \arrow[d, "-" description, no head] & g \arrow[ld, "-" description, no head, shift left=2] \arrow[d, "+" description, no head] & h \arrow[d, "+" description, no head] \\
    x                                                                                       & y \arrow[ru, "-" description, no head]                                                   & z                                    
\end{tikzcd}


### Basic order theory

Of course, not all oriented graded poset will lead to a well-formed pasting diagram: before defining the one that will count, we introduce some terminology.

\begin{definition}\label{ogpos}
**(oriented graded poset)** \linebreak
A **graded poset** is a poset together with a rank function $\mathrm{dim} \colon P \to \mathbb{N}$ such that

*  if $x \lt y$, then $\mathrm{dim} x \lt \mathrm{dim} y$, 
*  if $x$ [[covering relation|covers]] $y$, then $\mathrm{dim} x = \mathrm{dim} y + 1$.

An **oriented graded poset** is a graded poset together with a sign $\alpha \in \{ -, + \}$ for each edge in its covering diagram.
\end{definition}


\begin{remark}
The grading function of an oriented graded poset defines a notion of dimension of an element. For instance, in the running pasting diagram, the dimensions of $x, f, s$ are repectively $0, 1, 2$. If $P$ is an oriented graded poset, we write $P_n$ for its elements of dimension $n$.
\end{remark}

\begin{definition}\label{faces}
**(faces)** \linebreak
Let $P$ be an oriented graded poset. For all $x$ in $P$, and $\alpha = -$ (resp. $\alpha = +$), we define the **input** (resp. **output**) **faces**
$$
    \Delta^\alpha x \coloneqq \{ y \in P \mid x \;\text{covers}\; y \;\text{with orientation}\; \alpha \}.
$$

Dually, we define the **input** (reps. **output**) **cofaces**
$$
    \nabla^\alpha x \coloneqq \{ y \in P \mid y \;\text{covers}\; x \;\text{with orientation}\; \alpha \}.
$$
\end{definition}

\begin{definition}\label{cat_ogpos}
**$\mathbf{ogPos}$**\linebreak
With that, we can define a morphism $f \colon P \to Q$ of oriented graded posets to be a function of the underlying sets such that, for all $x \in P$ and $\alpha \in \{ -, + \}$, $f$ induces a bijection between $\Delta^\alpha x$ and $\Delta^\alpha f(x)$.

Oriented graded posets and morphisms form the [[category]] $\mathbf{ogPos}$.
\end{definition}


\begin{definition}\label{maximal_element}
**(maximal element)**\linebreak
An element $x$ of an oriented graded poset is **maximal** if for $\alpha \in \{ -, + \}$, $\nabla^\alpha x = \emptyset$, that is, $x$ is maximal if it is covered by no element.
\end{definition}


\begin{definition}\label{boundaries}
**(boundaries)** \linebreak
Let $U$ be a closed subset of an oriented graded poset, let $\alpha = -$ (resp. $\alpha = +$), and let $n \in \mathbb{N}$, let
$$
    \Delta^\alpha_n U \coloneqq \{ x \in U_n \mid \nabla^{- \alpha} x \cap U = \emptyset \}. 
$$
The **input** (reps. **output**) **$n$-boundary** is the closed subset
$$
    \partial^\alpha_n U \coloneqq \mathrm{cl}(\Delta^\alpha_n U) \cup \bigcup_{k \lt n} \mathrm{cl}(\mathrm{Max} U)_k.
$$
\end{definition}

In the running pasting diagram, calling it $U$, we have
$$
    \partial^-_1 U = \{ x, f, y \},
$$
and
$$
    \partial^+_0 U = \{ z \}.
$$

\begin{notation}
We write 
$$
    \partial_n U \coloneqq \partial^-_n U \cup \partial^+_n U ,
$$
$$
    \Delta U \coloneqq \Delta^- U \cup \Delta^+ U,
$$
etc... The general convention is that if the superscript $\alpha$ is not provided to an operator, it is the union of the operator with $\alpha = -$, and with $\alpha = +$.

Similarly, if the subscript $n$ is not provided, it means "the dimension of the oriented graded poset minus 1", that is, we write:
$$
    \partial^- U \coloneqq \partial^-_{\dim U - 1} U.
$$
We also combine both in $\partial U$.

Last, if the index $n$ is negative, the result is the empty set, for instance,
$$
    \partial^-_{- 1} U \coloneqq \emptyset,
$$
etc.
\end{notation}
  
\begin{remark}
For any $\alpha, n$, $\partial^\alpha_n U$, $\partial_n U$, etc.. are subsets of $U$, and the inclusion they defines
$$
    \partial^\alpha_n U \hookrightarrow U \quad\quad \partial_n U \hookrightarrow U \quad\quad \text{etc},
$$
are all morphisms of oriented graded posets.
\end{remark}

The last bit of terminology we introduce is roundness. Consider a topological $n$-[[ball]] $U$, and its boundary the $n$-[[sphere]] $\partial U$. The latter is made of the gluing of two $(n - 1)$-balls $\partial^- U$ and $\partial^+ U$ along an $(n - 1)$-sphere $\partial_{n - 2} U$, in particular:
$$
 \partial^- U \cap \partial^+ U = \partial_{n - 2} U. 
$$ 
Similarly, $\partial U$ is an $(n - 1)$-sphere, which is made of a copie of two $(n - 2)$-balls which intersect at an $(n - 2)$-sphere, etc.. We will say that an oriented graded poset is round if it satisfies similar intersection conditions.

\begin{definition}\label{round}
**round**\linebreak
Let $P$ be an oriented graded poset of dimension $n$. We say that $P$ is round if for all $0 \le k \lt n$, we have
$$
\partial^-_k P \cap \partial^+_k P = \partial_{k - 1} P.
$$ 
\end{definition}


### Inductive construction of molecules.

We can now construct inductively a well-formed class of _globular_ oriented graded posets, called the **molecules**, which model _composable_ pasting diagrams. There are 3 constructors: 

*  (Point) the oriented graded poset $\mathbf{1}$ with a single point is a molecule.
*  (Paste) if $U, V$ are two molecules of dimensions $\gt n$ such that $\partial^+_n U \cong \partial^-_n V$, we compose them via the following pushout:
\begin{tikzcd}
    \partial^+_n U \cong \partial^-_n V \arrow[r] \arrow[d] & V \arrow[d] \\
    U \arrow[r]                                             & U \#_n V   
\end{tikzcd}
Then $U \#_n V$ is a molecule.
 
*  (Atom) if two molecules are _round_, of the same dimension $n$, and both their input and output $(n - 1)$-boundaries are coherently isomorphic, we can glue them together to form an "$n$-sphere", i.e. we construct the pushout
\begin{tikzcd}
    \partial_{n - 1} U \cong \partial_{n - 1} V \arrow[r] \arrow[d] & V \arrow[d]               \\
    U \arrow[r]                                                     & \partial(U \Rightarrow V)
\end{tikzcd}
Then, we add a top element $\top$ to $\partial(U \Rightarrow V)$ with orientation such that $\Delta^- \top =  \mathrm{Max} U$ and $\Delta^+ \top =  \mathrm{Max} V$. This defines $U \Rightarrow V$, which is a molecule.  
 


### Examples

If we take two copies of (Point) and applies (Atom) to them, we obtain the arrow $\vec I \coloneqq (\mathbf{1} \Rightarrow \mathbf{1})$:
\begin{tikzcd}
    \bullet \arrow[r] & \bullet
\end{tikzcd}
Then, we can use (Paste) with $\vec I$ and $\vec I$ on the 0-boundary to obtain $\vec I \#_0 \vec I$:
\begin{tikzcd}
    \bullet \arrow[r] & \bullet \arrow[r] & \bullet
\end{tikzcd}

Now we use (Atom) to construct $(\vec I \#_0 \vec I) \Rightarrow \vec I$:
\begin{tikzcd}
    \bullet \arrow[rd, bend right] \arrow[rr] & {}                                                   & \bullet \\
                                              & \bullet \arrow[ru, bend right] \arrow[u, Rightarrow] &        
\end{tikzcd}
(which is also the second [[oriental]]).

\begin{definition}\label{atom}
**([[atom category|atom]])**\linebreak
    An **atom** is a molecule with a maximal element.
\end{definition}

\begin{lemma}\label{atomAtomPoint}
If a molecule $U$ is an atom, then $U$ was produced by either (Point) or (Atom).  
\end{lemma}

\begin{definition}\label{rdcpx}
**(regular directed complex)** \linebreak
A **regular directed complex** is an oriented graded poset $P$ such that for all $x$ in $P$, $\mathrm{cl}(x)$ is an [[atom category|atom]].
\end{definition}

For instance,
\begin{tikzcd}
    \bullet \arrow[r, bend right=49] \arrow[r, bend left=49] & \bullet
\end{tikzcd}
is a regular directed complex but not a molecule.



## Properties

It seems that the above construction of molecules depends on the choice of an isomorphism during the construction. However we prove already:

\begin{proposition}
Isomorphisms of molecules are unique.
\end{proposition}
\begin{proof}
See ([Corollary 3.4.12](#Hadzihasanovic2024))
\end{proof}

We will write $U = V$ to mean that there exists a unique isomorphism between $U$ and $V$.


### Strict $\omega$-[[strict omega-category|categorical]] structure.

The category of molecule, with pastings $\#_n$ and boundaries $\partial^\alpha_n$ satisfies all the axioms of strict $\omega$-categories. More precisely, we have the following results.
  
\begin{proposition}
**(globularity)**\linebreak
Any molecule $U$ is **globular**, that is, for all $\alpha, \beta \in \{ -, + \}$ and all $k \lt n$, we have
$$
    \partial^\alpha_k(\partial^\beta_n U) = \partial^\alpha_k U. 
$$
\end{proposition}

\begin{proposition}
**(boundaries)**\linebreak
Let $U, V$ be molecules such that $U \#_k V$ is defined, let $\alpha \in \{ -, + \}$ and $n \geq 0$, then
$$
    \partial^\alpha_n (U \#k V) =
    \begin{cases}
        \partial^\alpha_n U = \partial^\alpha_n V & \text{if}\; n \lt k, \\
        \partial^-_k U &\text{if}\; n = k, \alpha = -, \\
        \partial^+_k V &\text{if}\; n = k, \alpha = +, \\
        \partial^\alpha_n U \#_k \partial^\alpha_n V &\text{if}\; n \gt k.
    \end{cases}
$$
\end{proposition}

\begin{proposition}
**([[unitality]])**\linebreak
Let $U$ be a molecule of dimension $n$, then for all $k \lt n$, we have
$$
    \partial^-_k U \#_k U = U = U \#_k \partial^+_k U.
$$
\end{proposition}

\begin{proposition}
**([[associativity]])**\linebreak
Let $U, V, W$ be molecules such that $(U \#_k V) \#_k W$ is defined, then
$$
    (U \#_k V) \#_k W = U \#_k (V \#_k W).
$$
\end{proposition}


\begin{proposition}
**([[exchange law|exchange]])**\linebreak
Let $U, V, U', V'$ be molecules, let $k \lt n$ such that $(U \#_n U') \#_k (V \#_n V')$ is defined, then
$$
    (U \#_n U') \#_k (V \#_n V') = (U \#_k V) \#_n (U' \#_k V').
$$
\end{proposition}

\begin{corollary}
The set of all molecules is a strict $\omega$-[[strict omega-category|category]], with 

*  source and target given by the boundaries;
*  composition given by the pasting operations $\#_n$;

\end{corollary}

In fact, we can do better, for $P$ an oriented graded poset, we let $\mathrm{Mol} / P$ to be the category whose objects are (the isomorphism classes of) morphisms $f \colon U \to P$, for $U$ a molecule. Precomposing $f$ by $\partial^\alpha_n U \hookrightarrow U$ defines $\partial^\alpha_n f$, while if $g \colon V \to P$ is in $\mathrm{Mol} / P$, such that $\partial^+_n f = \partial^-_n g$, then the universal property of the [[pushout]] defines a unique element $f \#_k g \colon U \#_n V \to P$ in $\mathrm{Mol} / P$. Hence:
\begin{proposition}
For all oriented graded poset $P$, $\mathrm{Mol} / P$ is a strict $\omega$-category. Furthermore, any morphism $f \colon P \to Q$ induces a strict $\omega$-functor 
$$
    \mathrm{Mol} / f \colon \mathrm{Mol} / P \to \mathrm{Mol} / Q
$$
sending $U \to P$ to $U \to P \stackrel{f}{\to} Q$. This defines a functor $\mathrm{Mol} / - \colon \mathbf{ogPos} \to \mathbf{\omega Cat}$.
\end{proposition}



## Operations

Regular directed complexes are closed under many relevant operations useful for [[higher category theory]]

### Gray product

\begin{definition}\label{Gray_product}
**(Gray product)**\linebreak
Let $P, Q$ be oriented graded posets. The **Gray product** of $P$ and $Q$ is the oriented graded poset $P \otimes Q$ whose

*  underlying graded poset is the cartesian product $P \times Q$,
*  orientation is defined, for all $(x, y) \in P \times Q$ and $\a \in \{ -, + \}$, by the equation $\Delta^\a(x, y) = \Delta^\a x \times \{ y \} + \{ x \} \times \Delta^{(-)^{\mathrm{dim} x} \a} y$.

\end{definition}

\begin{example}
The Gray product $\vec{I} \otimes \vec{I}$ is
\begin{tikzcd}
    \bullet \arrow[r]           & \bullet                                  \\
    \bullet \arrow[r] \arrow[u] & \bullet \arrow[u] \arrow[lu, Rightarrow]
\end{tikzcd}
\end{example}

\begin{theorem}
Let $P, Q$ be regular directed complexes. Then $P \otimes Q$ is a regular directed complex. 
\end{theorem}
\begin{proof}
The proof is extremely combinatorial, and can be found in [Section 7.2](#Hadzihasanovic2024). 
\end{proof}

The Gray product is associtive and has [[unit object|unit]] the point $\mathbf{1}$. It is not symmetrical. 

### Join

Similarly, we can take the join of regular directed complexes. Unfolding the defintion can be quite involved, but once we have the Gray product, we can take the following shortcut.

\begin{definition}
**(augmentation and diminution)**\linebreak
Let $P$ be an oriented graded poset. 

*  The **augmentation** of and $P$ is the oriented graded poset $P_\bot \coloneqq P \cup \{ \bot \}$ such that $\nabla^+ \bot = P_0$ and $\nabla^- \bot = \emptyset$.
*  Suppose $P$ has a minimal element $\bot$, then the **diminution** of $P$ is the oriented graded poset $P_{\not{\bot}} \coloneqq P \backslash \{ \bot \}$.

\end{definition}

\begin{definition}
**([[join of topological spaces|join]])**\linebreak
Let $P, Q$ be an oriented graded poset. The **join** of $P$ and $Q$ is the oriented graded poset 
$$
    P \star Q \coloneqq (P_{\bot} \otimes Q_{\bot})_{\not\bot}.
$$
\end{definition}

\begin{theorem}
Let $P, Q$ be regular directed complexes. Then $P \star Q$ is a regular directed complex. 
\end{theorem}

The join is associtive and has [[unit object|unit]] $\emptyset$, the empty regular directed complex. It is not symmetrical.

\begin{example}
The $n$-iterated join $\mathbf{1} \star \ldots \star \mathbf{1}$ of the point is the $n$-th [[oriental]].
\end{example}

### Suspension

\begin{definition}
**(suspension)**\linebreak
Let $P$ be an oriented graded poset. The **suspension** of $P$ is the oriented graded poset $\mathsf{S}P$ whose

*  underlying set is
$$
    \{ \mathsf{S}x \mid x \in P \} \cup \{ \bot^-, \bot^+ \},
$$
*  partial order and orientation are defined by
$$
\nabla^\alpha x \coloneqq 
\begin{cases}
    \{ \mathsf{S}y \mid y \in \nabla^\alpha x' \} & \text{if}\; x = \mathsf{S}x', x' \in P, \\
    \{ \mathsf{S}y \mid y \in P_0 \} & \text{if}\; x = \bot^\alpha, \\
    \emptyset & \text{if}\; x = \bot^{-\alpha}.
\end{cases}
$$
for all $x \in \mathsf{S}P$ and $\alpha \in \{ -, + \}$.

\end{definition}

\begin{theorem}
Let $P$ be a regular directed complex. Then $\mathsf{S}P$ is a regular directed complex.
\end{theorem}

\begin{example}
The $n$-th iterated suspension $\mathsf{S}\ldots\mathsf{S}\mathbf{1}$ is the $n$-th [[globe]]. 
\end{example}

## Proof techniques

### Structural induction
Since molecules are defined inductively, we can use [[induction]] to prove statement about them. To prove that a statement $\mathcal{P}$ is true for all molecule, we can do as follows:

*  We prove that it is true for the (Point) $\mathbf{1}$.
*  We let $U, V$ be molecules such that $U \#_n V$ is defined, and we suppose that $\mathcal{P}$ holds for both $U$ and $V$. Then we prove that $\mathcal{P}$ holds for $U \#_n V$.
*  We let $U, V$ be molecules such that $U \Rightarrow V$ is defined, and we suppose that $\mathcal{P}$ holds for both $U$ and $V$. Then we prove that $\mathcal{P}$ holds for $U \Rightarrow V$.

For instance:
\begin{lemma}
Any molecule is a regular directed complex.
\end{lemma}
\begin{proof}
Let $U$ be a molecule, we need to prove that for all $x \in U$, $\mathrm{cl}(x)$ is an atom. We proceed by induction on the construction of $U$. If $U$ was produced by (Point), then $x$ must be the unique element of $U$ whose closure is $U$ itself. If $U$ was produced by (Paste), then $U = V \#_k W$ , and $x \in V$ or $x \in W$ ; the inductive hypothesis applies. If $U$ was produced by (Atom), it is equal to $(V \cup W ) + \{ \top \}$, and either $x \in V$ or $x \in W$, in which case the inductive hypothesis applies, or $x = \top$, and $\mathrm{cl}(x) = U$ is an atom by definition.
\end{proof}

### Other methods


(todo: submolecule induction, layering)

## References

The main reference on regular directed complexes:

* {#Hadzihasanovic2024} [[Amar Hadzihasanovic]], _Combinatorics of higher-categorical diagrams_, 2024 ([link](https://arxiv.org/abs/2404.07273))

(todo)