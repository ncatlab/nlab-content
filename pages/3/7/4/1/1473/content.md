[[!redirects Tychonoff's theorem]]
[[!redirects Tychonoff theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

* table of contents
{: toc}

## Statement 

What is known as the **Tychonoff theorem** or as **Tychonoff's theorem** ([Tychonoff 35](#Tychonoff35)) is a basic [[theorem]] in the field of [[topology]]. Assuming the [[axiom of choice]], then it states that the  [[product topological space]] (with its [[Tychonoff topology]]) of an arbitrary [[set]] of [[compact topological spaces]] is itself [[compact space|compact]]:

$$
  \left(
    \underset{i \in I}{\forall}
    \left(
       X_i \, \text{compact}
    \right)
  \right)
    \;\Rightarrow\;
  \left(
     \underset{i \in I}{\prod} X_i
     \, \text{compact}
  \right)
  \,.
$$

For a [[finite number]] of factors the proof of this statement is elementary (see [below](#ElementaryProofOfFinitaryCase)), but this already essentially  implies for instance the [[Heine-Borel theorem]]. For an arbitrary [[set]] of factors the proof is non-trivial, but is conveniently given using [[nets]] (see [below](#ProofViaNets)) [[ultrafilters]] ([further below](#ProofViaUltrafilters)).

In its [[classical mathematics|classical]] form, Tychonoff's theorem is equivalent to the [[axiom of choice]]. (Compare the statement of the axiom of choice: a product of sets is [[inhabited set|inhabited]] if each set is inhabited.) 

Notice that no [choice](axiom+of+choice#Variants) whatsoever is needed to prove the analogous theorem for [[locales]]: even in [[constructive mathematics]], a [[Cartesian product]] of locales is compact if each of the locales is compact.  From that perspective, the statement equivalent to the axiom of choice is this: a product of locales is [[spatial locale|spatial]] if each of the locales is spatial.  Either of these may be considered a Tychonoff theorem for locales.

To prove Tychonoff's theorem for [[Hausdorff topological spaces]] only, the full [[axiom of choice]] is not needed; the [[ultrafilter theorem]] (and possibly [[excluded middle]]) are enough.


## Proofs

* [elementary proof for the finitary case](#ElementaryProofOfFinitaryCase)

* [elementary proof via closed-projection characterization](#ElementaryProofViaClosedProjectionCharacterization)

* [proof via net convergence](#ProofViaNets)

* [proof via ultrafilter convergence](#ProofViaUltrafilters)


### Elementary proof of finitary case
 {#ElementaryProofOfFinitaryCase}

The finitary case of Tychonoff's theorem, where products with only a [[finite number]] of factors are considered, may be proven with elementary means from basic topology. Such a proof is spelled out _[here](Introduction+to+Topology+--+1#BinaryTychonoffTheorem)_ at _[[Introduction to Topology -- 1]]:

+-- {: .proof}
###### Proof
of the finitary Tychonoff theorem

Let $X,Y$ be two twopological spaces, with [[product topological space]] $X \times Y$.  Let $\{ U_i \subset X \times Y \}_{i \in I}$ be an [[open cover]] of the product space. We need to show that
this has a finite subcover.

By definition of the product space topology, each $U_i$ is the union, indexed by some set $K_i$, of [[Cartesian products]]
of open subsets of $X$ and $Y$:

$$
  U_i
    \;=\;
  \underset{k_i \in K_i}{\cup} \left( 
     V_{k_i} \times W_{k_i}
  \right)
  \phantom{AAAA}
  V_{k_i} \in \tau_{X} \,\phantom{A}\text{and} \phantom{A}\, W_{k_i} \in \tau_{Y}
  \,.
$$

Consider then the [[disjoint union]] of all these index sets

$$
   K
    \,\coloneqq\,
  \underset{i \in I}{\sqcup}
  K_i
  \,.
$$

This is such that

$$
  (\star)
  \phantom{AA}
  \left\{
    V_{k_i} \times W_{k_i}
      \subset
    X \times Y
  \right\}_{k_i \in K}
$$

is again an open cover of $X \times Y$.

But by construction, each element $V_{k_i} \times W_{k_i}$ of this new cover is contained in at least one
$U_{j(k_i)}$ of the original cover. 
Therefore it is now sufficient to show that there is
a finite subcover of $(\star)$, consisting of elements indexed by $k_i \in K_{fin} \subset K$ for some
[[finite set]] $K_{fin}$. Because then the corresponding $U_{j(k_i)}$ for $k_i \in K_{fin}$ form a finite subcover
of the original cover.

In order to see that $(\star)$ has a finite subcover, first fix a point $x \in X$ and 
write $\{x\} \subset X$ for the corresponding [[singleton]] [[topological subspace]].
This is [[homeomorphism|homeomorphic]] to the abstract
[[point]] space $\ast$.
and there is thus a [[homeomorphism]] of the form

$$
  \{x\} \times Y \simeq Y
  \,.
$$

Therefore, since $(Y,\tau_Y)$ is assumed to be [[compact topological space|compact]], the open cover

$$
  \left\{
    \left(
      (V_{k_i} \times W_{k_i}) \cap (\{x\} \times Y) 
    \right)
      \;\subset\; 
    \{x\}\times Y 
  \right\}_{k_i \in K}
$$

has a finite subcover, indexed by a [[finite set|finite]] [[subset]] $J_x \subset K$.

Here we may assume without restriction of generality that $x \in V_{k_i}$ for all $k_i \in J_x \subset K$,
because if not then we may simply remove that index and still have a (finite) subcover.

By finiteness of $J_x$ it now follows that the intersection

$$
  V_x 
    \;\coloneqq\; 
  \underset{k_i \in J_x}{\cap} V_{k_i}
$$

is still an open subset, and by the previous remark we may assume without restriction that

$$
  x \in V_x
  \,.
$$

Now observe that by the nature of the above cover of $\{x\} \times Y$ we have

$$
  \{x\} \times Y
    \subset
  \underset{k_i \in J_x \subset K}{\cup}  V_{k_i} \times W_{k_i}
$$

and hence

$$
  \{x\} \times Y \subset \{x\} \times \underset{k_i \in J_x \subset K}{\cup} W_{k_i}
  \,.
$$

Since by construction $V_x \subset V_{k_i}$ for all $k_i \in J_x \subset K$, it follows 
that we have found a finite cover not just of $\{x\} \times Y$ but of $V_x \times Y$

$$
  V_x \times Y
    \subset
  \underset{k_i \in J_x \subset K}{\cup} \left( V_{k_i} \times W_{k_i} \right)
  \,.
$$

To conclude, observe  that $\{V_x \subset X\}_{x \in X}$ is clearly an open cover of $X$,
so that by the assumption that also $X$ is compact there is a finite set of points $S \subset X$
so that $\{V_x \subset X\}_{x \in S \subset X}$ is still a cover. 
In summary then

$$
  \left\{
    V_{k_i} \times W_{k_i}
    \subset X \times Y
  \right\}_{{x \in S \subset X} \atop { k_i \in J_x \subset K }}
$$

is a finite subcover as required.
t

=--


### Elementary proof of general case via closed-projection characterization
 {#ElementaryProofViaClosedProjectionCharacterization}

Another equivalent characterization of compactness of a space $X$ is that for all spaces $Y$ then the [[projection]] $\pi_Y \;\colon\; Y \times X \to Y$ out of the [[product topological space]] is a [[closed map]], see at _[[closed-projection characterization of compactness]]_.

This characterization allows an elementary proof of the general Tychonoff theorem, see [there](closed-projection+characterization+of+compactness#TychonoffTheorem).



### Proof via net convergence
 {#ProofViaNets}

We give the proof of the Tychonoff theorem using the characterization of compactness via [[convergence]] of [[nets]] ([ths prop](net#CompactSpacesEquivalentlyHaveConvergetSubnets)). This proof is due to ([Chernoff 92](#Chernoff92)).

+-- {: .proof #ProofOfTychonoffTheoremViaNets}
###### Proof
(of the [[Tychonoff theorem]] via [[convergence]] of [[nets]])

By [this prop.](net#CompactSpacesEquivalentlyHaveConvergetSubnets) a topological space is compact precisely if every [[net]]
in that space has a [[convergence|convergent]] [[subnet]].
This in turn is equivalently the case if every net has a [[cluster point]]. We will show that
this is the case for the product of compact spaces.

So let

$$
  \nu \;\colon\; A \to \underset{i \in I}{\prod} X_i
$$

be a net in the product space. We need to show that this has a cluster point.

For every [[finite set|finite]] [[subset]] $J \subset I$, write

$$
  \nu\vert_I
    \;\colon\;
  A
    \overset{\nu}{\longrightarrow}
  \underset{i \in I}{\prod} X_i
    \overset{pr_J}{\longrightarrow}
  \underset{i \in J \subset I}{\prod}
    X_i
$$

for the image of the net under [[projection]] to the product space of factors
with indices in the subset $J$.

Say that a _partial cluster point_ of $\nu$ is

1. a finite subset $J \subset I$;

1. a cluster point $c_J \in \underset{i \in J \subset I}{\prod} X_i $ of $\nu\vert_J$.

Write $PartialClusterPt(\nu)$ for the set of all partial cluster points of $\nu$.
Equip this with the [[partial order]] $\leq$ given by the evident extension of domains.

Observe that, by definition, a partial cluster point $c_J$ for which $J = I$ is an actual
cluster point of $\nu$

We claim now that if the partially ordered set  $(PartialClusterPt_{\leq})$ has a [[maximal element]]
then this is an actual cluster point of $\nu$.

To see this, assume it were not, hence that the maximal element were a partial cluster point $c_J$
with $I \backslash J \neq \emptyset$. Then there were an element $k \in I\backslash J$. Since
$X_k$ is a compact space by assumption, it would follow that the net $\nu\vert_{\{k\}}$ had a cluster point
$c_k$. But then adjoining that to $c_J$ would yield a partial cluster point with larger domain $J \cup \{k\}$,
in contradiction with the assumption that $c_J$ is already maximal. Hence we have a [[proof by contradiction]]
that every maximal element in $PartialClusterPt(\nu)_{\leq}$ is an actual cluster point.

Therefore we may now conclude by showing that the partially ordered set $PartialClusterPt(\nu)_{\leq}$
does have a maximal element. To this end we invoke [[Zorn's lemma]]. This says that we need to check that
$PartialClusterPt(\nu)$ is not [[empty set|empty]], and that every subset $L_{\leq} \subset PartialClusterPt(\nu)_{\leq}$
on which the partial order restricts to a [[total order]] has an [[upper bound]] partial cluster point.

Now non-emptyness follows immediately because there is always the partial cluster point with empty domain $c_{\emptyset}$.

Hence consider a totally ordered subset $S = \{ (c_k)_{J_k} \}_{k \in K}$ of partial cluster points.

For

$$
  J_{tot} \coloneqq \underset{k \in K}{\cup} J_k
$$

the union of the domains of the partial cluster points in the subset, then this induces a point

$$
  c_{tot} \in \underset{ i \in J_{tot}  }{\prod} X_i
  \,.
$$

If this is a partial cluster point, then it is clearly an upper bound of $S$. Hence we may conclude by showing that
$c$ is indeed a partial cluster point. 

This means that we need to show that for every Tychonoff-basic
open neighbourhood $U \subset \underset{i \in J_{tot}}{\prod}$ of $c_{tot}$ and every element $a \in A$ (in the domain of the net) there exists
$b \geq a$ such that $\nu_b \in U$. 

But by definition of the [[Tychonoff topology]], $U$ is a product $\underset{i \in J_{tot}}{\prod} U_i$ of open subsets $U_i \subset X_i$ such that only over a finite subset of $J_{tot}$ they differ from the total spaces $X_i$.
By construction of $c_{tot}$, that finite subset of $J_{tot}$ must be contained in $J_k$ for some $k \in K$, and since $c_{J_k}$ is a partial
cluster point, the claim follows. 

=--



### Proof via ultrafilter convergence 
 {#ProofViaUltrafilters}

One method of proof uses [[ultrafilter]] [[convergence]]. 
This is sometimes called "[Bourbaki's proof](#BourbakiGeneralTopology)", following [Cartan 37](#Cartan37).

#### First version

+-- {: .proof #UltrafilterProof}
###### Proof

Let $\langle X_\alpha \rangle_{\alpha \in A}$ be a family of compact spaces. 

1. Every ultrafilter $U_\alpha$ on the underlying set of $X_\alpha$ converges to some point $x_\alpha$. (Consider the collection of all closed sets belonging to $U_\alpha$. Finite subcollections have nonempty intersection ([[finite intersection property]]), so by compactness the intersection of the collection is also nonempty ([this prop.](compact+space#fip)). Let $x_\alpha$ be a point belonging to that intersection. Every closed set disjoint from $x_\alpha$ belongs to the complement of $U_\alpha$, hence every open set containing $x_\alpha$ belongs to $U_\alpha$, i.e., $U_\alpha$ converges to $x_\alpha$.)

1. Let $U$ be an ultrafilter on $\prod_\alpha X_\alpha$. Since the set-of-ultrafilters construction $S \mapsto \beta S$ is [[functor]]ial, we have a push-forward ultrafilter $U_\alpha = \beta(\pi_\alpha)(U)$ on each $X_\alpha$, where $\pi_\alpha$ is a projection map. Choose a point $x_\alpha$ to which $U_\alpha$ converges. Then it is easily checked that $U$ converges to the point $\langle x_\alpha \rangle$ in the product space.

1. Since every ultrafilter $U$ on $\prod_\alpha X_\alpha$ converges to a point, the product is compact. (If it were not, then we could find a collection of nonempty closed sets whose intersection is empty, but closed under finite intersections. This collection generates a filter which is contained in some ultrafilter $U$, by the [[ultrafilter theorem]]. Since every ultrafilter $U$ converges to some $x$, it cannot contain any closed set in the complement of $x$, hence cannot contain some closed set in the original collection, contradiction.) 

=--

+-- {: .num_remark #TyCH} 
###### Remark 

The [[axiom of choice]] is used in step 2 of the proof [abov](#UltrafilterProof), to combine the $x_\alpha$ into a single family $\langle x_\alpha \rangle$; if the $X_\alpha$ were Hausdorff, then the $x_\alpha$ would be unique, and we would not need the axiom of choice at this step.  The [[ultrafilter theorem]] is used in step 3, and this is the only other place where a choice principle is needed. In other words, working over a choice-free set theory like [[ZFC|ZF]] or even BZ (bounded Zermelo set theory), the ultrafilter principle (UF) implies Tychonoff's theorem for [[Hausdorff spaces]]. 

=-- 

#### Second version

[Bourbaki](#BourbakiGeneralTopology) gives an alternative proof using ultrafilters, which may be formulated in terms of categorical lifting/extension properties. For any set $X$ and ultrafilter $U$ on $X$, form a space $X_U$ whose underlying set is $X \sqcup \{\infty\}$ (adjoin an extra point $\infty$) and where a subset of $X \sqcup\{\infty\}$ is open iff it either does not contain $\infty$ or is of form $Z \sqcup\{\infty\}$ where $Z\in U$, i.e., is "big" according to the ultrafilter $U$. The inclusion of the set $X$ with its discrete topology into $X_U$ is a subspace inclusion. 

+-- {: .num_theorem} 
###### Theorem (Bourbaki) 
A map $g: Y \to Z$ is [[proper map|proper]] if and only if it has the [[lifting property|right lifting property]] with respect to the inclusion $i: X \hookrightarrow X_U$ for any such pair $(X, U \in \beta(X))$ (in symbols: $i \rightthreetimes g$). In other words: iff for each commutative diagram 

$$\array{
X & \to & Y \\
\mathllap{i} \downarrow & & \downarrow \mathrlap{g} \\ 
X_U & \to & Z
}$$ 

there is a lift $X_U \to Y$ making the evident triangles commute. 
=-- 

+-- {: .num_remark} 
###### Remark 
Actually the topology on $X$ does not have to be discrete: the same result extends to any space $X$ and its inclusion into $X\sqcup\{\infty\}$ where we declare a subset in $X \sqcup \{\infty\}$ to be open iff it either does not contain $\infty$ and is open in $X$, or is of form $Z\sqcup\{\infty\}$
where $Z\in U$ is and $Z$ is open in $X$.
=-- 

A space $K$ is compact iff the map $K\longrightarrow \{*\}$ is proper. Thus to see that a product $\prod_{i \in I} Y_i$ of compact spaces is compact, it suffices to show that for any $(X, U)$ and any $f: X \to \prod_{i \in I} Y_i$, there is a continuous extension $\tilde{f}: X_U \to \prod_{i \in I} Y_i$. But (using the axiom of choice) this is clear from the universality property of the product: choose a continuous extension $\widetilde{\pi_i f}: X_U \to Y_i$ for each $\pi_i f: X \to Y_i$, and then assemble these into an extension 

$$\tilde{f} \coloneqq \langle \widetilde{\pi_i f} \rangle_{i \in I}: X_U \to \prod_{i \in I} Y_i.$$ 


### Proof via Taimanov theorem and lifting properties
 {#ProofViaTaimanovTheoremAndLiftingProperties}

+-- {: .num_remark #Taimanov} 
###### Remark

One can avoid mentioning ultrafilters altogether, at least for [[Hausdorff spaces]], using the [[Taimanov theorem]]. 

Call a map $f$ _ultrafilter-like_ iff $f$ has the [[left lifting property]] wrt each proper, equivalently closed,
map of [[finite topological spaces]]. The [[Taimanov theorem]] implies that a map $g$ of normal (T4) spaces is [[proper maps|proper]] 
iff it has the [[lifting property]] $f \rightthreetimes g$ against each ultrafilter-like $f$.  


Using notation explained just below,  this can expressed as follows:
The [[Taimanov theorem]] says that
a Hausdorff space $K$ is compact iff
$K\longrightarrow \{*\} \,\in\,  (\{\{a\}\longrightarrow \{a{\searrow}b\}\}^r_{\le 3})^{lr}$,
or in fact  
 $$     \{\, \{a\leftrightarrow b\}\longrightarrow \{a=b\},\, \{a{\searrow}b\}\longrightarrow \{a=b\},\,
     \{b\}\longrightarrow \{a{\searrow}b\},\,\{a{\swarrow}o{\searrow}b\}\longrightarrow \{a=o=b\}\,\,\}^{lr}$$  
For a property ${C}$ of arrows (morphisms) in a category, define

$$ C^l \coloneqq \left\{ {f} \colon \underset{g \in C}{\forall}\,{f} \,\rightthreetimes\,  {g} \right\} 
$$

$$ C^r \coloneqq \left\{ {g} : \underset{f \in C}{\forall}\,{f} \,\rightthreetimes\,  {g} \right\} $$

$$ C^{lr} \coloneqq (C^l)^r, ... $$

here $f \,\rightthreetimes\,  g$ reads " $f$ has the left [[lifting property]] wrt $g$ ",
" $f$ is (left) orthogonal to $g$ ",
i.e.  for  $f:A\longrightarrow B$, $g:X\longrightarrow Y$,
$f \,\rightthreetimes\, g$ iff for each $i:A\longrightarrow X$, $j:B\longrightarrow Y$ such that $ig=fj$ ("the square commutes"),
there is $j':B\longrightarrow X$ such that $fj'=i$ and $j'g=j$ ("there is a diagonal
making the diagram commute").

Finally,
$$
  C_{\le n} := \{ {f} : {f} \in {C},\text{ both the domain and range of }f \text{ are finite of size less or equal than }\,n \}.
$$
and
$\{a\}\longrightarrow \{a{\searrow}b\}$ denotes the inclusion of the open point $a$ into the Sierpinski space $ \{a{\searrow}b\}$.
=--

These observations give rise to the following question.

+-- {: .num_remark #TaimanovQ} 
###### Question
Question. Is $((\{a\}\longrightarrow \{a{\searrow}b\})^r_{\le 4})^{lr}$
the class of proper maps?
=--

Considerations above show that it is contained in the class of proper maps and that it contains proper maps between normal (T4) spaces (this is what gives the standard proof of the Taimanov theorem).


### Proof of converses

Now we will prove that Tychonoff's theorem implies the [[axiom of choice]], while Tychonoff's theorem for Hausdorff spaces implies the ultrafilter theorem.  This is done by judicious choice of examples.

**Tychonoff's theorem implies axiom of choice**: let $\{X_\alpha\}_{\alpha \in A}$ be a family of nonempty sets. Let $Y_\alpha$ be obtained by adjoining a point $p$ to $X_\alpha$. Topologize $Y_\alpha$ by taking the nontrivial open sets to be $X_\alpha$ and $\{p\}$. Then $Y_\alpha$ is compact; assuming Tychonoff, $Y = \prod_\alpha Y_\alpha$ is compact. For each $\alpha$, put 

$$K_\alpha = \{y \in Y: y_\alpha \in X_\alpha\}$$ 

Then $K_\alpha$ is closed, and any finite intersection of the $K_\alpha$ is nonempty (use $p$ in all but finitely many components). Hence 

$$\prod_\alpha X_\alpha = \bigcap_\alpha K_\alpha$$ 

is nonempty as well, by compactness. Thus the axiom of choice follows. 

**Tychonoff's theorem for Hausdorff spaces implies ultrafilter theorem**: let $F$ be a filter on a set $X$, i.e., a filter in the Boolean algebra $P X$. An ultrafilter $U$ containing $F$ is tantamount to a Boolean algebra map $2^X \to 2$ which sends all of $F$ to $1$, or equivalently to a Boolean algebra map $\phi: B = 2^X/F \to 2$. Thus it suffices to prove the following result: 

+-- {: .num_prop #nonempty} 
###### Proposition 
For every (non-terminal) Boolean algebra $B$, there exists a homomorphism $B \to 2$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $|B|$ denote the underlying set of $B$. The set of all functions $f: |B| \to 2$ is a $|B|$-indexed product of copies of $2$; considering $2$ as a compact Hausdorff space, this set is compact Hausdorff, assuming Tychonoff's theorem for Hausdorff spaces. For each finite subset $S \subseteq |B|$, let $K_S$ be the [[subspace]] of functions $f: |B| \to 2$ for which the equations 

$$f(x \wedge y) = f(x) \wedge f(y) \qquad f(\neg x) = \neg f(x)$$ 

hold for all $x, y \in S$. As the space $2^{|B|}$ is Hausdorff, $K_S$ being defined by an equalizer is a closed subspace, and it is easy (and classical) that it is nonempty: the subalgebra $B(S) \subseteq B$ generated by $S$ is finite and in particular [[atom|atomic]] and thus admits a homomorphism $f: B(S) \to 2$ defined by $f(x) = 1$ iff $a \leq x$ for some given atom $a$, and then we can take $f(b) = 1$ for any $b$ outside $B(S)$. By compactness of $2^{|B|}$, the intersection of all the $K_S$ is nonempty, and this is precisely the set of Boolean algebra maps $\phi: B \to 2$. 
=-- 

* This proof may be seen as a classical illustration of the [[compactness theorem]] for propositional logic. We may think of a Boolean algebra $B$ as a Lindenbaum algebra for a [[propositional logic|propositional]] [[theory]], and a Boolean algebra map $\phi: B \to 2$ as a [[model]] for that theory. A model exists iff a model exists for every theory generated by a finite subset of propositions, by the compactness theorem. In fact, the proof above suggests the topological provenance of the term "compactness theorem". 

## Tychonoff's theorem for locales 

Given the close connection between Tychonoff's theorems and choice principles, it may come as a surprise that Tychonoff's theorem for [[locales]] -- the product of a small collection of compact locales is compact, equivalently that the coproduct of a small collection of compact [[frames]] is compact -- may be proved without the [[axiom of choice]] and even [[constructive mathematics|constructively]]. 

More details to appear at [[Tychonoff theorem for locales]]. 

## Related theorems

* [[Tietze extension theorem]]

* [[Heine-Borel theorem]]

* [[topological invariance of dimension]]

* [[Brouwer's fixed point theorem]]

* [[Jordan curve theorem]]



## References
 {#References}

The statement of Tychonoff's theorem is made in 

* {#Tychonoff35} [[A. N. Tychonoff]], p. 272 of _Ein Fixpunktsatz_, Mathematische Annalen, December 1935, Volume 111, Issue 1, pp 767&#8211;776

where he says that the proof is the same as the one he gave for a product of [[closed intervals]] in 

* {#Tychonoff30} [[A. N. Tychonoff]],  _&#220;ber die topologische Erweiterung von R&#228;umen_, Mathematische Annalen, December 1930, Volume 102, Issue 1, pp 544&#8211;561

An explicit proof was then given in

* [[Eduard Cech]], p. 830 of _On bicompact spaces_, Annals of Mathematics 38 (1937)

The proof using ultrafilters is due to 

* [[Henri Cartan]], _Theorie des filtres_, Comptes Rendus de l'Acad. Sci. (Paris) 205 (1937), 595-598

and reproduced in

* {#BourbakiGeneralTopology} [[Bourbaki]], _General Topology_, I\S10.2, Thm.1(d), p.101

whence often known as "Bourbaki's proof".

* {#Cartan37} [[Henri Cartan]], _Filtres et ultrafiltres_, Comptes Rendus de l'Acad. Sci. (Paris) 205 (1937), 777-779.

and its modern version is due to 

* [[John Kelley]], _Convergence in topology_, Duke Math. J. 17 (1950), 277-283.

The proof using convergence of nets is due to

* {#Chernoff92} Paul R. Chernoff, _A Simple Proof of Tychonoff's Theorem Via Nets_,  The American Mathematical Monthly Vol. 99, No. 10 (Dec., 1992), pp. 932-934 ([jstor](http://www.jstor.org/stable/2324485))




See also

* Wikipedia, _[Tychonoff's theorem](https://en.wikipedia.org/wiki/Tychonoff%27s_theorem)_


[[!redirects Tihonov's theorem]]
[[!redirects Tihonov theorem]]
[[!redirects Tihonov's topology]]
[[!redirects The Tychonoff theorem]]

