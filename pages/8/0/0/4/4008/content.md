#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **connected limit** is a [[limit]] over a [[connected category]]. Similarly, a **connected colimit** is a colimit over a connected category. 


## Connection with wide pullbacks

A basic example of a connected limit is a [[wide pullback]], where the limit is taken over a diagram whose underlying shape is the [[poset]] obtained by freely adjoining a [[top element|terminal element]] to a [[set|discrete poset]]. 

+-- {: .un_lem}
######Lemma 
A category $C$ with all wide pullbacks and a [[terminal object]] $1$ is [[complete category|complete]]. If $C$ is complete and $F: C \to D$ preserves wide pullbacks and the terminal object, then it preserves all limits. 
=-- 

+-- {: .proof}
######Proof 
To build up arbitrary products $\prod_{i \in I} c_i$ in $C$, take the wide pullback of the family $c_i \to 1$. Then to build equalizers of diagrams $f, g: c \stackrel{\to}{\to} d$, construct the pullback of the diagram 
$$\array{
 & & d \\
 & & \downarrow \delta \\
c & \underset{\langle f, g \rangle}{\to} & d \times d
}$$ 
From products and equalizers, we can get arbitrary limits. 
=--

+-- {: .un_thm}
######Theorem
Let $C$ be a complete category, and let $D$ be [[locally small category|locally small]]. Then a functor $G: C \to D$ preserves connected limits if and only if it preserves wide pullbacks. 
=-- 

+-- {: .proof}
######Proof
The forward direction is clear since wide pullbacks are examples of connected limits. Now suppose $G: C \to D$ preserves wide pullbacks. Then 
$$C \stackrel{G}{\to} D \stackrel{hom(d, -)}{\to} Set \qquad (1)$$ 
preserves wide pullbacks for every object $d$ of $D$. Put $I = hom(d, G 1)$. Then the underlying functor 
$$\sum: Set/I \to Set$$ 
reflects and preserves connected limits and in particular wide pullbacks, so that the evident lift 
$$\hom(d, G-): C \to Set/I$$ 
preserves wide pullbacks. It also preserves the terminal object, hence by the lemma it preserves arbitrary limits. Therefore the composite 
$$C \stackrel{\hom(d, G-)}{\to} Set/I \stackrel{\sum}{\to} Set$$ 
preserves connected limits, for every object $d$. Since this is the same composite as in (1), and since the representables $\hom(d, -)$ jointly reflect arbitrary limits, we conclude that $G$ preserves connected limits. 
=-- 

In particular, for $C$ complete, a functor $G: C \to D$ that preserves wide pullbacks also preserves [[equalizers]]. 


## Related pages

* [[parametric right adjoint]]


[[!redirects connected limit]]
[[!redirects connected limits]]
