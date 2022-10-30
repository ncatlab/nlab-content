[[!redirects Volodin spaces]]
#Volodin space
* table of contents
{: toc}

##Idea

_Volodin spaces_ are the [[Vietoris complex]] analogues of the nerve of a family of subgroups discussed in the entry, [[higher generation by subgroups]].  They provide a way of building a geometric object that provides a means of comparing the information on the 'big group' that is 'stored' by subgroups within the family.

They were essentially introduced by [[Volodin]] as part of his approach to higher [[algebraic K-theory]]. We will discuss them via another approach that is explicit in work by [[Suslin]], on the equivalence of the Volodin K-theory with that of [[Quillen]].

##Preliminaries

Let $X$ be a non-empty set, and denote by $E(X)$, the [[simplicial set]] having $E(X)_p = X^{p+1}$, so a $p$-simplex is a $p+1$ tuple, $\underline{x}= (x_0,\ldots, x_p)$, each $x_i \in X$, and in which
$$d_i(\underline{x}) = (x_0,\ldots, \hat{x_i}, \ldots x_p),$$and
$$s_j(\underline{x}) = (x_0,\ldots, x_j, x_j, \ldots x_p),$$
so $d_i$ omits $x_i$, whilst $s_j$ repeats $x_j$.
+--{: .un_lemma}
######Lemma
The simplicial set, $E(X)$, is contractible.
=--
The proof is fairly easy to construct and is 'well known'.


The case we are really interested in is when we replace the general set, $X$, by the underlying set of a group, $G$. (As is often done, we will not introduce a special notation for the underlying set of $G$, just writing $G$ for it.) In this case, we have the simplicial set $E(G)$  and the group, $G$, acts freely on $E(G)$ by

$$g\cdot(g_0,\ldots , g_p) = (gg_0,\ldots, gg_p).$$

(Here we have used a left action of $G$, and leave you to check that the evident right action could equally well be used.)

The quotient simplicial set of orbits, will be denoted $G\backslash E(G)$. It is often useful to write $[g_1,\ldots,g_p]$ for the orbit of the $p$-simplex $(1,g_1,g_1g_2,\ldots, g_1g_2\ldots g_p)\in E(G)_p$.

It is 'instructive' to calculate the faces and degeneracy maps in this notation.  We will only look at $[g_1,g_2]$ in detail. This element has representative $(1,g_1,g_1g_2)$. We thus have:


* $d_0(1,g_1,g_1g_2) = (g_1,g_1g_2) \equiv (1,g_2)$,
so $d_0[g_1,g_2] = [g_2]$;
*  $d_1(1,g_1,g_1g_2) = (1,g_1g_2)$,
so $d_1[g_1,g_2] = [g_1g_2]$;
*  $d_2(1,g_1,g_1g_2) = (1,g_1)$,

so $d_2[g_1,g_2] = [g_1]$.

(That looks familiar!)

For the degeneracies,

*  $s_0(1,g_1,g_1g_2) = (1,1,g_1,g_1g_2)$, so $s_0 [g_1,g_2] =[1,g_1,g_2] $;
*  $s_1(1,g_1,g_1g_2) = (1,g_1,g_1,g_1g_2)$, so $s_1 [g_1,g_2] =  [g_1,1,g_2] ;$

and similarly $s_2 [g_1,g_2] =  [g_1,g_2,1]$. 

The general formulae are now easy to guess and to prove - so they will be left to you, and then the following should be obvious.

+--{: .un_lemma}
######Lemma
There is a natural simplicial isomorphism,
$$G\backslash E(G)\xrightarrow{\cong}Ner(G[1])= BG.$$
=--
We thus have that $G\backslash E(G)$ is a [[classifying space]] for $G$.


This construction of $E(G)$ is exactly that of the nerve of the [[action groupoid]] of the action of $G$ on itself by left multiplication.

##Volodin spaces

We put ourselves in the context of a group, $G$, and a family, $\mathcal{H}$, of subgroups of $G$ as in the context of [[higher generation by subgroups]].  We suppose that $\mathcal{H}= \{H_i\mid i\in I\}$ for some indexing set, $I$. 
+--{.un_defn}
(cf. Suslin-Wodzicki, (ref. below) p. 65.) 
We denote by $V(G,\mathcal{H})$, or $V(\mathfrak{H})$, the simplicial subset of $E(G)$ formed by simplices, $(g_0,\ldots,g_p)$, that satisfy the condition that there is some $i\in I$ such that, for all $0\leq j,k\leq p$, $g_j g_k^{-1}\in H_i$.

The simplicial set, $V(G,\mathcal{H})$, will be called the _Volodin space_ of $(G,\mathcal{H})$.
=--

##References

*  A. A. [[Suslin]] and M. Wodzicki, _Excision in algebraic K-theory_, The Annals of Mathematics, 
136, (1992), 51 &#8211; 122.

* [[I. Volodin]], _Algebraic K-theory as extraordinary homology theory on the category of associative 
rings with unity_, Izv. Akad. Nauk. SSSR, 35, (Translation: Math. USSR Izvestija Vol. 5 (1971) 
No. 4, 859-887)
