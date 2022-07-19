
# Contents (or put a title here)
* this block creates the table of contents, leave as is
{: toc}

## Idea

Super convex spaces generalize the idea of a convex space by replacing finite affine sums with countable affine sums.


## Definition 

 Given any set $A$, a sequence $\mathbf{a}: \mathbbmss{N} \rightarrow A$, and any $\mathbf{p} \in \Delta_{\mathbb{N}}$, which is equivalent to saying that  $\mathbf{p} \in \G{\bN}$  because we have only forgotten the measurable structure of $\G{\mathbb{N}}$, we refer to the formal expression  ``$\sum_{i \in \mathbbmss{N}} p_i \, a_i$''  as a \emph{countably affine sum} of elements of $A$, and for brevity we use the notation ``$\sum_{i\in \mathbbmss{N}} p_i a_i$''  to refer to a countably affine sum dropping the explicit reference to the condition that the limit of partial sums $\sum_{i=0}^N p_i$ converges to one.  An alternative notation to the countable affine sum notation is to use the integral notation
 \begin{equation} \nonumber
  \int_{\mathbbmss{N}} \mathbf{a} \, d\mathbf{p} := \sum_{i \in \mathbbmss{N}} p_i a_i.
 \end{equation}

We say a set $A$ has the structure of a super convex space $A$ if and only if the following three axioms are satisfied:


\textbf{Axiom 1}. For every sequence $\mathbf{a}: \mathbbmss{N} \rightarrow A$ and every $\mathbf{p} \in \G(\mathbb{N})$ it follows that 
\begin{equation} \nonumber
\int_{\mathbbmss{N}} \mathbf{a} \, d\mathbf{p}  \in A.
\end{equation}


Axiom 2. For every sequence $\mathbf{a}: \Nat \rightarrow A$ and every  $j \in \mathbbmss{N}$ the property 
\begin{equation} \nonumber
\int_{\mathbbmss{N}} \mathbf{a} \, \, d\delta_j = a_j
\end{equation}
holds.  


Axiom 3. If $\mathbf{p} \in \G(\mathbb{N})$ and $\mathbf{Q}: \mathbbmss{N} \rightarrow \G(\mathbb{N})$ is a sequence of probability measures on $(\mathbbmss{N}, \powerset{\mathbb{N}})$   then 
\be \nonumber
\int_{j \in \mathbbmss{N}} \big( \int_{\mathbbmss{N}} \mathbf{a} \, d\mathbf{Q}^j \big) \, d\mathbf{p} = \int_{\mathbbmss{N}} \mathbf{a} \,  d(  \int_{j \in \mathbbmss{N}} \mathbf{Q}^{\bullet} \, d\mathbf{p}  \big).
\ee
Stated alternatively,  $ \displaystyle{\sum_{j \in \mathbbmss{N}}} p_j ( \displaystyle{\sum_{i \in \mathbbmss{N}}} Q^j_i a_i) 
= \displaystyle{\sum_{i \in \mathbbmss{N}}}( \displaystyle{\sum_{j \in \mathbbmss{N}}} p_j Q_i^j)a_i$.




## Properties

(...)


## Examples

(...)


## References

(...)