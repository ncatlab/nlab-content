
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contemts#
* table of contents
{:toc}

## Idea

The [[projective spaces]] over [[ground ring]] $\mathbb{K}$ being the [[real numbers]] $\mathbb{R}$, [[complex numbers]] $\mathbb{C}$, [[quaternions]] $\mathbb{H}$ or [[octonions]] $\mathbb{O}$ admit, respectively, [[CW-complex|CW-]]-[[cell complex]] [[mathematical structure|structure]] with a single cell in each dimension $k$, $2 k$, $4 k$ or $8k$, respectively.

We discuss the cases $\mathbb{K} \,\in\, \{\mathbb{R}, \mathbb{C}, \mathbb{H}\}$. For the case $\mathbb{K} \,=\, \mathbb{O}$ see [Lackman 19, Lemma 3.4](#Lackman19)

## Preliminaries


Let $\mathbb{K} \,\in\, \big\{ \mathbb{R}, \mathbb{C}, \mathbb{H} \big\}$
be one of the [[associative algebra|associative]] [[real normed division algebras]], hence either the [[real numbers]], or the [[complex numbers]] or the [[quaternions]]. We regard this as a [[topological ring]] with respect to the canonical underlying [[topological space|topology]] of the [[Euclidean space]] $\mathbb{R}^{ dim_{_{\mathbb{R}}}(\mathbb{K}) }$.

For $n \in \mathbb{N}$, consider

$$
  \mathbb{K}P^n 
  \;\;
  \coloneqq
  \;\;
  \big(
    \mathbb{K}^{n+1} \setminus \{0\}
  \big) / \mathbb{K}^\times
$$

the $\mathbb{K}$-[[projective space]], i.e. the [[topological space|topological]] [[quotient space]] of the [[complement]] of zero in the $n+1$-fold [[Cartesian product]] of $\mathbb{K}$ by the right (say) [[multiplication]] [[action]] by the [[group of units]] $\mathbb{K}^\times \,=\, \mathbb{K} \setminus \{0\}$.

Notice the canonical [[topological subspace|subspace]] inclusion

$$
  \array{
    \mathbb{K}P^n
    &\hookrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big[
      z_0 \,:\, \cdots \,:\, z_n
    \big]
    &\mapsto&
    \big[
      z_0 \,:\, \cdots \,:\, z_n \,:\, 0
    \big]
    \,.
  }
$$

with induced [[complement]] $\mathbb{K}P^{n+1} \setminus \mathbb{K}P$ with [[topological boundary]]

$$
  \partial
  \big(
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P
  \big)
  \;\;
    \coloneqq
  \;\;
  \overline{
    \big(
      \mathbb{K}P^{n+1} \setminus \mathbb{K}P
    \big)
  }
  \setminus
  \big(
    \mathbb{K}P^{n+1} \setminus \mathbb{K}P
  \big)
  \,.
$$

## Statement

+-- {: .num_prop #CellStructureOfKProjectiveSpace} 
###### Proposition
**(cell structure of $\mathbb{K}$-projective space)**

We have a [[pushout diagram]] in [in topological spaces](Top#UniversalConstructions) of the form

$$
  \array{
    D^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) }
    &\longrightarrow&
    \mathbb{K}P^{n+1}
    \\
    \big\uparrow
    &{}_{^{(po)}}&
    \big\uparrow
    \\
    S^{ (n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K}) - 1 }
    &\longrightarrow&
    \mathbb{K}P^n
  }
$$

exhibiting $\mathbb{K}P^{n+1}$ as the result of an $(n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K})$-[[cell attachment]] to $\mathbb{K}P^{n}$ with [[attaching map]] the canonical projection

$$
  \array{
     S^{(n+1)\cdot dim_{{}_{\mathbb{R}}}(\mathbb{K})-1}
     \;\simeq\;
     \big(
       \mathbb{K}^{n+1} \setminus \{0\}
     \big) / \mathbb{R}_+^\times
     &\longrightarrow&
     \big(
       \mathbb{K}^{n+1} \setminus \{0\}
     \big) / \mathbb{K}^\times
     \;\simeq\;
     \mathbb{K}P^n
     \,.
  }
$$

=--

+-- {: .num_prop #CellStructureOfKProjectiveSpace} 
###### Corollary
**([[CW-complex]]-[[mathematical structure|structure]] on $\mathbb{K}$-[[projective spaces]])**

The $\mathbb{K}$-[[projective spaces]] appear in [[cotowers]]

$$
  \ast \,\simeq\,
  \mathbb{K}P^0
  \overset{\phantom{AAA}}{\hookrightarrow}
  \mathbb{K}P^1
  \overset{\phantom{AAA}}{\hookrightarrow}
  \mathbb{K}P^2
  \overset{\phantom{AAA}}{\hookrightarrow}
  \cdots
  \overset{\phantom{AAA}}{\hookrightarrow}
  \mathbb{K}P^\infty
$$

which at each stage $n$ exhibit [[CW-complex]]-[[mathematical structure|structure]] on $\mathbb{K}P^n$ with single cells in degree $k \cdot dim_{\mathbb{R}}(\mathbb{K})$.


=--

## Related statements

* [[zero-section into Thom space of universal line bundle is weak equivalence]]

## References

The case of [[octonionic projective space]]:

* {#Lackman19} [[Malte Lackmann]], Lemma 3.4 in: _The octonionic projective plane_ ([arXiv:1909.07047](https://arxiv.org/abs/1909.07047))

[[!redirects cell structure of projective space]]

[[!redirects cell structure of K-projective spaces]]
[[!redirects cell structure of K-projective space]]

