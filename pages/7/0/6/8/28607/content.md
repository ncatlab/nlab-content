
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

### Binary products

Given two objects $X, Y$, we will define their binary product to have underlying set $X\times Y$, and effective PER
$$\{ (\langle n, m \rangle, (x_1, y_1), (x_2, y_2) \mid (n \Vdash x_1 \equiv x_2) \wedge (m \Vdash y_1 \equiv y_2). \}$$
For symmetry, we can use the function
$$s_{X\times Y} : \langle n, m \rangle \mapsto \langle s_X(n), s_Y(m) \rangle,$$
and for transitivity, we can use the function
$$t_{X\times Y} : (\langle n, m \rangle, \langle n', m' \rangle) \mapsto \langle t_X(n, n'), t_Y(m, m').$$

To define the first projection, we will use the effective functional relation defined by
$$\pi_1 \coloneqq \{ (\langle n, m \rangle, (x, y), x') \mid (n \Vdash x \equiv x') \wedge (m \Vdash y \equiv y) \}.$$
To check the required properties:

(Domain condition) Suppose
$$n \Vdash (x, y) \xmapsto{\pi_1} x'.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv x', & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y \equiv y, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & x' \equiv x, & \quad & n_3 & \coloneqq & s_X(n_1) \\
\implies n_4 & \Vdash & x \equiv x, & \quad & n_4 & \coloneqq & t_X(n_1, n_3) \\
\implies n_5 & \Vdash & (x, y) \equiv (x, y), & \quad & n_5 & \coloneqq & \langle n_4, n_2 \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_5$ on the right satisfies the required condition for $d_{\pi_1}$.

(Codomain condition) Suppose
$$n \Vdash (x, y) \xmapsto{\pi_1} x'.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv x', & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y \equiv y, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & x' \equiv x, & \quad & n_3 & \coloneqq & s_X(n_1) \\
\implies n_4 & \Vdash & x' \equiv x', & \quad & n_4 & \coloneqq & t_X(n_3, n_1).
\end{array}
\]
Therefore, the composition $n \mapsto n_4$ on the right satisfies the required condition for $c_{\pi_1}$.

(Uniqueness of images) Suppose
$$n \Vdash (x, y) \xmapsto{\pi_1} x_1'$$
and
$$m \Vdash (x, y) \xmapsto{\pi_1} x_2'.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv x_1', & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y \equiv y, & \quad & n_2 & \coloneqq & p_2(n), \\
n_3 & \Vdash & x \equiv x_2', & \quad & n_1 & \coloneqq & p_1(m), \\
n_4 & \Vdash & y \equiv y, & \quad & n_4 & \coloneqq & p_2(m) \\
\implies n_5 & \Vdash & x_1' \equiv x, & \quad & n_5 & \coloneqq & s_X(n_1) \\
\implies n_6 & \Vdash & x_1' \equiv x_2', & \quad & n_6 & \coloneqq & t_X(n_5, n_3).
\end{array}
\]
Therefore, the composition $(n, m) \mapsto n_6$ on the right satisfies the required condition for $u_{\pi_1}$.

(Totality) Suppose
$$n \Vdash (x, y) \equiv (x, y).$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x \equiv x, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y \equiv y, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & (x, y) \xmapsto{\pi_1} x, & \quad & n_3 & \coloneqq & \langle n_1, n_2 \rangle = n.
\end{array}
\]
Therefore, the identity function satisfies the required condition for $t_{\pi_1}$.

(Respectfulness) Suppose
$$n \Vdash (x_1, y_1) \xmapsto{\pi_1} x_1',$$
$$m \Vdash (x_1, y_1) \equiv (x_2, y_2),$$
and
$$p \Vdash x_1' \equiv x_2'.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & x_1 \equiv x_1', & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & y_1 \equiv y_1, & \quad & n_2 & \coloneqq & p_2(n), \\
n_3 & \Vdash & x_1 \equiv x_2, & \quad & n_3 & \coloneqq & p_1(m), \\
n_4 & \Vdash & y_1 \equiv y_2, & \quad & n_4 & \coloneqq & p_2(m) \\
\implies n_5 & \Vdash & x_2 \equiv x_1, & \quad & n_5 & \coloneqq & s_X(n_3) \\
\implies n_6 & \Vdash & x_2 \equiv x_1', & \quad & n_6 & \coloneqq & t_X(n_5, n_1) \\
\implies n_7 & \Vdash & x_2 \equiv x_2', & \quad & n_7 & \coloneqq & t_X(n_6, p) \\
\implies n_8 & \Vdash & y_2 \equiv y_1, & \quad & n_8 & \coloneqq & s_Y(n_4) \\
\implies n_9 & \Vdash & y_2 \equiv y_2, & \quad & n_9 & \coloneqq & t_Y(n_8, n_4) \\
\implies n_{10} & \Vdash & (x_2, y_2) \xmapsto{\pi_1} x_2', & \quad & n_{10} & \coloneqq & \langle n_7, n_9 \rangle.
\end{array}
\]
Therefore, the composition $(n, m, p) \mapsto n_{10}$ on the right satisfies the required condition for $r_{\pi_1}$.

Similarly, we will let $\pi_2$ be the effective functional relation between $X\times Y$ and $Y$ defined by
$$\pi_2 \coloneqq \{ (\langle n, m \rangle, (x, y), y') \mid (n \Vdash x \equiv x) \wedge (m \Vdash y \equiv y') \}.$$
The proof that this is an effective functional relation is similar to the proof for $\pi_1$.

Now, suppose we have two effective functional relations, $f$ between $T$ and $X$, and $g$ between $T$ and $Y$. We will then let $(f,g)$ be the effective functional relation defined by
$$(f, g) \coloneqq \{ (\langle n, m \rangle, t, (x, y)) \mid (n \Vdash t \xmapsto{f} x) \wedge (m \Vdash t \xmapsto{g} y) \}.$$
To check this does indeed give an effective functional relation:

(Domain condition) Suppose
$$n \Vdash t \xmapsto{(f,g)} (x,y).$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & t \xmapsto{f} x, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & t \xmapsto{f} y, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & t \equiv t, & \quad & n_3 & \coloneqq & d_f(n_1).
\end{array}
\]
Therefore, the composition $d_f \circ p_1$ satisfies the required condition for $d_{(f,g)}$.

(Codomain condition) Suppose
$$n \Vdash t \xmapsto{(f,g)} (x,y).$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & t \xmapsto{f} x, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & t \xmapsto{f} y, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & x \equiv x, & \quad & n_3 & \coloneqq c_f(n_1) \\
\implies n_4 & \Vdash & y \equiv y, & \quad & n_4 & \coloneqq c_g(n_2) \\
\implies n_5 & \Vdash & (x, y) \equiv (x, y), & \quad & n_5 & \coloneqq \langle n_3, n_4 \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_5$ on the right satisfies the required condition for $c_({f,g})$.

(Image uniqueness) Suppose
$$n \Vdash t \xmapsto{(f,g)} (x_1, y_1)$$
and
$$m \Vdash t \xmapsto{(f,g)} (x_2, y_2).$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & t \xmapsto{f} x_1, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & t \xmapsto{g} y_1, & \quad & n_2 & \coloneqq & p_2(n), \\
n_3 & \Vdash & t \xmapsto{f} x_2, & \quad & n_3 & \coloneqq & p_1(m), \\
n_4 & \Vdash & t \xmapsto{g} y_2, & \quad & n_4 & \coloneqq & p_2(m) \\
\implies n_5 & \Vdash & x_1 \equiv x_2 & \quad & n_5 & \coloneqq & u_f(n_1, n_3) \\
\implies n_6 & \Vdash & y_1 \equiv y_2 & \quad & n_6 & \coloneqq & u_g(n_2, n_4) \\
\implies n_7 & \Vdash & (x_1, y_1) \equiv (x_2, y_2) & \quad & n_7 & \coloneqq & \langle n_5, n_6 \rangle.
\end{array}
\]
Therefore, the composition $(n, m) \mapsto n_7$ on the right satisfies the required condition for $u_{(f,g)}$.

(Totality) Suppose
$$n \Vdash t \equiv t.$$
Then
\[
\begin{array}{rclcrcl}
\exists x\in X, n_1 & \Vdash & t \xmapsto{f} x, & \quad & n_1 & \coloneqq & t_f(n), \\
\exists y\in Y, n_2 & \Vdash & t \xmapsto{g} y, & \quad & n_2 & \coloneqq & t_g(n) \\
\implies n_3 & \Vdash & t \xmapsto{(f,g)} (x,y), & \quad & n_3 & \coloneqq & \langle n_1, n_2 \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_3$ on the right satisfies the required condition for $t_{(f,g)}$.

(Respectfulness) Suppose
$$n \Vdash t_1 \xmapsto{(f,g)} (x_1, y_1),$$
$$m \Vdash t_1 \equiv t_2,$$
and
$$p \Vdash (x_1, y_1) \equiv (x_2, y_2).$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & t_1 \xmapsto{f} x_1 & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & t_1 \xmapsto{g} y_1 & \quad & n_2 & \coloneqq & p_2(n), \\
n_3 & \Vdash & x_1 \equiv x_2 & \quad & n_3 & \coloneqq & p_1(p), \\
n_4 & \Vdash & y_1 \equiv y_2 & \quad & n_4 & \coloneqq & p_2(p) \\
\implies n_5 & \Vdash & t_2 \xmapsto{f} x_2 & \quad & n_5 & \coloneqq & r_f(n_1, m, n_3) \\
\implies n_6 & \Vdash & t_2 \xmapsto{g} y_2 & \quad & n_6 & \coloneqq & r_f(n_2, m, n_4) \\
\implies n_7 & \Vdash & t_2 \xmapsto{(f,g)} (x_2, y_2) & \quad & n_7 & \coloneqq & \langle n_5, n_6 \rangle.
\end{array}
\]
Therefore, the composition $(n, m, p) \mapsto n_7$ on the right satisfies the required condition for $r_{(f,g)}$.

We now claim that $\pi_1 \circ (f, g)$ is equivalent to $f$. Thus, suppose that
$$n \Vdash t \xmapsto{\pi_1 \circ (f, g)} x.$$
Then there exists $(x', y') \in X\times Y$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & t \xmapsto{(f,g)} (x', y'), & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & (x', y') \xmapsto{\pi_1} x, & \quad & n_2 & \coloneqq & p_2(n) \\
\implies n_3 & \Vdash & t \xmapsto{f} x', & \quad & n_3 & \coloneqq & p_1(n_1), \\
n_4 & \Vdash & t \xmapsto{g} y', & \quad & n_4 & \coloneqq & p_2(n_1), \\
n_5 & \Vdash & x' \equiv x, & \quad & n_5 & \coloneqq & p_1(n_2), \\
n_6 & \Vdash & y' \equiv y', & \quad & n_6 & \coloneqq & p_2(n_2) \\
\implies n_7 & \Vdash & t \equiv t, & \quad & n_7 & \coloneqq & d_f(n_3) \\
\implies n_8 & \Vdash & t \xmapsto{f} x, & \quad & n_8 & \coloneqq & r_f(n_3, n_7, n_5).
\end{array}
\]
Therefore, the composition $n \mapsto n_8$ on the right satisfies the required condition for $e_{\pi_1 \circ (f, g), f}$. The proof that $\pi_2 \circ (f, g)$ is equivalent to $g$ is similar,

Finally, to establish the uniqueness of $(f, g)$ up to equivalence, it suffices to show that the pair of morphisms $[\pi_1], [\pi_2]$ is [[jointly epimorphic family|jointly monomorphic]]. Thus, suppose we have two effective functional relations $a, b$ between $T$ and $X\times Y$ such that $\pi_i \circ a$ is equivalent to $\pi_i \circ b$, $i \in \{1,2\}$. Now suppose that
$$n \Vdash t \xmapsto{a} (x, y).$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & (x, y) \equiv (x, y), & \quad & n_1 & \coloneqq & c_a(n) \\
\implies n_2 & \Vdash & x \equiv x, & \quad & n_2 & \coloneqq & p_1(n_1), \\
n_3 & \Vdash & y \equiv y, & \quad & n_3 & \coloneqq & p_2(n_1) \\
\implies n_4 & \Vdash & (x, y) \xmapsto{\pi_1} x, & \quad & n_4 & \coloneqq & \langle n_2, n_3 \rangle \\
\implies n_5 & \Vdash & t \xmapsto{\pi_1 \circ a} x, & \quad & n_5 & \coloneqq & \langle n, n_5 \rangle \\
\implies n_6 & \Vdash & t \xmapsto{\pi_1 \circ b} x, & \quad & n_6 & \coloneqq & e_{\pi_1 \circ a, \pi_1 \circ b}(n_5) \\
\implies \exists (x', y') \in X\times Y, n_7 & \Vdash & t \xmapsto{b} (x', y') & \quad & n_7 & \coloneqq & p_1(n_5), \\
n_8 & \Vdash & (x', y') \xmapsto{\pi_1} x, & \quad & n_8 & \coloneqq & p_2(n_5) \\
\implies n_9 & \Vdash & x' \equiv x, & \quad & n_9 & \coloneqq & p_1(n_8), \\
n_{10} & \Vdash & y' \equiv y', & \quad & n_{10} & \coloneqq & p_2(n_8) \\
\implies n_{11} & \Vdash & (x, y) \xmapsto{\pi_2} y, & \quad & n_{11} & \coloneqq & \langle n_2, n_3 \rangle \\
\implies n_{12} & \Vdash & t \xmapsto{\pi_2 \circ a} y, & \quad & n_{12} & \coloneqq & \langle n, n_{11} \rangle \\
\implies n_{13} & \Vdash & t \xmapsto{\pi_2 \circ b} y, & \quad & n_{13} & \coloneqq & e_{\pi_2\circ a, \pi_2\circ b}(n_{12}) \\
\implies \exists (x'', y'') \in X\times Y, n_{14} & \Vdash & t \xmapsto{b} (x'', y''), & \quad & n_{14} & \coloneqq & p_1(n_{13}), \\
n_{15} & \Vdash & (x'', y'') \xmapsto{\pi_2} y, & \quad & n_{15} & \coloneqq & p_2(n_{13}) \\
\implies n_{16} & \Vdash & x'' \equiv x'', & \quad & n_{16} & \coloneqq & p_1(n_{15}), \\
n_{17} & \Vdash & y'' \equiv y, & \quad & n_{17} & \coloneqq & p_2(n_{15}) \\
\implies n_{18} & \Vdash & (x', y') \equiv (x'', y''), & \quad & n_{18} & \coloneqq & u_b(n_7, n_{13}) \\
\implies n_{19} & \Vdash & x' \equiv x'', & \quad & n_{19} & \coloneqq & p_1(n_{18}), \\
n_{20} & \Vdash & y' \equiv y'', & \quad & n_{20} & \coloneqq & p_2(n_{18}) \\
\implies n_{21} & \Vdash & y' \equiv y, & \quad & n_{21} & \coloneqq & t_Y(n_{20}, n_{17}) \\
\implies n_{22} & \Vdash & t \equiv t, & \quad & n_{22} & \coloneqq & d_a(n) \\
\implies n_{23} & \Vdash & (x', y') \equiv (x, y), & \quad & n_{23} & \coloneqq & \langle n_9, n_{21} \rangle \\
\implies n_{24} & \Vdash & t \xmapsto{b} (x, y), & \quad & n_{24} & \coloneqq & r_b(n_7, n_{22}, n_{23}).
\end{array}
\]
Therefore, the composition $n \mapsto n_{24}$ on the right satisfies the required condition for $e_{a,b}$.

### Equalizers

Suppose we have two effective functional relations $f, g$ between $X$ and $Y$. We can then define the equalizer $E$ to have underlying set $X \times Y$, and effective PER where we will say
$$\langle n, m, p, q \rangle \Vdash (x_1, y_1) \equiv (x_2, y_2)$$
if and only if
$$n \Vdash x_1 \xmapsto{f} y_1,$$
$$m \Vdash x_1 \xmapsto{g} y_1,$$
$$p \Vdash x_1 \equiv x_2,$$
and
$$q \Vdash y_1 \equiv y_2.$$
(Here, $\langle n, m, p, q \rangle$ will be syntactic sugar for $\langle \langle \langle n, m \rangle, p \rangle, q \rangle$, and we will define corresponding projections $p_{i / 4} : \mathbb{N} \to \mathbb{N}$ for $1\le i\le 4$. We will use similar notations for other arities of tuples below.)

To construct the required symmetry tracker, we can use the function which transports $n$ and $m$ to $(x_2, y_2)$ using respectfulness of $f$ and $g$, and applies symmetry to $p$ and $q$. Similarly, for the transitivity tracker, we preserve the $n$ and $m$ components of the first input, and apply transitivity to the $p$ and $q$ components.

For the inclusion map, we will define an effective functional relation $i$ between $E$ and $X$ where
$$\langle n, m, p \rangle \Vdash (x, y) \xmapsto{i} x'$$
if and only if
$$n \Vdash x \xmapsto{f} y,$$
$$m \Vdash x \xmapsto{g} y,$$
and
$$p \Vdash x \equiv x'.$$

(Domain condition) Suppose
$$\langle n, m, p \rangle \Vdash (x, y) \xmapsto{i} x'.$$
Then
\[
\begin{array}{rclcrcl}
n & \Vdash & x \xmapsto{f} y, & & & & \\
m & \Vdash & x \xmapsto{g} y, & & & & \\
p & \Vdash & x \equiv x' & & & & \\
\implies n_1 & \Vdash & x \equiv x, & \quad & n_1 & \coloneqq & d_f(n) \\
\implies n_2 & \Vdash & y \equiv y, & \quad & n_2 &
\coloneqq & c_f(n) \\
\implies n_3 & \Vdash & (x, y) \equiv (x, y), & \quad & n_3 & \coloneqq & \langle n, m, n_1, n_2 \rangle.
\end{array}
\]
Therefore, the composition $\langle n, m, p \rangle \mapsto n_3$ on the right satisfies the required condition for $d_i$.

(Codomain condition) Suppose
$$\langle n, m, p \rangle \Vdash (x, y) \xmapsto{i} x'.$$ Then
\[
\begin{array}{rclcrcl}
n & \Vdash & x \xmapsto{f} y, & & & & \\
m & \Vdash & x \xmapsto{g} y, & & & & \\
p & \Vdash & x \equiv x' & & & & \\
\implies n_1 & \Vdash & x' \equiv x, & \quad & n_1 & \coloneqq & s_X(p) \\
\implies n_2 & \Vdash & x' \equiv x', & \quad & n_2 & \coloneqq & t_X(n_1, p).
\end{array}
\]
Therefore, the composition $\langle n, m, p \rangle \mapsto n_2$ on the right satisfies the required condition for $c_i$.

(Image uniqueness) Suppose
$$\langle n, m, p \rangle \Vdash (x, y) \xmapsto{i} x_1'$$
and
$$\langle n', m', p' \rangle \Vdash (x, y) \xmapsto{i} x_2'.$$
Then
\[
\begin{array}{rclcrcl}
n & \Vdash & x \xmapsto{f} y, & & & & \\
m & \Vdash & x \xmapsto{g} y, & & & & \\
p & \Vdash & x \equiv x', & & & & \\
n' & \Vdash & x \xmapsto{f} y, & & & & \\
m' & \Vdash & x \xmapsto{g} y, & & & & \\
p' & \Vdash & x \equiv x'' & & & & \\
\implies n_1 & \Vdash & x' \equiv x, & \quad & n_1 & \coloneqq & s_X(p) \\
\implies n_2 & \Vdash & x' \equiv x'', & \quad & n_2 & \coloneqq & t_X(n_1, p').
\end{array}
\]
Therefore, the composition $(\langle n, m, p \rangle, \langle n', m', p' \rangle) \mapsto n_2$ on the right satisfies the required condition for $u_i$.

(Totality) Suppose
$$\langle n, m, p, q \rangle \Vdash (x, y) \equiv (x, y).$$
Then
\[
\begin{array}{rclcrcl}
n & \Vdash & x \xmapsto{f} y, & & & & \\
m & \Vdash & x \xmapsto{g} y, & & & & \\
p & \Vdash & x \equiv x, & & & & \\
q & \Vdash & y \equiv y & & & & \\
\implies n_1 & \Vdash & (x, y) \xmapsto{i} x, & \quad & n_1 & \coloneqq & \langle n, m, p \rangle.
\end{array}
\]
Therefore, $\langle n, m, p, q \rangle \mapsto \langle n, m, p \rangle$ satisfies the required condition for $t_i$.

(Respectfulness) Suppose
$$\langle n, m, p \rangle \Vdash (x_1, y_1) \xmapsto{i} x_1',$$
$$\langle n', m', p', q' \rangle \Vdash (x_1, y_1) \equiv (x_2, y_2),$$
and
$$n'' \Vdash x_1' \equiv x_2'.$$
Then
\[
\begin{array}{rclcrcl}
n & \Vdash & x_1 \xmapsto{f} y_1, & & & & \\
m & \Vdash & x_1 \xmapsto{g} y_1, & & & & \\
p & \Vdash & x_1 \equiv x_1', & & & & \\
n' & \Vdash & x_1 \xmapsto{f} y_1, & & & & \\
m' & \Vdash & x_1 \xmapsto{g} y_1, & & & & \\
p' & \Vdash & x_1 \equiv x_2, & & & & \\
q' & \Vdash & y_1 \equiv y_2 & & & & \\
\implies n_1 & \Vdash & x_2 \xmapsto{f} y_2, & \quad & n_1 & \coloneqq & r_f(n, p', q') \\
\implies n_2 & \Vdash & x_2 \xmapsto{g} y_2, & \quad & n_2 & \coloneqq & r_g(m, p', q') \\
\implies n_3 & \Vdash & x_2 \equiv x_1, & \quad & n_3 & \coloneqq & s_X(p') \\
\implies n_4 & \Vdash & x_2 \equiv x_1', & \quad & n_4 & \coloneqq & t_X(n_3, p) \\
\implies n_5 & \Vdash & x_2 \equiv x_2', & \quad & n_5 & \coloneqq & t_X(n_4, n'') \\
\implies n_6 & \Vdash & (x_2, y_2) \xmapsto{i} x_2', & \quad & n_6 & \coloneqq & \langle n_1, n_2, n_5 \rangle.
\end{array}
\]
Therefore, the composition $(\langle n, m, p \rangle, \langle n', m', p', q' \rangle, n'') \mapsto n_6$ on the right satisfies the required condition for $r_i$.

We first claim that $f\circ i$ is equivalent to $g\circ i$. Thus, suppose
$$\langle n, m \rangle \Vdash (x, y) \xmapsto{f\circ i} y'.$$
Then there exists $x' \in X$ such that
\[
\begin{array}{rclcrcl}
n & \Vdash & (x, y) \xmapsto{i} x', & & & & \\
m & \Vdash & x' \xmapsto{f} y' & & & & \\
\implies n_1 & \Vdash & x \xmapsto{f} y, & \quad & n_1 & \coloneqq & p_{1/3}(n), \\
n_2 & \Vdash & x \xmapsto{g} y, & \quad & n_2 & \coloneqq & p_{2/3}(n), \\
n_3 & \Vdash & x \equiv x', & \quad & n_3 & \coloneqq & p_{3/3}(n) \\
\implies n_4 & \Vdash & y \equiv y, & \quad & n_4 & \coloneqq & c_f(n_1) \\
\implies n_5 & \Vdash & x' \xmapsto{f} y, & \quad & n_5 & \coloneqq & r_f(n_1, n_3, n_4) \\
\implies n_6 & \Vdash & y \equiv y', & \quad & n_6 & \coloneqq & u_f(m, n_5) \\
\implies n_7 & \Vdash & x' \xmapsto{g} y', & \quad & n_7 & \coloneqq & r_f(n_2, n_3, n_6) \\
\implies n_8 & \Vdash & (x, y) \xmapsto{g\circ i} y', & \quad & n_8 & \coloneqq & \langle n, n_7 \rangle.
\end{array}
\]
Therefore, the composition $\langle n, m \rangle \mapsto n_8$ on the right satisfies the required condition for $e_{f\circ i, g\circ i}$.

Now, suppose we have an effective functional relation $h$ between $T$ and $X$ such that $f\circ h$ is equivalent to $g\circ h$; we then want to show $h$ factors through $i$. To this end, we will define an effective functional relation $\tilde h$ between $T$ and $E$ where
$$\langle n, m \rangle \Vdash t \xmapsto{\tilde h} (x, y)$$
if and only if
$$n \Vdash t \xmapsto{h} x$$
and
$$m \Vdash x \xmapsto{f} y.$$

The following intermediate result will be useful several times:
\begin{lemma}
There is a partial recursive function $\varphi : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash t \xmapsto{h} x$$
and
$$m \Vdash x \xmapsto{f} y,$$
then $\varphi(n, m)$ is defined and
$$\varphi(n, m) \Vdash x \xmapsto{g} y.$$
\end{lemma}
\begin{proof}
We have
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & t \xmapsto{f\circ h} y, & \quad & n_1 & \coloneqq & \langle n, m \rangle \\
\implies n_2 & \Vdash & t \xmapsto{g\circ h} y, & \quad & n_2 & \coloneqq & e_{f\circ h, g\circ h}(n_1) \\
\implies \exists x'\in X, n_3 & \Vdash & t \xmapsto{h} x', & \quad & n_3 & \coloneqq & p_1(n_2), \\
n_4 & \Vdash & x' \xmapsto{g} y, & \quad & n_4 & \coloneqq & p_2(n_2) \\
\implies n_5 & \Vdash & x' \equiv x, & \quad & n_5 & \coloneqq & u_h(n_4, n) \\
\implies n_6 & \Vdash & y \equiv y, & \quad & n_6 & \coloneqq & c_f(m) \\
\implies n_7 & \Vdash & x \xmapsto{g} y, & \quad & n_7 & \coloneqq & r_g(n_4, n_5, n_6).
\end{array}
\]
Therefore, the composition $(n, m) \mapsto n_7$ on the right satisfies the required condition for $\varphi$.
\end{proof}

(Domain condition) Suppose
$$\langle n, m \rangle \Vdash t \xmapsto{\tilde h} (x, y).$$
Then
$$n \Vdash t \xmapsto{h} x$$
so
$$d_h(n) \Vdash t \equiv t.$$
Thus, $\langle n, m \rangle \mapsto d_h(n)$ satisfies the required condition for $d_{\tilde h}$.

(Codomain condition) Suppose
$$\langle n, m \rangle \Vdash t \xmapsto{\tilde h} (x, y).$$
Then
\[
\begin{array}{rclcrcl}
n & \Vdash & t \xmapsto{h} x, & & & & \\
m & \Vdash & x \xmapsto{f} y & & & & \\
\implies n_1 & \Vdash & x \xmapsto{g} y, & \quad & n_1 & \coloneqq & \varphi(n, m) \\
\implies n_2 & \Vdash & x \equiv x, & \quad & n_2 & \coloneqq & c_h(n) \\
\implies n_3 & \Vdash & y \equiv y, & \quad & n_3 & \coloneqq & c_f(m) \\
\implies n_4 & \Vdash & (x, y) \equiv (x, y), & \quad & n_4 & \coloneqq & \langle m, n_1, n_2, n_3 \rangle.
\end{array}
\]
Therefore, the composition $\langle n, m \rangle \mapsto n_4$ on the right satisfies the required condition for $c_{\tilde h}$.

(Image uniqueness) Suppose
$$\langle n, m \rangle \Vdash t \xmapsto{\tilde h} (x, y)$$
and
$$\langle n', m' \rangle \Vdash t \xmapsto{\tilde h} (x', y').$$
Then
\[
\begin{array}{rclcrcl}
n & \Vdash & t \xmapsto{h} x, & & & & \\
m & \Vdash & x \xmapsto{f} y, & & & & \\
n' & \Vdash & t \xmapsto{h} x', & & & & \\
m' & \Vdash & x' \xmapsto{f} y' & & & & \\
\implies n_1 & \Vdash & x \xmapsto{g} y, & \quad & n_1 & \coloneqq & \varphi(n, m) \\
\implies n_2 & \Vdash & x \equiv x', & \quad & n_2 & \coloneqq & u_h(n, n') \\
\implies n_3 & \Vdash & y' \equiv y', & \quad & n_3 & \coloneqq & c_f(m') \\
\implies n_4 & \Vdash & x' \xmapsto{f} y, & \quad & n_4 & \coloneqq & r_f(m, n_2, n_3) \\
\implies n_5 & \Vdash & y \equiv y', & \quad & n_5 & \coloneqq & u_f(n_4, m') \\
\implies n_6 & \Vdash & (x, y) \equiv (x', y'), & \quad & n_6 & \coloneqq & \langle m, n_1, n_2, n_5 \rangle.
\end{array}
\]
Therefore, the composition $(\langle n, m \rangle, \langle n', m' \rangle) \mapsto n_5$ on the right satisfies the required condition for $u_{\tilde h}$.

(Totality) Suppose
$$n \Vdash t \equiv t.$$
Then
\[
\begin{array}{rclcrcl}
\exists x\in X, n_1 & \Vdash & t \xmapsto{h} x, & \quad & n_1 & \coloneqq & t_h(n) \\
\implies \exists y\in Y, n_2 & \Vdash & x \xmapsto{f} y, & \quad & n_2 & \coloneqq & t_f(n_1) \\
\implies n_3 & \Vdash & t \xmapsto{\tilde h} (x, y), & \quad & n_3 & \coloneqq & \langle n_1, n_2 \rangle.
\end{array}
\]
Therefore, the composition $n \mapsto n_3$ on the right satisfies the required condition for $t_{\tilde h}$.

(Respectfulness) Suppose
$$n \Vdash t \xmapsto{\tilde h} (x, y),$$
$$m \Vdash t \equiv t',$$
and
$$p \Vdash (x, y) \equiv (x', y').$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & t \xmapsto{h} x, & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & x \xmapsto{f} y, & \quad & n_2 & \coloneqq & p_2(n), \\
n_3 & \Vdash & x \xmapsto{f} y, & \quad & n_3 & \coloneqq & p_{1/4}(p), \\
n_4 & \Vdash & x \xmapsto{g} y, & \quad & n_4 & \coloneqq & p_{2/4}(p), \\
n_5 & \Vdash & x \equiv x', & \quad & n_5 & \coloneqq & p_{3/4}(p), \\
n_6 & \Vdash & y \equiv y', & \quad & n_6 & \coloneqq & p_{4/4}(p) \\
\implies n_7 & \Vdash & t' \xmapsto{h} x', & \quad & n_7 & \coloneqq & r_h(n_1, m, n_5) \\
\implies n_8 & \Vdash & x' \xmapsto{f} y', & \quad & n_8 & \coloneqq & r_f(n_2, n_5, n_6) \\
\implies n_9 & \Vdash & t' \xmapsto{\tilde h} (x', y'), & \quad & n_9 & \coloneqq & \langle n_7, n_8 \rangle.
\end{array}
\]
Therefore, the composition $(n, m, p) \mapsto n_9$ on the right satisfies the required condition for $r_{\tilde h}$.

We now claim that $i \circ \tilde h$ is equivalent to $h$. Thus, suppose
$$\langle n, m \rangle \Vdash t \xmapsto{i \circ \tilde h} x.$$
Then there exists $(x', y') \in E$ such that
\[
\begin{array}{rclcrcl}
n & \Vdash & t \xmapsto{\tilde h} (x', y'), & & & & \\
m & \Vdash & (x', y') \xmapsto{i} x & & & & \\
\implies n_1 & \Vdash & t \xmapsto{h} x', & \quad & n_1 & \coloneqq & p_1(n), \\
n_2 & \Vdash & x' \xmapsto{f} y', & \quad & n_3 & \coloneqq & p_2(n), \\
n_3 & \Vdash & x' \xmapsto{f} y', & \quad & n_3 & \coloneqq & p_{1/3}(m), \\
n_4 & \Vdash & x' \xmapsto{g} y', & \quad & n_4 & \coloneqq & p_{2/3}(m), \\
n_5 & \Vdash & x' \equiv x, & \quad & n_5 & \coloneqq & p_{3/3}(m) \\
\implies n_6 & \Vdash & t \equiv t, & \quad & n_6 & \coloneqq & d_h(n_1) \\
\implies n_7 & \Vdash & t \xmapsto{h} x, & \quad & n_7 & \coloneqq & r_h(n_1, n_6, n_5).
\end{array}
\]
Therefore, the composition $\langle n, m \rangle \mapsto n_7$ on the right satisfies the required condition for $e_{i \circ \tilde h, h}$.

Finally, in order to establish that $\tilde h$ is unique up to equivalence, it suffices to show that the equivalence class of $i$ is a [[monomorphism]]. Thus, suppose we have two functional relations $a, b$ between $T$ and $E$ such that $i \circ a$ is equivalent to $i \circ b$. Now suppose that
$$n \Vdash t \xmapsto{a} (x, y).$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & (x, y) \equiv (x, y), & \quad & n_1 & \coloneqq & c_a(n) \\
\implies n_2 & \Vdash & x \xmapsto{f} y, & \quad & n_2 & \coloneqq & p_{1/4}(n_1), \\
n_3 & \Vdash & x \xmapsto{g} y, & \quad & n_3 & \coloneqq & p_{2/4}(n_1), \\
n_4 & \Vdash & x \equiv x, & \quad & n_4 & \coloneqq & p_{3/4}(n_1), \\
n_5 & \Vdash & y \equiv y, & \quad & n_5 & \coloneqq & p_{4/4}(n_1) \\
\implies n_6 & \Vdash & (x, y) \xmapsto{i} x, & \quad & n_6 & \coloneqq & \langle n_2, n_3, n_4 \rangle \\
\implies n_7 & \Vdash & t \xmapsto{i\circ a} x, & \quad & n_7 & \coloneqq & \langle n, n_6 \rangle \\
\implies n_8 & \Vdash & t \xmapsto{i\circ b} x, & \quad & n_8 & \coloneqq & e_{i\circ a, i\circ b}(n_7) \\
\implies \exists (x', y')\in E, n_9 & \Vdash & t \xmapsto{b} (x', y'), & \quad & n_9 & \coloneqq & p_1(n_8), \\
n_{10} & \Vdash & (x', y') \xmapsto{i} x, & \quad & n_{10} & \coloneqq & p_2(n_8) \\
\implies n_{11} & \Vdash & x' \xmapsto{f} y', & \quad & n_{11} & \coloneqq & p_{1/3}(n_{10}), \\
n_{12} & \Vdash & x' \xmapsto{g} y', & \quad & n_{12} & \coloneqq & p_{2/3}(n_{10}), \\
n_{13} & \Vdash & x' \equiv x, & \quad & n_{13} & \coloneqq & p_{3/3}(n_{10}) \\
\implies n_{14} & \Vdash & y' \equiv y', & \quad & n_{14} & \coloneqq & c_f(n_{11}) \\
\implies n_{15} & \Vdash & x \xmapsto{f} y', & \quad & n_{15} & \coloneqq & r_f(n_{11}, n_{13}, n_{14}) \\
\implies n_{16} & \Vdash & y' \equiv y, & \quad & n_{16} & \coloneqq & u_f(n_{15}, n_2) \\
\implies n_{17} & \Vdash & (x', y') \equiv (x, y), & \quad & n_{17} & \coloneqq & \langle n_{11}, n_{12}, n_{13}, n_{16} \rangle \\
\implies n_{18} & \Vdash & t \equiv t, & \quad & n_{18} & \coloneqq & d_a(n) \\
\implies n_{19} & \Vdash & t \xmapsto{b} (x, y), & \quad & n_{19} & \coloneqq & r_b(n_9, n_{18}, n_{17}).
\end{array}
\]
Therefore, the composition $n \mapsto n_{19}$ on the right satisfies the required condition for $e_{a, b}$.

## Power objects

### Preliminaries

Since the definition of power objects involves pullback squares and monomorphisms, it will be appropriate to establish convenient criteria for establishing both. First, we start with isomorphisms.

\begin{lemma}
Suppose $f$ is an effective functional relation between $X$ and $Y$. Then the equivalence class of $f$ is an isomorphism if and only if

(a) There exists a partial recursive function $i_f : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x_1 \xmapsto{f} y$$
and
$$m \Vdash x_2 \xmapsto{f} y,$$
then $i_f(n, m)$ is defined and
$$i_f(n, m) \Vdash x_1 \equiv x_2.$$

(b) There exists a partial recursive function $s_f : \mathbb{N} \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash y \equiv y,$$
then $s_f(n)$ is defined and there exists $x\in X$ such that
$$s_f(n) \Vdash x \xmapsto{f} y.$$
\end{lemma}
\begin{proof}
($\Rightarrow$) Suppose the equivalence class of $g$ is inverse to the equivalence class of $f$.

To establish (a), suppose
$$n \Vdash x_1 \xmapsto{f} y$$
and
$$m \Vdash x_2 \xmapsto{f} y.$$
Then
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & y \equiv y & \quad & n_1 & \coloneqq & c_f(n) \\
\implies \exists x_3\in X, n_2 & \Vdash & y \xmapsto{g} x_3, & \quad & n_2 & \coloneqq & t_g(n_1) \\
\implies n_3 & \Vdash & x_1 \xmapsto{g\circ f} x_3, & \quad & n_3 & \coloneqq & \langle n, n_2 \rangle \\
\implies n_4 & \Vdash & x_1 \xmapsto{\operatorname{id}_X} x_3 & \quad & n_4 & \coloneqq & e_{g\circ f, \operatorname{id}_X}(n_3) \\
\implies n_5 & \Vdash & x_1 \equiv x_3, & \quad & n_5 & \coloneqq & n_4 \\
\implies n_6 & \Vdash & x_2 \xmapsto{g\circ f} x_3, & \quad & n_6 & \coloneqq & \langle m, n_2 \rangle \\
\implies n_7 & \Vdash & x_2 \xmapsto{\operatorname{id}_X} x_3, & \quad & n_7 & \coloneqq & e_{g\circ f, \operatorname{id}_X}(n_6) \\
\implies n_8 & \Vdash & x_2 \equiv x_3, & \quad & n_8 & \coloneqq & n_7 \\
\implies n_9 & \Vdash & x_3 \equiv x_2, & \quad & n_9 & \coloneqq & s_X(n_8) \\
\implies n_{10} & \Vdash & x_1 \equiv x_2, & \quad & n_{10} & \coloneqq & t_X(n_5, n_9).
\end{array}
\]
Therefore, the composition $(n, m) \mapsto n_{10}$ on the right satisfies the required condition for $i_f$.

To establish (b), suppose
$$n \Vdash y \equiv y.$$
Then there exists $x\in X$ such that
\[
\begin{array}{rclcrcl}
n_1 & \Vdash & y \xmapsto{g} x, & \quad & n_1 & \coloneqq & t_g(n) \\
n_2 & \Vdash & x \equiv x, & \quad & n_2 & \coloneqq & c_g(n_1) \\
\implies \exists y' \in Y, n_3 & \Vdash & x \xmapsto{f} y', & \quad & n_3 & \coloneqq & t_f(n_2) \\
\implies n_4 & \Vdash & y \xmapsto{f\circ g} y', & \quad & n_4 & \coloneqq & \langle n_1, n_3 \rangle \\
\implies n_5 & \Vdash & y \xmapsto{\operatorname{id}_Y} y', & \quad & n_5 & \coloneqq & e_{f\circ g, \operatorname{id}_Y}(n_4) \\
\implies n_6 & \Vdash & y \equiv y', & \quad & n_6 & \coloneqq & n_5 \\
\implies n_7 & \Vdash & y' \equiv y, & \quad & n_7 & \coloneqq & s_Y(n_6) \\
\implies n_8 & \Vdash & x \xmapsto{f} y, & \quad & n_8 & \coloneqq & r_f(n_3, n_2, n_7).
\end{array}
\]
Therefore, the composition $n \mapsto n_8$ on the right satisfies the required condition for $s_f$.

($\Leftarrow$) Let $f^\dagger\subseteq \mathbb{N} \times Y \times X$ be the relational inverse of $f$. Then we can see that condition (a) is exactly in the form needed for $u_{f^\dagger}$, and condition (b) is exactly in the form needed for $t_{f^\dagger}$. On the other hand, the other conditions for $f^\dagger$ to be an effective functional relation between $Y$ and $X$ are automatic: namely, we can use
$$d_{f^\dagger} \coloneqq c_f,$$
$$c_{f^\dagger} \coloneqq d_f,$$
and
$$r_{f^\dagger}(n, m, p) \coloneqq r_f(n, p, m).$$
Thus, $f^\dagger$ is an effective functional relation between $Y$ and $X$. We now claim that the equivalence class of $f^\dagger$ is inverse to the equivalence class of $f$. To see this, suppose
$$\langle n, m \rangle \Vdash x \xmapsto{f^\dagger \circ f} x'.$$
Then there exists $y\in Y$ such that
\[
\begin{array}{rclcrcl}
n & \Vdash & x \xmapsto{f} y, & & & & \\
m & \Vdash & y \xmapsto{f^\dagger} x' & & & & \\
\implies n_1 & \Vdash & x' \xmapsto{f} y, & \quad & n_1 & \coloneqq & m \\
\implies n_2 & \Vdash & x \equiv x', & \quad & n_2 & \coloneqq & i_f(n, n_1) \\
\implies n_3 & \Vdash & x \xmapsto{\operatorname{id}_X} x', & \quad & n_3 & \coloneqq & n_2.
\end{array}
\]
Therefore, the composition $\langle n, m \rangle \mapsto n_3$ on the right satisfies the required condition for $e_{f^\dagger \circ f, \operatorname{id}_X}$.

Similarly, suppose
$$\langle n, m \rangle \Vdash y \xmapsto{f \circ f^\dagger} y'.$$
Then there exists $x\in X$ such that
\[
\begin{array}{rclcrcl}
n & \Vdash & y \xmapsto{f^\dagger} x, & & & & \\
m & \Vdash & x \xmapsto{f} y' & & & & \\
\implies n_1 & \Vdash & x \xmapsto{f} y, & \quad & n_1 & \coloneqq & n \\
\implies n_2 & \Vdash & y \equiv y', & \quad & n_2 & \coloneqq & u_f(n_1, m) \\
\implies n_3 & \Vdash & y \xmapsto{\operatorname{id}_Y} y', & \quad & n_3 & \coloneqq & n_2.
\end{array}
\]
Therefore, the composition $\langle n, m \rangle \mapsto n_3$ on the right satisfies the required condition for $e_{f \circ f^\dagger, \operatorname{id}_Y}$.
\end{proof}

\begin{lemma}
Given appropriate effective functional relations $h,f,g$, then
$$E \underset{\quad [h] \quad}{\to}X\underoverset{\quad [g] \quad}{[f]}{\rightrightarrows}Y$$
is an equalizer diagram if and only if

(a) $f\circ h$ is equivalent to $g\circ h$.

(b) There is a partial recursive function $i_h : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash e_1 \xmapsto{h} x$$
and
$$m \Vdash e_2 \xmapsto{h} x,$$
then $i_h(n, m)$ is defined and
$$i_h(n, m) \Vdash e_1 \equiv e_2.$$

(c) There is a partial recursive function $eq_{h,f,g} : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \xmapsto{f} y$$
and
$$m \Vdash x \xmapsto{g} y,$$
then $eq_{h,f,g}(n, m)$ is defined and there exists $e\in E$ such that
$$eq_{h,f,g}(n, m) \Vdash e \xmapsto{h} x.$$
\end{lemma}
\begin{proof}
The diagram being an equalizer diagram, when (a) is satisfied, is equivalent to the induced effective functional relation $\tilde h$ being an isomorphism. It is then straightforward to check that (b) is equivalent to the effective injectivity of $\tilde h$, and (c) is equivalent to the effective surjectivity of $\tilde h$.
\end{proof}

\begin{lemma}
Given appropriate effective functional relations $f,g,h,j$, then
\[
\begin{array}{rcl}
X & \overset{[f]}{\to} & Y \\
[g] \downarrow & & \downarrow [h] \\
Z & \underset{[j]}{\to} & W
\end{array}
\]
is a pullback square if and only if

(a) $h\circ f$ is equivalent to $j \circ g$.

(b) There is a partial recursive function $i_{f,g} : \mathbb{N}^4 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x_1 \xmapsto{f} y,$$
$$m \Vdash x_2 \xmapsto{f} y,$$
$$p \Vdash x_1 \xmapsto{g} z,$$
and
$$q \Vdash x_2 \xmapsto{g} z,$$
then
$i_{f,g}(n,m,p,q)$ is defined, and
$$i_{f,g}(n,m,p,q) \Vdash x_1 \equiv x_2.$$

(c) There are partial recursive functions $pb^1_{f,g,h,j} : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ and $pb^2_{f,g,h,j} : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash y \xmapsto{h} w$$
and
$$m \Vdash z \xmapsto{j} w,$$
then $pb^1_{f,g,h,j}(n, m)$ and $pb^2_{f,g,h,j}(n, m)$ exists, and there exists $x\in X$ such that
$$pb^1_{f,g,h,j}(n, m) \Vdash x \xmapsto{f} y$$
and
$$pb^2_{f,g,h,j}(n, m) \Vdash x \xmapsto{g} z.$$
\end{lemma}

\begin{proof}
By abstract nonsense, the pullback condition is equivalent to $[(f, g)] : X \to Y\times Z$ being an equalizer of $[h \circ \pi_1] : Y \times Z \to W$ and $[j \circ \pi_2] : Y \times Z \to W$. It is then straightforward to check that the conditions above are equivalent to the conditions in the respective parts of the equalizer lemma.
\end{proof}

\begin{corollary}
If $f$ is an effective functional relation between $X$ and $Y$, then the equivalence class $[f]$ of $f$ is a monomorphism if and only if there exists a partial recursive function $i_f : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x_1 \xmapsto{f} y$$
and
$$m \Vdash x_2 \xmapsto{f} y,$$
then $i_f(n, m)$ is defined and
$$i_f(n, m) \Vdash x_1 \equiv x_2.$$
\end{corollary}
\begin{proof}
By abstract nonsense, $[f]$ is a monomorphism if and only if
\[
\begin{array}{rcl}
X & \overset{\operatorname{id}_X}{\to} & X \\
\operatorname{id}_X \downarrow & & \downarrow [f] \\
X & \underset{[f]}{\to} & Y
\end{array}
\]
is a pullback square. However, in this particular pullback square, conditions (a) and (b) are automatically satisfied, whereas condition (c) is easily equivalent to the existence of $i_f$.
\end{proof}