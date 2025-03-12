

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Brauer induction theorem_ ([Brauer 46](#Brauer46)) states that, for [[ground field]] the [[complex numbers]], [[finite dimensional vector space|finite-dimensional]] [[linear representations]] $V$ of a [[finite group]] $G$ all arise as [[virtual representation|virtual combinations]] of [[induced representations]] $ind_{H}^G \big(W\big)$ of just 1-dimensional representations $W$, $dim_{\mathbb{C}}(W) =1$:


\[
  \label{GenericExampleOfBrauerInduction}
  [V] 
  \;=\;
  \underset{
    \mathclap{
    {
      H_i \hookrightarrow G
    }
    \atop
    {
      {W_i \in Rep(H_i)\,,}
      \atop
      { dim(W_i) = 1 }
    }
    }
  }{\sum}
  \,
  n_i
  \, 
  \Big[ 
    ind_{H_i}^G \big(W_i\big)
  \Big]
  \,,
  \phantom{AAA}
  n_i \in \mathbb{Z}
  \,.
\]

In other words, this says that the [[representation ring]] $R_{\mathbb{C}}(G)$ is generated from [[isomorphism classes]] $\left[ind_{H}^big(W\big)\right]$ of  [[induced representations]] $ind_{H}^G \big(W\big)$ of 1-dimensional representations $W$ of [[subgroups]] $H \subset G$.

This may be thought of as (implying) a [[splitting principle]] for [[linear representations]] ([Symonds 91](#Symonds91)), for more on this see at _[[characteristic classes of linear representations]]_ the section _[splitting principle](characteristic+class+of+a+linear+representation#SplittingPrinciple)_.

Brauer induction generalizes the immediate statement that [[finite dimensional vector space|finite-dimensional]] [[permutation representations]] are all [[direct sums]] of [[induced representations]] of the _[[trivial representation|trivial]]_ 1-dimensional representation; see at _[[induced representation of the trivial representation]]_.

The analogous statement holds true also for [[ground ring]] the [[quaternions]], while for [[ground field]] the [[real numbers]] one has to induce not just from 1-dimensional but also from 2-dimensional representations.

Of course, the expansions (eq:GenericExampleOfBrauerInduction) are not unique. But one may find [[functor|functorial]] choices that satisfy good extra properties, see below _[Snaith's explicit Brauer induction](#SnaithExpansion)_ and _[Symond's explicit Brauer induction](#SymondExplicitBrauerInduction)_.

We may also restrict the collection of subgroups needed.  For example, in the representation ring of a finite group $G$, every element is a difference of elements induced from representations of "elementary" subgroups of $G$, where an elementary subgroup is a group of order $p^n$ times a cyclic group whose order is relatively prime to $p$.  This result is a partner to the [[Artin induction theorem]] saying that every element of the representation ring of $G$ is a _rational_ linear combination of elements induced from _cyclic_ subgroups of $G$.  (For both cyclic and elementary groups, every representation is a direct sum of 1-dimensional representations.)

<br/>

## Properties

### Snaith's explicit Brauer induction
 {#SnaithExpansion}

(...)

### Symonds' explicit Brauer induction
 {#SymondExplicitBrauerInduction}

We state an explicit and [[natural transformation|natural]] choice of Brauer induction due to [Symonds 91](#Symonds91) (Prop. \ref{SymondsExplicitBrauerInd}) below. Its main property is good compatibility with the [[total Chern classes of linear representations]] via a certain multiplicative transfer map on [[integral cohomology]] (the latter recalled as Lemma \ref{TransferEvens} below). 

+-- {: .num_lemma #TransferEvens}
###### Lemma
**(Evens' multiplicative transfer)**

For $G$ a [[finite group]] and $H \subset G$ a [[subgroup]], there is a [[linear map]]

$$
  \mathcal{N}_H^G
  \;\colon\;
  \underset{k \in \mathbb{N}}{\prod} H^{2k}\big( B H, \mathbb{Z}\big)
  \longrightarrow
  \underset{k \in \mathbb{N}}{\prod} H^{2k}\big( B G, \mathbb{Z}\big)
$$

from the [[cohomology ring]] of the [[classifying space]] of $H$ to that of $G$ which is multiplicative in that its respects the product structure, hence the [[cup product]], on both sides

$$
  \mathcal{N}_H^G\big( \alpha \smile \beta\big)
  \;=\;
  \mathcal{N}_H^G\big( \alpha\big)  \smile \mathcal{N}_H^G\big( \beta\big)
  \,.
$$

=--

This is due to [Evens 63](#Evens63). There, the maps themselves are introduced on the bottom of p. 7, while their multiplicativity is stated as Prop. 4 on p. 10. 


+-- {: .num_prop #SymondsExplicitBrauerInd}
###### Proposition
**(Symonds' explicit Brauer induction)**

For $G \in $ [[FinGrp]]
there is a [[linear map]] ([[homomorphism]] of [[abelian groups]])

$$
  R_{\mathbb{C}}\big( G \big)
  \overset
  {L}
  {\longrightarrow}
  \underset{
    [H \subset G]
  }{\prod}
  \mathbb{Z}
  \left[
    1dRep_{\mathbb{C}}\big( H \big)_{/\sim}
  \right]
$$

from the underlying abelian group of the [[representation ring]] to the [[product group]] of the [[free abelian groups]] that are spanned by the [[isomorphism classes]] of 1-dimensional representations over all [[conjugacy classes]] of [[subgroup]] $H \subset G$,

such that 

1. $L$ is a [[natural transformation]] of [[functors]] $FinGrp^{op} \to Ab$, 

   hence $L\big( f^\ast V\big) = f^\ast( L(V) )$;

1. $L$ is a [[section]] of the [[natural transformation]]

    $$
      \underset{
       [H \subset G]
      }{\prod}
      R^{1d}_{\mathbb{Z}}\big( H\big)
       \overset
       {\sum ind}
       {\longrightarrow}
      R_{\mathbb{C}}\big( G \big)
   $$
 
   which applies [[induced representation|induction]] and then sums everything up, in that the [[composition]] $\big( \sum ind \big) \circ L$ is the [[identity morphism|identity]]:

   $$
     \big( \sum ind \big) \circ L(V)
     \coloneqq
     \underset{
       [H \subset G]
     }{
       \sum
     }
     ind_H^G\left[ L(V)_H  \right]
     \;=\;
     V
   $$   

1. $L$ is compatible with the [[total Chern classes of linear representations]] 

   $$
     R_{\mathbb{C}}\big( G \big)
     \overset{c}{\longrightarrow}
     \underset{ k \in \mathbb{N} }{\prod}
     H^{2k}\big( B G, \mathbb{Z} \big)
   $$

   via their multiplicative transfer $\mathcal{N}_H^G$ (Lemma \ref{TransferEvens}) in that 

   $$
     c
     \big( 
       V
     \big)
     \;=\;
     \underset{ [H \subset G] }{\smile}
     \mathcal{N}_H^G
     \Big(
       c
       \big(
         L(V)_H 
       \big)
     \Big)
     \,,
   $$

   hence in that the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       R_{\mathbb{C}}\big( G\big)
         &\overset{L}{\longrightarrow}&
       \underset{
         [H \subset G]
       }{\prod}   
       \mathbb{Z}
       \left[
         1dRep_{\mathbb{C}}\big( H \big)_{/\sim}
       \right]
       \\
       {}^{\mathllap{c}}\Big\downarrow
       &&
       \Big\downarrow
       {}^{
         \underset{
           [H \subset G]
         }{\prod}   
         \left( 
           c
           \circ
           \mathcal{N}_H^G
         \right)
       }
       \\
       \underset{
         k \in \mathbb{N}
       }{\prod}
       H^{2k}\big( B G, \mathbb{Z} \big)
       &
         \underset{
           \underset{ [H \subset G] }{\smile}
         }{\longleftarrow}
       &
       \underset{
         [H \subset G]
       }{\prod}   
       \underset{
        k \in \mathbb{Z}
       }
       {\Prod}
       H^{2k}\big( B G, \mathbb{Z}\big)
     }
   $$
   
1. a 1-dimensional representation $W \in 1dRep\big(G\big)_{/\sim} \subset R_{\mathbb{C}}\big(G\big)$ is sent to the [[tuple]] $L(W) = (W,0,0, \cdots)$ whose component over $G \subset G$ is $V$ itself, and all whose other components vanish;

1. in contrast, if $V \in Rep_{\mathbb{C}}\big( G \big)_{/\sim}$ has no 1-dimensional [[direct sum|direct summand]], then the $G$-compnents of $L(V)$ is zero;


=--  

([Symonds 91, Prop. 2.1, Theorem 2.2, and Theorem 2.4](#Symonds91))



(...)

## References

Due to 

* {#Brauer46} [[Richard Brauer]], ... (1946)

See also 

* Wikipedia, _[Brauer's theorem on induced characters](https://en.wikipedia.org/wiki/Brauer%27s_theorem_on_induced_characters)_

In the context of [[characteristic classes of linear representations]]:

* {#Symonds91} [[Peter Symonds]], _A splitting principle for group representations_, Comment. Math. Helv. (1991) 66: 169 ([dml:140229](https://eudml.org/doc/140229), [doi:10.1007/BF02566643](https://doi.org/10.1007/BF02566643))

based on

* {#Evens63} [[Leonard Evens]], _A Generalization of the Transfer Map in the Cohomology of Groups_, Transactions of the American Mathematical Society Vol. 108, No. 1 (Jul., 1963), pp. 54-65 ([doi:10.1090/S0002-9947-1963-0153725-1](https://doi.org/10.1090/S0002-9947-1963-0153725-1), [jstor:1993825](https://www.jstor.org/stable/1993825))

and

* {#Kroll87} Ove Kroll, _An Algebraic Characterisation of Chern Classes of Finite Group Representations_, Bulletin of the LMS, Volume19, Issue3 May 1987 Pages 245-248 ([doi:10.1112/blms/19.3.245](https://doi.org/10.1112/blms/19.3.245))



[[!redirects Brauer's theorem]]

[[!redirects Brauer's theorem on induced characters]]

[[!redirects Brauer induction]]
[[!redirects Brauer inductions]]

[[!redirects explicit Brauer induction]]
[[!redirects explicit Brauer inductions]]
