
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

\begin{definition}
An **initial object** in a [[category]] $\mathcal{C}$ is an [[object]] $\emptyset$ such that for all objects $x \,\in\, \mathcal{C}$, there is a unique [[morphism]] 
$\varnothing \xrightarrow{\exists !} x$ 
with 
[[source]] $\varnothing$.
and 
[[target]] $x$.
\end{definition}

\begin{remark}
An initial object, if it exists, is unique up to unique [[isomorphism]], so that we may speak of [[the]] initial object.
\end{remark}

\begin{remark}
When it exists, the initial object is the [[colimit]] over the [[empty diagram]].
\end{remark}

\begin{remark}
Initial objects are also called _coterminal_, and (rarely, though): _coterminators_, _universal initial_, _co-universal_, or simply _universal_.
\end{remark}

\begin{definition}
An initial object $\varnothing$ is called a **[[strict initial object]]** if all morphisms $x \xrightarrow{\;} \varnothing$ into it are [[isomorphisms]].  
\end{definition}

\begin{remark}
Initial objects are the [[duality|dual]] concept to [[terminal objects]]: an initial object in $C$ is the same as a terminal object in the [[opposite category]] $C^{op}$.  
\end{remark}

\begin{remark}
An object that is both initial and [[terminal object|terminal]] is called a [[zero object]].
\end{remark}


## Examples

* An initial object in a [[partial order|poset]] is a [[bottom element]].

* The [[empty set]] is an initial object in [[Set]].

* Likewise, the [[empty category]] is an initial object in [[Cat]], the [[empty space]] is an initial object in [[Top]], and so on.

* The [[trivial group]] is the initial object (in fact, the [[zero object]]) of [[Grp]] and [[Ab]].

* The [[integers]] comprise the initial object of [[Ring]].

* An initial object in a category of [[central extensions]] of a given algebraic object is called a _[[universal central extension]]_.



## Properties

### Left adjoints to constant functors


+-- {: .num_prop }
###### Proposition

Let $\mathcal{C}$ be a [[category]].

1. The following are equivalent:

   1. $\mathcal{C}$ has a [[terminal object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[right adjoint]]

      $$
        \ast 
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \mathcal{C}
      $$

    Under this equivalence, the [[terminal object]] is identified with the image under the right adjoint of the unique object of the [[terminal category]].

1. Dually, the following are equivalent:

   1. $\mathcal{C}$ has an [[initial object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[left adjoint]]

      $$
        \mathcal{C}
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \ast
      $$

    Under this equivalence, the [[initial object]] is identified with the image under the left adjoint of the unique object of the [[terminal category]].

=--


+-- {: .proof}
###### Proof

Since the unique [[hom-set]] in the [[terminal category]] is [[generalized the|the]] [[singleton]], the hom-isomorphism characterizing the [[adjoint functors]] is directly the [[universal property]] of an [[initial object]] in $\mathcal{C}$
 
$$
  Hom_{\mathcal{C}}( L(\ast) , X )
  \;\simeq\;
  Hom_{\ast}( \ast, R(X) ) 
  =
  \ast 
$$

or of a [[terminal object]]

$$
  Hom_{\mathcal{C}}( X , R(\ast) )
  \;\simeq\;
  Hom_{\ast}( L(X), \ast ) = \ast
  \,,
$$

respectively.

=--


### Cones over the identity
 {#ConesOverTheIdentity}

By definition, an initial object is equipped with a universal [[cocone]] under the unique functor $\emptyset\to C$ from the [[empty category]].  On the other hand, if $I$ is initial, the unique morphisms $!: I \to x$ form a cone *over* the [[identity functor]], i.e. a natural transformation $\Delta I \to Id_C$ from the [[constant functor]] at the initial object to the identity functor.  In fact this is almost another characterization of an initial object (e.g. [MacLane, p. 229-230](#MacLane)):

+--{: .num_lemma #cone}
###### Lemma

Suppose $I\in C$ is an object equipped with a natural transformation $p:\Delta I \to Id_C$ such that $p_I = 1_I : I\to I$.  Then $I$ is an initial object of $C$.

=--

+--{: .proof}
###### Proof

Obviously $I$ has at least one morphism to every other object $X\in C$, namely $p_X$, so it suffices to show that any $f:I\to X$ must be equal to $p_X$.  But the naturality of $p$ implies that $\Id_C(f) \circ p_I = p_X \circ \Delta_I(f)$, and since $p_I = 1_I$ this is to say $f \circ 1_I = p_X \circ 1_I$, i.e. $f=p_X$ as desired.

=-- 

+-- {: .num_theorem #LimitOverIdentityFunctorIsInitialObject} 
###### Theorem 

An object $I$ in a [[category]] $C$ is initial iff $I$ is the [[limit]] of the [[identity functor]] $Id_C$. 

=-- 

+-- {: .proof} 
###### Proof 

If $I$ is initial, then there is a [[cone]] $(!_X: I \to X)_{X \in Ob(C)}$ from $I$ to $Id_C$.  If $(p_X: A \to X)_{X \in Ob(C)}$ is any cone from $A$ to $Id_C$, then $p_X = f \circ p_Y$ for any $f:Y\to X$, and so in particular $p_X = !_X \circ p_I$.   Since this is true for any $X$, $p_I: A \to I$ defines a morphism of cones, and it is the unique morphism of cones since if $q$ is any morphism of cones, then $p_I = !_I \circ q = 1_I \circ q = q$ (using that $!_I = 1_I$ by initiality). Thus $(!_X: I \to X)_{X \in Ob(C)}$ is the limit cone. 

Conversely, if $(p_X: L \to X)_{X \in Ob(C)}$ is a limit cone for $Id_C$, then $f\circ p_Y = p_X$ for any $f:Y\to X$, and so in particular $p_X \circ p_L = p_X$ for all $X$. This means that both $p_L: L \to L$ and $1_L: L \to L$ define morphisms of cones; since the limit cone is the terminal cone, we infer $p_L = 1_L$. Then by Lemma \ref{cone} we conclude $L$ is initial. 

=-- 

+-- {: .num_remark #RelevanceForAdjointFunctorTheorem}
###### Remark
**(relevance for [[adjoint functor theorem]])**

Theorem \ref{LimitOverIdentityFunctorIsInitialObjecty} is actually a key of entry into the [[adjoint functor theorem|general adjoint functor theorem]]. Showing that a functor $G: C \to D$ has a [[left adjoint]] is tantamount to showing that each functor $D(d, G-)$ is [[representable functor|representable]], i.e., that the [[comma category]] $d \downarrow G$ has an initial object $(c, \theta: d \to G c)$ (see at _[[adjoint functor]]_, [this prop.](#PointwiseExpressionOfLeftAdjoints)).  This is the limit of the identity functor, but typically this is the limit over a large diagram whose existence is not guaranteed. The point of a solution set condition is to replace this with a small diagram which is cofinal in the large diagram. 

=--

## Related concepts

* [[terminal object]], [[bi-terminal object]]

* [[bottom type]]

* [[initial object in a 2-category]]

* [[initial object in an (∞,1)-category]]

* [[h-initial object]]

* [[adjoint functor theorem]] 

## References

Textbook accounts:

* [[Francis Borceux]], Section 2.3 in Vol. 1: *Basic Category Theory* of: *[[Handbook of Categorical Algebra]]*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))


* {#MacLane} [[Saunders MacLane]], _[[Categories for the Working Mathematician]]_




[[!redirects initial object]]
[[!redirects initial objects]]
[[!redirects initial]]
[[!redirects coterminal object]]
[[!redirects coterminal objects]]
[[!redirects coterminator]]
[[!redirects coterminators]]
