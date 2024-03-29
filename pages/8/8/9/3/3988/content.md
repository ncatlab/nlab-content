
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea##


The **K-topology** is a [[topological space|topology]] on the set of [[real numbers]] $\mathbb{R}$ which is [[finer topology|finer]] than the [[Euclidean space|Euclidean]] [[metric topology]], but such that the new open sets are 'piled up' on the positive side of 0 (and actually are all contained in the [[half-open interval]] $[0,1)$) and have lots of 'holes'. It is useful for constructing counterexamples in [[topology]].

For instance the K-topology is an example of a [[topological space]] that is [[Hausdorff topological space|Hausdorff]] $(T_2)$ but not [[normal Hausdorff space|normal]] ($T_4$).


##Definition ##


+-- {: .num_defn #KTopology}
###### Definition

Write

$$
  K \coloneqq \{1/n \,\vert\, n \in \mathbb{N}_{\geq 1}\} \subset \mathbb{R}
$$

for the [[subset]] of [[natural number|natural]] [[fractions]] inside the [[real numbers]].

Define a [[topological basis]] $\beta \subset P(\mathbb{R})$ on $\mathbb{R}$ consisting of all the [[open intervals]] as well as the [[complements]] of $K$ inside them:  

$$
  \beta
    \;\coloneqq\;
  \left\{
    (a,b), 
    \,\vert\,
    a\lt b \in \mathbb{R}
  \right\}
   \,\cup\,
  \left\{
    (a,b) \backslash K, 
    \,\vert\,
    a\lt b \in \mathbb{R}
  \right\}
  \,.
$$

The [[topological space|topology]] $\tau_{\beta} \subset P(\mathbb{R})$ which is generated from this [[topological basis]] is called the _K-topology_.

We may denote the resulting [[topological space]] by

$$
  \mathbb{R}_K
   \;\coloneqq\;
  ( \mathbb{R}, \tau_{\beta})
  \,.
$$

=--

## Properties

+-- {: .num_defn }
###### Proposition

The real numbers with their K-topology (def. \ref{KTopology}) $\mathbb{R}_K$ are a [[Hausdorff topological space]] which is not a [[regular Hausdorff space]] (hence in particular not a [[normal Hausdorff space]]).

=--

+-- {: .proof}
###### Proof

By construction the K-topology is [[finer topology|finer]] than the usual [[Euclidean space|euclidean]] [[metric topology]]. Since the latter is Hausdorff, so is $\mathbb{R}_K$. It remains to see that $\mathbb{R}_K$ contains a point and a [[disjoint subset|disjoint]] closed subset such that do not have [[disjoint subset|disjoint]] [[open neighbourhoods]].

But this is the case essentially by construction: Observe that 

$$
  \mathbb{R} \backslash K
  \;=\;
  (-\infty,-1/2)
    \cup
  \left( 
    (-1,1) \backslash K
  \right)
    \cup
  (1/2, \infty)
$$

is an open subset in $\mathbb{R}_K$, whence

$$
  K = \mathbb{R} \backslash ( \mathbb{R} \backslash K  )
$$

is a [[closed subset]] of $\mathbb{R}_K$. 


But every [[open neighbourhood]] of $\{0\}$ contains at least $(-\epsilon, \epsilon) \backslash K$ for some positive real number $\epsilon$. There exists then $n \in \mathbb{N}_{\geq 0}$ with $1/n \lt \epsilon$ and $1/n \in K$. An open neighbourhood of $K$ needs to contain an open interval around $1/n$, and hence will have non-trivial intersection with $(-\epsilon, \epsilon)$. Therefore $\{0\}$ and $K$ may not be separated by disjoint open neighbourhoods, and so $\mathbb{R}_K$ is not normal.



=-- 


+-- {: .num_example #RationalNumbersWithKTopology}
###### Example

The set of [[rational numbers]], with the [[subspace topology]] inherited from the inclusion $\mathbb{Q} \hookrightarrow \mathbb{R}_K$ into the real numbers with their K-topology, is an example of a non-[[regular space|regular]], [[path-connected space|totally path-disconnected]] [[Hausdorff space|Hausdorff]] space. This space can be used to construct a [[quasitopological groupoid]] which isn't a [[internal groupoid|topological groupoid]].

=--

## Related concepts

* [[Dowker space]]


[[!redirects K-topologies]]
