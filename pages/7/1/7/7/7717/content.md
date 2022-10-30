[[!redirects III.8, Dieudonné modules (p-divisible groups)]]
[[!redirects III.8, Dieudonne modules (p-divlsible groups)]]
[[!redirects Dieudonne modules (p-divlsible groups)]]

This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

+-- {: .num_lemma}
###### Lemma


Let $M_{n+1}\stackrel{\pi_n}{\to}M_n\stackrel{\pi_{n-1}}{\to}\cdots\stackrel{\pi_n}{\to}M_1$ a system of $W(k)$[[W(k)-module|-modules]] such that for all $n$

1. $M_{n+1}\stackrel{p^n}{\to}M_{n+1}\stackrel{\pi_n}{\to}M_n\to 0$ is exact

1. $M_n$ is of finite length.

then $M:=lim M_n$ is a finitely generated $W(k)$-module and the canonical map $M\to M_n$ identifies $M_n\simeq M/p^n M$
=--

+-- {: .num_defn}
###### Definition
($p$-torsion formal group)
A formal group $G$ is called *$p$-torsion formal group* if

1. $G=\cup ker p^n id_G$

1. $ker p id_G$ is finite.

There are exact sequences

$$0\to ker p^n \to ker p^{n+1}\stackrel{p^n}{\to}ker p^{n+1}$$

$$0\to ker p^n \to ker p^{n+m}\stackrel{p^n}{\to}ker p^m$$

showing by induction the also $ker p^n$ is finite for all $n$. Define $M(G)= colim M(ker p^n)$
=--

+-- {: .num_theorem}
###### Theorem

$G\to M(G)$ is a (contravariant) equivalence between the category of $p$[[p-torsion formal group|-torsion]][[formal group|formal groups]] and the category of tuples $(M,F_M,V_M)$ where M 
is a finitely generated $W(k)$[[Dieudonné module|-module]] and $F_M$, $V_M$ to groups of endomorphisms of $M$ with

$$F_M(wm)=w^{(p)}F_M (m)$$

$$V_M(w^{(p)}_m)=w V_n(m)$$

$$F_M V_M=V_M F_M=p id_M$$

 It follows from the lemma that $M(G)$ is finitely generated and that

$$M_n=M(G)/p^n M(G)$$

Conversely if $M$ is as before we define $G:=colim G_n$ where $M(G_n)=M/p^n M$

Moreover we have:

1. $G$ is finite iff $M(G)$ is finite and in that case $M(G)$ is the same as in &#167; 7.

1. $G$ is $p$-divisible iff $M(G)$ is torsion-less (= free) and $height(G)=dim M(G)$.

1. For any [[perfect field extension|perfect extension]] $K/k$ there is a functorial isomorphism $M(G\otimes_k K)\simeq W(k)\otimes_{W(k)}M(G)$

1. If $G$ is $p$-divisible with [[Serre dual]] $G^\prime$ then $M(G^\prime)=Mod_{W(k)}(M(G),W(k)$ with

$$(F_{M(G^\prime)}f)(m)=f(V_M m)(p)$$

and

$$(V_{M(G^\prime)}f)(m)=f(F_M m)^{(p^{-1})}$$

([Demazure Theorem p.71-72](#lecturesOnPDivGroups))
=--

+-- {: .num_theorem}
###### Theorem
a) The Dieudonn&#233; functor

$$\begin{cases}
Torf_p\to (fin W(k)-Mod,F,V)
\\
G\to M(G)
\end{cases}$$

is a contravariant equivalence between the category of $p$-torsion formal groups, and the category of all triples $(M,F_M,V_M)$ where $M$ is a finitely generated $W(k)$-module and $F_M$, $V_M$ two group endomorphisms of $M$ satisfying

$$F_M(\lambda m)=\lambda^{p} F_M(m)$$

$$V_M(\lambda^{(p)}m)=\lambda V_M(m)$$

$$F_M V_M=V_M F_M=p\cdot id_M$$

It follows from the lemma that $M(G)$ is finitely generated and $M_n\simeq M(G)/p^n M(G)$. Conversely if $M$ is as before, then we define $G$ as $colim G_n$ where $M(G_n)= M/ p^n M$.
=--

+-- {: .num_remark}
###### Remark
From the definition and what we already verified follows:

1. $G$ is finite iff $M(G)$ is finite, and in that case $M(G)$ is the same as defined in &#167; 7.

1. $G$ is finite iff $M(G)$ is torsion-less (= free), and $height(G)=dim M(G)$.

1. For any perfect extension $K/k$, there is a functorial isomorphism $M(G\otimes_k K)\simeq W(K)\otimes_{W(k)} M(G)$.

1. If $G$ is $p$-divisible, with Serre dual $G^\prime$, then $M(G^\prime)=Mod_{W(k)}M(G)$, with $F_{M(G^\prime)} f)(m)=f(V_M m)^{(p)}$ and $(V_{M(G^\prime)}f)(m)=f(F_M m)^{(p^{(-1)}}$.

=--

## References

{#lecturesOnPDivGroups} Michel Demazure, lectures on p-divisible groups [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)