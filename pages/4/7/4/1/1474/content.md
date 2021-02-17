
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[topological space]] (or more generally, a [[convergence space]]) is _Hausdorff_ if [[convergence]] is unique.  The concept can also be defined for [[locales]] (see Definition \ref{proper} below) and [[categorification|categorified]] (see [Beyond topological spaces](#BeyondTopologicalSpaces) below).  A Hausdorff space is often called $T_2$, since this condition came second in the original list of four [[separation axioms]] (there are more now) satisfied by [[metric spaces]].

[[!include main separation axioms -- table]]


Hausdorff spaces are a kind of [[nice topological space]]; they do not form a particularly [[nice category of spaces]] themselves, but many such nice categories consist of only Hausdorff spaces.  In fact, [[Felix Hausdorff]]\'s original definition of 'topological space' actually required the space to be Hausdorff, hence the name.  Certainly [[homotopy theory]] (up to [[weak homotopy equivalence]]) needs only Hausdorff spaces.  It is also common in analysis to assume that all spaces encountered are Hausdorff; if necessary, this can be arranged since every space has a Hausdorff quotient (in fact, the Hausdorff spaces form a [[reflective subcategory]] of [[Top]]), although usually an easier method is available than this sledgehammer.


## Definitions
 {#Definitions}

There are many equivalent ways of characterizing a space $S$ as __Hausdorff__. The traditional definition is this:

+-- {: .num_defn #classical}
###### Definition

Given points $x$ and $y$ of $S$, if $x \neq y$, then there exist [[open neighbourhoods]] $U$ of $x$ and $V$ of $y$ in $S$ that are [[disjoint subsets|disjoint]]: sutch that their [[intersection]] $U \cap V$ is the [[empty set]] (or explicitly, such that $x' \ne y'$ whenever $x' \in U$ and $y' \in V$).
=--

That is, any two distinct points can be _separated_ by open neighbourhoods, and it is simply a mundane way of saying that $\ne$ is [[open subset|open]] in the [[product topology]] on $S \times S$.


Here is a classically equivalent definition that is more suitable for [[constructive mathematics]]:

+-- {: .num_defn #constructive}
###### Definition

Given points $x$ and $y$ of $S$, if every neighbourhood $U$ of $x$ in $S$ meets every neighbourhood $V$ of $y$ in $S$ (which means that $U \cap V$ is [[inhabited set|inhabited]]), then $x = y$.
=--

This is the mundane way of saying that $=$ is [[closed subset|closed]] in $S \times S$.

Another way of saying this, which makes sense also for [[locales]], is the following:

+-- {: .num_defn #proper}
###### Definition

The [[diagonal]] embedding $S \to S \times S$ is a [[proper map]] (or equivalently a [[closed map]], since any closed subspace inclusion is proper).
=--

This way of stating the definition generalizes to [[topos theory]] and thus to many other contexts; but it is not always a faithful generalization of the classical notion for topological spaces.  See _[Beyond topological spaces](#BeyondTopologicalSpaces)_ below for more.


Here is an equivalent definition (constructively equivalent to Definition \ref{constructive}) that makes sense for arbitrary [[convergence spaces]]:

+-- {: .num_defn #convergence}
###### Definition

Given a [[net]] (or equivalently, a proper [[filter]]) in $S$, if it converges to both $x$ and $y$, then $x = y$.
=--

That is, convergence in a Hausdorff space is unique.

## Examples

+-- {: .num_prop }
###### Proposition

[[a CW-complex is a Hausdorff space]].

=--


## Properties

### Hausdorff reflection
 {#HausdorffReflections}

+-- {: .num_prop #HausdorffReflection}
###### Proposition
**(Hausdorff reflection)**

For every [[topological space]] $X$ there exists
a [[Hausdorff topological space]] $H X$ and a [[continuous function]]

$$
  h_X
    \;\colon\;
  X \longrightarrow H X
$$

which is the  "closest approximation from the left" to $X$ by a Hausdorff topological space, in that
for $Y$ any [[Hausdorff topological space]], then [[continuous functions]] of the form

$$
  f \;\colon\; X \longrightarrow Y
$$

are in [[bijection]] with [[continuous function]] of the form

$$
  \tilde f \;\colon\; H X \longrightarrow Y
$$

and such that the bijection is constituted by

$$
  f = \tilde f \circ h_X
  \;\colon\;
    X
      \overset{h_X}{\longrightarrow}
    H X
      \overset{\tilde f}{\longrightarrow}
    Y
  \,.
$$

Here $H X$ (or more precisely $h_X$) is also called the _Hausdorff reflection_ (or _Hausdorffication_ or similar) of $X$.

Moreover, the operation $H(-)$ extends to [[continuous functions]] $f \colon X \to Y$

$$
  (X \overset{f}{\to} Y)
    \;\mapsto\;
  (H X \overset{H f}{\to} H Y)
$$

by setting 

$$
  H f \;\colon\; [x] \mapsto [f(x)]
  \,,
$$

where $[x]$ denotes the [[equivalence class]] under $\sim_X$ of any $x \in X$.

Finally, the comparison map is compatible with this in that the follows [[commuting squares|squares commute]]:

$$
  \array{
      X &\overset{f}{\longrightarrow}& Y
      \\
      {}^{\mathllap{h_X}}\downarrow && \downarrow^{\mathrlap{h_Y}}
      \\
      H X &\underset{H f}{\longrightarrow}& H Y
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

There are various ways to construct $h_X$, see below prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces} and prop. \ref{HausdorffReflectionViaTransitiveClosureOfDiagonal}


=--

+-- {: .num_remark }
###### Remark

In the language of [[category theory]] the Hausdorff reflection of prop. \ref{HausdorffReflection}
says that 

1. $H$ is a _[[functor]]_ $H \;\colon\; Top \longrightarrow Top_{Haus}$ from the [[category]] [[Top]] of [[topological spaces]] to the [[full subcategory]] $Top_{Haus} \overset{\iota}{\hookrightarrow} Top$ of Hausdorff topological spaces;

1. $h_X \colon X \to H X$ is a [[natural transformation]] from the [[identity functor]] on [[Top]] to the functor $\iota \circ H$

1. [[Hausdorff topological spaces]] form a [[reflective subcategory]] of all [[topological spaces]] in that $H$ is [[left adjoint]] to the inclusion functor $\iota$

   $$
     Top_{Haus}
       \underoverset{\underset{\iota}{\hookrightarrow}}{\overset{H}{\longleftarrow}}{\bot}
     Top
     \,.
   $$


=--

There are various ways to see the existence and to construct the Hausdorff reflection. The following is maybe the quickest way to see the existence, even though it leaves the actual construction rather implicit.


+-- {: .num_prop #HausdorffReflectionViaHomsIntoAllHausdorffSpaces}
###### Proposition

Let $(X,\tau)$ be a [[topological space]] and consider the [[equivalence relation]] $\sim$ on the underlying set $X$
for which $x \sim y$ precisely if for every [[surjective function|surjective]] [[continuous function]] $f \colon X \to Y$ into any
[[Hausdorff topological space]] $Y$ we have $f(x) = f(y)$. 

Then the set of [[equivalence classes]]

$$
  H X \coloneqq X /{\sim}
$$

equipped with the [[quotient topology]] is a [[Hausdorff topological space]] and the quotient map $h_X \;\colon\; X \to X/{\sim}$ exhibits the Hausdorff reflection of $X$, according to prop. \ref{HausdorffReflection}.

=--

+-- {: .proof}
###### Proof

First observe that every continuous function $f \colon X \longrightarrow Y$ into a Hausdorff space $Y$
factors uniquely via $h_X$ through a continuous function $\tilde f$

$$
  f = \tilde f \circ h_X
$$

where

$$
  \tilde f \colon [x] \mapsto f(x)
  \,.
$$

That this is well defined and continuous follows directly from the definitions.

What remains to be seen is that $H X$ is indeed a Hausdorff space. Hence assume that $[x] \neq [y] \in H X$.
By construction of $H X$ this means that there exists a Hausdorff space $Y$ and a surjective continuous function
$f \colon X \longrightarrow Y$ such that $f(x) \neq f(y) \in Y$. Accordingly, since $Y$ is Hausdorff,
there exist disjoint open neighbourhoods $U_x, U_y \in \tau_Y$. Moreover, by the previous statement there
exists a continuous function $\tilde f \colon H X \to Y$ with $\tilde f([x]) = f(x)$ and $\tilde f([y]) = f(y)$.
Since, by the nature of continuous functions,
the pre-images $\tilde f^{-1}( U_x ), \tilde f^{-1}(U_y) \subset H X$ are still disjoint and open,
we have found disjoint neighbourhoods of $[x]$ and $[y]$. Hence $H X$ is Hausdorff.

=--


Some readers may find the following a more direct way of constructing the Hausdorff reflection:

+-- {: .num_prop #HausdorffReflectionViaTransitiveClosureOfDiagonal}
###### Proposition

For $(Y,\tau_Y)$ a [[topological space]], write $r_Y \subset Y \times Y$
for the [[transitive relation|transitive closure]] of the [[relation]] given by the [[topological closure]] $Cl(\Delta_Y)$ of the [[image]] of the [[diagonal]] $\Delta_Y \colon Y \hookrightarrow Y \times Y$.

$$
  r_Y \coloneqq Trans(Cl(Delta_Y))
  \,.
$$

Now for $(X,\tau_X)$ a [[topological space]], define by [[induction]] for each [[ordinal number]] $\alpha$ an [[equivalence relation]] $r^\alpha$ on $X$ as follows, where we write $q^\alpha \colon X \to H^\alpha(X)$ for the corresponding [[quotient topological space]] projection:

We start the induction with the trivial equivalence relation:

* $r^0_X \coloneqq \Delta_X$;

For a [[successor ordinal]] we set

* $r_X^{\alpha+1} \coloneqq \left\{ (a,b) \in X \times X  \,\vert\, (q^\alpha(a), q^\alpha(b)) \in r_{H^\alpha(X)} \right\}$

and for a [[limit ordinal]] $\alpha$ we set

* $r_X^\alpha \coloneqq \underset{\beta \lt \alpha}{\cup} r_X^\beta$.

Then:

1. there exists an ordinal $\alpha$ such that $r_X^\alpha = r_X^{\alpha+1}$

1. for this $\alpha$ then $H^\alpha(X) = H(X)$ is the Hausdorff reflection from prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces}.


=--

([vanMunster 14, section 4](#vanMunster14))


### Monadicity

The topology on a [[compact space|compact]] Hausdorff space is given precisely by the (existent because compact, unique because Hausdorff) limit of each [[ultrafilter]] on the space.  Accordingly, compact Hausdorff topological spaces are (perhaps surprisingly) described by a (large) [[algebraic theory]].  In fact, the category of compact Hausdorff spaces is [[monadic functor|monadic]] (over [[Set]]); the [[monad]] in question maps each set to the set ultrafilters on it.  (The results of this paragraph require the [[ultrafilter theorem]], a weak form of the [[axiom of choice]]; see [[ultrafilter monad]].)

A compact Hausdorff [[locale]] (or space) is necessarily [[regular locale|regular]]; a regular locale (or $T_0$ space) is necessarily Hausdorff.  Accordingly, [[locale]] theory usually speaks of 'compact regular' locales instead of 'compact Hausdorff' locales, since the definition of regularity is easier and more natural.  Then a version of the previous paragraph works for compact regular locales *without* the ultrafilter theorem, and indeed [[constructive mathematics|constructively]] over any [[topos]].


### Sobriety

Using [[classical logic]] (but not in [[constructive logic]]) every Hausdorff space is a [[sober topological space]]: _[[Hausdorff implies sober]]_.  


### Relation to compact spaces

+-- {: .num_prop }
###### Proposition

[[compact subspaces of Hausdorff spaces are closed]].

=--

+-- {: .num_prop }
###### Proposition

[[maps from compact spaces to Hausdorff spaces are closed and proper]]

=--

### Dense subspaces and Epimorphisms


\begin{proposition}
 \label{DenseSubspaceInclusionsAreEpimorphismsAmongHausdorffSpaces}

In the [[category]] of [[Hausdorff topological spaces]] (with [[continuous functions]] between them), the inclusion of a [[dense subspace]] 

$$
  A \overset{\;\;i\;\;}{\hookrightarrow} X
$$ 

is an [[epimorphism]]. 

\end{proposition}

Here is a proof in the language of [[category theory]]:

\begin{proof}

We have to show that for $(f,g)$ any [[pair]] of [[parallel morphisms]] out of $X$

$$
  A 
  \overset{\;\;i\;\;}{\hookrightarrow}
  X 
  \underoverset
  {\;\;g\;\;}
  {\;\;f\;\;}
  {\rightrightarrows}
  Y
$$

into a [[Hausdorff space]] $Y$, the [[equality]] $f \circ i = g \circ i$ implies $f = g$. Equivalently, that $f \circ i = g \circ i$ implies that $1_X \colon X \to X$ is the [[equalizer]] of the pair $(f, g)$. But the equalizer $E \to X$ is formed by taking a [[pullback]] of the [[diagonal map]] $\Delta \colon Y \to Y \times Y$ along $(f, g) \colon X \to Y \times Y$: 

$$\array{
E & \to & Y \\
\downarrow & & \downarrow \mathrlap{\Delta} \\
X & \underset{(f, g)}{\to} & Y \times Y. 
}$$ 

Since $Y$ is Hausdorff, the subset $\Delta: Y \to Y \times Y$ is closed, and the pullback $E \hookrightarrow X$ of this closed subset along the continuous map $h = (f, g)$, which is $E = h^{-1}(\Delta)$, is also closed. Since $E$ is a closed subset of $X$ and contains a dense subspace $i: A \hookrightarrow X$, it must be all of $X$ (as a subset of itself). 
\end{proof} 

Note, incidentally, that $X$ itself doesn't have to be Hausdorff for the argument to go through. 

Alternatively, here is a proof in the language of [[general topology|basic topology]]:

\begin{proof}

We have to show that for $(f,g)$ any [[pair]] of [[parallel morphisms]] out of $X$

$$
  A 
  \overset{\;\;i\;\;}{\hookrightarrow}
  X 
  \underoverset
  {\;\;g\;\;}
  {\;\;f\;\;}
  {\rightrightarrows}
  Y
$$

into a [[Hausdorff space]] $Y$, the [[equality]] $f \circ i = g \circ i$ implies $f = g$. With [[classical logic]] we may equivalently show the [[contrapositive]]: That $f \neq g$ implies $f \circ i \neq  g \circ i$.

So assume that $f \neq g$. This means that there exists $y \in Y$ with $f(y) \neq g(y)$. Since $Y$ is Hausdorff, there exist then [[disjoint subset|disjoint]] [[open neighbourhoods]] $O_{f(y)},\;O_{g(y)} \subset Y$, i.e. $f(x) \in O_{f(x)}$ and $g(x) \in O_{g(x)}$ with $O_{f(x)} \cap O_{g(x)} = \varnothing$.

But their [[preimages]] must intersect at least in $x \in f^{-1}\big( O_{f(x)} \big) \cap g^{-1}\big(  O_{g(x)} \big)$. Since this intersection is an [[open subset]] (as preimages of open subsets are open by definition of [[continuous functions]], and since finite [[intersections]] of open subsets are open by the definition of [[topological spaces]]) there exists a point $a \in A$ with $i(a) \in f^{-1}\big( O_{f(x)} \big) \cap g^{-1}\big(  O_{g(x)} \big)$ (by definition of [[dense subset]]). But since then $f(i(a)) \in O_{f(x)}$ and $g(i(a)) \in O_{g(x)}$ while $O_{f(x)}$ is [[disjoint subset|disjoint]] from $O_{g(x)}$, it follows that $f(i(a)) \neq g(i(a))$. This means that $f \circ i \neq g \circ i$. 
\end{proof}


\linebreak

In fact the converse holds: any [[epimorphism]] in the category of Hausdorff spaces has dense image (e.g. [LL 18](#LL18)).


## Related notions

Arguably, the desire to make spaces Hausdorff ($T_2$) in analysis is really a desire to make them $T_0$; nearly every space that arises in analysis is at least [[regular space|regular]], and a regular $T_0$ space must be Hausdorff.  Forcing a space to be $T_0$ is like forcing a [[category]] to be [[skeletal category|skeletal]]; indeed, forcing a [[preorder]] to be a [[partial order]] is a special case of both (see [[specialisation topology]] for how).  It may be nice to assume, when working with a particular space, that it is $T_0$ but not to assume, when working with a particular underlying set, that every topology on it is $T_0$.

Whatever one thinks of that, there is a non-$T_0$ version of Hausdorff space, an __$R_1$ space__.  (The symbol here comes from being a weak version of a **r**egular space; in general a $T_i$ space is precisely both $R_{i-1}$ and $T_0$).  This is also called a __preregular space__ (in _[[HAF]]_) and a __reciprocal space__ (in convergence theory).

+-- {: .un_defn}
###### Definition (of $R_1$)
Given points $a$ and $b$, if every neighbourhood of $a$ meets every neighbourhood of $b$, then every neighbourhood of $a$ is a neighbourhood of $b$.  Equivalently, if any net (or proper filter) converges to both $a$ and $b$, then every net (or filter) that converges to $a$ also converges to $b$.
=--

There is also a notion of __sequentially Hausdorff space__:
+-- {: .un_defn}
###### Definition (of sequentially Hausdorff)
Whenever a [[sequence]] converges to both $x$ and $y$, then $x = y$.
=--
Some forms of [[predicative mathematics]] find this concept more useful.  Hausdorffness implies sequential Hausdorffness, but the converse is false even for [[sequential space]]s (although it is true for [[first-countable space]]s).

The reader can now easily define a _sequentially $R_1$ space_.


## Beyond topological spaces
 {#BeyondTopologicalSpaces}

### Hausdorff locales
 {#HausdorffLocale}

The most obvious definition for a [[locale]] $X$ to be **Hausdorff** is that its [[diagonal]] $X\to X\times X$ is a [[closed map|closed]] (and hence [[proper map|proper]]) inclusion.  However, if $X$ is a [[sober space]] regarded as a locale, this might not coincide with the condition for $X$ to be Hausdorff as a space, since the [[Cartesian product]] $X\times X$ in the [[category]] [[Loc]] of locales might not coincide with the product in the category [[Top]] of topological spaces (the [[Tychonoff product]]).  But it does coincide if $X$ is a [[locally compact locale]], so in that case the two notions of Hausdorff are the same.


### Separated toposes and schemes

This notion of a _Hausdorff locale_ is a special case of that of _[[Hausdorff topos]]_ in [[topos theory]]. This also is formally similar to notions such as a _[[separated scheme]]_ etc.  The corresponding relative notion (over an arbitrary [[base topos]]) is that of _[[separated geometric morphism]]_. For schemes see _[[separated morphism of schemes]]_.


## In constructive mathematics

In [[constructive mathematics]], the Hausdorff notion multifurcates further, due to the variety of possible meanings of [[closed subspace]].  If we ask the diagonal to be *weakly* [[closed subspace|closed]], then in the spatial case, this means that it contains all its limit points, giving Definition \ref{constructive} above.  But if we ask the diagonal to be *strongly* closed, i.e. the complement of an open set, then in the spatial case this means that there is a [[tight inequality]] $\ne$ (the [[exterior]] of $=$) relative to which Definition \ref{classical} holds.  (We use $\ne$ twice in that definition: in the hypothesis that $x \ne y$ and in the conclusion that $x' \ne y'$.)

It is natural to call these conditions *weakly Hausdorff* and *strongly Hausdorff*, but one should be aware of terminological clashes: in classical mathematics there is a different notion of a [[weak Hausdorff space]], whereas (strong) Hausdorffness for locales has by some authors been called "strongly Hausdorff" only to contrast it with Hausdorffness for spaces.

As a simple example, consider a [[discrete space]] $X$ regarded as a locale.  Since it is locally compact, the locale product $X\times X$ coincides with the space product (a theorem that is valid constructively); but nevertheless we have:

1. The diagonal $X\to X\times X$ always has an open complement.
2. Definition \ref{constructive} above always holds, since $\{x\}$ and $\{y\}$ are neighborhoods of $x$ and $y$, and if they intersect then $x=y$.  That is, $X$ is spatially weakly Hausdorff.
3. The diagonal $X\to X\times X$ is the complement of an open subset (i.e. $X$ is spatially strongly Hausdorff) if and only if equality in $X$ is stable under [[double negation]], in other words if $X$ admits a tight [[inequality relation]].
4. The locale diagonal $\Delta:X\to X\times X$ is a closed sublocale (i.e. $X$ is localically strongly Hausdorff) if and only if $X$ has [[decidable equality]].  For closedness of $\Delta$ means that $\Delta_\ast(U\cup \Delta^\ast(V)) \subseteq \Delta_\ast(U) \cup V$ for any $U\in O(X)$ and $V\in O(X\times X)$, where $x\in \Delta^\ast(V)$ means $(x,x)\in V$, while $(x,y)\in \Delta_\ast(U)$ means $(x=y)\to (x\in U)$.  Now let $U = \emptyset$ and $V = \{ (x,x) \mid x\in X \}$.  Then $(x,y) \in \Delta_\ast(U\cup \Delta^\ast(V))$ means $(x=y) \to (\bot \vee (x=x))$, which is a tautology; while $(x,y) \in \Delta_\ast(U) \cup V$ means $((x=y)\to \bot) \vee (x=y)$, i.e. $\neg(x=y) \vee (x=y)$.
5. I don't know what it means for $X$ to be localically weakly Hausdorff.  (Weak closure in locales is very inexplicit.)

In particular, the statement "all discrete locales are localically strongly Hausdorff" is equivalent to [[excluded middle]].

However, non-discrete spaces can constructively be localically strongly Hausdorff without having decidable equality.  For instance, any [[regular space]] is also regular as a locale, and hence localically strongly Hausdorff.  We can also say:

+-- {: .num_theorem #Apartness}
###### Theorem
In any topological space $X$, let $x\#y$ mean that there exist opens $U,V$ with $x\in U$ and $y\in V$ and $U\cap V = \emptyset$; then $\#$ is always an [[inequality relation]].  If the spatial product $X\times X$ coincides with the locale product (such as if $X$ is [[locally compact space|locally compact]]), then $X$ is localically strongly Hausdorff if and only if $\#$ is an [[apartness relation]] and every open set in $X$ is $\#$-open (i.e. for any $x\in U$ and $y\in X$ we have $y\in U \vee x\#y$).
=--
+-- {: .proof}
###### Proof
Note that $\#$ is, as a subset $W_\# \subseteq X\times X$, the exterior of the diagonal in the product topology, mentioned above.  If $X$ is localically strongly Hausdorff, then $W_\#$ *must* be the open set of which the diagonal is the complementary closed sublocale, since it is the largest open set disjoint from the diagonal.

To say that the diagonal *is* its complementary closed sublocale implies in particular that for any open set $U\subseteq X$, the open set $(U\times U) \cup W_\#$ is the largest open subset of $X\times X$ whose intersection with the diagonal is contained in $U\cap U = U$.  Specifically, therefore, $(U\times U) \cup W_\#$ contains $U\times X$ (since $U\times X$ is an open subset of $X\times X$ whose intersection with the diagonal is $U$).  That is, if $x\in U$ and $y\in X$, then either $(x,y)\in U\times U$ (i.e. $y\in U$) or $(x,y)\in W_\#$ (i.e. $x\#y$).  This shows that $U$ is $\#$-open.

To show that $\#$ is an apartness, note that for any $x$ the set $\{ z \mid x\# z \}$ is open, since it is the preimage of $W_\#$ under a section of the second projection $X\times X \to X$.  Thus, it is $\#$-open, which is to say that if $x\# z$ then for any $y$ either $x\#y$ or $y\#z$, which is the missing [[comparison]] axiom for $\#$ to be an apartness.

Conversely, suppose $\#$ is an apartness and every open set is $\#$-open (i.e. the apartness topology refines the given topology on $X$).  Let $A\subseteq X\times X$ be an open set; we must show that $A\cup W_\#$ is the largest open subset of $X\times X$ whose intersection with the diagonal is contained in $A\cap \Delta_X$.  In other words, suppose $U\times V$ is a basic open in $X\times X$ and $(U\times V)\cap \Delta_X$ (which is $U\cap V$) is contained in $A\cap \Delta_X$; we must show $U\times V\subseteq A\cup W_\#$.  In terms of elements, we assume that if $x\in U$ and $x\in V$ then $(x,x)\in A$, and we must show that if $x\in U$ and $y\in V$ then $(x,y)\in A \vee x\#y$.

Assuming $x\in U$ and $y\in V$, since $U$ and $V$ are $\#$-open we have either $y\in U$ or $x\# y$, and either $x\in V$ or $x\#y$.  Since we are done if $x\#y$, it suffices to assume $y\in U$ and $x\in V$.  Therefore, by assumption, $(x,x)\in A$ and $(y,y)\in A$.  Since $A$ is open in the product topology, we have opens $U',V'$ with $x\in U'$ and $y\in V'$ and $U'\times U'\subseteq A$ and $V'\times V' \subseteq A$.  But now $\#$-openness of $U'$ and $V'$ tells us again that either $x\#y$ (in which case we are done) or $y\in U'$ and $x\in V'$.  In the latter case, $(x,y)\in U'\times U'$ (and also $V'\times V'$), and hence is also in $A$.
=--

Note that the apartness $\#$ need not be [[tight relation|tight]], and in particular $X$ need not be spatially Hausdorff.  In particular, if $X$ might not even be $T_0$: since localic Hausdorffness is (of course) only a property of the open-set lattice, it only "sees" the [[sobrification]] and in particular the $T_0$ quotient ([[Kolmogorov quotient]]).  However, this is all that can go wrong: if $\neg(x\# y)$, then by $\#$-openness every open set containing $x$ must also contain $y$ and vice versa, so if $X$ is $T_0$ then $x=y$ and $\#$ is tight.

If the locale product $X\times X$ does not coincide with the spatial product, then the "only if" direction of the above proof still works, if we define $W_\#$ to be the open part of the locale product $X\times X$ given by $W_\# = \bigvee \{ U\otimes V \mid U\cap V = \emptyset \}$.  A different proof is to recall that by [this theorem](/nlab/show/apartness+relation#ClosedLocalicEquivalenceRelation), an apartness relation is the same as a (strongly) closed equivalence relation on a discrete locale, and the quotient of such an equivalence relation is the $\#$-topology.  Thus, if $X$ is localically strongly Hausdorff, its diagonal is a closed equivalence relation, which yields by pullback a closed equivalence relation on the discrete locale $X_d$ on the same set of points.  This is the [[kernel pair]] of the canonical surjection $X_d \to X$, and hence its quotient (the $\#$-topology) maps to $X$, i.e. refines the topology of $X$.


## Related concepts

* [[non-Hausdorff topological space]]

* [[locally Hausdorff topological space]]

* [[Kolmogorov topological space]]

* [[nice topological space]]

## References

Due to 

* [[Felix Hausdorff]], 1914

See also

* Wikipedia, _[Hausdorff space](https://en.wikipedia.org/wiki/Hausdorff_space)_

A detailed discussion of Hausdorff reflection is in 

* {#vanMunster14} Bart van Munster, _The Hausdorff quotient_, 2014 ([pdf](https://www.math.leidenuniv.nl/scripties/BachVanMunster.pdf))

On epimorphisms of Hausdorff spaces:

* {#LL18} Jérôme Lapuyade-Lahorgue, _The epimorphisms of the category Haus are exactly the image-dense morphisms_ ([arXiv:1810.00778](https://arxiv.org/abs/1810.00778))


Comments on the relation to [[topos theory]]:

* S. Niefield, _A note on the locally Hausdorff property_, Cahiers TGDC (1983) ([numdam](http://www.numdam.org/item?id=CTGDC_1983__24_1_87_0))


[[!redirects Hausdorff]]
[[!redirects Hausdorff space]]
[[!redirects Hausdorff spaces]]
[[!redirects Hausdorff topological space]]
[[!redirects Hausdorff topological spaces]]
[[!redirects Hausdorff convergence space]]
[[!redirects Hausdorff convergence spaces]]
[[!redirects Hausdorff locale]]
[[!redirects Hausdorff locales]]

[[!redirects sequentially Hausdorff space]]
[[!redirects sequentially Hausdorff spaces]]

[[!redirects R1 space]]
[[!redirects R1 spaces]]
[[!redirects preregular space]]
[[!redirects preregular spaces]]
[[!redirects reciprocal space]]
[[!redirects reciprocal spaces]]

[[!redirects Hausdorffication]]
[[!redirects Hausdorffications]]

[[!redirects Hausdorffification]]
[[!redirects Hausdorffifications]]

[[!redirects Hausdorff reflection]]
[[!redirects Hausdorff reflections]]

[[!redirects Hausdorff quotient]]
[[!redirects Hausdorff quotients]]


[[!redirects Hausdorffzation]]
[[!redirects Hausdorffizations]]

