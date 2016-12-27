This is a sub-entry for [[gerbe]].

For related entries see

* [[bundle gerbe]]
* [[gerbe (general idea)]]


##Idea## 

(The definitions of [[sheaf]] and [[stack]] are elsewhere in the nLab but we will have to review them briefly. There is also  [[motivation for sheaves, cohomology and higher stacks]], which provides other insights. For simplicity of exposition, we will initially look at sheaves, stacks and gerbes over a base space $B$ rather than in the more general setting of a topos.)

Naively a [[sheaf]] is a [[family of sets]] indexed 'continuously' by the points of a space $B$.  It corresponds either to a [[presheaf]] satisfying a 'gluing condition' (which is the version of [[descent]] in one of its simplest cases), or to an [[etale space|étale space]] over $B$.  The relationship between them is that the presheaf is the presheaf of local sections of the &#233;tale space, and the 'gluing condition' is that local sections that agree on the intersections of  open sets can be glued uniquely to give a section over the union of the open sets.

An important class of sheaves are the [[torsor|torsors]].  Let $G$ be a sheaf of groups on $B$.   The category, $Tors(B;G)$ of $G$-torsors on $B$ is a groupoid.  The notion of $G$-torsor 'localises' well, so that if $U$ is an open set of $B$, then we can restrict $G$ to a sheaf on $U$, and look at the torsors over $U$ using the restricted $G$. (We abuse notation and just write $Tors(U;G)$ for the corresponding groupoid. If $V$ is another open set contained in $U$, there is a restriction functor from $Tors(U;G)$ to $Tors(V;G)$, so it looks as if we have a presheaf of groupoids on $B$, but things are not quite right here.

The assignment of $Tors(G)_U$ to $U$ only gives a [[pseudofunctor]] not a functor from the category $Open(B)^{op}$ to the category of groupoids. It thus corresponds to a [[Grothendieck fibration]] or **fibred category** over $Open(B)$.  It does have quite nice 'gluing properties' however, it is a [[stack]] of groupoids.  (Roughly 'morphisms glue, objects glue up to isomorphism'. For enlightenment note that there are almost presheaves of objects and of morphisms in this 'pseudo' presheaf.) This stack will be called $\mathcal{T}ors(G)$.

There is a **stackcompletion** functor from fibred categories to stacks.  If we take the sheaf of groups $G$, think of it as a presheaf of groupoids $BG$, in the usual way, then it is a pseudo-functor from $Open(B)^{op}$ to the category of groupoids. If we stack complete it, we get ... $\mathcal{T}ors(G)$.

We thus can think of a stack of groupoids as a 'lax' generalisation of a sheaf of groupoids.  What about **gerbes**?

(It should be mentioned that often in topological settings, the sheaf of groups is actually a constant sheaf and that in that case a $G$-torsor is just a principal $G$-bundle.)


Groups 'are' groupoids with a single object, but groupoids are not 'groups with many objects' (although that is a nice phrase to use when introducing them). A groupoid need not have any objects ... if it is empty! Of course, we think of the vertex groups of a groupoid, but, if the groupoid is not connected, there may be many different non-isomorphic ones. So a group *is* a very special type of groupoid.

Similarly, the term 'gerbe' refers to a special sort of stack of groupoids. 

+-- {: .standout}
A gerbe is to a general stack what, up to equivalence, a group is to a general groupoid. It is non-empty and connected.
=--

+--{: .query}

[[David Roberts]]: This is reflected in the fact that the fibres of bundle gerbes (either abelian or $G$-bundles gerbes) are transitive groupoids. I believe Tim and I had a bit of discussion of this sort of thing last year (or before - mists of time...). Or maybe this comment should go in [[gerbe (general idea)]]?
=--

To make this precise we use some additional notions:

We will have a pseudofunctor $F : Open(B)^{op}\to Grpd$, and this will be a stack.


##Definitions## 

*   A stack of groupoids, $F$, on $B$ is *locally non-empty* if there is an open covering $\mathcal{U}$ of $B$ for which each groupoid $F(U)$ is non-empty, for $U \in \mathcal{U}$.

*   A stack of groupoids, $F$, on $B$ is said to be *locally connected*  if for each open $U$ in $B$ there is an open covering $\mathcal{U}$ of $B$ such that all elements in $F(U)$ become connected in all $F(U_i)$.


and finally:

*  A *gerbe* $F$ on $B$ is a locally non-empty, locally connected stack of groupoids on $B$.


It is important to note that it does not state in the definition of a gerbe that the open cover that we have over which it is non-empty is or is not one over which it is connected.

_Local connectedness_ can be well stated by saying that for the various $U$, if $x$ and $y$ are local objects defined over $U$, the set $F(U)(x,y)$ is not empty. (Translation: a 'local object', or 'locally defined object', of $F$ is a 'local section'  of $Ob(F)$, say, over $U$, in other words, an element in $Ob(F(U))$.



## Important example## 


+-- {: .un_proposition}

###### Proposition
$\mathcal{T}ors(G)$ is a gerbe on $B$.
=--

+-- {: .proof}
######Proof
To see _locally non-empty_: If $U$ is any open set in $B$, then as $\mathcal{T}ors(G)(U) = Tors(U;G)$, the category of $G_U$-torsors over $U$, it has at least the [[trivial torsor|trivial G-torsor]] (over $U$) amongst its objects, so $\mathcal{T}ors(G)$ is locally non-empty.

Next look at $\mathcal{T}ors(G)(U)$ again.  Any two $G_U$-torsors are locally isomorphic to each other, since they are both locally isomorphic to the trivial $G_U$-torsor, so, if $F$ and $F^\prime$ are two $G_U$-torsors, there is an open cover such that over that cover $F$ and $F^\prime$ are isomorphic, hence $\mathcal{T}ors(G)$ is locally connected.  We thus have that $\mathcal{T}ors(G)$ is a gerbe.
=--

##$\mathcal{A}$-Gerbes##

The notion of a $G$-gerbe arises in the article [[gerbe (general idea)|gerbe ]], but one needn't use just a group $G$. Fix a sheaf of abelian (possibly not necessary) groups $\mathcal{A}$ on $B$. Then an $\mathcal{A}$-gerbe is a gerbe $F$ on $B$ such that for any open $U$ on $B$ we have a functorial isomorphism $\mathcal{A}(U)\stackrel{\sim}{\to} \text{Aut}(s)$ for all $s\in F(U)$.

Note that since $F$ is a stack, $\text{Aut}(s)$ is a sheaf, so by isomorphism we mean an isomorphism as sheaves, and by functorial we mean given another object $t\in F(U)$, the isomorphism commutes 

$$ 
\begin{matrix} \mathcal{A}(U) & \to & \text{Aut}(s) \\
Id \downarrow &  & \downarrow \\
\mathcal{A}(U) & \to & \text{Aut}(t) \end{matrix}  
$$

In particular, we get that for any two objects $C, D\in F(U)$ we have that the sheaf $Isom(C,D)$ is an $\mathcal{A}$-torsor. This gives that if there is some object over $U$, namely that $F(U)\neq \emptyset$, then the set of isomorphism classes of obects in $F(U)$ is in natural bijection with $H^1(U, \mathcal{A}_U)$.

For example, consider the stack of rank 1 vector bundles on a scheme $X$, $\text{Vect}_1$. One can check that $\text{Vect}_1$ is a $\mathbb{G}_m$-gerbe by noting that the automorphism group of any vector bundle over $U$ will be precisely $\mathcal{O}_X(U)^\times$, and everything is functorial. By the interpretation in cohomology, we see that the global vector bundles (up to isomorphism) are in correspondence with $H^1(X, \mathcal{O}_X^\times)$ which is just $\text{Pic}(X)$.


One can form the *classifying stack*, $B\mathcal{A}$ from the important example above by taking $B\mathcal{A}(U)=\mathcal{T}ors(\mathcal{A}(U))$. A basic theorem about $\mathcal{A}$-gerbes is that an $\mathcal{A}$-gerbe, $F$, is isomorphic to $B\mathcal{A}$ if and only if $F(B)\neq \emptyset$. This says that $F$ is isomorphic to the classifying stack if and only if it has a global object.


For information on how gerbes play a role in differential geometry see [[gerbe (in differential geometry)]].


##References

There is a lengthier description of gerbes (at this level of generality) in the Menagerie notes that are available from [[Tim Porter|Tim Porter's]] home page.

Other material available online includes the following:

* I. Moerdijk, _Introduction to the language of stacks and gerbes_ ([arXiv](http://arxiv.org/abs/math/0212266))

* Larry Breen, _Notes on 1- and 2-gerbes_ ([arXiv](http://arxiv.org/abs/math/0611317))

Further references are given in the other entries on gerbes.
