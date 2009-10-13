# Idea #

"Thin elements" occur in various contexts.  The basic idea is that  many [[higher category theory|higher categorical structures]] have cells (of [[geometric shapes for higher structures|various shapes]]).  However, in some contexts, some of these cells should be regarded as "more canonical," "more [[equivalence]]-like," or "more identity-like" than others.  The cells with this property are frequently called **thin** and the extra information of which cells are thin is called a **thin structure** or a **stratification**.


# Thin cells in higher groupoids #

In the simplicial [[singular complex]] $S X$ of a [[topological space]] $X$, a singular simplex $f: \Delta^n \to X$ is called **thin** if it factors through a [[retraction]] $r: \Delta^n \to \Lambda^{n-1}_i$ to some horn of $\Delta^n$.  Then the well known [[Kan complex|Kan]] condition on $S X$ can be strengthend to say that every horn in $S X$ has a _thin_ filler.  There are also, usually, other non-thin fillers which depend on $X$.

It is difficult to decide the laws that these these thin elements should satisfy.  Keith Dakin's axioms on thin elements in a simplicial  set $K$ with subsets $T_n \subseteq K_n, n \geq 1$, of elements called _thin_ are 
1. Degenerate elements are thin;
1. Any horn has a unique thin filler;
1. If all faces but one of a thin element are thin, then so is the remaining face. 

Ashley's theorem, conjectured by Dakin, is that the category of such  $T$-[[T-complex|complexes]] is equivalent to that of [[crossed complexes]].

As for relations with complexes having cells of different shapes, Brown and Higgins proved that cubical $T$-complexes are equivalent to crossed complexes, and to strict cubical $omega$-groupoids with connections.  In that theory, the notion of thin element is crucial because it can be proved that any (multiple) composition of thin elements is thin, and because of the relation of thin elements to commutative shells.  David Jones in his thesis developed the notion of polyhedral $T$-complex, and gave sufficient axioms for these to be equivalent to crossed complexes.


# Thin structures in double categories #

Among other things, a **thin structure** on a [[double category]] can be seen as giving the information of which squares should be thought of as _commuting_ rather than simply _containing a 2-cell_.  The most general definition seems to be that a thin structure on a double category $D$ is a morphism of double categories $\Theta: \square C \to D$ where $C$ is any category and $\square C$ is the double category of commuting squares in $C$. 

Note that $D$ contains the categories $D_v, D_h$ of vertical and horizontal edges respectively, and it is often convenient to take $C$ to be say $D_v$ and for $\Theta$ to be the identity on $D_v$. Then $\Theta$ defines a function $\Gamma: D_v \to D$ to the set of squares of $D$ which is called a _connection_, and also a functor $\gamma: D_v \to D_h$ which is called the _holonomy_ of the connection $\Gamma$. The laws which $\Gamma$ satisfies allow $\Theta$ to be recovered from $\Gamma$ in some cases.  


Thus some thin structures  contain a way to represent any vertical arrow as a horizontal arrow (or vice versa, depending on one's conventions).  Thin structures can equivalently be described by "foldings" and "connection pairs."  It turns out that when they exist, they are unique up to a (suitably weak) notion of equivalence; see also [[framed bicategory]].


# Simplicial nerves for higher categories #

Following on the work mentioned above for thin elements in Kan complexes, one can consider thin elements in [[nerves]] of higher categories.  In "The algebra of oriented simplices" Street constructed the simplicial nerve for a [[strict omega-category]], which comes equipped with a collection of thin simplices that are identities (rather than merely cells).  Thus this nerve is not just a simplicial set, but a [[stratified simplicial set]] (a simplicial set equipped with a collection of "thin simplices" containing all degeneracies).

Street and Roberts conjectured that the nerves of strict $\omega$-categories could be characterized as stratified simplicial sets such that
1. every [[complicial horn]] has a unique thin filler, and 
1. for such a thin filler, if all faces but the one missing face in the complicial horn are thin, then so is the last one.

Such stratified simplicial sets are called [[complicial sets]].  This conjecture was later proved by Verity.

A [[weak complicial set]] is a stratified simplicial set satisfying the above conditions except that thin fillers need not be unique. Street conjectured that these represent the nerves of _weak_ $\omega$-categories, where now the thin simplices are supposed to be the _equivalences_ rather than the identities.  But since every complicial set is weak complicial, one should also require that the collection of thin simplices is "maximal" in some sense; Street gave one proposed characterization.  Weak complicial sets have been studied extensively by Verity.


#References#

Verity's work can be found in 

*   D. R. Verity, 2005, Complicial Sets , URL http://arxiv.org/abs/math.CT/0410412. 

*   D. Verity, 2006, Weak complicial sets I: basic homotopy theory , available from : 
arXiv.org:math/0604414. 

*    D. R. Verity, 2006, Weak complicial sets. III. Enriched and internal quasi-category theory , 
(in preparation). 

*    D. R. Verity, 2007, Weak complicial sets. II. Nerves of complicial Gray-categories , in Cate
gories in algebra, geometry and mathematical physics , volume 431 of Contemp. Math., 441 &#8211; 
467, Amer. Math. Soc., Providence, RI. 



[[!redirects thin elements]]
[[!redirects thin]]