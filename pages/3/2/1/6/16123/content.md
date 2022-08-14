
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A polynomial all of whose monomial terms have the same degree. See also [[polynomial]].

## Definition

If $R$ is a commutative rig, then the set $R_{n}[X_{1},...,X_{q}]$ of homogeneous polynomials of degree $n$ with variables $X_{1},...,X_{q}$ is given by all the expressions of the form $\underset{\substack{0\le i_{1},...,i_{q} \le n\\ i_{1}+...+i_{q} = n}}{\sum} a_{i_{1},...,i_{q}}X_{1}^{i_{1}}...X_{q}^{i_{q}}$.

## Euler identity

A specific property of homogeneous polynomials is the Euler identity:

\begin{theorem}
If $R$ is a commutative rig and if $P \in R_{n}[X_{1},...,X_{q}]$ then $\underset{1 \le k \le q}{\sum} \frac{\partial P}{\partial X_{k}}X_{k} = n.P$. Reciprocally, if $R$ is a commutative [[multiplicatively cancellable rig]], if $P \in R[X_{1},...,X_{q}]$ and $\underset{1 \le k \le q}{\sum} \frac{\partial P}{\partial X_{k}}X_{k} = n.P$, then $P \in R_{n}[X_{1},...,X_{q}]$.
\end{theorem}

\begin{proof}
Suppose that $P \in R_{n}[X_{1},...,X_{q}]$ and write $P=\underset{\substack{0\le i_{1},...,i_{q} \le n\\ i_{1}+...+i_{q} = n}}{\sum} a_{i_{1},...,i_{q}}X_{1}^{i_{1}}...X_{q}^{i_{q}}$. Then $\underset{1 \le k \le q}{\sum} \frac{\partial P}{\partial X_{k}}X_{k} = \underset{1 \le k \le q}{\sum}\underset{\substack{0\le i_{1},...,i_{q} \le n\\ i_{1}+...+i_{q} = n}}{\sum} a_{i_{1},...,i_{q}}.i_{k}.X_{1}^{i_{1}}...X_{q}^{i_{q}}$

$ = \underset{\substack{0\le i_{1},...,i_{q} \le n\\ i_{1}+...+i_{q} = n}}{\sum} a_{i_{1},...,i_{q}}.(i_{1}+...+i_{q}).X_{1}^{i_{1}}...X_{q}^{i_{q}}$

$ = \underset{\substack{0\le i_{1},...,i_{q} \le n\\ i_{1}+...+i_{q} = n}}{\sum} a_{i_{1},...,i_{q}}.n.X_{1}^{i_{1}}...X_{q}^{i_{q}}$

$=n.P$

Reciprocally, suppose that $R$ is multiplicatively cancellable, that $P \in R[X_{1},...,X_{q}]$ and that $\underset{1 \le k \le q}{\sum} \frac{\partial P}{\partial X_{k}}X_{k} = n.P$. Write $P=\underset{0 \le i_{1},...,i_{q} \le n}{\sum} a_{i_{1},...,i_{q}}X_{1}^{i_{1}}...X_{q}^{i_{q}}$.

Then $\underset{1 \le k \le q}{\sum} \frac{\partial P}{\partial X_{k}}X_{k} = \underset{1 \le k \le q}{\sum}\underset{0 \le i_{1},...,i_{q} \le q}{\sum} a_{i_{1},...,i_{q}}.i_{k}.X_{1}^{i_{1}}...X_{q}^{i_{q}}$

$ = \underset{0 \le i_{1},...,i_{q} \le n}{\sum} a_{i_{1},...,i_{q}}.(i_{1}+...+i_{q}).X_{1}^{i_{1}}...X_{q}^{i_{q}}$.

Thus, if $\underset{1 \le k \le q}{\sum} \frac{\partial P}{\partial X_{k}}X_{k} = n.P$, then

$\underset{0 \le i_{1},...,i_{q} \le n}{\sum} a_{i_{1},...,i_{q}}.n.X_{1}^{i_{1}}...X_{q}^{i_{q}}  = \underset{0 \le i_{1},...,i_{q} \le n}{\sum} a_{i_{1},...,i_{q}}.(i_{1}+...+i_{q}).X_{1}^{i_{1}}...X_{q}^{i_{q}}$

which is equivalent to $a_{i_{1},...,i_{q}}.(i_{1}+...+i_{q}) = a_{i_{1},...,i_{q}}.n$ for all $0 \le i_{1},...,i_{q} \le n$ which is equivalent to $a_{i_{1},...,i_{q}}.(i_{1}+...+i_{q}) = a_{i_{1},...,i_{q}}.n$ for all $0 \le i_{1},...,i_{q} \le n$ such that $a_{i_{1},...,i_{q}} \neq 0$. $R$ is multiplicatively cancellable, thus it is equivalent to $i_{1}+...+i_{q} = n$ for all $0 \le i_{1},...,i_{q} \le n$ such that $a_{i_{1},...,i_{q}} \neq 0$ which is equivalent to $P\in R_{n}[X_{1},...,X_{q}]$.
\end{proof}

[[!redirects homogeneous polynomials]]
[[!redirects Euler identity]]