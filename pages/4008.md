
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A connected limit is the [[limit]] of a [[diagram]] that has just one [[connected component]].  For example, the [[product]] of two objects is not a connected limit because the relevant diagram has two connected components.  A [[pullback]], on the other hand, is a connected limit.

## Definition

A **connected limit** is a [[limit]] over a [[connected category]]. Similarly, a **connected colimit** is a colimit over a connected category. 

## Examples

The following are all connected limits:

* [[pullbacks]]

* [[wide pullbacks]]

* [[equalizers]]

* [[cofiltered limits]]

* [[split idempotents]]

## Properties

### Construction from pullbacks and equalizers

+-- {: .num_theorem #PbEqToFinConnLim}
###### Theorem
If a category $C$ has [[pullbacks]] and [[equalizers]], then it has all [[finite limit|finite]] connected limits.
=--
+-- {: .proof}
###### Proof
Let $I$ be a finite connected category and $F\colon I\to C$ a functor.  Since $I$ is connected, it is inhabited; choose some object $x_0\in I$.  For each object $x\in I$, let $\ell(x)$ be the length of the shortest [[zigzag]] from $x_0$ to $x$.  Now order the objects of $I$ as $x_0, x_1, \dots, x_n$ such that for all $i$ we have $\ell(x_i) \le \ell(x_{i+i})$.

Now we inductively define objects $P_i\in C$, for $0\le i\le n$, with projections $p_{i j}\colon P_i \to F(x_j)$ for $j\le i$.  We begin with $P_0 = x_0$ and $p_{0 0}= 1_{x_0}$.  Assuming $P_i$ and $p_{i j}$ defined, choose a zigzag from $x_0$ to $x_{i+1}$ of minimal length, say
$$ x_0 \leftrightarrow y_1 \leftrightarrow \dots \leftrightarrow y_k \leftrightarrow x_{i+1}. $$
By our choice of the ordering of the objects of $I$, we have $y_k = x_j$ for some $j\le i$, and thus we have $q = p_{i j}\colon P_i \to y_k$.

If the final arrow $y_k \leftrightarrow x_{i+1}$ in the zigzag is directed as $y_k \to x_{i+1}$, then let $P_{i+1} = P_i$, let $p_{i+1, i+1}$ be the composite $P_i \xrightarrow{q} F(y_k) \to F(x_{i+1})$, and keep the other $p_{i j}$ unchanged.  On the other hand, if $y_k \leftrightarrow x_{i+1}$ is directed as $y_k \leftarrow x_{i+1}$, let $P_{i+1}$ be the pullback
$$ \array{
& P_{i+1} & \to & P_i \\
^{p_{i+1,i+1}} & \downarrow & & \downarrow^q \\
& F(x_{i+1}) & \to & F(y_k)
}$$
and define $p_{i+1,j}$ for $j\le i$ by composition with $P_{i+1}\to P_i$.

At the end of this procedure, we have an object $P_n$ with projections $p_{n,j}\colon P_n \to F(x_j)$ for all objects $x_j\in I$.  Now we order the morphisms in $I$ as $g_0,\dots,g_m$ and define, inductively, an object $Q_i$ with a morphism $q_i\colon Q_i \to P_n$.  We begin with $Q_0 = P_n$ and $q_0 = 1_{P_n}$.  Given $Q_i$ and $q_i$, we let $e\colon Q_{i+1} \to Q_{i}$ be the equalizer of $F(g_{i+1}) \circ p_{n,?} \circ q_i$ and $p_{n,?} \circ q_i$, where the ?s denote the indices of the objects that are the source and target of $g_{i+1}$.  We then set $q_{i+1} = q_i \circ e$.

At the end of this procedure, we have an object $Q_{m+1}$ together with a cone over the diagram $F$, which is easily verified to be a limit of $F$.
=--

Similarly, arbitrary connected limits may be built from [[wide pullbacks]] and equalizers. 

+-- {: .num_theorem #internalsum}
###### Theorem 
Let $C$ be (finitely) complete, and let $X$ be an object of $C$. Then the forgetful functor 

$$\sum_X: C/X \to C$$ 

preserves and reflects (finite) connected limits. 
=-- 

+-- {: .proof}
###### Proof 
The wide pullback of the diagram $f_i: X_i \to X$ where $f_i = 1_X$ for all $i$ is clearly $X$, as is the equalizer of the pair of identity arrows. Since the product functor $C \times C \to C$ preserves arbitrary limits, we see that 

$$X \times lim (c_i \stackrel{g_i}{\to} c) = (lim X_i \stackrel{f_i = 1_X}{\to} X) \times (lim c_i \stackrel{g_i}{\to} c) = lim X \times c_i \stackrel{1 \times g_i}{\to} X \times c,$$ 

i.e., $X \times -$ preserves wide pullbacks. The same line of argument shows $X \times -$ preserves equalizers, so $X \times -$ preserves connected limits. 

The functor $X \times -$ carries a canonical [[comonad]] structure, whose category of coalgebras is $C/X$. The forgetful functor $C/X \to C$ is comonadic, and thus preserves and reflects any class of limits preserved by the comonad $X \times -$. Thus $\sum_X: C/X \to C$ preserves and reflects all connected limits. 
=-- 

### Preservation from wide pullbacks

Recall that a [[wide pullback]] is a limit over a [[diagram]] whose underlying shape is the [[poset]] obtained by [[free functor|freely]] adjoining a [[top element|terminal element]] to a [[set|discrete poset]], which is certainly connected.

It is not true that if $C$ has wide pullbacks then it has connected limits.  The [[saturated class of limits|saturation]] of the class of wide pullbacks is the class of connected and "simply connected" limits (limits over categories $C$ whose groupoid reflection $\Pi_1(C)$ is trivial).

However, the following is true.

+-- {: .num_theorem #PreservesWidePbToConnected}
###### Theorem
Let $C$ be a complete category, and let $D$ be [[locally small category|locally small]]. Then a functor $G\colon C \to D$ preserves connected limits if and only if it preserves wide pullbacks. 
=-- 

+-- {: .proof}
###### Proof
The forward direction is clear since wide pullbacks are examples of connected limits. Now suppose $G\colon C \to D$ preserves wide pullbacks. Then 
\[C \stackrel{G}{\to} D \stackrel{hom(d, -)}{\to} Set \label{Gwithhom}  \]
preserves wide pullbacks for every object $d$ of $D$. Put $I = hom(d, G 1)$. The underlying functor 
$$\sum\colon Set/I \to Set$$ 
reflects and preserves connected limits and in particular wide pullbacks, so that the evident lift 
$$\hom(d, G-)\colon C \to Set/I$$ 
preserves wide pullbacks. It also preserves the terminal object, hence by [this proposition](/nlab/show/wide+pullback#WidePbToComplete) it preserves arbitrary limits. Therefore the composite 
$$C \stackrel{\hom(d, G-)}{\to} Set/I \stackrel{\sum}{\to} Set$$ 
preserves connected limits, for every object $d$. Since this is the same composite as in \eqref{Gwithhom}, and since the representables $\hom(d, -)$ jointly reflect arbitrary limits, we conclude that $G$ preserves connected limits. 
=-- 

The analogous argument works for finite limits. In particular, for $C$ finitely complete, a functor $G\colon C \to D$ that preserves pullbacks also preserves [[equalizers]].


## Related pages

* [[parametric right adjoint]]

* [[connected category]] 

* [[wide pullback]] 

* [[wide pushout]] 

## References

* [[Robert Paré]], *Simply connected limits*.  Can. J. Math., Vol. XLH, No. 4, 1990, pp. 731-746, [CMS](http://math.ca/10.4153/CJM-1990-038-6)

[[!redirects connected limit]]
[[!redirects connected limits]]
