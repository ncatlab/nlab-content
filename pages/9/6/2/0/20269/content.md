#Contents#
* Contents
{:toc}

## Idea

The order type of a [[partially ordered set]] (poset) $P$ is an invariant $ot(P)$ of the poset which is finer than its [[cardinal number]] $|P|$. The cardinal numbers classify sets according to how many elements they contain, however they don't pay attention to any potential order-theoretic properties on the sets in question -- for example

\begin{centre}
$\omega+1\cong\omega$
\end{centre}

in **Set** but not in **Pos** since the bijections in **Set** all send $\omega$ to some finite ordinal and thusly don't preserve ordering. This is expressed in terms of cardinalities and order types by observing that $|\omega+1|=|\omega|=\omega$ but $ot(\omega+1)=\omega+1\neq\omega=ot(\omega)$ since each ordinal is its own order type but generally not its own cardinal number.

##Definition

Let $P$ be a poset. We say that another poset $Q$ has the same **order type** as $P$ iff there exists an order preserving bijection $P\cong Q$, or equivalently an iso $P\cong Q\in {Hom}_{Pos}$. We define an equivalence relation $\sim$ on posets by 

\begin{centre}
$P\sim Q\iff \exists f:P\cong Q\in {Hom}_{Pos}$,
\end{centre}

and we define the order type of $P$, denoted $ot(P)$, to be either the equivalence class $\sim/P$ or an arbitrary representative of the equivalence class $\sim/P$ depending on context.

### Examples

We have that $ot(\alpha)\cong\alpha$ in **Pos** for each ordinal $\alpha$ by definition, and further the order type of any well-ordered sets 'is' the ordinal one would expect (up to iso):

$$ot(\{0,1,4,5\})\cong4,$$ 

$$ot(\{0,2,4,6,\dots\omega,\omega+2,\omega+4,\omega+6\})\cong\omega+4,$$ 

$$\vdots$$

For well-ordered posets it seems natural to take the order type to be the ordinal representative of the equivalence class, yielding the literal equalities in the idea section above, however this is not strictly necessary.

The order type of the negative integers is denoted by $^*\omega$ and the order type of the rationals is denoted by $\eta$, and neither of these order types have representatives in the ordinals since they aren't well-ordered.

## References 

* Cantor, Georg [ "Ueber eine Eigenschaft des Inbegriffes aller reellen algebraischen Zahlen"](https://gdz.sub.uni-goettingen.de/download/pdf/PPN243919689_0077/LOG_0014.pdf)