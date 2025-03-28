
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The *Seifert-van Kampen theorem* is a classical theorem in [[algebraic topology]] which computes the [[fundamental group]] of a pointed [[topological space]]   in terms of a decomposition into [[open subsets]].

It is most naturally expressed by saying that the [[fundamental groupoid]] [[functor]] preserves certain [[colimits]].  Here there is a bifurcation in possible generalizations, however.  The colimits of spaces we consider (covers by open subsets) are both strict colimits and [[homotopy colimits]].  But we can ask the resulting colimit of groupoids to be either a [[homotopy colimit]] (i.e. a [[2-colimit]]) or a [[strict 2-colimit|strict colimit]].  The first is more natural for formal work; the second is more useful for computation.  Accordingly, we will speak of *homotopy van Kampen theorems* and *strict van Kampen theorems*.

## Statement

### For fundamental groups

The most classical version of the **Seifert-van Kampen theorem** for the [[fundamental group]] is the following.

+-- {: .un_theorem}
###### Theorem

Let $X$ be a [[topological space]] [[covering|covered]] by [[open subsets]] $U,V \subset X$ such that $U \cap V$ is [[path-connected space|path connected]]. Then for every choice of basepoint $x \in U \cap V$, the [[diagram]] of [[homotopy group]]s

$$
  \array{
    \pi_1(U \cap V, x) &\to& \pi_1(U,x)
    \\
    \downarrow && \downarrow
    \\
    \pi_1(V,x) &\to& \pi_1(X,x)
  }
$$

is a [[pushout]] square in [[Grp]].

=--


### From groups to groupoids

We can regard the classical theorem as being a statement about fundamental groupoids as follows.  Recall that any group $G$ can be considered as a 1-object groupoid $\mathbf{B}G$ by [[delooping]].  It is easy to see that the functor $\mathbf{B}$ takes colimits of groups to strict colimits of groupoids.  Moreover, a strict pushout of one-object groupoids is also a 2-pushout, because the maps we are pushing out are [[bo functor|bijective on objects]], hence [[cofibrations]] in the [[canonical model structure]] on $Gpd$.  Thus, under the hypotheses of the classical van Kampen theorem, we have a square

$$
  \array{
    \mathbf{B}\pi_1(U \cap V, x) &\to& \mathbf{B}\pi_1(U,x)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}\pi_1(V,x) &\to& \mathbf{B}\pi_1(X,x)
  }
$$

which is both a strict pushout and a [[2-colimit|2-pushout]] in $Gpd$.

Now let $X'$ be the [[path component]] of $X$ which contains $U\cap V$ (there is exactly one such, because $U\cap V$ is path-connected), and similarly $U'$ and $V'$.  Then the [[fundamental groupoid]] $\Pi_1(X')$ is equivalent to $\mathbf{B}\pi_1(X,x)$, and similarly in the other cases.  Since 2-pushouts are invariant under equivalence of groupoids, we also have a 2-pushout square

$$
  \array{
    \Pi_1(U \cap V) &\to& \Pi_1(U')
    \\
    \downarrow && \downarrow
    \\
    \Pi_1(V') &\to& \Pi_1(X')
  }
$$

This is an instance of what we referred to above as a *homotopy van Kampen theorem*.  But we can easily make it a *strict van Kampen theorem* as well.

Note that the functors $\Pi_1(U\cap V) \to \Pi_1(U')$ and $\Pi_1(U\cap V) \to \Pi_1(U')$ are injective on objects, hence cofibrations in the canonical model structure, and so their strict pushout is also a 2-pushout.  This strict pushout is therefore equivalent to $\Pi_1(X')$.  (It need not be isomorphic to it, but this can be remedied by defining the *fundamental groupoid on a set of specified basepoints* as below.)

We now consider more general versions of the van Kampen theorem which do not require $U\cap V$ to be path-connected, and which compute all of $\Pi_1(X)$ rather than just $\Pi_1(X')$.


### Strict van Kampen theorem for groupoids

Let us define $\Pi_1(X,X_0)$ of a space $X$ and a subset $X_0 \subseteq X$ to be the full subgroupoid of $\Pi_1(X)$ on the set $X_0$.  More generally, if $U$ is given as a subspace of $X$ and $X_0 \subseteq X$, we write $\Pi_1(U,X_0)$ for $\Pi_1(U,X_0\cap U)$.

If $X_* =(X,X_0)$ is a pair consisting of a space $X$ and a set $X_0$ of base points, we say $X_*$ is _connected_ if $X_0$ meets each path component of $X$.  This is clearly a necessary and sufficient condition for $\Pi_1(X,X_0)$ to be equivalent to $\Pi_1(X)$.

Now let $\{U^i \to X\}$ for $i \in I$ be an [[open cover]] of $X$.  If $d=(i,j) \in I^2$ we write $U^d$ for $U^i \cap U^j$, and similarly for $n$-fold intersections.  For any $n$-tuple $e\in I^n$, let $U^e_*$ be the pair $(U^e,X_0 \cap U^e)$.  We then have a [[coequaliser]] diagram of pairs of spaces, where $a,b,c$ are determined by inclusions:

$$
  \bigsqcup_{d \in I^2} U^d_* 
    \stackrel{\overset{a}{\to}}{\underset{b}{\to}}
  \bigsqcup _{i \in I} U^i_* \xrightarrow{c} X_*
  \,.
$$

+--{.un_theorem}
###### Theorem

If the pairs of spaces $U^f_*$ are connected for all 1-, 2-, or 3-fold  intersections $U^f_*$ of the pairs $U^i_*$, then

1. (Conn) The pair $X_*$ is connected; and

1. (Iso) The [[fundamental groupoid]] functor $\Pi_1$ takes the above coequaliser diagram of pairs of spaces to a (strict) coequaliser diagram of groupoids.

=--

The limit "3" on the connectivity hypothesis may be analyzed as "$1+2$", where $1$ is the categorical dimension of the fundamental groupoids we are considering and $2$ is a universal constant.  This becomes evident when generalizing to [[higher homotopy van Kampen theorems]].

In one proof of the theorem (due to Brown and Razak, see below), the number 3 arises from the Lebesgue covering dimension of $\mathbb{R}^2$.  This proof verifies the universal property for a coequaliser, using basic techniques: subdivide a path;  deform a subdivision so that it is product of paths joining points of $X_0$; subdivide a homotopy rel end points, and deform this subdivision so that _all_ subpaths join points of $X_0$; any composition of [[commutative square]]s in a groupoid is commutative.

In another, more categorical proof explained in the next section, the number $3$ arises from the fact that 2-colimits can be computed using coproducts and [[descent objects]] of 2-truncated [[simplicial objects]].

Note that the theorem about groupoids does _not_ reduce to a theorem about groups. For example, $X$ may be a connected space which is the union of two open sets each with many components and whose  intersection has many path components. Such examples arise commonly from applications to combinatorial group theory; consider for example a covering space of a wedge of spaces.    Or the connected $X$ may be the union of 23 open sets whose three fold intersections have 123 path components. In each case the fundamental group one might want to calculate  is in the middle of this complicated combinatorial situation, but at least the theorem has turned a topological problem into a group theory and combinatorial problem, and the remarkable fact is that the fundamental groups are _completely_ determined by the theorem. This is an "anomaly" for traditional algebraic topology, where invariants relating adjacent dimensions may be determined by exact sequences which do not give complete information. The reason for the success seems to be that groupoids have structure in dimensions 0 and 1, and so can model the gluing of spaces. 


This suggests that [[higher homotopy van Kampen theorem]]s could give new kinds of homotopical information, i.e. colimit theorems for higher homotopy invariants, which has proved to be so.


### Homotopy van Kampen theorem for groupoids

From a 2-categorical point of view, the strict van Kampen theorem above can be decomposed into the following parts:

1. When $X$ is the union of a family of open sets, then it is the homotopy colimit of a diagram involving these open sets.

1. The fundamental groupoid functor preserves homotopy colimits (i.e. takes them to homotopy colimits, or equivalently 2-colimits, of groupoids).

1. Certain 2-colimits of groupoids can be computed over "2-truncated" subdiagrams.

1. In certain situations, strict colimits of groupoids are also 2-colimits.

We can then prove the theorem by proving each of these three parts separately.  This is essentially accomplished in [Farjoun](#Farjoun).

+-- {: .num_theorem #Cechcover}
###### Theorem
If a space $X$ is the union of a family of open sets $(U^i)_{i\in I}$, then we have a [[weak equivalence]]
$$ hocolim C_\bullet(U) \xrightarrow{\sim} X, $$
where $C_\bullet(U)$ is the [[Cech cover]] of $X$, a [[simplicial space]] defined by
$$C_n(U) = \coprod_{J\subseteq I,\, |J|=n} \bigcap_{i\in J} U^i. $$
=--

See [Dugger-Isaksen 01](#DuggerIsaksen01).


+-- {: .num_theorem #Pi1Hocolim}
###### Theorem
Suppose $I$ is a small category and $(X^i)_{i\in I}$ is a [[diagram]] of spaces.  Then we have an equivalence of groupoids
$$ \Pi_1(\hocolim_i X^i) \simeq \hocolim_i \Pi_1(X^i). $$
=--
+-- {: .proof}
###### Proof
The functor $\Pi_1$ is, up to equivalence, the composite of itself with the 1st [[Postnikov approximation]] functor $P_1 : Top \to Top$.  We can regard $P_1$ as a [[Bousfield localization]] functor for $Top$ (for localizing at the map $S^2 \to \ast$), so it preserves homotopy colimits.  And $\Pi_1$ is part of a [[Quillen equivalence]] between $Gpd$ and the 1-localized model structure on $Top$, so it also preserves homotopy colimits.
=--

+-- {: .num_theorem #Codescent}
###### Theorem
If $X$ is the union of $(U^i)_{i\in I}$, and $X_0\subseteq X$ is a set of basepoints which intersects each 1-, 2-, and 3-fold intersection of opens $U^i$, then $\Pi_1(X,X_0)$ is equivalent to the [[2-colimit]] (i.e. [[codescent object]]) of the following diagram
$$ \coprod_{i,j,k} \Pi_1(U^{i j k},X_0) \;\underoverset{\to}{\to}{\to}\;
\coprod_{i,j} \Pi_1(U^{i j},X_0) \;\rightrightarrows\;
\coprod_i \Pi_1(U^i,X_0).
$$
=--
+-- {: .proof}
###### Proof
If we neglect the $X_0$'s, then what we have above is the 2-truncated part of the homotopy colimit of groupoids obtained by applying Theorem \ref{Pi1Hocolim} to Theorem \ref{Cechcover}.  Since homotopy colimits of simplicial objects in $Gpd$ are equivalent to codescent objects of their 2-truncations (essentially because groupoids are 1-groupoids), this has an equivalent homotopy colimit.  Finally, the assumption on $X_0$ ensures that restricting to it as a set of basepoints does not change the equivalence type of any of the groupoids in the 2-truncated diagram.
=--

+-- {: .num_theorem #CodescentCoeq}
###### Theorem
Under the hypotheses of Theorem \ref{Codescent}, we have that $\Pi_1(X,X_0)$ is isomorphic to the strict coequalizer of 
$$
\coprod_{i,j} \Pi_1(U^{i j},X_0) \;\rightrightarrows\;
\coprod_i \Pi_1(U^i,X_0).
$$
=--
+-- {: .proof}
###### Proof
Let $A = P(I)$ be the power set of the indexing set $I$, regarded as a poset, and consider the functor $F:A\to Gpd$ defined by $F(J) = \Pi_1(\bigcap_{i\in J} U^i, X_0)$.  We can verify that the 2-colimit of $F$ is equivalent to the codescent object in Theorem \ref{Codescent}, for essentially the same reasons cited there.  (Formally, one can say that the functor $P_{\le 3}(I) \to A$ is "2-final".)

However, $F$ is cofibrant in the [[projective model structure]] on $Gpd^A$, which is to say that the functor $A\xrightarrow{F} Gpd \xrightarrow{ob} Set$ is free (relative to the forgetful functor $Set^A \to Set^{ob(A)}$): its generators are the points $x\in F(J)$ such that $J = \{ i\in I \,|\, x\in U^i \}$.  Thus, the 2-colimit of $F$ is equivalent to its strict colimit, which in turn is easily seen to be the coequalizer shown above.

This shows that $\Pi_1(X,X_0)$ is equivalent to the strict coequalizer shown above.  But this equivalence is clearly also bijective on objects, so it is an isomorphism of groupoids.
=--


### Examples

Let $X=S^1$, $U= S^1 \setminus \{N\}$, and $V= S^1 \setminus \{S\}$, where $N$ and $S$ are antipodal points.  Then $U\cong V\cong (0,1)$ are contractible, while $U\cap V \cong (0,1) \sqcup (0,1)$.  Thus the homotopy van Kampen theorem gives a 2-pushout of groupoids that is equivalent to
$$ \array{ \ast\sqcup \ast & \to & \ast \\
  \downarrow && \downarrow \\
  \ast & \to & \Pi_1(S^1) } $$
It's not hard to compute that this 2-pushout must be $\mathbf{B}\mathbb{Z}$.  But we can also obtain this directly from the strict van Kampen theorem with a set $X_0 = \{u,v\}$ of two basepoints with $u\in U$ and $v\in V$, which yields a strict pushout of groupoids
$$ \array{ \ast\sqcup \ast & \to & \mathcal{I} \\
  \downarrow && \downarrow \\
  \mathcal{I} & \to & \Pi_1(S^1,X_0) } $$
where $\mathcal{I}$ is the invertible [[interval category]], which is (literally) $\Pi_1(U,X_0)$ and $\Pi_1(V,X_0)$.

Note that the version of the theorem for fundamental groups does not apply, since $U\cap V$ is not path-connected.

### van Kampen theorem in homotopy type theory 

The van Kampen theorem can be expressed in [[homotopy type theory]], a type theory under which one could do [[synthetic homotopy theory]], as follows:

Let $A, B, C$ be [[types]] and $f : A \to B$ and $g : A \to C$ [[functions]]. Let $P\equiv B \sqcup_A C$ be their [[pushout]].

By defining a special *code* function using the [[encode-decode method]] the van Kampen theorem says that:

$$\Pi_1 P(u, v) \simeq code(u,v)$$

There are (at least) two code functions that can be given, which are listed in section 8.7 of the [[HoTT Book]]. (it would be good if somebody could transcribe the code functions over here).  The first is a "naive" van Kampen theorem. The second version is the van Kampen at a set of basepoints.

## Generalizations

* [[van Kampen theorem for toposes]]

* [[higher homotopy van Kampen theorem]]

## References
 {#References}

The Seifert-van Kampen theorem is named after

* [[Herbert Seifert]]: *Konstruction drei dimensionaler geschlossener Räume*, Berichte Sachs. Akad. Leipzig, Math.-Phys. Kl. *83* (1931) 26–66

* [[Egbert van Kampen]]: *On the connection between the fundamental groups of some related spaces*, American Journal of Mathematics **55** (1933) 261–267 &lbrack;[jstor:51000091](https://www.jstor.org/stable/51000091)&rbrack;

Introduction and review:

* [[Peter May]], chapter 2 of: *[[A Concise Course in Algebraic Topology]]*, University of Chicago Press (1999) &lbrack;[ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf)&rbrack;

* {#Hatcher02} [[Allen Hatcher]], section 1.2 of: *Algebraic Topology*, Cambridge University Press (2002) \[<a href="https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401">ISBN:9780521795401</a>, [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)\]


See also: 

* Wikipedia: *[Seifert-van Kampen theorem](https://en.wikipedia.org/wiki/Seifert%E2%80%93Van_Kampen_theorem#References)*




The use of a set of base points for a pushout theorem and so determining the fundamental group of the circle was published in

* [[Ronnie Brown]], _Groupoids and van Kampen's theorem_, Proc. London Math. Soc. (3) 17 (1967) 385-401.

The more general theorem for the fundamental groupoid on a set of base points: 

* [[Ronnie Brown]] and A. Razak, _A van Kampen theorem for unions of non-connected  spaces_, Archiv. Math. 42 (1984) 85-88. [pdf](http://pages.bangor.ac.uk/pdffiles/brown-razak.pdf) 

See also this [mathoverflow discussion](http://mathoverflow.net/questions/40945/compelling-evidence-that-two-basepoints-are-better-than-one)


The pushout theorem is among  applications of groupoids to $1$-dimensional homotopy theory (e.g. gluing theorem, covering spaces, orbit spaces) and to the Jordan Curve Theorem in:

* [[Ronnie Brown]], _[Topology and Groupoids](http://groupoids.org.uk/topgpds.html)_, Booksurge (2006). pdf available;  book available from amazon. 

The proof for  pushouts  is discussed in some detail in

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_

as a background to the following chapters  on versions for crossed modules and crossed complexes,  i.e. for higher dimensional versions. 

The proof via homotopy colimits is roughly taken from

* {#Farjoun} [[Emmanuel Dror Farjoun]], _Fundamental group of homotopy colimits_, Adv. in Math. 182 (2004), 1-27.  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/farjoun.pdf))

Other references cited above:

* {#DuggerIsaksen01} [[Dan Dugger]], [[Daniel Isaksen]], _Hypercovers in topology_ ([arxiv:math/0111287](https://arxiv.org/abs/math/0111287))

Discussion of [[persistent homotopy]] with focus on the [[van Kampen theorem]], [[excision]] and the [[Hurewicz theorem]]:

* Mehmet Ali Batan, Mehmetcik Pamuk, Hanife Varli, *Persistent Homotopy* $[$[arXiv:1909.08865](https://arxiv.org/abs/1909.08865)$]$

For the van Kampen theorem in [[homotopy type theory]]:

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

Formalization of the van Kampen theorem in [[proof assistants]]: 

* [In Agda](https://github.com/HoTT/HoTT-Agda/tree/e48a16bcd719e2fcb409d79e3f7df6c6b81223bb/theorems/homotopy/vankampen)
* [In Lean](https://github.com/leanprover/lean2/blob/master/hott/homotopy/vankampen.hlean)

[[!redirects Seifert-van Kampen theorem]]
