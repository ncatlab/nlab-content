
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



\tableofcontents

## Overview

Here we give the [[proofs]] that are necessary to show that the definition of the [[effective topos]] does in fact give a well-defined [[category]].

In general, this follows the strategy of taking a proof that the category of partial [[setoid|setoids]] (where an object is a set equipped with a [[partial equivalence relation]] and a morphism is a respectful functional relation) is a category, and keeping track of realizers at each step. The resulting partial recursive functions will generally be closely related to the corresponding proof terms under the [[Curry-Howard correspondence]].

## Category

### Equivalence relation

We first need to show that equivalence of effective functional relations is in fact an equivalence relation.

The reflexivity property is easy, since the identity function on $\mathbb{N}$ works for $e_{f,f}$.

For symmetry, suppose that $f, g \subseteq \mathbb{N} \times X \times Y$ are two equivalent effective functional relations, and choose an equivalence tracker $e_{f,g} : \mathbb{N} \dashrightarrow \mathbb{N}$, along with trackers $d_f, c_f, \ldots, d_g, c_g, \ldots$ associated with $f$ and $g$ being effective functional relations. Now, suppose that
$$n \Vdash x \xmapsto{g} y.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv x, & \quad & n_1 & \coloneqq & d_g(n) \\
\implies \exists y'\in Y, n_2 & \Vdash & x \xmapsto{f} y', & \quad & n_2 & \coloneqq & t_f(n_1) \\
\implies n_3 & \Vdash & x \xmapsto{g} y', & \quad & n_3 & \coloneqq & e_{f,g}(n_2) \\
\implies n_4 & \Vdash & y' \equiv y, & \quad & n_4 & \coloneqq & u_g(n_3, n) \\
\implies n_5 & \Vdash & x \xmapsto{f} y, & \quad & n_5 & \coloneqq & r_f(n_2, n_1, n_4).
\end{array}
\]
Now, it is easy to see that the function which takes $n$ and follows the steps on the right to calculate $n_5$ is a partial recursive function, which satisfies the necessary property for $e_{g,f}$.

For transitivity, this is again easy: given equivalence trackers $e_{f,g}$ and $e_{g,h}$, then the composition $e_{g,h} \circ e_{f,g}$ satisfies the necessary property for $e_{f,h}$.

### Well-definedness of category operations

Here, we first show that $\operatorname{id}_X$ is an effective functional relation.

(Domain condition) Suppose
$$n \Vdash x \xmapsto{\operatorname{id}_X} y.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv y, & \quad & n_1 & \coloneqq & n \\
\implies n_2 & \Vdash & y \equiv x, & \quad & n_2 & \coloneqq & s_X(n_1) \\
\implies n_3 & \Vdash & x \equiv x, & \quad & n_3 & \coloneqq & t_X(n_1, n_2).
\end{array}
\]
Therefore, the composition $n \mapsto n_3$ on the right satisfies the necessary property for $d_{\operatorname{id}_X}$.

(Codomain condition) Similarly, if we replace the last line in the proof directly above with
$$n_3 \Vdash y \equiv y, \quad n_3 \coloneqq t_X(n_2, n_1),$$
then the composition $n \mapsto n_3$ on the right satisfies the necessary property for $c_{\operatorname{id}_X}$.

(Image uniqueness) Suppose
$$n \Vdash x \xmapsto{\operatorname{id}_X} y_1$$
and
$$n \Vdash x \xmapsto{\operatorname{id}_X} y_2.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv y_1, & \quad & n_1 & \coloneqq & n, \\
n_2 & \Vdash & x \equiv y_2, & \quad & n_2 & \coloneqq & m \\
\implies n_3 & \Vdash & y_1 \equiv x, & \quad & n_3 & \coloneqq & s_X(n_1) \\
\implies n_4 & \Vdash & y_1 \equiv y_2, & \quad & n_4 & \coloneqq & t_X(n_3, n_2).
\end{array}
\]
Therefore, the composition $(n, m) \mapsto n_4$ on the right satisfies the necessary property for $u_{\operatorname{id}_X}$.

(Totality) Suppose
$$n \Vdash x \equiv x.$$
Then
$$n \Vdash x \xmapsto{\operatorname{id}_X} x.$$
Thus, the identity function satisfies the necessary property for $t_{\operatorname{id}_X}$.

(Respectfulness) Suppose
$$n \Vdash x_1 \xmapsto{\operatorname{id}_X} y_1,$$
$$m \Vdash x_1 \equiv x_2,$$
and
$$p \Vdash y_1 \equiv y_2.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x_1 \equiv y_1, & \quad & n_1 & \coloneqq & n, \\
n_2 & \Vdash & x_2 \equiv x_1, & \quad & n_2 & \coloneqq & s_X(m) \\
\implies n_3 & \Vdash & x_2 \equiv y_1 & \quad & n_3 & \coloneqq & t_X(n_2, n_1) \\
\implies n_4 & \Vdash & x_2 \equiv y_2 & \quad & n_4 & \coloneqq & t_X(n_3, p).
\end{array}
\]
Therefore, the composition $(n, m, p) \mapsto n_4$ on the right satisfies the necessary property for $r_{\operatorname{id}_X}$.

Similarly, we need to show that the composition of two effective functional relations $f$ between $Y$ and $Z$, and $g$ between $X$ and $Y$, is again an effective functional relation between $X$ and $Z$.

(Domain condition) Suppose
$$n \Vdash x \xmapsto{f\circ g} z.$$
Then there exists $y\in Y$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \xmapsto{g} y, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y \xmapsto{f} z, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & x \equiv x, & \quad & n_3 & \coloneqq & d_g(n_1).
\end{array}
\]
Therefore, the composition $n \mapsto n_3$ on the right satisfies the necessary property for $d_{f\circ g}$.

(Codomain condition) Similarly, if we replace the last line in the proof directly above with
$$n_3 \Vdash y \equiv y, \quad n_3 \coloneqq c_f(n_2),$$
then the composition in $n \mapsto n_3$ on the right satisfies the necessary property for $c_{f\circ g}$.

(Image uniqueness) Suppose
$$n \Vdash x \xmapsto{f\circ g} z_1$$
and
$$m \Vdash x \xmapsto{f\circ g} z_2.$$
Then there exist $y_1, y_2 \in Y$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \xmapsto{g} y_1, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y_1 \xmapsto{f} z_1, & \quad & n_2 & \coloneqq & p_2(n), \\
n_3 & \Vdash & x \xmapsto{g} y_2, & \quad & n_3 & \coloneqq & p_1(m), \\
n_4 & \Vdash & y_2 \xmapsto{f} z_2, & \quad & n_4 & \coloneqq & p_2(m) \\
\implies n_5 & \Vdash & y_1 \equiv y_2, & \quad & n_5 & \coloneqq & u_g(n_1, n_3) \\
\implies n_6 & \Vdash & z_1 \equiv z_1, & \quad & n_6 & \coloneqq & d_f(n_2) \\
\implies n_7 & \Vdash & y_2 \xmapsto{f} z_1, & \quad & n_7 & \coloneqq & r_f(n_2, n_5, n_6) \\
\implies n_8 & \Vdash & z_1 \equiv z_2, & \quad & n_8 & \coloneqq & u_f(n_4, n_7).
\end{array}
\]
Therefore, the composition $(n, m) \mapsto n_8$ on the right satisfies the necessary property for $u_{f\circ g}$.

(Totality) Suppose
$$n \Vdash x \equiv x.$$
Then there exists $y\in Y$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \xmapsto{g} y, & \quad & n_1 & \coloneqq & t_g(n) \\
\implies n_2 & \Vdash & y \equiv y, & \quad & n_2 & \coloneqq & c_g(n_1).
\end{array}
\]
It follows that there exists $z\in Z$ such that
\[
\begin{array}{rclcrcl}
n_3 & \Vdash & y \xmapsto{f} z, & \quad & n_3 & \coloneqq & t_f(n_2) \\
\implies n_4 & \Vdash & x \xmapsto{f\circ g} z, & \quad & n_4 & \coloneqq & \langle n_1, n_3.
\end{array}
\]
Therefore, the composition $n \mapsto n_4$ on the right satisfies the necessary property for $t_{f\circ g}$.

(Respectfulness) Suppose
$$n \Vdash x_1 \xmapsto{f\circ g} z_1,$$
$$m \Vdash x_1 \equiv x_2,$$
and
$$p \Vdash z_1 \equiv z_2.$$
Then there exists $y\in Y$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x_1 \xmapsto{g} y, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y \xmapsto{f} z_1, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & y \equiv y, & \quad & n_3 & \coloneqq & c_g(n_1) \\
\implies n_4 & \Vdash & x_2 \xmapsto{g} y, & \quad & n_4 & \coloneqq & r_g(n_1, m, n_3) \\
\implies n_5 & \Vdash & y \xmapsto{f} z_2, & \quad & n_5 & \coloneqq & r_f(n_2, n_3, p) \\
\implies n_6 & \Vdash & x_2 \xmapsto{f\circ g} z_2, & \quad & n_6 & \coloneqq & \langle n_4, n_5 \rangle.
\end{array}
\]
Therefore, the composition $(n, m, p) \mapsto n_6$ on the right satisfies the necessary property for $r_{f\circ g}$.

Finally, we show that composition is well-defined up to equivalence of effective functional relations. Thus, suppose we have equivalence trackers $e_{g_1, g_2}$ and $e_{f_1, f_2}$, where $f_i$ are effective functional relations between $Y$ and $Z$, and $g_i$ are effective functional relations between $X$ and $Y$. Then whenever
$$n \Vdash x \xmapsto{f_1 \circ g_1} z,$$
then there exists $y\in Y$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \xmapsto{g_1} y, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y \xmapsto{f_1} z, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & x \xmapsto{g_2} y, & \quad & n_3 & \coloneqq & e_{g_1, g_2}(n_1) \\
\implies n_4 & \Vdash & y \xmapsto{f_2} z, & \quad & n_4 & \coloneqq & e_{f_1, f_2}(n_2) \\
\implies n_5 & \Vdash & x \xmapsto{f_2 \circ g_2} z, & \quad & n_5 & \coloneqq & \langle n_3, n_4 \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_5$ on the right satisfies the necessary property for $e_{f_1 \circ g_1, f_2 \circ g_2}$.

### Identity properties

In order to establish the identity properties of the category, it suffices to show that for $f$ an effective functional relation between $X$ and $Y$, $\operatorname{id}_Y \circ f$ and $f \circ \operatorname{id}_X$ are both equivalent to $f$. Thus, suppose that
$$n \Vdash x \xmapsto{f} y.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & y \equiv y, & \quad & n_1 & \coloneqq & c_f(n) \\
\implies n_2 & \Vdash & y \xmapsto{\operatorname{id}_Y} y, & \quad & n_2 & \coloneqq & n_1 \\
\implies n_3 & \Vdash & x \xmapsto{\operatorname{id}_Y \circ f} y, & \quad & n_2 & \coloneqq & \langle n, n_2 \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_3$ on the right satisfies the necessary property for $e_{f, \operatorname{id}_Y \circ f}$.

Similarly,
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv x, & \quad & n_1 & \coloneqq & d_f(n) \\
\implies n_2 & \Vdash & x \xmapsto{\operatorname{id}_X} x, & \quad & n_2 & \coloneqq & n_1 \\
\implies n_3 & \Vdash & x \xmapsto{f \circ \operatorname{id}_X} y, & \quad & n_3 & \coloneqq & \langle n_2, n \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_3$ on the right satisfies the necessary property for $e_{f, f \circ \operatorname{id}_X}$.

### Associativity of composition

In order to establish associativity of composition in the category, it suffices to show that for $f$ an effective functional relation between $Z$ and $W$, $g$ an effective functional relation between $Y$ and $Z$, and $h$ an effective functional relation between $X$ and $Y$, then $f \circ (g\circ h)$ is equivalent to $(f\circ g) \circ h$. Thus, suppose that
$$n \Vdash x \xmapsto{f\circ (g\circ h)} w.$$
Then there exists $z\in Z$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \xmapsto{g\circ h} z, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & z \xmapsto{f} w, & \quad & n_2 & \coloneqq & p_2(n).
\end{array}
\]
By the $g\circ h$ condition, we can also find $y\in Y$ such that
\[
\begin{array}{rclcrcl}
n_3 & \Vdash & x \xmapsto{h} y, & \quad & n_3 & \coloneqq & p_1(n_1), \\
n_4 & \Vdash & y \xmapsto{g} z, & \quad & n_4 & \coloneqq & p_2(n_1) \\
\implies n_5 & \Vdash & y \xmapsto{f\circ g} w, & \quad & n_5 & \coloneqq & \langle n_4, n_2 \rangle \\
\implies n_6 & \Vdash & x \xmapsto{(f\circ g)\circ h} w, & \quad & n_6 & \coloneqq & \langle n_3, n_5 \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_6$ on the right satisfies the necessary property for $e_{f \circ (g \circ h), (f\circ g) \circ h}$. (This composition can be described as the function $\langle \langle a, b \rangle, c \rangle \mapsto \langle a, \langle b, c \rangle \rangle$.)

## Finite completeness

### Terminal object

We define the terminal object $1$ to have underlying set $\{ * \}$ and effective PER $\mathbb{N} \times \{ * \} \times \{ * \}$. For $s_1 : \mathbb{N} \dashrightarrow \mathbb{N}$ and $t_1 : \mathbb{N}^2 \dashrightarrow \mathbb{N}$, we can in fact choose any full recursive functions.

Given any object $X$, we can define an effective functional relation $!_X$ between $X$ and $1$ by
$$!_X \coloneqq \{ (n, x, *) \mid n \Vdash x \equiv x \}.$$
Checking the required properties is easy:

(Domain condition) The identity function $\mathbb{N} \to \mathbb{N}$ satisfies the required condition for $d_{!_X}$.

(Codomain condition) Any full recursive function $\mathbb{N} \to \mathbb{N}$ satisfies the required condition for $c_{!_X}$.

(Image uniqueness) Any full recursive function $\mathbb{N}^2 \to \mathbb{N}$ satisfies the required condition for $u_{!_X}$.

(Totality condition) The identity function $\mathbb{N} \to \mathbb{N}$ satisfies the required condition for $t_{!_X}$.

(Respectfulness condition) Suppose we have
$$n \Vdash x_1 \xmapsto{!_X} y_1,$$
$$m \Vdash x_1 \equiv x_2,$$
and
$$p \Vdash y_1 \equiv y_2.$$
Then certainly $y_2 = *$, and
$$t_X(s_X(m), m) \Vdash x_2 \equiv x_2,$$
so
$$t_X(s_X(m), m) \Vdash x_2 \xmapsto{!_X} *.$$
Therefore, the function $(n, m, p) \mapsto t_X(s_X(m), m)$ satisfies the required condition for $r_{!_X}$.

Now suppose we have any other effective functional relation $f$ between $X$ and $1$. Then whenever
$$n \Vdash x \xmapsto{f} y,$$
we have $y = *$, and
$$d_f(n) \Vdash x \equiv x,$$
so
$$d_f(n) \Vdash x \xmapsto{!_X} *.$$
Therefore, $d_f : \mathbb{N} \dashrightarrow \mathbb{N}$ satisfies the required condition for $e_{f, !_X}$, showing that $f$ is equivalent to $!_X$.
