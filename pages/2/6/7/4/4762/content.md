
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 


An _$n$-hypergroupoid_ is a model for an [[n-groupoid]]: it is an [[Kan complex]] that is like the [[nerve]] of a [[groupoid]] ($n= 1$), [[bigroupoid]] ($n = 2$) etc.

## Definition

+-- {: .num_defn }
###### Definition

An **$n$-hypergroupoid** is a [[Kan complex]] $K$ in which the [[horn]]-fillers are _unique_ in dimension greater than $n$:

$$
  (k \gt n) \Rightarrow
  \left(
     \array{
       \Lambda^i[k] &\to&  K
       \\
       \downarrow & \nearrow_{\exists !}
       \\
       \Delta[k]
     }
  \right)
  \,.
$$

=--

(The lower dimensional horn fillers of course also exist, but are not in general unique.)

This is due to ([Duskin 79](#Duskin79), [Glenn 82](#Glenn82)), however their definition does not ask $K$ has lower dimensional horn fillers. In [Beke 04](#Beke04) these are called _exact $n$-types_ instead. For a review on the definition see ([Pridham 09, section 2](#Pridham09)).

Equivalently, this are those [[Kan complex]]es which are $(n+1)$-[[coskeletal]] and such that the $(n+1)$-horns and $(n+2)$-horns have unique fillers.



## Properties

\begin{example}
\label{OneHypergroupoids}
1-Hypergroupoids are precisely the [[nerves]] of [[groupoids]], see also the example [here](simplicial+skeleton#CoskeletalityOfSimplicialNervesOfCategories).
\end{example}

\begin{example}
2-Hypergroupoids are precisely the [[Duskin nerves]] of [[bigroupoids]].
\end{example}

## References
 {#References}

The term _hypergroupoid_ is due to

* {#Duskin79} [[John Duskin]], _Higher-dimensional torsors and the cohomology of topoi: the abelian theory_, p. 255-279 in: _Applications of sheaves_,  Lecture Notes in Mathematics **753**, Springer (1979) &lbrack;[doi:10.1007/BFb0061822](https://doi.org/10.1007/BFb0061822)&rbrack; 
 
and

* {#Glenn82} [[Paul G. Glenn]], *Realization of cohomology classes in arbitrary exact categories*, J. Pure Appl. Algebra **25** 1 (1982) 33-105 &lbrack;<a href="https://doi.org/10.1016/0022-4049(82)90094-9">doi:10.1016/0022-4049(82)90094-9</a>&rbrack;


The term _exact $n$-type_ is used in

* {#Beke04} [[Tibor Beke]], *Higher &#268;ech theory*, K-Theory **32** 4 (2004) 293-322 &lbrack;[K:0646](https://faculty.math.illinois.edu/K-theory/0646)&rbrack;
 

On presentation of [[infinity-stack|higher stacks]] (higher [[geometric stacks]]) by hypergroupoid objects:

* {#Pridham09} [[Jonathan Pridham]], *Presenting higher stacks as simplicial schemes*,  Adv. Math. **238** (2013) 184-245 &lbrack;[arXiv:0905.4044](http://arxiv.org/abs/0905.4044), [doi:10.1016/j.aim.2013.01.009](https://doi.org/10.1016/j.aim.2013.01.009)&rbrack;
 


[[!redirects hypergroupoids]]

[[!redirects n-hypergroupoid]]
[[!redirects 1-hypergroupoid]]
[[!redirects 2-hypergroupoid]]

[[!redirects n-hypergroupoids]]
[[!redirects 1-hypergroupoids]]
[[!redirects 2-hypergroupoids]]