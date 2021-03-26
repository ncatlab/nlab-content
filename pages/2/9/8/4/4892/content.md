[[!redirects Cech homology]]
[[!redirects Čech homology]]

#&#268;ech homology#
* automatic table of contents goes here
{:toc}
Recall the definition of the nerve of an open cover from [[Čech methods]].

##Preliminary Definitions##

Given a (compact) space $X$ and a finite open cover, $\alpha$, of $X$, we can
form a [[simplicial set]], $C(X,\alpha)$, called the *nerve of the cover* whose $n$-[[simplex|simplices]] are $(n + 1)$-strings
of open sets  from $\alpha$, i.e. $\langle U_0, \ldots, U_n\rangle$, each $U_i \in \alpha$,
satisfying $\cap U_i \neq \emptyset$.

If $\beta$ is another cover such that for each $V\in \beta$, there is a $U\in
\alpha$ with $V\subseteq U$, then the assignment $V\to U$ in this case defines 
a map 

$$C(X,\alpha)\to C(X,\beta)$$

dependent on the choice of $U$ for each
$V$, but independent 'up to homotopy'.  This gives an inverse system of simplicial sets and homotopy classes of maps.

####Remarks:####

(i) The classical definition would require that the sets $U_i$, involved in the simplex were distinct, and that the ordering did not matter. That then gives a [[simplicial complex]] rather than a simplicial set. The simplicial complex definition yields something that is smaller but for some calculations is a lot less easy to work with.

(ii) The proof that the homotopy class of the 'binding' map from $C(X,\alpha)$to $C(X,\beta)$ is independent of the choices made is well known.  It shows that any two choices yield 'contiguous maps' in as much as the images of a simplex under the two maps, given by the two choices, form two faces of a higher dimensional simplex.  This allows an _explicit_ [[simplicial homotopy|homotopy]] of simplicial maps to be given.


Taking the simplicial homology groups of the $C(X,\alpha)$, gives, for each $n$, an inverse system of Abelian groups, which we will denote $H_n(X,\alpha)$.

##Definition##
The $n$th __Čech homology group__ of the space $X$ is defined to be
$$\check{H}_n(X) = lim H_n(X,\alpha),$$
where the limit is taken over all open covers of $X$.

It is to be noted that these groups do not constitute a [[homology theory]] in the sense of the [[Eilenberg-Steenrod axioms]] as the _exactness axiom_ fails in general. There is a "corrected" theory known under the name [[strong homology]]. 

## Literature and links

An expository account is available in Section 2 of

* [[David H. Fremlin]], _Singular homology for amateurs_, [PDF](https://www1.essex.ac.uk/maths/people/fremlin/n16703.pdf).

See also [[Čech methods]].

[[!redirects Čech homology theory]]
[[!redirects Cech homology]]