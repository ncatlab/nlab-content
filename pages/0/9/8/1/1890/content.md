
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Strong monads#
* table of contents
{:toc}

## Idea

A _strong monad_ over a [[monoidal category]] $V$ is a [[monad]] in the [[bicategory]] of $V$-[[actions]].

## Definition 

+-- {: .num_defn}
###### Definition

For $V$ a [[monoidal category]] a **strong monad** over $V$ is a [[monad]] 

* in the $2$-[[2-category|category]] $V\text{-}Act$ of left $V$-[[actions]] on [[category|categories]] 

* on the object $V$ itself.
=--

Here we regard $V$ as equipped with the canonical $V$-action on itself.


## Details ##

If we write $\mathbf{B}V$ for the one-object [[bicategory]] obtained by [[delooping]] $V$ once, we have

$$
  V\text{-}Act \simeq Lax2Funct(\mathbf{B}V, Cat)
  \,,
$$
where on the right we have the $2$-category of [[lax functor|lax 2-functors]] from $\mathbf{B}V$ to [[Cat]], lax [[natural transformations]] of and [[modifications]].

The category $V$ defines a canonical functor $\hat V : \mathbf{B}V \to Cat$.

The strong monad, being a [[monad]] in this [[lax functor]] [[bicategory]] is given by

* a lax [[natural transformation]] $T : \hat V \to \hat V$;

* [[modifications]] 

  * unit: $\eta : Id_V \Rightarrow T$ 

  * product: $\mu : T \circ T \Rightarrow T$

* satisfying the usual uniticity and associativity constraints.

By the general logic of $(2,1)$-[[(n,k)-transformation|transformations]] the components of $T$ are themselves a certain [[functor]].

Then the [usual diagrams](http://en.wikipedia.org/wiki/Strong_monad) that specify a strong monad


* unitalness and functoriality of the component functor of $T$;

* naturalness of unit and product modifications.

## Alternative definition

A more concrete definition is given in:

* [[Eugenio Moggi]]. Computational Lambda-Calculus and Monads. Proceedings of the Fourth Annual Symposium on Logic in Computer Science. 1989. p. 14&#8211;23. 

A _strong monad_ over a category $C$ with finite products is a monad $(T, \eta, \mu)$ together with a natural transformation $t_{A,B}$ from $A \times T\;B$ to $T(A\times B)$ subject to three diagrams.

"Strengthening with 1 is irrelevant":

\[
\begin{array}{ccc}
1\times T\, A & \rightarrow & T\, A\\
\\
 & t_{1,A}\searrow\phantom{t_{1,A}} & \downarrow\\
\\
 &  & T(1\times A)
\end{array}
\]

"Consecutive applications of strength commute":

\[
\begin{array}{ccccc}
(A\times B)\times T\, C & \xrightarrow{t_{A\times B,C}} & T\,((A\times B)\times C)\\
\\
\cong\downarrow\phantom{\cong} &  &  & \phantom{\cong}\searrow\cong\\
\\
A\times(B\times T\, C) & \xrightarrow[A\times t_{B,C}]{} & A\times T\,(B\times C) & \xrightarrow[t_{A,B\times C}]{} & T(A\times(B\times C))
\end{array}
\]


"Strength commutes with monad unit and multiplication":

\[
\begin{array}{ccccc}
A\times B\\
\\
A\times\eta_{B}\downarrow\phantom{A\times\eta_{B}} & \phantom{\eta_{A\times B}}\searrow\eta_{A\times B}\\
\\
A\times T\, B & \xrightarrow{t_{A,B}} & T(A\times B)\\
\\
A\times\mu_{B}\uparrow\phantom{A\times\mu_{B}} &  &  & \phantom{\mu_{A\times B}}\nwarrow\mu_{A\times B}\\
\\
A\times T^{2}\, B & \xrightarrow{t_{A,TB}} & T(A\times TB) & \xrightarrow{T\: t_{A,B}} & T^{2}(A\times B)
\end{array}
\]




## Related concepts

* [[tensorial strength]]

* [[monoidal monad]]

* [[commutative monad]]

* [[enriched monad]]

## References 

Usually strong monads are described explicitly in terms of the components of the above structure. The above repackaging of that definition is due to John Baez

* [[John Baez]], _The Monads Hurt My Head -- But Not Anymore_ ([blog](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025476))

Strong monads are important in Moggi's theory of notions of computation (see [[monad (in computer science)]]):

* [[Eugenio Moggi]]. Notions Of Computation And Monads. Information And Computation. 1991;93:55&#8211;92. 
* [[Eugenio Moggi]]. Computational Lambda-Calculus and Monads. Proceedings of the Fourth Annual Symposium on Logic in Computer Science. 1989. p. 14&#8211;23. 

[[!redirects strong monads]]