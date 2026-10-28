# Overview

We give the proofs here that are necessary to show that the definition of the [[effective topos]] does in fact give a well-defined category.

In general, this follows the strategy of taking a proof that the category of partial [[setoid|setoids]] (where an object is a set equipped with a [[partial equivalence relation]] and a morphism is a respectful functional relation) is a category, and keeping track of realizers at each step. The resulting partial recursive functions will generally be closely related to the corresponding proof terms under the [[Curry-Howard correspondence]].

# Equivalence relation

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
