
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc} 

## Idea

A generalization of the notion of [[foliation]] of a [[smooth manifold]] from manifolds to [[Lie algebroids]].

## Definition

One of several equivalent definitions of a (regular) foliation of a smooth manifold is

+-- {: .num_defn}
###### Definition

A [[regular foliation]] of a [[smooth manifold]] $X$ is a wide sub-[[Lie algebroid]] of its [[tangent Lie algebroid]], hence a [[Lie algebroid]] $\mathcal{P}$ over $X$ with [[injection|injective]] [[anchor map]]

$$
  \array{
    \mathcal{P} &\hookrightarrow & T X 
    \\
    \downarrow && \downarrow
    \\
    X &=& X
  } 
  \,.
$$

=--

In this spirit there is an evident generalization of the notion to a notion of foliations of Lie algebroids.

+-- {: .num_defn #Foliation}
###### Definition

A (regular) **foliation of a Lie algebroid** $A$ is a sub-[[double Lie algebroid]] of the tangent double Lie algebroid which is wide over $A$

$$
  \array{
    \mathcal{P} &\hookrightarrow& T A
    \\
    \downarrow && {}^{\mathllap{d p_A}}\downarrow & \searrow^{\mathrlap{p_{T A}}}
    \\
    \mathcal{P}_0 &\hookrightarrow& T X && A
    \\
    && & \searrow & \downarrow^{\mathrlap{p_A}}
    \\
    && && X
  }
  \,.
$$

=--

+-- {: .num_prop #CharacterizationByTriple}
###### Proposition

Foliations of a Lie algbroid $A \to X$ according to def. \ref{Foliation} are in natural [[bijection]] to the following data:

1. an ordinary [[foliation]] $\mathcal{P}_0 \hookrightarrow T X$

1. $\mathcal{P}_1 \hookrightarrow A$ a sub-[[vector bundle]] 

   (this is the joint [[kernel]] $\mathcal{P}_1 = ker(p_{T A}) \cap ker(d p_{A})$ naturally identified as a subspace of $A$)

1. $\nabla$ a [[flat connection]] on the [[quotient]] bundle $A/\mathcal{P}_1$ partially defined over [[vector fields]] in $\mathcal{P}_0$ 

   (this is the induced linear foliation of the total space $A$ regarded as a horizontal-subspace distribution) 

such that over every [[open subset]] $U \hookrightarrow X$

1. The [[sections]] of $A$ that become $\nabla$-[[covariant derivative|constant]] in $A/\mathcal{P}_1$ form a sub-[[Lie algebra]] of $\Gamma_U(A|_U)$ (an [[integrable distribution of subspaces]]);

1. the sections of $\mathcal{P}_1$ are a Lie ideal inside this sub-Lie algebra;

1. the [[image]] of $\mathcal{P}_1$ under the [[anchor map]] is in $\mathcal{P}_0$;

1. the quotiented [[anchor map]] $A/\mathcal{P}_1 \to T X / \mathcal{P}_0$ intertwines $\nabla$ with the $\mathcal{P}_0$-[[Bott connection]].

=--

This is ([EH, theorem 7.2](#EH)).


+-- {: .num_remark}
###### Remark

According to prop. \ref{CharacterizationByTriple} the notion of foliation of a Lie algebroid generalizes the notion of _ideal system_ of a Lie algebroid ([Higgins-Mackenzie](#HM), [Mackenzie](#Mackenzie)): A foliation as in def. \ref{Foliation} comes from an ideal system in this sense precisely of $\mathcal{P}_0$ is a [[simple foliation]] (the quotient map exists in smooth manifolds and is a [[surjective submersion]]) and the [[holonomy]] of $\nabla$ is trivial.

=--


## Examples

+-- {: .num_example}
###### Example

Let $\mathcal{G}_\bullet$ be a [[Lie groupoid]] and let

$$
  \array{
    \mathcal{P} &\hookrightarrow& T \mathcal{G}_1
    \\
    \downarrow\downarrow && {}^{\mathllap{d s}}\downarrow \downarrow^{\mathrlap{d t}}
    \\
    \mathcal{P}_0 &\hookrightarrow& T \mathcal{G}_0
  }
$$

be a [[foliation of a Lie groupoid]], regarded as an [[internal groupoid]] in [[Lie algebroids]]. Then applying [[Lie differentiation]] yields a foliation of the Lie algebroid $Lie(\mathcal{G}_\bullet)$.

=--


## Related concepts

* [[foliation of a Lie groupoid]]

* [[exterior differential system]]

## Referemces

Maybe the first discussion of foliations of Lie algebroids appears in 

* {#EH} Eli Hawkins, _A Groupoid Approach to Quantization_ ([arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363)) 
 

Ideal systems of Lie algebroids have been introduced and studied in

* {#HM} [[Philip Higgins]], [[Kirill Mackenzie]], _Algebraic constructions in the category of Lie algebroids_ . J. Algebra
129 (1990), no. 1, 194&#8211;230.MR1037400
 

* {#Mackenzie} [[Kirill Mackenzie]], _General theory of Lie groupoids and Lie algebroids_ Cambridge Univ. Press, Cambridge (2005)
 

Related discussion is in

* [[Cristian Ortiz]], _Multiplicative Dirac structures_ ([arXiv:1212.0176](http://arxiv.org/abs/1212.0176))


[[!redirects foliations of a Lie algebroid]]
[[!redirects foliations of Lie algebroids]]
