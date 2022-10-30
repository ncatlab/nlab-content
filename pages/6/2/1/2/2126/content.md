
<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

The **singular cohomology** of a [[topological space]] $X$ is the [[cohomology]] in [[∞Grpd]] of its [[fundamental ∞-groupoid]] $\Pi(X)$:

for $\mathcal{B}^n \mathbb{Z} \in \infty Grpd$ the [[Eilenberg-MacLane object]] with the group $\mathbb{Z}$ in degree $n$, the degree $n$-singular cohomology of $X$ is

$$
  H^n(X,\mathbb{Z}) := \pi_0 \infty Grpd(\Pi(X), \mathcal{B}^n \mathbb{Z})
  \,.
$$


With $\infty Grpd$ [[presentable (∞,1)-category|presented]] by the category [[sSet]] of [[simplicial set]]s, the fundamental $\infty$-groupoid $\Pi(X)$ is modeled by the [[Kan complex]] 

$$
  \Pi(X) = Sing X = Hom_{Top}(\Delta^\bullet_{Top}, X)
  \,,
$$

the [[singular simplicial complex]] of $X$. 

The object $\mathcal{B}^n \mathbb{Z}$ is usefully modeled by the simplicial set 

$$
  \mathcal{B}^n \mathbb{Z} = U (\Xi \mathbb{Z}[n])
$$

which is 

* the underlying simplicial set under the [[forgetful functor]] 

  $$
    (F \dashv U)
    sAb \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
    sSet
  $$

  from abelian [[simplicial group]]s to [[simplicial sets]];

* of the abelian [[simplicial group]] $\Xi \mathbb{Z}[n]$ which is the image under the [[Dold-Kan correspondence]]

  $$
    sAb \stackrel{\overset{\Xi}{\leftarrow}}{\underset{}{\to}}
    Ch^+
  $$

* of the [[chain complex]]

  $$
    \mathbb{Z}[n] =
    (\cdots \to \mathbb{Z} \to 0 \to 0 \to \cdots \to 0)
  $$

  concentrated in degree $n$.

So in this model we have

$$
  H^n(X,\mathbb{Z}) = \pi_0 sSet(Sing X, U(\Xi \mathbb{Z}[n]))
  \,.
$$

A [[cocycle]] in this cohomology theory is a [[cochain on a simplicial set]], on the singular complex $Sing X$.

Using the [[adjunction]] $(F \dashv U)$ this is [[isomorphism|isomorphic]] to

$$
  \cdots \simeq \pi_0 sAb( Ch_n(X), \Xi \mathbb{Z}[n] )
  \,,
$$

where 

$$
  F(Sing X) = \mathbb{Z}[Sing X]
$$

is the [[free functor|free]] abelian simplicial group on the simplicial set $Sing X$: this is the simplicial abelian group of **singular chains** of $X$. Its elements are formal sums of continuous maps $\Delta^n_{Top} \to X$. In this form

$$
  \cdots \simeq \pi_0 sAb( \mathbb{Z}[Sing X], \Xi \mathbb{Z}[n] )
  \,.
$$

Using next the [[Dold-Kan correspondence|Dold-Kan adjunction]] this is

$$
  \cdots \simeq H_0 Ch( Ch_\bullet(X), \mathbb{Z}[n] )
  \,,
$$

where

$$
  Ch_\bullet(X) := N^\bullet(\mathbb{Z}(Sing X))
$$

is the [[Moore complex]] of normalized chains of $\mathbb{Z}[Sing X]$: this is the complex of **singular chains**, formal sums over $\mathbb{Z}$ of simplices in $X$.


This way singular cohomology is the abelian dual of [[singular homology]].

...



## Related concepts

* [[cochain on a simplicial set]]

* [[cup product]]

* [[de Rham theorem]]


## Discussion

A previous version of this entry led to the following discussion, which later led to extensive discussion by email. Partly as a result of this and similar discussions, there is now more information on how Kan complexes _are_ $\infty$-groupoids at 

* [[Kan complex]]

* [[∞-groupoid]].

+-- {: .query}

_[[RonnieBrown]]_ Query: Why is the notation $\Pi(X)$ used here? The old notation $S(X)$ or $S^\Delta(X)$ is perfectly clear. The notation $\Pi(X)$ suggests it is some kind of $\infty$-groupoid, but the precise statement of such properties are unclear, and it conflicts with older use of $\Pi$ where some homotopy classes are taken in a more structured situation (filtered spaces, $n$-cubes of spaces) to give well defined strict structures closely related to classical construtions (relative homotopy groups, $n$-adic homotopy groups). 

There should also be some analysis of why globular or simplicial constructions are used rather than cubical ones. 
The case needs to be made, as this analysis of aims is useful. 

[[Urs Schreiber]]: I believe that [[Toby Bartels|Toby]] copied material which I typed elsewhere, so this is my fault. But I have adopted the habit of writing $\Pi(X)$ instead of $S(X)$, because the singular complex $S(X)$ _is_ the fundamental $\infty$-groupoid in its Kan complex incarnation. I find it conceptually very useful to make that explicit and I felt like here on the $n$Lab I can allow myself to do this. But I am prepared to be outvoted. In any case, we should certainly have a discussion of the notation and certainly of the different models: globular, simplicial, cubical. 

I'd do it myself if I had the time right now, but I have to run. Sorry.

=--

