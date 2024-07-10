
# Contents (or put a title here)
* this block creates the table of contents, leave as is
{: toc}

## Idea

The notion of _regular directed complex_, introduced by [[Amar Hadzihasanovic]], is a notion of [[pasting diagram]] shape. There, a pasting diagram is encoded as a kind of "directed [[cell complex]]", that is, a cell complex together with an orientation on each cell, which divides its boundary into two halves: an *input* half and an *output* half.


## Definition 

### Basic order theory

\begin{definition}\label{ogpos}
**(oriented graded poset)** \linebreak

A **graded poset** is a poset together with a rank function $\mathrm{dim} \colon P \to \mathbb{N}$ such that

*  if $x \lt y$, then $\mathrm{dim} x \lt \mathrm{dim} y$, 
*  if $x$ [[covering relation|covers]] $y$, then $\mathrm{dim} x = \mathrm{dim} y + 1$.

An **oriented graded poset** is a graded poset together with a sign $\alpha \in \{ -, + \}$ for each edge in its covering diagram.

\end{definition}

\begin{definition}\label{faces}
**(faces)** \linebreak

Let $P$ be an oriented graded poset. For all $x$ in $P$, and $\alpha = -$ (resp. $\alpha = +$), we define the **input** (resp. **output**) **face**
$$
    \Delta^\alpha x \coloneqq \{ y \in P \mid x \;\text{covers}\; y \;\text{with orientation}\; \alpha \}.
$$

\end{definition}

With that, we can define a morphism $f \colon P \to Q$ of oriented graded posets to be a function of the underlying sets such that, for all $x \in P$ and $\alpha \in \{ -, + \}$, $f$ induces a bijection between $\Delta^\alpha x$ and $\Delta^\alpha f(x)$.

Oriented graded posets and morphisms form the [[category]] $\mathbf{ogPos}$.

(todo: boundaries, round, max element, passage ogpos to pasting diagram)

### Inductive construction of molecules.

We will now construct inductively a well-formed class of oriented graded posets, called the **molecules**, which model _composable_ pasting diagrams. There are 3 constructors: 

*  (Point) the terminal oriented graded poset $\mathbf{1}$ is a molecule.
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
                                                        & {}                                                    &         \\
\bullet \arrow[rd, bend right] \arrow[rr, bend left=67] &                                                       & \bullet \\
                                                        & \bullet \arrow[ru, bend right] \arrow[uu, Rightarrow] &        
\end{tikzcd}
(which is also the second [[oriental]]).

\begin{definition}\label{rdcpx}
**Regular directed complex** \linebreak

A **regular directed complex** is an oriented graded poset $P$ such that for all $x$ in $P$, $\mathrm{cl}(x)$ is an atom.
  
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
## Examples

(todo)


## References

The main reference on regular directed complexes:

* {#Hadzihasanovic2024} [[Amar Hadzihasanovic]], _Combinatorics of higher-categorical diagrams_, 2024 ([link](https://arxiv.org/abs/2404.07273))

(todo)