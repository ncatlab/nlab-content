
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _multiplicative [[character]]_ of a [[group]] $G$ is a [[group homomorphism]] into the [[circle group]] $U(1)$, or more generally into the [[group of units]] $k^\times$ of a given [[ground field]] (for instance $\mathbb{C}^\times = U(1)$):

$$
  \chi
  \;\colon\;
  G \longrightarrow k^\times  
  \,.
$$

Since $k^\times$ is an [[abelian group]], this means that group characters are in particular [[class functions]].

Dually a co-character is a homomorphism out of $k^\times$ into $G$.

The collection of characters is itself an [[abelian group]] under the pointwise multiplication, this is called the **character lattice**
$ Hom(G,k^\times) $
of the group. Similarly the **cocharacter lattice** is $Hom(k^\times, G)$.


For [[topological groups]] one considers [[continuous map|continuous]] characters. Specifically, for a [[locally compact Hausdorff]] group $G$ (often further assumed to be an [[abelian group]]), a __character__ of $G$ is continuous homomorphism to the [[circle]] group $\mathbb{R}/\mathbb{Z}$. If $G$ is [[profinite group|profinite]], then this is the same as an continuous homomorphism to the [[discrete space|discrete]] group $\mathbb{Q}/\mathbb{Z}$.  (See [MO](http://mathoverflow.net/questions/86089/two-definitions-of-character-of-topological-groups).)


## Properties

### Restriction of group characters to maximal tori -- weights
 {#Weights}

Let $G$ be a [[connected topological space|connected]] [[compact Lie group]].

By the general [properties of maximal tori](maximal+torus#Properties) in this case, it follows that every group character $G \to U(1)$ is already fixed by its restriction along a [[maximal torus]] inclusion

$$
  T \hookrightarrow G \to U(1)
  \,.
$$

Now the group characters of the [[abelian group|abelian]] maximal torus $T\simeq U(1)^n$ are [[n-tuples]] of group characters of the [[circle group]] $U(1)$, which are [[integers]] -- the _[[weight (in representation theory)|weights]]_.

Explicitly, under a given identification of the [[circle group]] as a [[quotient]] of the additive group of [[real numbers]]

$$
  U(1) \simeq \mathbb{R}/h \mathbb{Z}
$$

for $h \in (0,\infty)$, then the character $\lambda$ on $U(1)^n\simeq T$ labeled by $(x_1, \cdots, x_n) \in \mathbb{Z}^n$ is

$$
  \lambda(t_1,\cdots t_n) 
  = 
  \exp(\tfrac{i}{\hbar} \sum_{j = 1}^n t_j n_j )
$$

(where $\hbar \coloneqq h/2\pi$ is "[[Planck's constant]]").


(e.g. [Johansen, section 2.10](#Johansen))


### Relation to Chern roots and the splitting principle
 {#RelationToChernRootsAndSplittingPrinciple}

A group character, hence a group [[homomorphism]] $G \to U(1)$ induces a map of [[classifying spaces]] $B G \to B U(1) \simeq K(\mathbb{Z},2)$. Similarly for the restriction to the [[maximal torus]] [above](#Weights), which induces

$$
  B U(1)^n \simeq B T \to B G \to B U(1)\simeq K(\mathbb{Z},2)
  \,.
$$

Under this identification the [weights](#Weights) $x_i$ of the group character, as above, are the "[[Chern roots]]" as the appear in the [[splitting principle]]. See there for more.


### Characters and fundamental group of tori
 {#CharactersAndFundamentalGroupsOfTori}
 
Write $S^1$ for the [[circle group]].

Let $T$ be a [[torus]], regarded as an [[abelian group]]. 
Write $[T,S^1]$ for its character group.

There is a [[bilinear form]]

$$
  \pi_1(T)\otimes [T, S^1] \longrightarrow \mathbb{Z}
$$

on the [[fundamental group]] of the [[torus]] and its character group, given by sending a [[homotopy class]] $[\gamma]$ of a [[continuous map]]

$$
  \gamma \colon S^1 \longrightarrow T
$$

to the [[homotopy class]] $c(\gamma)$ of the [[composition]] with a [[character]] $c \colon T \longrightarrow S^1$

$$
  c(\gamma) \;\colon\; S^1 \stackrel{\gamma}{\longrightarrow}
  T \stackrel{c}{\longrightarrow} S^1
$$

regarded as an element $[c(\gamma)] \in \pi_1(S^1) \simeq \mathbb{Z}$.

This [[bilinear form]] is non-degenerate, and hence constitutes an [[isomorphism]]

$$
  \pi_1(T) \simeq [T,S^1]
  \,.
$$

### Inner product and orthogonality

The complex [[class functions]] on a [[finite group]] $G$ have an [[inner product]] given by

$$
  \langle \alpha, \beta\rangle
  \coloneqq
  \frac{1}{{\vert G \vert}}
  \underset{g \in G}{\sum} \alpha(g) \overline{\beta(g)}
  \,.
$$

The _[[Schur orthogonality relation]]_ is the statement that the [[irreducible representation|irreducible]] group characters $\{\chi_i\}_i$ form an [[orthonormal basis]] of the space of [[class functions]] under this [[inner product]]:

$$
  \langle \chi_i, \chi_j \rangle 
  = 
  \left\{
    \array{
       1 & if \; i = j
       \\
       0 & otherwise
    }
  \right.
$$

Such properties arise from characters occurring as [[traces]] of [group representations](representation+ring#relation_to_the_character_ring).

### In terms of the classifying space of the group

Consider the [[classifying space]], $B G$, of the group. Then its [[free loop space]], $Map (S^1, B G)$, has as components $G$ modulo [[conjugation]]. Then, the characters of $G$ may be expressed as the zeroth cohomology of this loop space, $H^0(\mathcal{L} B G, \mathbb{C})$. This construction is useful in the generalisation to [[transchromatic characters]]. 

## Related concepts

* [[Pontryagin duality]], [[Pontryagin dual]]

* [[conjugacy class of subgroups]]

## References

Original articles on character rings/[[representation rings]] of [[compact Lie groups]] include

* [[Graeme Segal]], _The representation ring of a compact Lie group_, Publications Math&#233;matiques de l'Institut des Hautes &#201;tudes Scientifiques, January 1968, Volume 34, Issue 1, pp 113-128 ([numdam:PMIHES_1968__34__113_0](http://archive.numdam.org/numdam-bin/fitem?id=PMIHES_1968__34__113_0))

* Masaru Tackeuchi, _A remark on the character ring of a compact Lie group_, J. Math. Soc. Japan Volume 23, Number 4 (1971), 555-705 ([euclid:jmsj/1259849785](http://projecteuclid.org/euclid.jmsj/1259849785))

Lecture notes on characters of finite and compact Lie groups include

* {#Johansen} Troels Roussauc Johansen, _Character Theory for Finite Groups and Compact Lie Groups_ [pdf](http://www.math.upb.de/~johansen/character-theory.pdf)

* Andrei Yafaev, _Characters of finite groups_ ([pdf](http://www.ucl.ac.uk/~ucahaya/Characters.pdf))


Discussion for finite groups in the more general context of [[equivariant cohomology|equivariant]] [[complex oriented cohomology theory]] ([[transchromatic character]]) is in 

* [[Michael Hopkins]], [[Nicholas Kuhn]], [[Douglas Ravenel]], _Generalized group characters and complex oriented cohomology theories_, J. Amer. Math. Soc. 13 (2000), 553-594 ([publisher](http://www.ams.org/journals/jams/2000-13-03/S0894-0347-00-00332-5/), [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/hkr.pdf))



[[!redirects group characters]]

[[!redirects character lattice]]
[[!redirects character lattices]]

[[!redirects cocharacter lattice]]
[[!redirects cocharacter lattices]]

[[!redirects co-character lattice]]
[[!redirects co-character lattices]]

[[!redirects character group]]
[[!redirects character groups]]