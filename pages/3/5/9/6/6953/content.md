
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
#### Functional analysis
### Contents {: .clickToReveal}
### Contents {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Type and Cotype in Functional Analysis
* tic
{: toc}

## Idea

The **type** and **cotype** of a [[Banach space]] measure how far it is from being a [[Hilbert space]].  The definition is based on the observation, due to [[John von Neumann]], that a Banach space is a Hilbert space if and only if it satisfies the [[parallelogram identity]].  Recall that this states that in a Hilbert space,
$$
{\|x + y\|^2} + {\|x - y\|^2} = 2{\|x\|^2} + 2{\|y\|^2}.
$$
This can be thought of as a way of improving the triangle inequality, which relates $\|x \pm y\|$ to $\|x\|$ and $\|y\|$, by finding an equality relating $\|x \pm y\|$ to $\|x\|$ and $\|y\|$.

To measure the type and cotype of a Banach space, one takes the parallelogram identity and finds out how bad it gets.  Slightly more precisely, one tries to see what happens if one looks merely for an inequality, perhaps with a constant.  Since the equality can break in one of two ways, this leads to two notions.

## Definition ##

To define the type and cotype of a Banach space, we start with a finite family of vectors, say $\{x_1,\dots,x_n\}$.  Then we look for constants $T_2$ and $C_2$ such that the following inequalities are true:

$$
\begin{aligned}
\Average_\pm {\left\|\sum \pm x_i\right\|^2} &\le T_2^2 \sum {\|x_i\|^2}, \\
\Average_\pm {\left\|\sum \pm x_i\right\|^2} &\ge C_2^{-2} \sum {\|x_i\|^2}
\end{aligned}
$$

Here, the left-hand side is the average value over all choices of $\pm$ (so in the original parallelogram identity we have divided each side by $2$).

+-- {: .num_defn #type}
###### Definition ######
The smallest constant $T_2$ making the first inequality true for all finite sequences of vectors is the **type $2$ constant** of the space.

The smallest constant $C_2$ making the second inequality true for all finite sequences of vectors is the **cotype $2$ constant** of the space.

Either of these is allowed to be infinite.  A space is said to be **type $2$** if its type $2$ constant is finite.  Similarly, it is said to be **cotype $2$** if its cotype $2$ constant is finite.
=--

## Properties ##

If we consider all Banach spaces that are either of type $2$ or cotype $2$ then we find that these split into the two obvious classes with Hilbert spaces sitting plum in the middle.  Not only are Hilbert spaces the intersection of these classes, but also a continuous linear operator from a space of type $2$ into a space of cotype $2$ factors through a Hilbert space.
(This follows from a generalization/extension of Grothendieck's inequality.)

More precisely:

1. If a Banach space is of type $2$ and of cotype $2$ (ie both constants are finite) then it is a Hilbert space.  This is due to Kwapien.
2. Any bounded linear operator from a Banach space of type $2$ to a Banach space of cotype $2$ factors through a Hilbert space.

As type and cotype are isomorphism invariants, they can be used to distinguish between some Banach spaces.  See [[isomorphism classes of Banach spaces]] for more.

## Generalisations ##

In the inequalities for type $2$ and cotype $2$ it is possible to replace the $2$ by a real number $p$ and define the notions of *type $p$* and *cotype $p$*.  Taken as a whole, these provide more information and thus give a finer classification of Banach spaces.  In particular:

1. For $1 \le p \le 2$, the [[Lebesgue space]], $L_p$, has type $p$ and cotype $2$.
1. For $2 \le p \lt \infty$, the [[Lebesgue space]], $L_p$, has type $2$ and cotype $p$.

We also have the following properties:

1. For $r \lt p$, type $p$ implies type $r$.
1. For $r \gt p$, cotype $p$ implies cotype $r$.
1. Both type and cotype pass to subspaces.
1. Type passes to quotients, cotype does not in general but if the space has some type strictly larger than one then cotype does pass to quotients.
1. Type dualises to cotype, in that if $X$ has type $p$ then $X^*$ has cotype $p'$ (where $p^{-1} + {p'}^{-1} = 1$), but cotype does not dualise to type unless the space has some type strictly larger than one.

[[!redirects cotype (functional analysis)]]