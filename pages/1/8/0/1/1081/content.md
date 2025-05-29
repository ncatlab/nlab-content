
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Of chain complexes

### Idea 

Under the [[Dold-Kan correspondence]], [[∞-groupoids]] with strict abelian group structure (modeled by [[Kan complexes]] that are [[simplicial object|simplicial]] abelian groups) are identified with non-negatively graded [[chain complexes]] of abelian groups

$$
  N_\bullet : SimpAb \stackrel{\simeq}{\to} Ch_+
  \,.
$$

The **homology groups** of a [[chain complex]] of abelian groups are the image under this identification of the [[homotopy groups]] of the corresponding [[∞-groupoids]]. More details on this are at [[chain homology and cohomology]].


So at least for the case of chain complexes of abelian groups we have the slogan

+-- {: .standout}

**homology** = [[homotopy]] under [[Dold-Kan correspondence]]

=--

Of course historically the development of concepts was precisely the opposite: chain homology is an old fundamental concept in [[homological algebra]] that is simpler to deal with than [[simplicial homotopy groups]]. The computational simplification for chain complexes is what makes the [[Dold-Kan correspondence]] useful after all.

Conceptually, however, it can be useful to understand homology as a special kind of [[homotopy]]. This is maybe most vivid in the [[duality|dual]] picture: [[cohomology]] derives its name from that fact that [[chain homology and cohomology]] are dual concepts. But later generalizations of [[cohomology]] to [[generalized (Eilenberg-Steenrod) cohomology]] and further to [[nonabelian cohomology]] showed that the restricted notion of homology is an insufficient dual model for cohomology: what cohomology is really dual to is the more general concept of [[homotopy]].  More on this is at [[cohomotopy]] and [[Eckmann-Hilton duality]].


### Definition

The category of abelian groups is in particular an [[abelian category]].
We can define [[chain complexes]] and their homology in any [[abelian category]] $C$. 

Let $C$ be an [[abelian category]] and let
$$
  V_\bullet = ( \cdots  \to V_{n+1} \stackrel{\delta_n}{\to}
  V_n \stackrel{\delta_{n-1}}{\to}
  V_{n-1} \to \cdots
  )
$$
be a [[chain complex]] in $C$. For each integer $n \in \mathbb{N}$ this induces the following diagram of [[kernel]]s, [[cokernel]]s and [[image]]s

$$
  \array{
    && im \delta_n &&\to&& ker \delta_{n-1}
    \\
    & \nearrow && \searrow && \swarrow
    \\
    V_{n+1}
    &&\stackrel{\delta_n}{\to}&&
    V_n
    &&\stackrel{\delta_{n-1}}{\to}&&
    V_{n-1}
    \\
    & &&
    \swarrow && \searrow && \nearrow
    \\
    && coker \delta_n &&\stackrel{}{\to}&&
    im \delta_{n-1}
  }
$$

the **homology** $H_n(V)$ of $V$ in degree $n$ is the object

$$
  \begin{aligned}
    im(ker \delta_{n-1} \to  V_n \to coker \delta_{n}) 
    & \simeq
    coker(im \delta_n \to ker \delta_{n-1})
    \\
    & \simeq
    coker(V_{n+1} \to ker \delta_{n-1})
    \\
    & \simeq
    ker(coker \delta_n \to im \delta_{n-1})
    \\
    & \simeq
    ker(coker \delta_n \to V_{n-1})
  \end{aligned}
$$


* If $H_n(V) \simeq 0$ then one says that the complex $V$ is [[exact sequence|exact]] in degree $n$.

### Examples 

In the special case that $C$ is the category of abelian groups, or of vector spaces, this definition reduces to the more familiar simpler statement:

the $n$-th homology group of the [[chain complex]] $V_\bullet$ is the quotient group

$$
  H_n(V) = ker(\partial_n) / im(\partial_{n+1})
  \,.
$$

## Generalized homology

By the [[Brown representability theorem]] every [[spectrum]] $A$ induces a [[generalized (Eilenberg-Steenrod) cohomology]] theory, and dually a **generalized homology theory**.

For $X$ a [[topological space]] and $A$ a [[spectrum]], the generalized homology of spectrum of $X$ with coefficients in $A$ is 

$$
  X \wedge A := \Sigma^\infty(X)\wedge A
  \,,
$$

where on the right we have the [[smash product of spectra]] with the [[suspension spectrum]] of $X$ and on the left we abbreviate this to the [[(∞,1)-colimit|(∞,1)-tensoring]] of [[Spec]] over [[Top]].

The corresponding [[homology group]]s are the [[homotopy group]]s of this spectrum:

$$
  E_n(X,A) := \pi_n(X \wedge A) := [\Sigma^n \mathbb{S}, X \wedge A ]
  \,.
$$

where $\mathbb{S}$ is the [[sphere spectrum]]. For more see [[generalized homology]].

## Examples

* [[chain homology]]

  * [[relative homology]]

* [[simplicial homology]]

* [[singular homology]]

  * [[cellular homology]]

* [[generalized homology]]

* [[factorization homology]]

* [[Kan-Thurston Theorem]]

## Related concepts

* [[homology of loop spaces]]

* [[effective homology]]

* [[persistent homology]]

The relation between homology, cohomology and homotopy:

[[!include homotopy-homology-cohomology]]

The ingredients of homology and cohomology:

[[!include chains and cochains - table]]


## References

* {#Hilton69} [[Peter Hilton]] (ed.) _Category Theory, Homology Theory and Their Applications_, 

  vol 1: Lecture Notes in Mathematics **86**, Springer (1969) &lbrack;[doi:10.1007/BFb0079380](https://doi.org/10.1007/BFb0079380)&rbrack;

  vol 2: Lecture Notes in Mathematics **92**, Springer (1969) &lbrack;[doi:10.1007/BFb0080761](https://doi.org/10.1007/BFb0080761)&rbrack;

  vol 3: Lecture Notes in Mathematics **99**, Springer (1969) &lbrack;[doi:10.1007/BFb0081959](https://doi.org/10.1007/BFb0081959)&rbrack;

For a [[categorification]] of homology:

* Hadrian Heine, *On the categorification of homology* &lbrack;[arXiv:2505.22640](https://arxiv.org/abs/2505.22640)&rbrack;


[[!redirects homologies]]
[[!redirects homology group]]
[[!redirects homology groups]]

