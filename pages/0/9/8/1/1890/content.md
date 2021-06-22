
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Strong monads#
* table of contents
{:toc}

## Idea

A _strength_ and a _costrength_ for a [[monad]] on a [[monoidal category]] are [[structures]] relating the monad with the [[tensor product]] of the category "in one direction". A monad equipped with a strength is called a _strong monad_. 
The notion of strength can be motivated at least in the following ways.

* A strong monad over a [[monoidal category]] $V$ is a [[monad]] in the [[bicategory]] of $V$-[[actegory|actegories]], on the category $V$ (acting on itself on the left for a strength, on the right for a costrength). 
* A strength for a monad is a compatibility condition between the monad and the tensor product "from the left", less symmetric that being a [[monoidal monad]], as it lacks the [[commutative monad|commutativity]] property. A _costrength_ is a similar notion, where the action is on the right.
* A strength for a monad is a way of creating "slices", expressions over tensor products which are trivial in the first component. (The costrength gives expressions which are trivial in the second component.)
* A strong monad is a [[tensorial strength|strong endofunctor]] with a monad structure which is compatible with the strength.
* If $V$ is a [[monoidal closed category]], then a strong monad is the same thing as a $V$-[[enriched monad]], and a costrength is the same thing as a pointwise structure for the monad on the [[internal homs]]. In particular, every monad on [[Set]] is canonically strong.

On a [[symmetric monoidal category]], strength and costrength, if they exist, can be obtained from one another.

Under some conditions, the strength is a [[property-like structure]].

A more general notion of strength allows for general $V$-[[actegories]] instead of just the canonical action of $V$ on itself (see below).


## Abstract definition 

+-- {: .num_defn}
###### Definition

For $V$ a [[monoidal category]] a **strong monad** over $V$ is a [[monad]] in the $2$-[[2-category|category]] $V\text{-}Act$ of left $V$-[[actegory|actegories]] on [[category|categories]].
=--

The classical definition of strength is on the category $V$ itself, regarded as equipped with the canonical $V$-action on itself. The definition is useful in the general case too. 

The extra [[structure]] that a strong monad has as opposed to the underlying monad on [[Cat]] is called **strength**.

Dually, a **costrength** is the analogous concept where $V$ is instead acting on the right.


### Details 

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

Then the [usual diagrams](#concrete_definition) that specify a strong monad


* unitalness and functoriality of the component functor of $T$;

* naturalness of unit and product modifications.


## Concrete definition

A _strong monad_ over a [[monoidal category]] $(C,\otimes,1)$ is a monad $(T, \eta, \mu)$ together with a natural transformation $t_{A,B}:A \otimes T B \to T(A\otimes B)$, called the _strength_, such that the following diagrams commute.

"Strengthening with 1 is irrelevant" (and plays well with the [[unitors]]):
\begin{tikzcd}[column sep=small, nodes={scale=1.25}]
& TA \ar{ddr}{\cong} \ar{ddl}[swap]{\cong} \\ \\
1 \otimes TA \ar{rr}{t_{1,A}} && T(1\otimes A)
\end{tikzcd}

+-- {: .query}
  I think it only plays well with the left unitor?
=--

"Consecutive applications of strength commute" (and play well with the [[associators]]):
\begin{tikzcd}
(A\otimes B) \otimes TC \ar{d}{\cong} \ar{rr}{t_{A\otimes B, C}} && T((A\otimes B)\otimes C) \ar{d}{\cong} \\
A \otimes (B\otimes TC) \ar{r}{A\otimes t_{B,C}} & A\otimes T(B\otimes C) \ar{r}{t_{A,B\otimes C}} & T(A\otimes(B\otimes C))
\end{tikzcd}

"Strength commutes with the monad unit":
\begin{tikzcd}[column sep=small, nodes={scale=1.25}]
& A \otimes B \ar{ddl}[swap]{A\otimes\eta_B} \ar{ddr}{\eta_{A\otimes B}} \\ \\
A\otimes TB \ar{rr}{t_{A,B}} && T(A\otimes B)
\end{tikzcd}

"Strength commutes with the monad multiplication":
\begin{tikzcd}
A\otimes TTB \ar{d}{A\otimes\mu_B} \ar{r}{t_{A,TB}} & T(A\otimes TB) \ar{r}{Tt_{A,B}} & TT(A\otimes B) \ar{d}{\mu_{A\otimes B}} \\
A\otimes TB \ar{rr}{t_{A,B}} && T(A\otimes B)
\end{tikzcd}

More generally, if a monoidal category $V$ acts on a category $C$
\[
\bullet : V\times C\to C
\]
then a $V$-strength for a monad $T$ on $C$ is a family of morphisms
$t_{A,B}:A\bullet T(B)\to T(A\bullet B)$ satisfying similar commutative diagrams. 


In particular, the underlying [[endofunctor]] of a strong monad is a [[strong functor]].


### Costrength

A __costrength__ for the monad $T$ is a natural transformation $s_{A,B}:T A \otimes B \to T(A\otimes B)$ satisfying analogous diagrams to those for the strength.

Note that the "co-" in "costrength" does _not_ refer to the [[opposite category]]; instead it refers to the reversal of the tensor product, $A\otimes^{rev} B = B\otimes A$.  The terminology also makes sense in the context of [[closed monoidal categories]], where strength and costrength appear on the two sides of the [[internal hom]]. See [the dedicated section](#costrength_and_pointwise_structure) for the details.

When the category $C$ is [[symmetric monoidal category|symmetric monoidal]], the [[braiding]] $b$ allows to obtain a strength from a costrength and vice versa,
\begin{tikzcd}
T A \otimes B \ar{r}{b_{T A,B}}[swap]{\cong} & B\otimes T A \ar{r}{t_{B,A}} & T(B \otimes A) \ar{r}{Tb_{B,A}}[swap]{\cong} & T(A\otimes B) .
\end{tikzcd}

A __bistrength__ is a strength and a costrength such that the two induced maps $(X\otimes T Y) \otimes Z \to T((X\otimes Y)\otimes Z$ agree.  If the category is symmetric monoidal, then $T$ is a [[commutative monad]] if it is equipped with a strength (hence also a costrength) such that the two induced maps $T X \otimes T Y \to T(X\otimes Y)$ agree.


## Examples

Every monad on [[Set]] with its [[cartesian product]] is canonically strong (see below for why). 

* The strength for the [[list monad]] works in the following way. Given sets $X$ and $Y$, the strength is the map
$$
(x,[y_1,\dots,y_n]) \; \mapsto \; [(x,y_1),\dots,(x,y_n)] .
$$
In other words, it turns an element of $X$ and a list of elements of $Y$ into a list of elements of $X\times Y$, canonically.

* For the left [[action monad]] (on [[Set]] or on any other [[monoidal category]]) relative to a [[monoid]] or [[monoid object]] $M$, the costrength is inherited by the [[associator]] as follows (see [Brandenburg '14, Example 6.3.4](#Brandenburg2014)),
\begin{tikzcd}
(M \otimes X) \otimes Y \ar{r}{a_{M,X,Y}}[swap]{\cong} & M \otimes (X \otimes Y) .
\end{tikzcd}
* On a [[symmetric monoidal category]], a strength for a left action monad can be obtained analogously, using the [[braiding]]. (For right actions, the braiding is not needed.)
In that case, this strength is [[commutative monad|commutative]] precisely if $M$ is [[commutative monoid|commutative as a monoid]] (see [Brandenburg '14, Example 6.3.12](#Brandenburg2014)).

* For [[probability monads]] on [[cartesian monoidal categories]], the strength creates "slices", or probability distributions which are deterministic in one variable. For the [[Giry monad]], for example, the strength for measurable spaces $X$ and $Y$ is the map
$$
(x,p) \;\mapsto\; \delta_x\otimes p
$$
for all $x\in X$ and $y\in P Y$. This strength is [[commutative monad|commutative]] and it allows to define easily the [[product of measures]]. Most probability monads behave analogously.
(Note that the category [[Meas]] has another [[monoidal structure]], which is closed, different from the [[cartesian product]]. For that monoidal structure, the Giry monad is not strong - see [Sato '16](#sato).)


## Interaction with the Kleisli category

+-- {: .query}
Is what's written here somehow the same as the abstract definition?
Can we be more general than the Kleisli category and pick an arbitrary adjunction?
=--

Given a monad $M : C \to C$ on a monoidal category $(C, \otimes, I)$, let $Kl(M)$ be the [[Kleisli category]] of $M$ with $J : C \to Kl(M)$. If $X \in Obj(C)$, write $[X] \in Obj(Kl(M))$ for the corresponding object in the Kleisli category. Moreover, given $f : X \to MY$, write $[f] : [X] \to [Y]$.

Then there is a correspondence between

* strengths of $M$,
* functorial operations $\odot : C \times Kl(M) \to Kl(M)$ that are
  * left unital: $I \odot A \cong A$ (naturally),
  * right unital: $X \odot [I] \cong JX$ (naturally),
  * mixed associative: $(X \otimes Y) \odot [Z] \cong X \otimes (Y \odot [Z])$ (naturally),
  * subject to coherence laws.

+-- {: .query}
Right unitality entails that $X \odot [Y] \cong X \otimes Y \odot [I] \cong [X \otimes Y]$ so basically $\odot$ is fixed on objects. Is it better to fix this on the nose? Is this evil?
=--
  
This correspondence is used in the formulation of [[call-by-push-value]] as an adjoint logic.

Indeed, assume that $M$ is strong. Then we define

* $X \odot [Y] := [X \otimes Y]$
* $f^{X \to X'} \odot [g]^{[Y] \to [Y']} := [t_{X', Y'} \circ (f \otimes g)]$

This preserves

* identity because the strength commutes with the unit,
* composition because the strength commutes with monad multiplication.

This is

* left unital on objects (by mapping the left unitor into the Kleisli category),
* naturally so because the strength is compatible with the left unitor,
* right unital on objects (by mapping the right unitor into the Kleisli category),
* naturally so because the strength commutes with the unit (!),
* mixed associative on objects (by mapping the assiciator into the Kleisli category),
* naturally so because the strength is compatible with the associator.

The coherence laws will be satisfied.

Conversely, assume $\odot$ is given. Then we define
\[
  [t_{X, y}] : J(X \otimes MY) \cong X \otimes MY \odot [I] \cong X \odot JMY \xrightarrow{1_X \odot [1_{MY}]} X \odot JY \cong X \otimes Y \odot [I] \cong J(X \otimes Y).
\]
This is natural and

* commutes with the unit because $\odot$ preserves identity:

\begin{centre}
\begin{xymatrix}
J(X \otimes Y)
  \ar@{}[r]|{\cong}
  \ar[d]_{J(1_X \otimes \eta_Y)}
&
X \odot JY
  \ar@{=}[rd]^{1_X \odot J1_Y = 1_{X \odot JY}}
  \ar[d]_{1_X \otimes J\eta_{Y}}
\\
J(X \otimes MY)
  \ar@{}[r]|{\cong}
&
X \odot JMY
  \ar[r]_{1_X \odot [1_{MY}]}
&
X \odot JY
  \ar@{}[r]|{\cong}
&
J(X \otimes Y)
\end{xymatrix}
\end{centre}

* commutes with multiplication because $\odot$ preserves composition (similar reasoning),
* is compatible with the left unitor by naturality and the coherence laws,
* is compatible with the associator by naturality and the coherence laws.


## On closed and monoidal closed categories

If the category $C$ is [[closed monoidal category|monoidal closed]], strength and costrength induce particular structures on the [[internal homs]]. 

In this section, let $(C,\otimes 1)$ be monoidal closed, with internal hom denoted by $[-,-]$. Denote the [[unit of an adjunction|unit of the hom-tensor adjunction]] by $\eta_X:X \to [Y,X\otimes Y]$ and the counit (or _evaluation map_, see [[internal hom#EvaluationMap|internal hom - evaluation map]]) by $\epsilon_Y:X\otimes [X,Y]\to Y$.

+-- {: .query}
The unit is the unit of $- \otimes Y \dashv [Y, -]$ applied to $X$. The co-unit is the co-unit of $X \otimes - \dashv [X, -]$ applied to $Y$. The swapping of the variable names is already confusing, but more importantly, we're tensoring on the other side. Either we're assuming that the category is symmetric monoidal (then we should mention so), or we're not but then we should be consistent.
=--

### Strong monads are enriched monads

The original reference for this part is [Kock '72](#kock72). Note that in there the terminology is a little different:

* The strength as defined here is called _tensorial strength_;
* The enrichment of the monad is called _strength_.

Since the two notions are equivalent, the different terminology does not lead to confusion (once the equivalence is established).
For more on this see also the treatment at [[tensorial strength#description|the related discussion for strong endofunctors]].

First of all, a [[tensorial strength|strong endofunctor]] $T$ on a closed monoidal category $C$ is "the same thing" as a $C$-[[enriched functor|enriched endofunctor]]. To see this, note that an enriched endofunctor amounts to a [[natural transformation]] 
$$
[X,Y] \;\to\; [T X, T Y] 
$$
which satisfies the usual [[identity]] and [[composition]] rules (see [[enriched functor]]).
Notice also that a map as above, by the hom-tensor adjunction (or [[currying]]) is equivalently specified by a map
$$
[X,Y] \otimes T X \;\to\; T Y.
$$
The latter is provided by the strength $t$ as follows,
\begin{tikzcd}
{[X,Y]} \otimes T X \ar{r}{t} & T\big({[X,Y]}\otimes X \big) \ar{r}{T\epsilon} & TY.
\end{tikzcd}

Conversely, given a map $t':[X,Y] \otimes T X \to T Y$ natural in $Y$ and [[extranatural]] in $X$, one can define a strength as
\begin{tikzcd}
X \otimes T Y \ar{r}{\eta\otimes TY} & {[Y,X\otimes Y]} \otimes T Y \ar{r}{t'} & T(X\otimes Y).
\end{tikzcd}

One can verify that these assignments are inverse to each other. Moreover, the [strength diagrams](#concrete_definition) for $t$ commute if and only the resulting assigment is indeed an [[enriched monad]], and vice versa. 


#### Example in Set

_Every monad on [[Set]] is [[Set]]-enriched. In particular, it is strong._

Given a monad $T$ on [[Set]], the assignment 
$$
[X,Y] \;\to\; [T X, T Y] 
$$
is just the action of $T$ on the [[morphisms]],
$$
\mathrm{Hom}(X,Y) \;\to\; \mathrm{Hom}(T X, T Y) .
$$
Under [[currying]], this corresponds to the map 
\begin{tikzcd}[row sep=0, column sep=large, nodes={scale=1.25}]
\mathrm{Hom}(X,Y) \times T X \ar{r} & T Y \\
(f,k) \ar[mapsto]{r} & Tf (k) .
\end{tikzcd}
For example, for the [[list monad]], the map is given by
\begin{tikzcd}[row sep=0, column sep=large, nodes={scale=1.25}]
\mathrm{Hom}(X,Y) \times L X \ar{r} & L Y \\
(f,{[x_1,\dots,x_n]}) \ar[mapsto]{r} & {[f(x_1),\dots,f(x_n)]} .
\end{tikzcd}

The strength obtained this way is the usual strength of the list monad,
\begin{tikzcd}[row sep=0, column sep=large, nodes={scale=1.25}]
X \times T Y \ar{r}{\eta\times \mathrm{id}} & \mathrm{Hom}(Y,X\times Y) \times T Y \ar{r}{t'} & T(X\times Y) \\
(x,{[y_1,\dots,y_n]}) \ar[mapsto]{r} & \big( y\mapsto (x,y) , {[y_1,\dots,y_n]}\big) \ar[mapsto]{r} & {[(x,y_1),\dots,(x,y_n)]}.
\end{tikzcd}
(Compare with the [example above](#examples).)


### Costrength and pointwise structure

The reference for this part can be found in [Kock '71, Section 1](#kock71). 

Let's give a preliminary definition. A _pointwise structure_ or _cotensorial strength_ ([Kock '72](#kock72)) of a [[monad]] $T$ on a [[closed category]] $C$ is a [[natural transformation]]
$$
s' _{X,Y}: T[X,Y] \to [X, T Y]
$$
such that the following diagrams commute. 

* Compatibility with the unit of the monad $\eta^T$: 
\begin{tikzcd}[column sep=small, row sep=large, nodes={scale=1.25}]
& {[X,Y]} \ar{dl}[swap]{\eta^T} \ar{dr}{{[X,\eta^T]}} \\
T{[X,Y]}  \ar{rr}[swap]{s'} && {[X,TY]}
\end{tikzcd}

* Compatibility with the multiplication of the monad $\mu^T$:
\begin{tikzcd}[row sep=large, nodes={scale=1.25}]
TT{[X,Y]} \ar{dd}{\mu^T} \ar{rr}{Ts'} && T{[X,TY]} \ar{d}{s'} \\
&& {[X,TTY]} \ar{d}{{[X,\mu^T]}} \\
T{[X,Y]} \ar{rr}{s'} && {[X,TY]}
\end{tikzcd}

* Compatibility with the "unitor of the closed structure", the natural isomorphism $i:X\to [1,X]$ (see [[closed category#basic_definition]]):
\begin{tikzcd}[column sep=small, row sep=large, nodes={scale=1.25}]
& T X \ar{dl}[swap]{Ti} \ar{dr}{i} \\
T{[1,X]} \ar{rr}{s'} && {[1,T X]}
\end{tikzcd}

* Compatibility with the (curried) composition morphism of the closed structure, the morphism $l:[Y,Z]\to [[X,Y],[Y,Z]]$ (see [[closed category#basic_definition]]):
\begin{tikzcd}[sep=large, nodes={scale=1.25}]
T{[Y,Z]} \ar{rr}{s'} \ar{d}{Tl} && {[Y, T Z]}  \ar{d}{l} \\
T{[{[X,Y]}, {[X,Z]}]} \ar{r}{s'} & {[{[X,Y]}, T{[X,Z]}]} \ar{r}{{[\mathrm{id}, s']}} & {[{[X,Y]}, {[X, T Z]}]}
\end{tikzcd}


#### Equivalence with the notion of costrength

Suppose now that $C$ is a [[monoidal closed category]]. In this case, a pointwise structure and a costrength coincide. Let's see how.
Given a costrength $s:T X\otimes Y \to T(X\otimes Y)$ we can obtain a pointwise structure as follows,
\begin{tikzcd}[nodes={scale=1.25}, column sep=large]
T{[X,Y]} \ar{r}{\eta} & {[X,T{[X,Y]}\otimes X]} \ar{r}{{[X,s]}} & {[X,T({[X,Y]}\otimes X)]} \ar{r}{{[X,T\epsilon]}} & {[X,TY]} .
\end{tikzcd}

Conversely, given a pointwise structure $s':T[X,Y]\to [X,TY]$ we can obtain a costrength as
\begin{tikzcd}[nodes={scale=1.25}, column sep=large]
TX \otimes Y \ar{r}{\eta\otimes Y} & T{[Y,X\otimes Y]} \otimes Y \ar{r}{s'\otimes Y} & {[Y,T(X\otimes Y)]} \otimes Y \ar{r}{\epsilon} & T(X\otimes Y ) .
\end{tikzcd}

By [[currying]] it can be shown that the respective diagrams of costrength and pointwise structure are equivalent (the unit condition corresponds to the unit condition, and so on).



#### Algebra structure on the internal homs

A pointwise structure allows in particular to _form pointwise algebra structures_, in the following sense. Given a $T$-[[algebra over a monad|algebra]] $(A,a)$, and any object $X$, we can canonically define an algebra structure on $[X,A]$, given by

\begin{tikzcd}[nodes={scale=1.25}, column sep=large]
T{[X,A]} \ar{r} & {[X,TA]} \ar{r}{{[X,a]}} & {[X,A]} .
\end{tikzcd}

The diagrams above assure us that  

* This map gives indeed a $T$-algebra;
* $A$ and $[1,A]$ are canonically isomorphic as $T$-algebras too;
* The internal precomposition with a morphism $f:W\to X$ gives a morphism of $T$-algebras $[X,A]\to [W,A]$.



#### Example in Set

Consider the [[list monad]] on [[Set]]. The usual costrength gives the following pointwise structure:
\begin{tikzcd}[row sep=0, column sep=small, nodes={scale=1.25}]
L{[X,Y]} \ar{r}{\eta} & {[X,L{[X,Y]}\times X]} \ar{r}{{[X,s]}} & {[X,L({[X,Y]}\times X)]} \ar{r}{{[X,L\epsilon]}} & {[X,LY]} \\
{[f,g,h]} \ar[mapsto]{r} & \big( x\mapsto ({[f,g,h]},x) \big) \ar[mapsto]{r} & \big( x\mapsto {[(f,x), (g,x), (h,x)]}\big) \ar[mapsto]{r} & \big( x\mapsto {[f(x),g(x),h(x)]} \big) 
\end{tikzcd}

Indeed, this turns a list of functions into a function into lists, that maps $x\in X$ to the list of the results. 

If $(A,a)$ is an $L$-[[algebra over a monad|algebra]], i.e. a [[monoid]], this allows to equip function spaces with a monoid structure as follows: 
\begin{tikzcd}[row sep=0, column sep=small, nodes={scale=1.25}]
L{[X,A]} \ar{r} & {[X,LA]} \ar{r}{{[X,a]}} & {[X,A]} \\
{[f,g,h]} \ar[mapsto]{r} & \big( x\mapsto {[f(x),g(x),h(x)]} \big) \ar[mapsto]{r} & \big( x\mapsto f(x) + g(x) + h(x) \big)
\end{tikzcd}

In other words, functions into a monoid form canonically a monoid under _pointwise addition_ (or multiplication).  


## Moggi's typing rules and parameterized definition

Moggi ([Moggi '89](moggi89)) proposed the following typing rules for a sequence operator:
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

In other words, a monad being strong is a [[property-like structure]] in a category with enough points. 


## Related concepts

* [[tensorial strength]]

* [[monoidal monad]]

* [[commutative monad]]

* [[enriched monad]]

* [[monad (in computer science)]]

## References 

Strong monads were defined by Kock, as an alternative description of enriched monads.

* {#kock72} [[Anders Kock]], *Strong functors and monoidal monads*, Arch. Math. (Basel) 23 (1972), 113--120.


* {#kock70} [[Anders Kock]], _Monads on symmetric monoidal closed categories_, Arch. Math. 21 (1970), 1--10. 
[PDF](http://home.imf.au.dk/kock/SFMM.pdf).

* {#kock71} [[Anders Kock]], _Closed categories generated by commutative monads_, 1971 ([[KockMonoidalMonads.pdf:file]])


* H. Lindner, _Commutative monads_ in _Deuxi&#233;me colloque sur l'alg&#233;bre des cat&#233;gories_. Amiens-1975. R&#233;sum&#233;s des conf&#233;rences, pages 283-288. Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle cat&#233;goriques, tome 16, nr. 3, 1975.

* {#Keigher78} [[William Keigher]], _Symmetric monoidal closed categories generated by commutative adjoint monads_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 19 no. 3 (1978), p. 269-293  ([NUMDAM](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1978__19_3_269_0), [pdf](http://archive.numdam.org/article/CTGDC_1978__19_3_269_0.pdf))

More resources and surveys:

* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ ([arXiv:1205.0101](http://arxiv.org/abs/1205.0101))

* {#Brandenburg2014} [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))
Usually strong monads are described explicitly in terms of the components of the above structure. The above repackaging of that definition appears in the blog post

* [[John Baez]], _The Monads Hurt My Head -- But Not Anymore_ ([blog](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025476))

Strong monads are important in Moggi's theory of notions of computation (see [[monad (in computer science)]]):

* [[Eugenio Moggi]]. Notions Of Computation And Monads. Information And Computation. 1991;93:55&#8211;92. 
* {#moggi89} [[Eugenio Moggi]]. Computational Lambda-Calculus and Monads. Proceedings of the Fourth Annual Symposium on Logic in Computer Science. 1989. p. 14&#8211;23. 

More in-text references:

* {#sato} Tetsuya Sato, _The Giry monad is not strong for the canonical symmetric monoidal closed structure on Meas_,   Journal of Pure and Applied Algebra, Volume 222, Issue 10, October 2018, Pages 2888-2896. ([arXiv:1612.05939](https://arxiv.org/abs/1612.05939))


[[!redirects strong monads]]
[[!redirects strength of a monad]]
[[!redirects costrong monad]]
[[!redirects co-strong monad]]
[[!redirects costrong monads]]
[[!redirects co-strong monads]]
[[!redirects costrength of a monad]]
[[!redirects co-strength of a monad]]
[[!redirects strength and costrength]]
[[!redirects strengths and costrengths]]
[[!redirects strength and costrength of a monad]]
[[!redirects strengths and costrengths of monads]]