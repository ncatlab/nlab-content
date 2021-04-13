
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Locally compact spaces
* table of contents
{: toc}

## Idea 

A [[topological space]] is called _locally compact_ if every point has a [[compact topological space|compact]] [[neighbourhood]].

Or rather, if one does not at the same time assume that the space is [[Hausdorff topological space]], then one needs to require that these compact neighbourhoods exist in a controlled way, e.g. such that one may find them inside every prescribed open neighbourhood (def. \ref{LocalCompactnessViaCompactNeighbourhoodBase} below) and possibily such that they are topological closures of smaller open neighbourhoods (def. \ref{LocallyCompactSpace} below).

There are various definitions in use, which all coincide if the space is also [[Hausdorff topological space|Hausdorff]] (prop. \ref{InHausdorffSpacesDefinitionsOfLocalCompactnessAgree} below).

A locally compact [[Hausdorff space|Hausdorff]] space may also be called a _local compactum_; compare at _[[compactum]]_.


Local compactness is one of the conditions that are often required by default for working with topological spaces: locally compact spaces are a class of  "[[nice topological spaces]]". 



## Definition


+-- {: .num_defn #LocalCompactnessViaCompactNeighbourhoodBase}
###### Definition
**(local compactness via compact neighbourhood base)**

A [[topological space]] is _locally compact_ if every point has a [[neighborhood base]] consisting of [[compact subspaces]]. This means that for every point $x \in X$ every [[open neighbourhood]] $U_x \supset \{x\}$ contains a [[compact topological space|compact]] [[neighbourhood]] $K_x \subset U_x$.

=--

Alternatively:

+-- {: .num_defn #LocallyCompactSpace}
###### Definition
**(local compactness via compact closures inside neighbourhoods)**

A [[topological space]] $X$ is called _locally compact_ if for every point $x \in X$ and every [[open neighbourhood]] $U_x \supset \{x\}$
there exists a smaller open neighbourhood $V_x \subset U_x$ whose [[topological closure]]
is [[compact topological space|compact]] and still contained in $U$:

$$
  \{x\} \subset V_x \subset \underset{\text{compact}}{Cl(V_x)} \subset U_x
  \,.
$$

=--

+-- {: .num_prop #InHausdorffSpacesDefinitionsOfLocalCompactnessAgree}
###### Proposition

If $X$ is a [[Hausdorff topological space]] then definition \ref{LocalCompactnessViaCompactNeighbourhoodBase} is equivalent to definition \ref{LocallyCompactSpace}.

=--

+-- {: .proof}
###### Proof

Generally definition \ref{LocallyCompactSpace} implies definition \ref{LocalCompactnessViaCompactNeighbourhoodBase}. We need to show that Hausdorffness implies the converse.

Hence assume that for every point $x \in X$ then every open neighbourhood $U_x \supset \{x\}$ contains a compact neighbourhood. We need to show that it then also contains the closure $Cl(V_x)$ of a smaller open neighbourhood and such that this closure is compact.

So let $K_x \subset U_x$ be a compact neighbourhood. Being a neighbourhood, it has a non-trivial [[interior]] which is an open neighbourhood

$$
  \{x\} \subset Int(K_x) \subset K_x \subset U_x \subset X
  \,.
$$

Since [[compact subspaces of Hausdorff spaces are closed]], it follows that $K_x \subset X$ is a closed subset. This implies that the [[topological closure]] of its interior as a subset of $X$ is still contained in $K_x$ (since the topological closure is the smallest closed subset containing the given subset): $Cl(Int(K_x)) \subset K_x$. Since [[subsets are closed in a closed subspace precisely if they are closed in the ambient space]], $Cl(Int(K_x))$ is also closed as a subset of the compact subspace $K_x$.
Now since [[closed subsets of compact spaces are compact]], it follows that this closure is also compact as a subspace of $K_x$, and since [[continuous images of compact spaces are compact]], it finally follows that it is also compact as a subspace of $X$:

$$
  \{x\} \subset Int(K_x) \subset \underset{\text{compact}}{Cl(Int(K_x))} \subset \underset{}{K_x} \subset U_x \subset X
  \,.
$$


=--

+-- {: .num_remark}
###### Remark
**(remark on terminology)**

As for [[compact spaces]] ([this remark](compact+space#DifferingTerminology)), some authors choose to include the [[Hausdorff space|Hausdorff]] condition as a matter of course, calling locally compact not-necessarily-Hausdorff spaces 'locally quasi-compact'. We will not follow that convention here, but the reader should be warned that without the Hausdorff hypothesis, there are several inequivalent notions of local compactness in the literature; see [the English Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Locally_compact_space) for a survey and counterexamples.

Note, however, that a topological space $X$ satisfying Definition \ref{LocallyCompactSpace} is regular, because, as is immediate from the definition, closed neighbourhoods then form a neighbourhood basis of $X$, which is equivalent to regularity. Thus we only need that $X$ be $T_{0}$ for it to in fact be Hausdorff.  
 
=--

## Examples


+-- {: .num_example}
###### Example

Every [[discrete space]] is locally compact. 

=--


+-- {: .num_example}
###### Example
**([[open subspaces of compact Hausdorff spaces are locally compact]])** 


Every [[open subset|open]] [[topological subspace]] $X \underset{\text{open}}{\subset} K$ of a [[compact topological space|compact]]
[[Hausdorff space]] $K$ is a [[locally compact topological space]].

In particular every [[compact Hausdorff space]] itself is [[locally compact topological space|locally compact]].

Conversely, every locally compact Hausdorff space $X$ arises in this way, since it can be considered an open subspace in its [[one-point compactification]] $X \sqcup \{\infty\}$. See there _[this example](one-point+compactification#LocallyCompatcHausdorffSpaceIsOpenSubspaceOfCompactHausdorffSpace)_.

=--

+-- {: .num_example #real}
###### Example

The [[real numbers]], [[complex numbers]], and $\mathfrak{p}$-[[adic completions]] of [[algebraic number fields]] (with respect to a [[prime ideal]] $\mathfrak{p}$ in the [[ring of integers]]) are locally compact. In [[positive characteristic]] $p$, the field of [[Laurent series]] $\mathbb{F}_q((t))$ over a [[finite field]] with $q$ elements, topologized with respect to a discrete valuation, is locally compact. In fact, any non-discrete locally compact [[field]] must be of one of these types; they are called [[local fields]].

=-- 

+-- {: .num_example #product}
###### Example

Finite [[product topological spaces]] of locally compact spaces are locally compact. 

=--

+-- {: .num_example }
###### Example

[[closed subspace|Closed subspaces]] of locally compact spaces are locally compact. (Hence locally compact spaces form a [[finitely complete category]].) 

=--

+-- {: .num_example #TopologicalManifoldsAreLocallyCompact}
###### Example
**([[topological manifolds]] are [[locally compact topological spaces]])**

[[topological manifolds]], being locally [[homeomorphism|homeomorphic]] to the [[Euclidean space|Euclidean]] [[metric spaces]] $\mathbb{R}^n$, are locally compact, via examples \ref{real} and \ref{product}.

In fact this applies also to [[locally Euclidean spaces]] which are not necessarily [[paracompact topological space|paracompact]] [[Hausdorff topological spaces]], such as the [[long line]].


=--




+-- {: .num_example #CountablyInfiniteProductsOfNonCompactSpacesAreNotLocallyCompact}
###### Nonexample
**(countably infinite products of non-compact spaces are not locally compact)**

Let $X$ be a [[topological space]] which is not [[compact topological space|compact]]. Then the [[product topological space]] of a [[countable set|countably infinite set]] of copies of $X$ 

$$
  \underset{n \in \mathbb{N}}{\prod} X
$$

is not locally compact.

=--

+-- {: .proof}
###### Proof


Since the [[continuous image of a compact space is compact]], and since the [[projection]] maps $p_i \;\colon\; \underset{\mathbb{N}}{\prod} X \longrightarrow X$ are continuous, it follows that every compact subspace of the product space is contained in one of the form

$$
  \underset{i \in \mathbb{N}}{\prod} K_i
$$ 

for $K_i \subset X$ compact. 

But by the nature of the [[Tychonoff topology]], a [[base for a topology|base for the topology]] on $\underset{\mathbb{N}}{\prod} X$ is given by subsets of the form 

$$
  \left(
    \underset{i \in \{1,\cdots,n\}}{\prod}
    U_{i}
  \right)
  \times
  \left(
    \underset{j \in \mathbb{N}_{\gt n}}{\prod}
    X
  \right)
$$

with $U_i \subset X$ open. Hence every compact neighbourhood in $\underset{\mathbb{N}}{\prod} X$ contains a subset of this kind, but if $X$ itself is non-compact, then none of these is contained in a product of compact subsets.


=--

+-- {: .num_example #RationalsAreNotLocallyCompact}
###### Nonexample

The space of [[rational numbers]] as a subspace of the [[real numbers]] with the Euclidean topology is not locally compact since its compact subsets all have empty interior.

=--

## Properties

### General

+-- {: .num_prop}
###### Proposition
**([[proper maps to locally compact spaces are closed]])**

Let

1. $(X,\tau_X)$ be a [[topological space]],

1. $(Y,\tau_Y)$ a [[locally compact topological space]] according to def. \ref{LocallyCompactSpace},

1. $f \colon X \to Y$ a [[continuous function]].

Then:

If $f$ is a [[proper map]], then it is a [[closed map]].

=--

* [[locally compact and sigma-compact spaces are paracompact]]

* [[locally compact and second-countable spaces are sigma-compact]]

### Category-theoretic properties

Perhaps the most important consequence of local compactness (as defined above) for categorical topology is that locally compact spaces are [[exponential object|exponentiable]], i.e., if $Y$ is locally compact, then $Y \times -: Top \to Top$ has a [[adjunction|right adjoint]] $(-)^Y: Top \to Top$. In fact, this is almost an abstract definition of local compactness: for [[sober spaces]], local compactness is equivalent to being exponentiable. Cf. the situation for [[locales]]: a result of Hyland is that locale is [[locally compact locale|locally compact]] if and only if it is exponentiable.  (See [[exponential law for spaces]] and [[compact-open topology]] for more details.) 

As noted above, locally compact spaces form a finitely complete [[full subcategory]] of $Top$. It is not true that arbitrary products of locally compact spaces are locally compact. However, some important examples of locally compact spaces are constructed as restricted direct products, as follows. 

Let $(X_p, K_p)_{p \in P}$ be a collection of pairs of spaces where each $X_p$ is locally compact and $K_p \subseteq X_p$ is a compact _open_ subspace. The **restricted direct product** of the collection is the colimit of the [[filtered category|filtered diagram]] consisting of spaces 
$$D_F = \prod_{p \in F} X_p \times \prod_{p \notin F} K_p$$ 
where $F$ ranges over all finite subsets of $P$, together with inclusions $D_F \subseteq D_{F'}$ where $F \subseteq F'$. We observe that each of the $D_F$ is locally compact, and that a filtered colimit or union of a system of _open_ inclusions of locally compact spaces is again locally compact. Therefore, restricted direct products are locally compact, under the hypotheses stated above. 

These hypotheses are of course pretty severe; important examples of such restricted direct products include topologized [[adele ring]]s and [[idele group]]s. In the case of adele rings, the collection of pairs is $(K_{\mathfrak{p}}, O_{\mathfrak{p}})$ where $K_{\mathfrak{p}}$ is the $\mathfrak{p}$-adic completion of a [[number field]] $K$ and $O_{\mathfrak{p}}$ is the $\mathfrak{p}$-adic completion of the ring of integers $O \subseteq K$. 

In any event, the category of locally compact spaces does not admit general infinite products. If it did, then so would the category of locally compact Hausdorff spaces, and so would the category of locally compact Hausdorff abelian groups. However, there is no product of countably many copies of the real numbers in $LCHAb$, for if there were, then by utilizing the universal property of the product, it would become a Hausdorff TVS over the real numbers, in contradiction to the fact that the only locally compact Hausdorff TVS are finite-dimensional. 

Locally compact spaces _are_ closed under [[coproduct]]s in $Top$. They do not admit many types of [[colimit]]s generally; in some sense this is a _raison d\'&#234;tre_ for [[compactly generated topological spaces]]: they are precisely the colimits in $Top$ of diagrams of locally compact spaces. 

\begin{prop}\label{LocallyCompactHausdorffSpacesAreCompactlyGeneratedWeaklyHausdorff}
  Every [[locally compact Hausdorff space]] is
  [[compactly generated topological space|compactly generated]]
  and [[weakly Hausdorff topological space|weakly Hausdorff]].
\end{prop}

([Strickland 09, Prop. 1.7](compactly+generated+topological+space#Strickland09))



### Gelfand duality

Under [[Gelfand duality]] the category of compact Hausdorff topological spaces is equivalent to the [[opposite category]] of commutative [[C-star algebras]]. With some care there are generalizations of this also to locally compact topological spaces. See at _[[Gelfand duality]]_ for more.



### Further properties 

Locally compact Hausdorff spaces are [[paracompact space|paracompact]] whenever they are also [[second-countable space|second-countable]].


## Related concepts

* [[locally proper map]]

* [[locally compact locale]]

* [[compact topological space]], [[countably compact topological space]], [[paracompact topological space]], [[locally compact topological space]], [[strongly compact topological space]]

* [[Gelfand duality]]

* [[vanishing at infinity]]



[[!redirects locally compact topological space]]
[[!redirects locally compact topological spaces]]

[[!redirects locally compact Hausdorff topological space]]
[[!redirects locally compact Hausdorff topological spaces]]
[[!redirects locally compact Hausdorff]]

[[!redirects locally compact space]]
[[!redirects locally compact spaces]]
[[!redirects locally compact]]

[[!redirects locally compact Hausdorff space]]
[[!redirects locally compact Hausdorff spaces]]
[[!redirects local compactness]]
[[!redirects local compactum]]
[[!redirects local compactums]]
[[!redirects local compacta]]
[[!redirects locally compactum]]
[[!redirects locally compactums]]
[[!redirects locally compacta]]
