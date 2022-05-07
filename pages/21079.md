[[!redirects action monads]]
[[!redirects action monads]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _action monad_ or _writer monad_ is a construction generalizing many seemingly different concepts across mathematics and computer science.
It could be intuitively understood in the following ways. First of all, fix a [[group]] or [[monoid]] $M$.

* It is the [[monad]] associated to the [[free-forgetful adjunction]] between [[G-set|M-sets]] (sets equipped with an $M$-[[action]]) and [[sets]].
* It is the monad whose [[algebra over a monad|algebras]] are $M$-sets and whose morphisms are [[equivariant maps]].
* It is the [[monad in computer science|monad modeling computational effects]] that can be added or concatenated (using the multiplication map of $M$), such as writing into a log file or standard output to screen.

If one, more generally, replaces [[sets]] and a [[monoid]] with a [[monoidal category]] and an [[internal monoid]], a similar construction can be given. This generalizes, for example, the [[action]] that [[rings]] have on their [[modules]], and that [[Lie groups]] have on [[manifolds]].


## Definition

### In the category of sets

Let $M$ be a [[monoid]] with [[unit]] $e:1\to M$ and [[multiplication]] $\cdot:M\times M \to M$. The (left) **$M$-action monad** is a [[monad]] on [[Set]] where

* The [[endofunctor]] maps a set $X$ to the set $M\times X$;

* The unit is given by 
\begin{tikzcd}
X \ar{r}{\cong} & 1\times X \ar{r}{e\times\mathrm{id}} & M\times X
\end{tikzcd}
for each object $X$;

* The multiplication is given by 
\begin{tikzcd}
M\times (M\times X) \ar{r}{\cong} & (M\times M)\times X \ar{r}{\cdot\times\mathrm{id}} & M\times X
\end{tikzcd}
for each object $X$.

The monad axioms follow from the monoid axioms for $M$.

There exists an analogous monad for _right_ actions, whose endofunctor maps $X$ to $X\times M$.


### In a general monoidal category

More generally, let $(C,\otimes,1)$ be a [[monoidal category]].
Let $M$ be a [[monoid object]] in $C$ with [[unit]] $e:1\to M$ and [[multiplication]] $\cdot:M\otimes M \to M$. The (left) **$M$-action monad** is a [[monad]] on $C$ where

* The [[endofunctor]] maps an object $X$ of $C$ to the object $M\otimes X$;

* The unit is given by 
\begin{tikzcd}
X \ar{r}{\cong} & 1\otimes X \ar{r}{e\times\mathrm{id}} & M\otimes X
\end{tikzcd}
for each object $X$;

* The multiplication is given by 
\begin{tikzcd}
M\otimes (M\otimes X) \ar{r}{\cong} & (M\otimes M)\otimes X \ar{r}{\cdot\otimes\mathrm{id}} & M\otimes X
\end{tikzcd}
for each object $X$.

Again, the monad axioms follow from the monoid axioms for $M$. (And again there is an analogous notion for right actions).



## Algebras

The [[algebra over a monad|algebras]] over the action monad for a monoid (or group) $M$ can be seen as the [[G-space|$M$-spaces]], i.e. sets or spaces equipped with an [[action]] of $M$ (hence the name). 

Plugging in the definition, an algebra over this monad is then a set $A$ together with a map $e:M\times A\to A$, such that the following diagrams commute. 
The algebra diagrams
 \begin{tikzcd}
 A \ar{dr}[swap]{\mathrm{id}} \ar{r}{\eta} & M\times A \ar{d}{e} &&   M \times M \times A \ar{d}{\mu} \ar{r}{\mathrm{id}_M\times e} & M\times A \ar{d}{e} \\
 & A && M \times A\ar{r}{e} & A .
 \end{tikzcd}

say equivalently that for all $a\in A$ and $m,n\in M$,
 $$
 1\cdot a= a, \qquad (m n)\cdot a = m\cdot (n\cdot a) .
 $$

 In other words, a $T_M$-algebra is exactly a set equipped with an $M$-[[action]] in the traditional group-theoretical sense.

This gives a way to talk about monoid and group [[actions]] [[internally]] to any [[monoidal category]], giving the notion of a [[module object]].


### Examples

* In the category of [[manifolds]] with their [[cartesian product]], an [[internal group]] is a [[Lie group]]. The algebras of the corresponding action monad are the manifolds equipped with the action of the Lie group, such as [[homogeneous spaces]]. 

* The same can be said about [[topological spaces]] and continuous actions of [[topological groups]]. 

* In the category [[Ab]] of [[abelian groups]] with their [[tensor product]], an [[internal monoid]] is a [[ring]]. The algebras of the resulting action monad are the [[modules]] over that ring. 

* In the category of [[endofunctors]] of a category $C$, an [[internal monoid]] is the same as a [[monad]] $T$. An algebra of the resulting action monad is an instance of a [[module over a monad|module over a monad]] $T$. 


## Properties

* For the case of group actions on sets, a $G$-set is [[free action|free as an action]] if and only if it is [[algebra over a monad#free_algebras|free as an algebra]] (up to isomorphism).
* The action monad $X\mapsto M\times X$ on [[Set]] is canonically [[strong monad|strong]], with the strength given by the [[associator]] (see [[strong monad#examples]]). It is [[commutative monad|commutative]] if and only if $M$ is commutative as a monoid. 
* More generally, in an arbitrary [[symmetric monoidal category]], the action monad induced by tensoring with an [[internal monoid]] is commutative if and only the monoid object is commutative. (See for example [Brandenburg, Example 6.3.12](#Brandenburg2014).)
* Any action monad canonically [[distributive law|distributes]] over a [[strong monad]] $T$, with the distributive law $M \otimes T X \to T(M\otimes X)$ induced by the strength.

## In computer science

The action monad in computer science is known under the name of **writer monad**. See also [[writer comonad]]. 

A way to motivate this name is to look at its Kleisli morphisms.
The following explanation is taken from [Perrone, Example 5.1.14](#notesperrone).

Let $M$ be a monoid, and let's write it additively. Denote by $T_M$ its _right_ writer monad. A Kleisli morphism of $T_M$ is a map $k:X\to Y\times M$. We can interpret it as a process which, when given an input $x\in X$, does not just produce an output $y\in Y$, but also an element of $M$. 
 For example, it could be energy released by a chemical reaction, or waste, or a cost of the transaction. In computer science, this is the behaviour of a function that computes a certain value, but that also writes into a log file (or to the standard output) that something has happened (the monoid operation being the concatenation of strings). For example, when you compile a tex document, a log file is produced alongside your output file. Hence the name "writer monad".
 
 Let's now look at the Kleisli composition. If we have processes $k:X\to Y\times M$ and $h:Y\to Z\times M$, then $k\circ_{kl} Y:X\to Z\times M$ is given by
 \begin{tikzcd}[row sep=0, column sep=large, nodes={scale=1.25}]
  X \ar{r}{k} & Y\times M \ar{r}{h\times \mathrm{id}_M} & Z\times M \times M \ar{r}{\mathrm{id}_X\times +} & Z\times M \\
  x \ar[mapsto]{r} & (y,m) \ar[mapsto]{r} & (z,n,m) \ar[mapsto]{r} & (z, n+m) .
 \end{tikzcd}
 What it does is as follows:

1. It executes the process $k$ with an input $x\in X$, giving as output an element of $y\in Y$ as well as a cost (or extra output) $m\in M$.
1. It executes the process $k$ taking as input the $y\in Y$ produced by $k$, giving an element $z\in Z$ as well as an extra cost $n\in M$. (All of this while keeping track of the first cost $m$.)
1. The two costs $m$ and $n$ are summed (or the extra outputs are concatenated). 


 So, for example, the cost of executing two processes one after another is the sum of the costs. The same is true about the release of energy in a chemical reaction, and about waste. 
 Just as well, executing two programs one after another will produce a concatenation of text in a log file (or two log files).




## Related concepts

* [[action]], [[G-set]], [[equivariant map]]

* [[internalization]]

* [[monoidal category]], [[monoid object]], [[group object]], [[module object]]

* [[monad]], [[algebra over a monad]]

* [[monad in computer science]], 

  * [[function monad]], [[writer comonad]]


## References 

* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ ([arXiv:1205.0101](http://arxiv.org/abs/1205.0101))

* {#Brandenburg2014} Martin Brandenburg, _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))

* {#notesperrone} [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_, Chapter 5. ([arXiv](http://arxiv.org/abs/1912.10642))



[[!redirects action monads]]
[[!redirects monoid action monad]]
[[!redirects monoid action monads]]
[[!redirects group action monad]]
[[!redirects group action monads]]
[[!redirects writer monad]]
[[!redirects writer monads]]
