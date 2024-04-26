
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Cyclic groups
* table of contents
{: toc}


## Definition

A *cyclic group* is a [[quotient group]] of the additive group of [[integers]] (hence of the [[free group]] on the [[singleton]]).

Generally one considers cyclic groups as abstract [[groups]], that is without specifying which element comprises the generating singleton.  But see at *[Ring structure](#Ring)* below.


## Examples
 {#Examples}

There is (up to [[isomorphism]]) one cyclic group 

$$
  \mathbb{Z}\!/\!n 
  \,\coloneqq\,
  \mathbb{Z}/n\mathbb{Z}
$$

for every [[natural number]] $n \in \mathbb{N}$, this being the [[quotient group]] by the (necessarily [[normal subgroup|normal]]) [[subgroup]] $n \mathbb{Z} \hookrightarrow \mathbb{Z}$ of integers divisible by $n$.

For $n = 0$ this subgroup is the [[trivial group]], hence this quotient is just the [[integers]] itself

$$
  \mathbb{Z}\!/\!0 \,\simeq\, \mathbb{Z}
  \,,
$$

as such also called the *infinite cyclic group*, since its [[order of a group|order]]/[[cardinality]] is [[countable set|countably]] [[infinite set|infinite]].

For $n \gt 0$, the [[order of a group|order]] ([[cardinality]]) of $\mathbb{Z}\!/\!n$ is the [[finite number]]

$$
  ord\big(
    \mathbb{Z}\!/\!n
  \big)
  \;=\;
  card\big(
    \mathbb{Z}\!/\!n
  \big)
  \;=\;
  n
  \,.
$$

Explicitly this means that 

* [[elements]] of $\mathbb{Z}\!/\!n$ are [[equivalence classes]] $[k]$ of [[integers]], where the [[equivalence relation]] is "[[modulo]] $n$":

  $$
    [k] = [k']
    \;\;\;
    \in
    \;
    \mathbb{Z}\!/\!n
    \;\;\;\;\;\;\;\;\;
    \Leftrightarrow
    \;\;\;\;\;\;\;\;\;
    \underset{r \in \mathbb{Z}}{\exists}
    \big(
      k ' = k + r \cdot n
    \big)
    \,.
  $$

* the [[binary operation]] in the group is [[addition]] of representatives

  $$
    \array{
      \mathbb{Z}\!/\!n \times \mathbb{Z}\!/\!n
      &\longrightarrow&
      \mathbb{Z}\!/\!n
      \\
      \big( [k_1], \, [k_2] \big)
      &\mapsto&
      [k_1 + k_2]
      \,.
    }
  $$

The cyclic group $\mathbb{Z}\!/\!n$ of order $n$ may also be identified with a [[subgroup]] of the multiplicative [[group of units]] $\mathbb{C}^\times \hookrightarrow \mathbb{C}$ of [[complex numbers]] (or [[algebraic numbers]]), namely the group of $n$th [[roots of unity]]:

$$
  \array{
    \mathbb{Z}\!/\!n
    &\xhookrightarrow{\phantom{---}}&
    \mathbb{C}^\times
    \\
    [k] &\mapsto& \exp\big(2 \pi \mathrm{i} \tfrac{k}{n}\big)
    \mathrlap{\,.}
  }
$$

Dedicated entries exist for the examples of the

* [[cyclic group of order 2]]

* [[cyclic group of order 3]]

* [[cyclic group of order 4]]


## Notation
 {#Notation}

Some alternative notations for the finite cyclic groups are in use. Many authors use subscript notation

*  "$\mathbb{Z}_n$" for $\mathbb{Z}\!/\! n \mathbb{Z}$. 

However, at least for $n = p$ a [[prime number]], this notation clashes with standard notation "$\mathbb{Z}_p$" for the [[ring]] of [[p-adic integers|$p$-adic integers]].

Therefore, in fields where both [[cyclic groups]] as well as [[p-adic integers]] play an important role (such as in [[algebraic topology]] and [[arithmetic geometry]], see e.g. the theory of [[cyclotomic spectra]]), it is common to choose different notation for the cyclic groups, typically

* "$C_n$" for $\mathbb{Z}\!/\! n \mathbb{Z}$.

Here "$C$" is, of course, for "cyclic".  Other authors may keep the letter "Z" with a subscript but resort to another font, such as 

* "$Z_n$" for $\mathbb{Z}\!/\! n \mathbb{Z}$.

Often this last notation is meant to indicate that not just the group but the [[ring]]-[[structure]] inherited from $\mathbb{Z}$ is referred to, see [below](#Ring) (which of course makes the possible confusion with notation for the [[p-adic integers]] only worse).

Incidentally, while the notation "$\mathbb{Z}$" for the [[integers]] derives from the German word *Zahl* (for *number*), that letter happens to also be the first one in the German word *zyklisch* (for *cyclic*).


## Properties

### Ring structure
   {#Ring}

Let $A$ be a cyclic group, and let $x$ be a generator of $A$.  Then there is a unique [[ring]] structure on $A$ (making the original group the additive group of the ring) such that $x$ is the multiplicative identity $1$.

If we identify $A$ with the additive group $\mathbb{Z}/n$ and pick (the equivalence class of) the integer $1$ for $x$, then the resulting ring is precisely the [[quotient ring]] $\mathbb{Z}/n$.

In this way, a cyclic group equipped with the [[extra structure]] of a generator is the same thing (in the sense that their [[groupoids]] are [[equivalence of categories|equivalent]]) as a ring with the [[extra property]] that the underlying additive group is cyclic.

For $n \gt 0$, the number of ring structures on the cyclic group $\mathbb{Z}/n$, which is the same as the number of generators, is $\phi(n)$, the [[totient function|Euler totient]] of $n$; the generators are those $i$ that are [[relatively prime numbers|relatively prime]] to $n$.  While $\phi(1) = 1$, otherwise $\phi(n) \gt 1$ (another way to see that we have a structure and not just a property).  For $\mathbb{Z}$ itself, there are two ring structures, since $1$ and $-1$ are the generators (and these are relatively prime to $0$).

\lineabreak

### Fundamental theorem of cyclic groups
  {#FundamentalTheoremOfCyclicGroups}

For $n \in \mathbb{N}$, there is precisely one [[subgroup]] of the cyclic group $\mathbb{Z}/n\mathbb{N}$ of [[order of a group|order]] $d \in \mathbb{N}$ for each factor of $d$ in $n$, and this is the subgroup [[generators and relations|generated]] by $n/d \in \mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$.

Moreover, the [[lattice of subgroups]] of $\mathbb{Z}/n\mathbb{Z}$ is equivalently the dual of the lattice of natural numbers $\leq n$ ordered by divisibility.

(e.g [Aluffi 09, pages 83-84](#Aluffi09))

This is a special case of the _[[fundamental theorem of finitely generated abelian groups]]_. See there for more.


### Relation to finite abelian groups

+-- {: .num_prop}
###### Proposition

Every [[finite abelian group]] is a [[direct sum of abelian groups]] over cyclic groups.

=--

See at _[[finite abelian group]]_ for details.


### Group cohomology

For discussion of the [[group cohomology]] of cyclic groups see 

* at _[[projective resolution]]_ the section _[Cohomology of cyclic groups](http://ncatlab.org/nlab/show/projective+resolution#CohomologyOfCyclicGroups)_

* at *[[finite rotation group]]* the section *[Group cohomology](finite+rotation+group#GroupCohomology)*

* in [Golasiński & Gonçalves 2011](#GolasińskiGonçalves11) for the cases $H^n_{Grp}(/mathbb{Z}/n;\, \mathbb{Z}/m)$

For example, relevant for [[Dijkgraaf-Witten theory]] is the fact:

$$
  H^3_{grp}\big(\mathbb{Z}/n\mathbb{Z}, U(1)\big) 
  \;\simeq\; 
  \mathbb{Z}/n\mathbb{Z}
  \,.
$$

### Linear representations

We discuss some of the [[representation theory]] of cyclic groups.

+-- {: .num_example #IrreducibleRealRepresentationsOfCyclicGroups}
###### Example
**([[irreducible representation|irreducible]] [[real numbers|real]] [[linear representations]] of [[cyclic groups]])**

For $n \in \mathbb{N}$, $n \geq 2$,
the [[isomorphism classes]] of [[irreducible representation|irreducible]] [[real numbers|real]] [[linear representations]] of the [[cyclic group]] $\mathbb{Z}/n$ are given by precisely the following:

1. the 1-[[dimension|dimensional]] [[trivial representation]] $\mathbf{1}$;

1. the 1-[[dimension|dimensional]] [[sign representation]] $\mathbf{1}_{sgn}$;

1. the 2-[[dimension|dimensional]] standard representations $\mathbf{2}_k$ of [[rotations]] in the [[Euclidean plane]] by [[angles]] that are [[integer]] multiples of $2 \pi k/n$, for $k \in \mathbb{N}$, $0 \lt k \lt n/2$;

   hence the [[restricted representations]] of the defining real rep of [[SO(2)]] under the [[subgroup]] inclusions $\mathbb{Z}/n \hookrightarrow SO(2)$, hence the representations generated by [[real number|real]] $2 \times 2$ [[trigonometric function|trigonometric]] [[matrices]] of the form

   $$
    \rho_{\mathbf{2}_k}(1)
    \;=\;
     \left(
       \array{
         cos(\theta) & -sin(\theta)
         \\
         sin(\theta) & \phantom{-}cos(\theta)
       }
     \right)
     \phantom{AA}
     \text{with}
     \;
     \theta = 2 \pi \tfrac{k}{n}
     \,,
   $$ 

  (For $k = n/2$ the corresponding 2d representation is the [[direct sum]] of two copies of the [[sign representation]]: $\mathbf{2}_{n/2} \simeq \mathbf{1}_{sgn} \oplus \mathbf{1}_{sgn}$, and hence not [[irrep|irreducible]]. Moreover, for $k \gt n/2$ we have that $\mathbf{2}_{k}$ is irreducible, but [[isomorphism|isomorphic]] to $\mathbf{2}_{n-k} \simeq \mathbf{2}_{-k}$).

In summary:

$$
  Rep^{irr}_{\mathbb{R}}
  \big(
    \mathbb{Z}/n  
  \big)_{/\sim}
  \;=\;
  \big\{
    \mathbf{1},
    \mathbf{1}_{sgn},
    \mathbf{2}_k
    \;\vert\;
    0 \lt k \lt n/2
  \big\}
$$

=--

(e.g. [tom Dieck 09 (1.1.6), (1.1.8)](representation+theory#tomDieck09))

## Related concepts

* [[group of order 2]]

* [[binary cyclic group]]

* [[permutation cycle]], [[cyclic permutation]]

* [[multiplicative group of integers modulo n]]

* [[Q/Z]]

* [[integers modulo n]]

* [[p-localization]]

* [[profinite completion of the integers]]

* [[cyclotomic field]]

* [[cyclotomic spectrum]]


## References

Historical discussion of the cyclic group in the context of the [[classification of finite rotation groups]]:

* {#Klein1884} [[Felix Klein]], chapter I.3 of: _Vorlesungen über das Ikosaeder und die Auflösung der Gleichungen vom fünften Grade_, 1884, translated as _Lectures on the Icosahedron and the Resolution of Equations of Degree Five_ by George Morrice 1888, [online version](https://archive.org/details/cu31924059413439)


Textbook accounts:

* {#Aluffi09} [[Paolo Aluffi]], Part 0 of: *Algebra: Chapter 0*, Graduate Studies in Mathematics **104**,  AMS (2009) &lbrack;[ISBN:978-1-4704-1168-8](https://bookstore.ams.org/gsm-104/)&rbrack;

* [[Joseph A. Gallian]], Section 4 of: *Contemporary Abstract Algebra*, Chapman and Hall/CRC (2020)  &lbrack;[doi:10.1201/9781003142331](https://doi.org/10.1201/9781003142331), [pdf](https://ict.iitk.ac.in/wp-content/uploads/CS203-Mathematics-for-Computer-Science-III-Gallian.pdf)&rbrack;


Further review:

*  Philippe B. Laval, _Cyclic groups_ &lbrack;[pdf](http://math.kennesaw.edu/~plaval/math4361/groups_cyclic.pdf)&rbrack;

On the [[fundamental theorem of cyclic groups]]:

*  {#Gallian10} Joseph A. Gallian, _Fundamental Theorem of Cyclic Groups_, Contemporary Abstract Algebra, p. 77, (2010)


On the [[group cohomology]] of cyclic groups with [[coefficients]] in cyclic groups:

* {#GolasińskiGonçalves11} [[Marek Golasiński]], [[Daciberg Lima Gonçalves]], *On cohomologies and extensions of cyclic groups*, Topology and its Applications **158** (2011) 1858–1865 &lbrack;[doi:10.1016/j.topol.2011.06.022](https://doi.org/10.1016/j.topol.2011.06.022)&rbrack;


[[!redirects cyclic group]]
[[!redirects cyclic groups]]

[[!redirects infinite cyclic group]]
[[!redirects infinite cyclic groups]]


