# Meros
* this block creates the table of contents, leave as is
{: toc}

## Idea

A **meros** (plural **meroi**) is a relational analogue of topoi. The morphisms of meroi are like relations, and they are a venue for generalized [[relational set theory]].


## Definition 

Following Kawahara, we define an auxiliary venue for meroi first. An I-category is a [[dagger category]] where every [[hom-set]] has [[lattice]] structure. Specifically,

\begin{defn} \label{I-category}

An I-category is a dagger category where, for all objects $A, B$, there is a partial order $\sqsubseteq$ on the morphisms $A \to B$, a least relation $0_{A,B}$ and greatest relation $\Theta_{A,B}$ such that

$$
\forall \alpha : A \to B, 0_{A,B} \sqsubseteq \alpha \sqsubseteq \Theta_{A,B}
$$

and the partial order commutes with the dagger structure:

$$
\forall \alpha, \beta : A \to B, \alpha \sqsubseteq \beta \iff \alpha^\dagger \sqsubseteq \beta^\dagger
$$

\end{defn}

I-categories can have a [[zero object]] like typical dagger categories, but also a [[terminal object]].

\begin{defn} \label{Terminal object}
When it exists, a terminal object in an I-category is an object $1$ such that $0_{1,1} \neq id_1 = \Theta_{1,1}$ and for all objects $A, B$, $\Theta_{1,B} \circ \Theta_{A,1} = \Theta_{A,B}$.
\end{defn}

We next highlight specific morphisms within I-categories.

\begin{defn} \label{Partial function}
A morphism $f : A \to B$ is a partial function, or univalent, when $f \circ f^\dagger \sqsubseteq id_B$.
\end{defn}

\begin{defn} \label{Function}
A partial function $f : A \to B$ is a total function, or function, when $id_A \sqsubseteq f^\dagger \circ f$.
\end{defn}

\begin{defn} \label{Rationality}
A morphism $\alpha : A \to B$ is rational when there exist functions $f : X \to A$ and $g : X \to B$ such that $\alpha = g \circ f^\dagger$ and $f^\dagger \circ f \sqcap g^\dagger \circ g = id_X$.
\end{defn}

\begin{defn} \label{Quotient}
For all $\alpha : A \to B, \beta : A \to C, \gamma : B \to C$ there exists a quotient $\beta \div \gamma : A \to B$ such that $\gamma \circ \alpha \sqsubseteq \beta \iff \alpha \sqsubseteq \beta \div \gamma$.
\end{defn}

We also need the Dedekind formula, which relates any three morphisms between three objects.

\[
\label{DedekindFormula}
\forall \alpha : A \to B, \beta : B \to C, \gamma : A \to C,
\beta \circ \alpha \sqcap \gamma \sqsubseteq ( \beta \sqcap \gamma \circ \alpha^\dagger ) \circ \alpha
\]

We are now ready to define meroi. Instead of a lattice, we will now expect a [[complete Heyting algebra]] for each hom-set.

\begin{defn} \label{Meros}

A meros is an I-category where:

* The partial order $\sqsubseteq$ is not just a lattice, but a complete Heyting algebra
* Every relation is rational
* The Dedekind formula holds whenever possible
* There is a terminal object
* All quotients exist

\end{defn}

## Properties

\begin{prop} \label{Zero relations}
For all $\alpha : A \to B$, $0 \circ \alpha = \alpha \circ 0 = 0$.
\end{prop}

\begin{proof}
$0 \sqsubseteq 0 \div \alpha \iff \alpha \circ 0 \sqsubseteq 0 \iff \alpha \circ 0 = 0$. ([Kawahara 1995](#Kawahara95))
\end{proof}


## Examples

[[Rel]] is the example meros, by analogy with [[Set]] and topoi.


## References

Meroi were introduced in:

* {#Kawahara95} [[Kawahara Yasuo]], _Relational Set Theory_, in Proceedings of the 6th International Conference on Category Theory and Computer Science, 1995 ([doi:10.1007/3-540-60164-3_19](http://dx.doi.org/10.1007/3-540-60164-3_19), [pdf](https://www.researchgate.net/profile/Yasuo-Kawahara/publication/226561376_Relational_set_theory/links/569f960908ae21a564270542/Relational-set-theory.pdf))