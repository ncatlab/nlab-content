
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

A _strong monad_ over a [[monoidal category]] $V$ is a [[monad]] in the [[bicategory]] of $V$-[[actegory|actegories]]. 

If $V$ is a [[monoidal closed category]], then a strong monad is the same thing as a $V$-[[enriched monad]]. 

## Definition 

+-- {: .num_defn}
###### Definition

For $V$ a [[monoidal category]] a **strong monad** over $V$ is a [[monad]] 

* in the $2$-[[2-category|category]] $V\text{-}Act$ of left $V$-[[actegory|actegories]] on [[category|categories]] 

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

## Concrete definition

A more concrete definition is given in:

* [[Anders Kock]], *Strong functors and monoidal monads*, Arch. Math. (Basel) 23 (1972), 113--120.

and later in 

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
A\times T^{2}\, B & \xrightarrow{t_{A,T B}} & T(A\times T B) & \xrightarrow{T\: t_{A,B}} & T^{2}(A\times B)
\end{array}
\]

More generally, if a monoidal category $V$ acts on a category $C$
\[
\bullet : V\times C\to C
\]
then a $V$-strength for a monad $T$ on $C$ is a family of morphisms
$t_{A,B}:A\bullet T(B)\to T(A\bullet B)$ satisfying similar commutative diagrams. 

## Moggi's typing rules and parameterized definition

Moggi proposed the following typing rules for a sequence operator:
\[
\frac{\Gamma \vdash t:X}{\Gamma\vdash \eta(t):T(X)}
\qquad
\frac{\Gamma,x:X \vdash u: T(Y)\quad \Delta\vdash t:T(X)}
{\Gamma,\Delta\vdash let\,x=t\,in\,u:T(Y)}
\]
To interpret these rules in a category, where types are interpreted as objects and judgements are interpreted as morphisms, we require 

* For each object $X$, an object $T(X)$; 

* a morphism $
\eta_X:X\to T(X)$ for each $X$ (equivalently, 
a natural family of functions $C(\Gamma,X)\to C(\Gamma, T(X))$); 

* a family of functions $*_{\Gamma,\Delta}:C(\Gamma\otimes X, T(Y))\times C(\Delta,T(X))\to C(\Gamma\otimes \Delta,T(Y))$ natural in $\Gamma$ and $\Delta$,

such that 

* $f * \eta =f$, $\eta * f=f$, and $h*(g*f)=(h*g)*f$. 

With the subscripts:

* $f *_{\Gamma,X} \eta_X = f$ and $\eta *_{I,\Delta} f=f$, and
$h *_{\Gamma,\Delta\otimes \Xi} (g *_{\Delta,\Xi} f) = (h *_{\Gamma,\Delta\otimes X} g) *_{\Gamma\otimes\Delta,\Xi} f$. 

Such a structure is the same thing as a strong monad. One way to see this is to notice that it is essentially the same as the Kleisli triple form of an $\hat C$-[[enriched monad]] on $C$, where $\hat C$ is the category of [[presheaves]] on $C$ regarded with the [[Day convolution]] monoidal structure. More concretely, 

\[\eta_{X\otimes Y}*_{X,T(Y)} id_{T(Y)}:X\otimes T(Y)\to T(X\otimes Y)\] 

is a strength map. 

## Uniqueness of strength with enough points

+-- {: .num_theorem}
###### Theorem
**(Moggi)** 

Let $C$ be a category with finite products and let $T$ be a strong monad on $C$. 
For any points $x:1\to X$, $y:1\to T(Y)$, we have
\[
t\circ(x,y)\ = \ 
T((x\circ !_Y),id_Y)\circ y\ : 1 \to T(X\times Y)
\]
Hence if $1$ is a [[generator]], i.e. $C(1,-):C\to Set$ is faithful, then there is at most one strength for any ordinary monad on $C$. 
=--

In other words, a monad being strong is a property rather than structure in a category with enough points. 

## Related concepts

* [[tensorial strength]]

* [[monoidal monad]]

* [[commutative monad]]

* [[enriched monad]]

* [[monad (in computer science)]]

## References 

Strong monads were defined by Kock, as an alternative description of enriched monads.

* [[Anders Kock]], *Strong functors and monoidal monads*, Arch. Math. (Basel) 23 (1972), 113--120.

Usually strong monads are described explicitly in terms of the components of the above structure. The above repackaging of that definition appears in the blog post

* [[John Baez]], _The Monads Hurt My Head -- But Not Anymore_ ([blog](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025476))

Strong monads are important in Moggi's theory of notions of computation (see [[monad (in computer science)]]):

* [[Eugenio Moggi]]. Notions Of Computation And Monads. Information And Computation. 1991;93:55&#8211;92. 
* [[Eugenio Moggi]]. Computational Lambda-Calculus and Monads. Proceedings of the Fourth Annual Symposium on Logic in Computer Science. 1989. p. 14&#8211;23. 

[[!redirects strong monads]]