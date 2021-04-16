+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

\tableofcontents

## Idea

A _torsor_ (in the [[category of sets]]) is, roughly speaking, a [[group]] that has forgotten its identity element; given any (non-empty) torsor with respect to a group $G$, we recover a group isomorphic to $G$ by making what is known as a _trivialisation_ of the torsor, which roughly corresponds to choosing an identity element. That we wish to keep track of the choice is precisely the reason for working with torsors.

Something analogous is present in the theory of [[Grothendieck fibration|fibrations]], where it can be important to make a choice of lifts ('cloven fibrations').

The notion of a torsor can be [[internalisation|internalised]] to any category with products, and more generally to any category in which the notion of an internal group can be made good sense of. We discuss this general notion below, after first discussing the notion in the category of sets. 


## In the category of sets

### Definition

\begin{defn} Let $G$ be a [[group]]. A _$G$-torsor_ is a [[set]] $T$ together with an [[action]] $a: G \times T \rightarrow T$ of $G$ on $T$ such that the [[shear map]] $a \times p_2: G \times T \rightarrow T \times T$ is an [[isomorphism]], where $p_2$ is the canonical [[projection]] map $G \times T \rightarrow T$. \end{defn}

\begin{rmk} \label{RemarkTorsorIsomorphicToStructureGroup} If $T$ is non-empty, we shall prove [below](#TrivialisationInSets) that it follows from the definition that $T$ is isomorphic to the underlying set of $G$.  There are many such isomorphisms, and where torsors are used it is often important to choose/fix one. Such a choice is known as a _trivialisation_ of $T$. See [below](#TrivialisationInSets) for more details. \end{rmk} 

\begin{rmk} As a consequence of Remark \ref{RemarkTorsorIsomorphicToStructureGroup}, a torsor with respect to some group can be thought of as a [[heap]]. \end{rmk}

\begin{rmk} Asking that $a \times p_2$ be an isomorphism is the same as to say that it is both [[free action|free]] and [[transitive action|transitive]]: free-ness corresponds to injectivity of $a \times p_2$, and transitivity corresponds to surjectivity of it. \end{rmk}

\begin{example} An [[affine space]] of dimension $n$ over a [[field]] $k$ is a torsor for the additive group $k^n$: this acts by _translation_. \end{example}

\begin{example} A [[unit of measurement]] is (typically) an element in an $\mathbb{R}^\times$-torsor, for $\mathbb{R}^\times$ the multiplicative group of non-zero [[real number]]s: for $u$ any unit and $r \in \mathbb{R}$ any non-vanishing real number, also $r u$ is a unit. And for $u_1$ and $u_2$ two units, one is expressed in terms of the other by a unique $r \neq 0$ as $u_1 = r u_2$. For instance for units of [[mass]] we have the unit of [[kilogram]] and that of gram and there is a unique number, $r = 1000$ with

  $$
    kg = 1000 g
    \,.
  $$

\end{example}

\begin{example} \label{ExampleTorsorFromAGroup} Let $G$ be a [[group]]. The action of $G$ on itself equips the underlying set of $G$ with the structure of a $G$-torsor. \end{example}

\begin{rmk} We shall see in Remark \ref{RemarkGroupStructureFromTrivialisation} that all torsors actually arise as in Example \ref{ExampleTorsorFromAGroup}.  \end{rmk}

### Trivialisation {#TrivialisationInSets}

\begin{prpn} \label{PropositionTorsorIsomorphicAsSetToStructureGroup} Let $G$ be a [[group]], and let $\underline{T} = \left( T, a: G \times T \rightarrow T \right)$ be a $G$-torsor. If $T$ is non-empty, it is isomorphic to the underlying set of $G$. \end{prpn}

\begin{proof} Let $t$ be an [[element]] of $T$. The following diagram is [[cartesian square|cartesian]]. 

\begin{centre}
  \begin{tikzcd}
    G \ar[r, "id \times t"] \ar[d, swap, "a \circ (id \times t)"] & G \times T \ar[d, "a \times p_2"] \\
    T \ar[r, swap, "id \times t"] & T \times T
  \end{tikzcd} 
\end{centre}

Since $\underline{T}$ is a $G$-torsor, we have that $a \times p_2$ is an isomorphism. The proposition thus follows immediately from the fact that pullbacks of isomorphisms are isomorphisms (as proven at [[pullback]]).

\end{proof} 

\begin{defn} Let $G$ be a [[group]], and let $\underline{T} = \left( T, a: G \times T \rightarrow T \right)$ be a $G$-torsor. A _trivialisation_ of $\underline{T}$ is an [[isomorphism]] between $T$ and the underlying set of $G$. \end{defn} 

\begin{rmk} By Proposition \ref{PropositionTorsorIsomorphicAsSetToStructureGroup}, if $T$ is non-empty, $T$ is always isomorphic to the underlying set of $G$. Thus the notion of a trivialisation of $\underline{T}$ is a question of a _choice_ of isomorphism between $T$ and the underlying set of $G$. 

The proof of Proposition \ref{PropositionTorsorIsomorphicAsSetToStructureGroup} shows that any choice of element of $T$ gives rise to a trivialisation. Some of these may of course coincide. \end{rmk} 

\begin{rmk} \label{RemarkGroupStructureFromTrivialisation} Let $\rho : G \rightarrow T$ be a trivialisation of a torsor $\underline{T}$. The map 

$$p_{1} \circ \left( \rho^{-1} \times id \right): T \times T \rightarrow G \times T \rightarrow G$$ 

where $p_1$ is the canonical map, can be interpreted as a notion of _division_ $d : T \times T \to G$, 'dividing' one element of $T$ by another to obtain an element of $G$. If we further compose $d$ with $\rho$ 

$$\rho \circ d : T \times T \rightarrow G \rightarrow T,$$

we can think of the resulting map $D$ as a 'division structure' on $T$ for which $\rho$ behaves as an identity, namely such that $D(g, g) = \rho$ for all $g \in G$. In this way, $T$ acquires a group structure isomorphic to that of $G$. 

Thus a trivialisation of a torsor equips with it a _choice_ of group structure amongst all of those isomorphic to $G$. 

\end{rmk} 

### Functoriality (change of structure group)

Torsors can be transported, or in other words pushed forward, along group homomorphisms, as we shall now show. (See also at *[G-space -- change of structure group](topological+G-space#ChangeOfGroupsAndFixedLoci)*).

\begin{prpn} Let $h : G_1 \rightarrow G_2$ be a [[homomorphism|group homomorphism]], and let $\underline{T} = \left( T, a \right)$ be a $G_1$-torsor. Observe that $\left(g_1, g_2, t \right) \mapsto \left( g_2 \cdot h(g_1)^{-1}, a(g_1, t) \right)$ defines an action $G_1 \times G_2 \times T \rightarrow G_2 \times T$ of $G_1$ on $G_2 \times T$. Then $\left(G_2 \times T \right) / G_1$, the quotient of $G_2 \times X$ with respect to this $G_1$-action, defines a $G_2$-torsor with respect to the action of $G_2$ induced by left multiplication, namely that given by $\left( g, \left[ (g', t') \right] \right) \mapsto \left[ \left(g g', t' \right) \right]$, where $\left[ p \right]$, for some $p \in G_2 \times T$, denotes the [[orbit]] of $p$ with respect to the action of $G_1$ on $G_2 \times T$. \end{prpn}

\begin{proof} We shall demonstrate that the map 

$$i : \left( G_2 \times T \right) \times \left( \left( G_2 \times T \right) / G_1 \right) \rightarrow G_2 \times \left( \left( G_2 \times T \right) / G_1 \right)$$

given by 

$$\left( (g, t), \left[ (g', t') \right] \right) \mapsto \left( g\left(g'\right)^{-1}, \left[ (g', t') \right] \right)$$

induces a map 

$$\overline{i} : \left( \left( G_2 \times T \right) / G_1 \right) \times \left( \left( G_2 \times T \right) / G_1 \right) \rightarrow G_2 \times \left( \left( G_2 \times T \right) / G_1 \right).$$

That is, it respects, in its left factor, the passage to the quotient by the action of $G_1$.

Suppose indeed that we have $(g, t) \in G_2 \times T$ and $\left( g_1, g'', t'' \right) \in G_1 \times G_2 \times T$ such that $(g, t) = \left( g'' \cdot h(g_1)^{-1}, a(g_1, t'') \right)$. We make the following observations.

1. $g''  h(g_1)^{-1} \left(g'\right) ^{-1} = g'' \left( g' h(g_1) \right)^{-1}$
1. $\left[ (g', t') \right] = \left[ \left( g' h\left(g_1^{-1}\right)^{-1}, a(g_1^{-1}, t') \right) \right] = \left[ \left( g' h(g_1), a\left(g_1^{-1}, t'\right) \right) \right]$

Putting these together, we obtain that

$$
\begin{aligned}
i\left( \left( g'', t'' \right), \left[ \left( g', t' \right) \right] \right) &= i\left( \left( g'', t'' \right), \left[ \left( g' h(g_1), a\left( g_1^{-1}, t' \right) \right) \right] \right) \\
  &= \left( g'' h(g_1)^{-1} \left(g' \right)^{-1}, \left[ \left( g' h(g_1), a\left( g_1^{-1}, t' \right) \right) \right] \right) \\
  &= \left( g \left(g' \right)^{-1}, \left[ \left( g', t' \right) \right] \right) \\
  &= i\left( g, \left[ \left( g', t' \right) \right] \right),    
\end{aligned}
$$

as required.

We now observe that $\overline{i}$ defines an inverse to $a' \times p_{2}$, where $a'$ is the action of $G_2$ on $\left( G_2 \times T \right) / G_1$ induced by left multiplication, and $p_2$ is the projection map $G_2 \times \left( \left( G_2 \times T \right) / G_1 \right) \rightarrow \left( \left( G_2 \times T \right) / G_1 \right)$. In one direction, for any $g, g' \in G_2$ and $t \in T$, we have that 

$$\overline{i}\left( \left[ \left(g' g, t \right) \right], \left[ \left( g, t \right) \right] \right) = \left( g' g g^{-1}, \left[ \left( g, t \right) \right] \right) = \left( g', \left[ \left( g, t \right) \right] \right),$$ 

as required. In the other direction, suppose that we have $\left( \left[ \left(g, t \right) \right], \left[ \left( g', t' \right) \right] \right) \in \left( \left( G_2 \times T \right) / G_1 \right) \times \left( \left( G_2 \times T \right) / G_1 \right)$. Since the map $a \times p_2 : G_1 \times T \rightarrow T \times T$ is an isomorphism, there is a $g_1 \in G_1$ such that $t' = a(g_1, t)$, and we have that $\left[ \left(g, t \right) \right] = \left[ \left( g h(g_1)^{-1}, t' \right) \right]$. We then have that $a' \times p_2$ applied to 

$$\overline{i}\left( \left[ \left(g, t \right) \right], \left[ \left( g', t' \right) \right] \right) = \overline{i}\left( \left[ \left(g h(g_1)^{-1}, t' \right) \right], \left[ \left( g', t' \right) \right] \right) =  \left( g h(g_1)^{-1} \left(g'\right)^{-1}, \left[ \left( g', t' \right) \right] \right)$$ 

is

$$\left( \left[ \left(g h(g_1)^{-1} \left( g' \right)^{-1} g', t' \right) \right],  \left[ \left( g', t' \right) \right] \right) = \left( \left[ \left(g h(g_1)^{-1}, t' \right) \right], \left[ \left( g', t' \right) \right] \right) = \left( \left[ \left(g, t \right) \right], \left[ \left( g', t' \right) \right] \right),$$

as required.

\end{proof}

\begin{defn} Let $h : G_1 \rightarrow G_2$ be a [[homomorphism|group homomorphism]], and let $\underline{T} = \left( T, a \right)$ be a $G_1$-torsor. We refer to the $G_2$-torsor constructed from $\underline{T}$ using $h$ as in Proposition \ref{PropositionTorsorChangeOfStructureGroup} as the torsor obtained from $\underline{T}$ by _change of structure group_, and denote it $h_{*}\left(\underline{T}\right)$. \end{defn}


## In general

More generally, one may consider torsors over some base space $B$ (in other words, working in the [[topos]] of sheaves over $B$ instead of $Set$). In this case the term __$G$-torsor__ is often used more or less a synonym for the term $G$-[[principal bundle]], but torsors are generally understood in contexts much wider than the term "principal bundle" is usually taken to apply. And a principal bundle is strictly speaking a torsor that is required to be _locally trivial_ . Thus, while the terminology 'principal bundle' is usually used in the setting of [[topological spaces]] or [[smooth manifold]]s, the term _torsor_ is traditionally used in the more general contex of [[Grothendieck topology|Grothendieck topologies]] (faithfully flat and &#233;tale topology in particular), [[topos|topoi]] and for generalizations in various category-theoretic setups. While in the phrase '$G$-principal bundle' $G$ is usually a (topological) [[group]] or [[groupoid]], when we say '$G$-torsor', $G$ is usually a [[presheaf]] or [[sheaf]] of group(oid)s, or $G$ is a plain [[category]] (not necessarily even a groupoid).

A __$G$-torsor__, without any base space given, can also simply be an inhabited transitive free $G$-[[action|set]], which is the same as a principal $G$-bundle over the [[point]]. The notion may also be defined in any category with products: a torsor over a [[group object]] $G$ is a [[well-supported object]] $E$ together with a $G$-action $\alpha: G \times E \to E$ such that the arrow 

$$\langle \pi_1, \alpha \rangle: G \times E \to E \times E$$ 

is an [[isomorphism]].

### Definition

Let $G$ be a [[group]] object in some [[category]] $C$, that in the following is assumed, for simplicity, to be a [[cartesian monoidal category]].
The [[object]]s of $C$ we sometimes call [[space]]s. Examples to keep in mind are $C = $ [[Set]] (in which case $G$ is an ordinary [[group]]) or [[Top]] (in which case it is a [[topological group]]) or [[Diff]] (in which case it is a [[Lie group]]).

\begin{defn} A left **$G$-torsor** is an [[inhabited object]] $P$ equipped with a $G$-[[action]], $\rho: G \times P \to P$ (subject to the usual laws for actions) such that the map 

$$\langle \rho, \pi_2 \rangle: G \times P \to P \times P$$ 

is an [[isomorphism]]. \end{defn}

More generally, suppose $C$ is [[finitely complete category|finitely complete]], and let $B$ be an object. Then the [[slice category|slice]] $C/B$ is finitely complete, and the pullback functor $- \times B: C \to C/B$ preserves finite limits. Thus $\pi_2: G \times B  \to B$ acquires a group structure in $C/B$. 

\begin{defn} A left **$G$-torsor over $B$** is a $G$-torsor in $C/B$. \end{defn}

Thus, if $B = 1$ is a point, a torsor over a point is the same as an ordinary torsor in $C$, but sometimes the additional "over a point" is convenient for the sake of emphasis. 

We restate this definition equivalently in more nuts-and-bolts terms. The ambient category is $C$, as before.

\begin{defn} A left $G$-torsor over $B \in C$ is a [[bundle]] $P\stackrel{\pi}{\to} B$ over $B$ together with a left group [[action]]

$$
  \rho : G\times_B P \to P
$$

which in terms of [[generalized element]]s we write

$$
  (g,p)\to g.p
$$

such that the induced morphism of [[product]]s

$$
  \phi := (\rho, p_2) : G\times_B P \to P\times_B P
$$

which on elements acts as

$$
  (g,p)\to (g.p,p)
$$ 

is an [[isomorphism]].  

\end{defn}

\begin{rmk} As we explain [below](#LocalTrivialization), a torsor is in some tautological sense **locally trivial**, but some care must be taken in interpreting this. One sense is that there is a cover $U$ of $1$ (so that $U \to 1$ is epi, i.e., $U$ is inhabited) such that the torsor, when pulled back to $U$, becomes trivial (i.e., isomorphic to $G$ as $G$-torsor). But this is a very general notion of "cover". A more restrictive sense frequently encountered in the literature is that "cover" means a coproduct of subterminal objects $U_i \hookrightarrow 1$ such that $U = \sum_i U_i$ is inhabited (e.g., an open cover of a space $B$ seen as the terminal object of the sheaf topos $Sh(B)$), and "torsor" would then refer to the local triviality condition for some such $U$. This is the more usual sense when referring to principal bundles as torsors. Or, "cover" could refer to a covering sieve in a [[Grothendieck topology]]. 

(The condition on the action can be translated to give transitivity etc. in the case of $B$ is a point (left as a standard exercise).)

\end{rmk}

### Examples

#### In topological spaces

Let $C = $ [[Top]], so that all objects are [[topological space]]s and groups $G$ are [[topological group]]s. 

A topological $G$-[[principal bundle]] $\pi: P \to B$ is an example of a torsor over $B$ in $Top$. This becomes a definition of principal bundle if we demand local triviality with respect to some open cover of $B$ (see the remarks [below](#LocalTrivialization)). 

#### In sheaves

Let $C = Sh(S)$ be a [[category of sheaves]] over a [[site]] $S$.

The canonical example for a torsor in $C$ is the [[trivial torsor]] over a [[sheaf]] of groups, $G$.

#### Group extensions {#GroupExtensions}

Every [[group extension]] $A \to \hat G \to G$ canonically equips $\hat G$ with the structure of an $A$-torsor over $G$. See <a href="http://ncatlab.org/nlab/show/group+extension#Torsors">Group extensions as torsors</a> for details

### Local trivialization {#LocalTrivialization}

In other categories $C$ besides $Set$, we cannot just "pick a point" of $P$ even if $P \to 1$ is an [[epimorphism]], so this argument cannot be carried out, and indeed trivializations may not exist. However, it is possible to construct a local trivialization of a torsor, following a general philosophy from [[topos theory]] that a statement is "locally true" in a category $C$ if it becomes true when reinterpreted in a slice after pulling back $C \to C/U$, where $U$ is inhabited. (This in some sense is the basis of [[Kripke-Joyal semantics]].) 

In the present case, we may take $U = P$. Although we cannot "pick a point" of $P$ (= global section of $P \to 1$), we can pick a point of $P$ if we reinterpret it by pulling back to $C/P$. In other words, $\pi_2: P \times P \to 1 \times P \cong P$ does have a global section regarded as an arrow in $C/P$. In fact, there is a "generic point": the diagonal $\Delta: P \to P \times P$. Then, we may mimic the argument above, and consider the pullback diagram 

$$\array{
G \times P & \to & G \times P \times P \\
\downarrow & & \downarrow \mathrlap{\langle \rho, \pi_2 \rangle \times id} \\
P \times P & \underset{id \times \Delta}{\to} & P \times P \times P
}$$ 

living in $C/P$. As argued above, the vertical arrow on the left is an isomorphism; in fact, it is the isomorphism $\langle \rho, \pi_2 \rangle: G \times P \to P \times P$ we started with! 

Thus, a $G$-torsor in a category with products can be tautologically interpreted in terms of $G$-actions on objects $P$ which become trivialized upon pulling back to the slice $C/P$. 


## Generalizations

* Instead of a torsor over a group, one can consider a torsor over a [[category]]. See [[torsor with structure category]]. 

* In [[noncommutative algebraic geometry]], faithfully flat [[Hopf-Galois extension]]s are considered a generalization of (affine) torsors in algebraic geometry.

## Related concepts

* [[homogeneous space]]
* [[principal bundle]] / [[associated bundle]]
* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]
* [[principal 3-bundle]] / [[bundle 2-gerbe]]
* [[principal ∞-bundle]] / [[associated ∞-bundle]]
* [[descent along a torsor]], [[Schneider's descent theorem]]
* [[Hopf-Galois extension]], [[quantum homogeneous space]],
* [[noncommutative principal bundle]], [[quantum heap]]

* [[physical unit]]

## References 

Elementary exposition:

* {#Baez} [[John Baez]], _Torsors made easy_, ([web](http://math.ucr.edu/home/baez/torsors.html))

  > (discussion for [[discrete groups]])


Textbook accounts:

* {#Milne80} [[James Milne]], Prop. III.4.1 in: _[[Étale Cohomology]]_, Princeton Mathematical Series __33__, 1980. xiii+323 pp. ([jstor:j.ctt1bpmbk1](https://www.jstor.org/stable/j.ctt1bpmbk1))

  > (discussion for [[algebraic groups]] in [[algebraic geometry]])

For more see the references at _[[principal bundle]]_ (which are torsors in the generality [[internalization|internal]] to [[slice categories]]).

A general [[topos theory|topos theoretic]] account is in  

* [[Peter Johnstone]], Section B3.2 of: _[[Sketches of an Elephant]]_ .

See also the references at _[[Diaconescu's theorem]]_.

Discussion in [[homotopy type theory]]/[[univalent mathematics]]:

* {#SymmetryBook} Def. 4.6.1 in: _Symmetry_ ([pdf](https://unimath.github.io/SymmetryBook/book.pdf))

Some further [[category theory|category theoretic]] articles discussing torsors:

* [[Tomasz Brzeziński]], _On synthetic interpretation of quantum principal bundles_, AJSE D - Mathematics 35(1D): 13-27, 2010 [arXiv:0912.0213](http://arxiv.org/abs/0912.0213)

* D. H. Van Osdol, _Principal homogeneous objects as representable functors_,
Cahiers Topologie G&#233;om. Diff&#233;rentielle 18 (1977), no. 3, 271--289, [numdam](http://www.numdam.org/item?id=CTGDC_1977__18_3_271_0)

*  K. T. S. Mohapeloa, _A $2$-colimit characterization of internal categories of torsors_, J. Pure Appl. Algebra 71 (1991), no. 1, 75--91, [doi](http://dx.doi.org/10.1016/0022-4049%2891%2990041-Y) 

* Thomas Booker, Ross Street, _Torsors, herds and flocks_ ([arXiv:0912.4551](http://arxiv.org/abs/0912.4551))

* J. Duskin, _Simplicial methods and the interpretation of 'triple' cohomology_, Memoirs AMS __3__, issue 2, n&#176; 163, 1975.  MR393196

* A. Vistoli, _Grothendieck topologies, fibered categories and descent theory_, in: [[FGA explained]], 1--104, Math. Surveys Monogr., 123, AMS 2005, [math.AG/0412512](http://front.math.ucdavis.edu/0412.5512)

* [[Ieke Moerdijk]], _Introduction to the language of stacks and gerbes_, [math.AT/0212266](http://arxiv.org/abs/math/0212266).

Much further material is also in Giraud's book on nonabelian cohomology. 

In a [[model theory|model theoretic]] context of [[definable set]]s, principal homogeneous spaces are studied in

* [[Anand Pillay]], _Remarks on Galois cohomology and definability_, The Journal of Symbolic Logic __62__:2 (1997) 487-492 [doi](https://doi.org/10.2307/2275542)

See also

* MathOverflow, _[torsors-for-monoids](http://mathoverflow.net/questions/25863/torsors-for-monoids/25886)_

[[!redirects torsors]]

[[!redirects principal homogeneous space]]
[[!redirects principal homogeneous spaces]]
