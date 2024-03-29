In this exposition we will follow the book listed below in writing crossed modules with operations on the right. Thus a [[crossed module]] is in the first instance a morphism $\mu: M \to  P$ of groups together with an operation of the group $P$ on the right of the group $M$ written $(m,p) \mapsto
m^p$, satisfying the following two axioms:  

CM1) $ \mu (m^p)= p(\mu m)p^{-1}$; 

CM2) $ mnm^{-1} = n^{\mu m} $; 

for all $m,n \in M, p \in P$. 


The notion of _free crossed module_ was developed by J.H.C. Whitehead in the period 1941-1949 to model algebraically the structure of the second relative homotopy group  of an adjunction space 
$\pi_2(A \cup \{e^2_\lambda\}_{\lambda \in \Lambda},A,x)$ considered as a crossed module over $\pi_1(A,x)$. This work is also related to independent work of Peiffer and Reidemeister on Identities among relations. 

It can also be considered as arising from the notion of a resolution for a group, by analogy with resolutions for modules, but in a nonabelian framework. So in combinatorial group theory we consider a presentation $ \langle X \mid R \rangle $ of a group $G$. Thus $X$ is a set of generators of the group $G$ and $R$ is a set of relators, that is, $R$ is a subset of $F(X)$, the free group on the set $X$. So we have an  epimorphism $\phi: F(X) \to G$ with kernel $N$, say, a normal subgroup of $F(X)$, and $N$ is the normal closure of $R$ in $F(X)$. All this reflect the fact that if $\phi (u) =1$, where $u \in F(X)$, then 
$\phi (pup^{-1} ) = 1$ for all $p \in F(X)$. 

Let  $P=F(X)$, and write $\langle R\rangle^P$ for the normal closure of the set $R$ in $P$. The elements of $\langle R\rangle^P$ are all _consequences_ of
$R$ in $P$, namely all products 

 $$ c=(r_{1}^{\epsilon _{1}})^{p_{1}} \dots (r_{m}^{\epsilon
_{m}})^{p_{m}}$$ 

where $r_{i} \in R$, $\epsilon _{i} = \pm 1$,
$p_{i} \in P$ and $m \geq 1$, and $u^p = pup^{-1}$. An important point is that if
$\phi \colon P \to Q$ is any morphism of groups  such that $\phi
(R)=\{1\} $, then $\phi (\langle R\rangle^P) =\{1\}$, since Ker $
\phi$ is normal. Thus $\phi$ factors as $P \to P/\langle R\rangle^P
\to Q$ where the first morphism is the quotient morphism. 

It is also convenient to allow for repeated relators, which, as we shall see, corresponds to attaching several cells by the same map. So we replace the subset $R$ of $P=F(X)$ by a function $\omega: R \to P$. 

We now drop the assumption that $P$ is free. We form the free $P$-group $F^P(R)$ on the set $R$: this is the free group on elements $(r,p) \in R \times P$, and has an action of the group $P$ determined  by 
$(r,p)^q=(r,pq)$. There is a morphism of groups $\theta : F^P(R) \to P$ given by $\theta (r,p)= (\omega(r))^p$. Then $\theta $ is a $P$-morphism: $\theta (w^p)= \theta (w)^p$ for all $w \in F^P(R), p \in P$.

We now define for $u,v \in F^P(R)$ the _Peiffer commutator_ to be the element 

 $$ [\! [ u,v]\! ] = uvu^{-1}(v^{\theta u})^{-1}.$$

 Note that $\theta([ \! [ u,v] \! ] )=1 \in F^P(R)$. It may be proved that the Peiffer commutators generate a normal subgroup called the Peiffer group  of $\theta$, and written $ [ \! [ F^P(R), F^P(R)]\! ] $. The quotient group $F^P(R)/ [\! [ F^P(R),F^P(R) ]\! ] $ is written $FC(\omega)$ and there is an induced morphism

$$\delta : FC(\omega) \to P$$

with image $\langle(\omega(R))\rangle^P$. This construction is called the _free crossed module_ on $\omega: R \to P$. The kernel of $\delta$ is actually a $P$-module, and is called the _module of identities among relations_.

A useful fact is that this free crossed module may also be described as the pushout in the category of crossed modules 

 $$\begin{matrix}(1 \to F(R))&\to & (1 \to P) \\ \downarrow&& \downarrow \\ (F(R) \to F(R)) &\to& (FC(\omega) \to P)\end{matrix}$$

where the morphism of groups $i:F(R) \to FC(\omega)$ is given by $i(w) = [(w,1)]$, the class of $(w,1)$ in $FC(\omega)$. This shows the relevance of a Seifert-Van Kampen Theorem for second relative homotopy groups, since the above pushout comes from applying the fundamental crossed module functor $\Pi_2$ on based pairs given by 

$$\Pi_2(X,A,x)= (\delta: \pi_2(X,A,x) \to \pi_1(A,x))$$

to the  pushout of pairs of spaces defining the based pair $(A \cup \{e^2_\lambda\}_{\lambda \in \Lambda}, A,x)$. This theorem  also shows that we can generalise this situation to a pushout of crossed modules

 $$\begin{matrix}(1 \to S)&\to & (1 \to P) \\ \downarrow&& \downarrow \\ (S \to S) &\to& ( M \to P)\end{matrix}$$

where $S$ is now any group; the crossed module $M \to P$ then gives the fundamental crossed module of the pair $(A \cup CY,A,x)$ determined by a map $f: Y \to A$ and where $S=\pi_1(Y,y)$. Note that $(A \cup CY,A)$  arises in a pushout diagram of the form 
$$\begin{matrix}(Y,Y)&\to & (A,A) \\ \downarrow&& \downarrow \\ (CY,Y) &\to& (A \cup CY,A)\end{matrix}$$

This generalisation of Whitehead's theorem on free crossed modules was discovered as a consequence of the 2-dimensional Seifert-van Kampen Theorem. It has been used to give explicit computations of the crossed module $\pi_2(A \cup CY,A,x)\to \pi_1(A,x)$ in the case the map $Y \to A$ is the map of classifying spaces $ BG \to BP $ induced by a morphism $\phi: G \to P$ of groups. It may also be proved that if $G,P$ are finite groups, so also is the group $M$. This gives impetus to calculations, and some of these are best done with a computer.

For more information on these topics see Part I of the book on "Nonabelian algebraic topology" listed below. 

It is convenient to generalise the above to crossed modules over groupoids, to model the situation of attaching cells at different points. So we assume given $\mu: M \to P$ where $M,P$ are groupoids, $\mu$ is the identity on objects, $M$ is a union of groups $M(x), x \in P_0 = Ob(P)$ and the operation of $P$ on $M$ is such that if $p \in P(x,y), m \in M(x)$, then $m^p \in M(y)$, with the obvious axioms. 



## References## 

* Whitehead, J. H.~C., "Combinatorial homotopy. II". _Bull. Amer. Math. Soc._ 55 (1949) 453--496.

* Brown, R. and Higgins, P.J., "On the connection between the second
relative homotopy groups of some related spaces", _Proc.
London Math.  Soc._ (3) 36 (1978) 193--212.

* R. Brown, P.J. Higgins, R. Sivera,  _Nonabelian algebraic
topology: filtered spaces, crossed complexes, cubical homotopy
groupoids_, EMS Tracts in Mathematics Vol. 15, 703 pages. (August
2011).