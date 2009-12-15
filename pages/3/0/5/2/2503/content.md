#Contents#

* automatic table of contents
{:toc}


## Idea

The string Lie 2-algebra is the [[infinitesimal object|infinitesimal approximation]] to the [[string 2-group]].

In the strict sense of the word, the String Lie 2-algebra $\mathfrak{string}(n)$ is a shifted [[L-infinity-algebra|∞-Lie algebra]] central extension

$$
  0 \to \mathbf{b} \mathfrak{u}(1) \to \mathfrak{string}(n)
  \to \mathfrak{so}(n) \to 0
$$

of the [[Lie algebra]] $\mathfrak{so}(n)$ by the [[L-infinity-algebra|Lie 2-algebra]] $\mathbf{b} \mathfrak{u}(1)$.

This central extension is controled by the canonical (up to normalization) [[Lie algebra cohomology|Lie algebra 3-cocycle]] $\mu$ on $\mathfrak{so}(n)$.

When $\mu$ is normalized such that it represents the image in [[deRham cohomology]] of the generator of the [[integral cohomology]] $H^3(X,Spin(n))$ then the corresponding String Lie 2-algebra is the Lie 2-algebra of the [[String Lie 2-group]].

More generally, for $\mathfrak{g}$ an [[L-infinity-algebra|∞-Lie algebra]] and $\mu \in CE(\mathfrak{g})$ an $\infty$-Lie algebra cocycle (a closed element in the [[Chevalley?Eilenberg algebra]] of $\mathfrak{g}$) of degree $k$, there is a corresponding shifted central extension

$$
  0 \to \mathbf{b}^{k-2} \mathfrak{u}(1) \to \mathfrak{g}_\mu  \to \mathfrak{g} \to 0
  \,.
$$

For instance the [[supergravity Lie 3-algebra]] is such an extension of the [[super Poincare Lie algebra]] by a [[super Lie algebra]] 4-cocycle.


## Definition

As with any [[L-∞ algebra]], we may define the String Lie 2-algebra $\mathfrak{string}(n)$ equivalently in terms of its [[Chevalley?Eilenberg algebra]].

Write $\mathfrak{g} := \mathfrak{so}(n)$ in the following. The [[Chevalley?Eilenberg algebra]] $CE(\mathfrak{g})$ of $\mathfrak{g}$ has a degree 3 element

$$
  \mu = \langle -, [-,-]\rangle 
  \,,
$$

well defined up to normalization ($\langle - , \rangle$ is the canonical bilinear symmetric invariant form on $\mathfrak{g}$ and $[-,-]$ the Lie bracket), which is closed

$$
  d_{\mathfrak{g}} \mu = 0
  \,.
$$

Hence this is the canonical (up to normalization) 3-cocycle in the [[Lie algebra cohomology]] of $\mathfrak{g}$.

The Chevalley--Eilenberg algebra of $\mathfrak{string}(n)$ is

$$
  CE(\mathfrak{string}(n)) = (\wedge^\bullet \mathfrak{g}^* \oplus \langle b\rangle, d_{\mathfrak{string}})
  \,,
$$

where 

* $b$ is a single new generator in degree 2;

* the differental $d_{\mathfrak{string}}$ coincides with $d_{\mathfrak{g}}$ on $\mathfrak{g}^*$:

  $$
    d_{\mathfrak{string}} |_{\mathfrak{g}^*} = d_{\mathfrak{g}}
  $$

* on the new generator it is defined by

  $$
    d_{\mathfrak{string}} : b \mapsto \mu
    \,.
  $$

That the differential defined this way is indeed of degree +1 and squares to 0 is precisely the fact that $\mu$ is a degree 3-cocycle of $\mathfrak{g}$.


## References

In one incarnation or other the String Lie 2-algebra has been considered in literature of [[dg-algebra]]s, but its [[Lie theory|Lie theoretic]] interpretation as a Lie 2-algebra has been made fully explicit only in

* [[John Baez]], [[Alissa Crans]], _Lie 2-algebras_ .

After its relation to the [[String Lie 2-group]] under [[Lie integration]] was established by  in

* Andr&#233; Henriques, _Integrating $L_\infty$-algebras_

and 

* Crans, Baez, Schreiber, Stevenson, _From loop groups to 2-groups_, 

it was reconsidered in a wider $\infty$-Lie theoretic context in 

* Sati, Schreiber, Stasheff, _$L_\infty$-algebra connections_

where also the relation to the [[supergravity Lie 3-algebra]] and other structures is discussed.


[[!redirects string Lie 2-algebra]]