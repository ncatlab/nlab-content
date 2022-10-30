
> see at [[Galois theory]] for more

#Contents#
* table of contents
{:toc}

## Idea

Given a [[field extension]] one can consider the corresponding automorphism group.  The main statement of [[Galois theory]] is that, when the [[field extension]] is Galois, this [[group]] is called the Galois group and its [[subgroup]]s correspond to subextensions of the [[field extension]].

In [[algebraic geometry]], [[Grothendieck]] defined an analogue of the Galois group called the [[etale fundamental group]] of a connected [[scheme]].

Even more generally there is an analogue of the Galois group in [[stable homotopy theory]].  In fact one can define the Galois group of any [[presentable (infinity,1)-category|presentable]] [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[stable (infinity,1)-category]], and there is an analogue of the [[Galois theory|Galois correspondence]].  In particular one gets a Galois group associated to an [[E-infinity ring spectrum]].  One recovers the Galois group of a [[scheme]] as the Galois group of its [[derived category of quasi-coherent sheaves]].

## Definition

+-- {: .num_defn}
###### Definition

Let $K\hookrightarrow L$ denote a Galois [[field extension]], then the [[automorphism group]]

$$Gal(K\hookrightarrow L):=Aut_K(L)$$

consisting just of those automorphisms of $L$ whose restriction to $K$ is the identity is called *Galois group of the field extension $K\hookrightarrow L$.

=--

Every Galois group $Gal(K\hookrightarrow L)=lim_{K\hookrightarrow E\hookrightarrow L}Gal (K\hookrightarrow E)$  is a [[profinite group|profinite]] [[topological group]] in that it is the limit of the topologically discrete Galois groups of the intermediate finite extensions between $K$ and $L$.

The just defined Galois group is the one occurring in the classical [[Galois theory]] for fields. The analog of the Galois group in [[Galois theory|Galois theory for schemes]] is a [[fundamental group]] (of a scheme) and is rarely called a ''Galois group''.

The Galois group $Gal(K\hookrightarrow K_s)$ of the separable closure of $K$ is called the *[[absolute Galois group]]* of $K$. In this case we have $Gal(K\hookrightarrow K_s)\simeq \pi_1(Spec\; K)$ is equivalent to the [[fundamental group]] of the [[scheme]] $Spec K$. In particular the notion of [[fundamental group of a topos|fundamental group (of a point of) a topos]] generalizes that of Galois group. This observation is the starting point and motivating example of [[Grothendieck's Galois theory]] and more generally of that of [[homotopy groups in an (infinity,1)-topos]].

If the scheme, moreover, is a [[group scheme]] (i.e. endowed with a group structure) modules over the Galois group, which are called [[Galois module|Galois modules]], play an important role in [[algebraic number theory]].

## Properties

### Relation to &#233;tale fundamental goup
 {#RelationToEtaleFundamentalGroup}

For $K$ a [[field]], then the absolute Galois group of $K$ is equivalent to the [[étale fundamental group]]/[[algebraic fundamental group]] of the [[spectrum of a commutative ring|spectrum]] of $K$.

$$
   \pi_1(Spec(K)) \simeq Gal(K_{sep}/K)
  \,.
$$

If $K$ is a [[number field]], write $\mathcal{O}_K$ for its [[ring of integers]], so that $Spec(\mathcal{O}_K)$ is an [[arithmetic curve]]. Then 

$$
  \pi_1(Spec(\mathcal{O}_K)) \simeq Gal(K_{alg}^{ur}/K)
  \,,
$$

where $K_{alg}^{ur}$ is the maximal algebraic extension of $K$ that is [[unramified]] at all non-zero [[prime ideals]] (e.g. [Lenstra 85, Example 1.12](#Lenstra85)). 

See also at _[Galois theory -- Statement of the main theorem](Galois+theory#StatementOfMainTheorem)_.


### Relation to Frobenius maps
 {#RelationToFrobeniusMaps}

For $K$ a [[number field]] then the [[Frobenius maps]] induce canonical elements in the Galois group. See at _[Frobenius morphism -- As elements of the Galois group](Frobenius+morphism#AsElementsOfGaloisGroup)_.

This crucially enters the definition of [[Artin L-functions]] associated with [[Galois representations]].

## Related concepts

* [[Galois theory]]

* [[motivic Galois group]]

## References

A standard account is

* {#Lenstra85} [[Hendrik Lenstra]], _Galois theory for schemes_ , Mathematisch Instituut Universiteit van Amsterdam (1985) ([pdf](http://websites.math.leidenuniv.nl/algebra/GSchemes.pdf))
 

For the Galois group in [[stable homotopy theory]], see

* [[Akhil Mathew]], The Galois group of a stable homotopy theory, [arXiv](http://arxiv.org/abs/1404.2156).

[[!redirects Galois groups]]

category: Galois theory