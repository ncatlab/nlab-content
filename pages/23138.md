
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Meros
* this block creates the table of contents, leave as is
{: toc}

## Idea

The concept of **meros** (plural **meroi** or **meroses**) is a [[relation|relational]] analogue of that of a *[[topos]]*; where the [[morphisms]] in a topos are like [[functions]], the morphisms in a meros are like [[relations]]. Like [[Set]] is the canonical [[base topos]], so [[Rel]] is the archetypical meros. More generally, like topoi provide a context for generalized [[constructive set theory]], so meroi provide a context for generalized [[relational set theory]]. 

Where the [[boolean]] [[truth values]] of [[set theory]] are identified/generalized to [[elements]] of the [[subobject classifier]] of a topos, a meros instead represents Boolean values as degrees of inclusion between relations: between any two objects, there is a false relation (a [[zero morphism]]) and a true relation.


## Definition

Following [Kawahara 1995](#Kawahara95), we define an auxiliary venue for meroi first. An *I-category* is a [[dagger category]] where every [[hom-set]] has [[lattice]] structure. Specifically,

\begin{defn} \label{ICategory}

An *I-category* is a [[dagger category]] where, for all objects $A, B$, there is a [[partial order]] $\sqsubseteq$ on the morphisms $A \to B$, a least [[relation]] $0_{A,B}$ and greatest relation $\Theta_{A,B}$ such that

$$
  \underset{
     A \to B
  }{
    \forall  
  }
  \;\;
  0_{A,B}
    \sqsubseteq 
  \alpha 
    \sqsubseteq 
  \Theta_{A,B}
$$

and the partial order commutes with the dagger structure:

$$
  \underset{
    \alpha, \beta 
    \colon 
    A \to B, 
  }{
    \forall 
  }
  \;\;
  \alpha 
    \sqsubseteq  
  \beta 
    \;\;\iff\;\; 
  \alpha^\dagger \sqsubseteq \beta^\dagger
  \,.
$$

\end{defn}

I-categories can have a [[zero object]] like typical dagger categories, but also a [[terminal object]].

\begin{defn} \label{TerminalObject}
When it exists, a *terminal object* in an I-category (Def. \ref{ICategory}) is an [[object]] $1$ such that $0_{1,1} \neq id_1 = \Theta_{1,1}$ and for all objects $A, B$, $\Theta_{1,B} \circ \Theta_{A,1} = \Theta_{A,B}$.
\end{defn}

We next highlight specific morphisms within I-categories.

\begin{defn} \label{PartialFunction}
A morphism $f \colon A \to B$ in an I-category (Def. \ref{ICategory}) is called a *[[partial function]]*, or *univalent*, when $f \circ f^\dagger \sqsubseteq id_B$.
\end{defn}

\begin{defn} \label{Function}
A partial function $f \colon A \to B$ (Def. \ref{PartialFunction}) is a *total function*, or function, when $id_A \sqsubseteq f^\dagger \circ f$.
\end{defn}

\begin{defn} \label{Rationality}
A morphism $\alpha \colon A \to B$ in an I-category (Def. \ref{ICategory}) is *rational* when there exist functions  $f \,\colon\, X \to A$ and $g \,\colon\, X \to B$ (in the sense of Def. \ref{Function}) such that $\alpha = g \circ f^\dagger$ and $f^\dagger \circ f \sqcap g^\dagger \circ g = id_X$.
\end{defn}

\begin{defn} \label{Quotient}
For all $\alpha \,\colon\, A \to B, \beta \,\colon\, A \to C, \gamma \,\colon\, B \to C$ there exists a *quotient* $\beta \div \gamma \,\colon\, A \to B$ such that $\gamma \circ \alpha \sqsubseteq \beta \iff \alpha \sqsubseteq \beta \div \gamma$.
\end{defn}

We also need the Dedekind formula, which relates any three morphisms between three objects.

\[
  \label{DedekindFormula}
  \underset{
    {
      \alpha \colon A \to B
    }
    \atop
    {
    { \beta \colon B \to C }
    \atop
    { \gamma \colon A \to C }
    }
  }{
    \forall 
  }
  \;\;
   \beta \circ \alpha \sqcap \gamma 
     \,\sqsubseteq\, 
  ( \beta \sqcap \gamma \circ \alpha^\dagger ) \circ \alpha
\]

We are now ready to define meroi. Instead of a lattice, we will now expect a [[complete Heyting algebra]] for each [[hom-set]].

\begin{defn} \label{Meros}

A *meros* is an I-category (Def. \ref{ICategory}) where:

* The partial order $\sqsubseteq$ is not just a lattice, but a [[complete Heyting algebra]].

* Every relation is rational (in the sense of Def. \ref{Rationality}).

* The Dedekind formula (eq:DedekindFormula) holds whenever possible.

* There is a [[terminal object]] (in the sense of Def. \ref{TerminalObject}).

* All quotients (in the sense of Def. \ref{Quotient}) exist.

\end{defn}


## Properties

\begin{prop} \label{Zero relations}
For all $\alpha \,,\, A \to B$
we have  $0 \circ \alpha = \alpha \circ 0 = 0$.
\end{prop}
([Kawahara 1995](#Kawahara95))
\begin{proof}
$
  0 \sqsubseteq 0 \div \alpha 
  \;\;\iff\;\; 
  \alpha \circ 0 \sqsubseteq 0 
  \;\;\iff\;\; 
  \alpha \circ 0 = 0
  \,.
$
\end{proof}


## Examples

\begin{example}
[[Rel]] is the classic example of a meros, analogous to how [[Set]] is the archetypical [[topos]]. 

[Kawahara 1995](#Kawahara95) uses also the example of $Rel \times Rel$.
\end{example}


## Related Concepts

* [[SEAR]]


## References

The notion of meroi was introduced in:

* {#Kawahara95} [[Kawahara Yasuo]], _Relational Set Theory_, in Proceedings of the 6th International Conference on Category Theory and Computer Science, 1995 ([doi:10.1007/3-540-60164-3_19](http://dx.doi.org/10.1007/3-540-60164-3_19), [pdf](https://www.researchgate.net/profile/Yasuo-Kawahara/publication/226561376_Relational_set_theory/links/569f960908ae21a564270542/Relational-set-theory.pdf))


[[!redirects meros]]
[[!redirects meroi]]
[[!redirects meroses]]
