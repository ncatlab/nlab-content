#Preliminaries#

Let $K$ be a [[category]] and write $arr(K)$ for the [[arrow category]] of $K$: the category with arrows of $K$ as objects and commutative squares $gu=vf$ as morphisms $(u,v) : f \rightarrow g$. We may also refer to a commutative square $gu=vf$ as a **lifting problem** between $f$ and $g$.

We say a morphism $f$ has the **left lifting property** with respect to a morphism $g$, or equivalently that $g$ has the **right lifting property** with respect to $f$, if for every commutative square $(u,v) :f \rightarrow g$, there is an arrow from the codomain of $f$ to the domain of $g$ such that both triangles commute. We call such an arrow a **lift** or a **solution** to the lifting problem $(u,v)$.

#Definition#

A **weak factorization system** on a category $K$ is a pair $(L, R)$ of classes of morphisms such that

(i) Every morphism $f$ of $K$ can be factored as $f=rl$ with $l \in L$ and $r \in R$.

(ii) $L$ is the class of morphisms which have the left lifting property with respect to every morphism of $R$.

(iii) $R$ is the class of morphisms which have the right lifting property with respect to every morphism of $L$.

#Orthogonal Factorization Systems#

An **[[orthogonal factorization system]]** is a weak factorization system where we additionally require that the solutions to each lifting problem be _unique_.

While every OFS is evidently a WFS, the primary examples of each are different.  A "basic example" of an OFS is (epi, mono) in [[Set]], while a "basic example" of a WFS is (mono, epi) in $Set$.  The superficial similarity of these two examples masks the fact that they generalize in very different ways.  The OFS (epi, mono) generalizes to any [[topos]] or [[pretopos]], and in fact to any [[regular category]] if we replace "epi" with [[regular epimorphism|regular epi]].  Likewise it generalizes to any [[quasitopos]] if we instead replace "mono" with [[regular monomorphism|regular mono]].

On the other hand, saying that (mono,epi) is a WFS in $Set$ is equivalent to the [[axiom of choice]].  A less loaded statement is that $(L,R)$ is a WFS, where $L$ is the class of inclusions $A\hookrightarrow A\sqcup B$ into a binary coproduct and $R$ is the class of [[split epimorphism|split epis]].  In this form the statement generalizes to any [[extensive category]].

#Examples#

* [[model category|Model categories]] provide many examples of weak factorization systems.  In fact, most applications of WFS involve model categories or model-categorical ideas.

#Properties#

* The classes $(L,R)$ of a weak factorization system enjoy many good closure properties. Both are closed under [[retract]]s and contain all [[isomorphism]]s. $L$ is closed under [[pushout]]s and $R$ is closed under [[pullback]]s. $L$ is closed under arbitrary [[coproduct]]s and $R$ is closed under arbitrary [[product]]s. $L$ is also closed under [[transfinite composition]]. The closure properties for $L$ can be summarized by saying that $L$ is **saturated**, which means precisely this.

* However, $L$ is not closed under all [[colimit]]s in $arr(K)$ and similarly $R$ is not closed under all [[limit]]s in $arr(K)$; they are not necessarily closed under ([[coequalizer|co]])[[equalizer]]s. However, if $(L,R)$ is an _orthogonal_ factorzation system, then $L$ is closed under all colimits and $R$ is closed under all limits.

#Functorial Factorization#

The precise requirements for a factorization of morphisms to be _functorial_ are frequently misstated. What follows is a fairly uncommon (but correct) definition:

Write $[2]$ and $[3]$ for the [[ordinal number]]s, regarded as categories. So $arr(K)$ is isomorphic to the functor category $[[2],K]$. There are three injective functors $[2] \rightarrow [3]$; let $d_1$ be the functor that sends the objects $\{0,1\}$ of $[2]$ to the objects $\{0,2\}$ of $[3]$. This induces a functor $c : [[3],K] \rightarrow [[2],K]$ which can be thought of as "composition."

A **functorial factorization** is a functor $F : [[2],K] \rightarrow [[3],K]$ such that $cF$ is the identity on $arr(K)$.  Not all weak factorization systems are functorial, although most (including those produced by the [[small object argument]]) are, but all orthogonal ones are automatically functorial.
