
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

* [[special orthogonal Lie algebra]]

* **string Lie 2-algebra**

* [[fivebrane Lie 6-algebra]]

***


#Contents#

* automatic table of contents
{:toc}


## Idea

The _string Lie 2-algebra_ is the [[infinitesimal object|infinitesimal approximation]] to the [[Lie 2-group]] that is called the [[string 2-group]].

It is a shifted [[L-infinity-algebra|∞-Lie algebra]] central extension

$$
  0 \to \mathbf{b} \mathfrak{u}(1) \to \mathfrak{string}(n)
  \to \mathfrak{so}(n) \to 0
$$

of the [[Lie algebra]] $\mathfrak{so}(n)$ by the [[Lie 2-algebra]] $\mathbf{b} \mathfrak{u}(1)$ which is classified by the canonical (up to normalization) [[Lie algebra cohomology|Lie algebra 3-cocycle]] $\mu$ on $\mathfrak{so}(n)$, which may itself be understood as a morphism

$$
  \mu : \mathfrak{so}(n) \to b^2 \mathfrak{u}(1)
  \,.
$$

When $\mu$ is normalized such that it represents the image in [[deRham cohomology]] of the generator of the [[integral cohomology]] $H^3(X,Spin(n))$ of the [[Spin group]], then the [[Lie integration]] of the  String Lie 2-algebra is the [[String Lie 2-group]].


## Definition

We spell out first an explicit algebraic realization of the string Lie 2-algebra and then give its abstract definition as a [[homotopy fiber]] or [[principal ∞-bundle]].

### In components {#InComponents}

As with any [[L-∞ algebra]], we may define the String Lie 2-algebra $\mathfrak{string}(n)$ equivalently in terms of its [[Chevalley?Eilenberg algebra]].

There are various equivalent models we discuss a small one with a trinary bracket, and an infinite dimensional model which is however strict in that it comes from a [[differential crossed module]].

#### Skeletal model

Write $\mathfrak{g} := \mathfrak{so}(n)$ in the following. The [[Chevalley?Eilenberg algebra]] $CE(\mathfrak{g})$ of $\mathfrak{g}$ has a degree 3 element

$$
  \mu = \langle -, [-,-]\rangle 
  \,,
$$

well defined up to normalization ($\langle - ,- \rangle$ is the canonical bilinear symmetric [[invariant polynomial]] on $\mathfrak{g}$ and $[-,-]$ the Lie bracket), which is closed in $CE(\mathfrak{g})$

$$
  d_{\mathfrak{g}} \mu = 0
  \,.
$$

Hence this is the canonical (up to normalization) 3-cocycle in the [[Lie algebra cohomology]] of $\mathfrak{g}$.

The Chevalley--Eilenberg algebra of $\mathfrak{string}(n)$ is

$$
  CE(\mathfrak{string}(n)) = (\wedge^\bullet (\mathfrak{g}^* \oplus \langle b\rangle), d_{\mathfrak{string}})
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

One can equivalently describe the $L_\infty$-algebra structure of $\mathfrak{string}(n)$ in terms of lots of brackets 
$$
[-,-,\dots,-]_k:\wedge^k \mathfrak{string}(n)\to \mathfrak{string}(n),
$$
of degree $2-k$.
In addition to the Lie bracket of $\mathfrak{g}$, there is only a further nontrivial bracket: it is the 3-bracket
$$
[-,-,-]_3:\wedge^3 \mathfrak{g}\to \langle b\rangle^*
$$
given by
$$
[x,y,z]_3=\mu(x,y,z)\cdot \beta,
$$
where $\beta:\langle b\rangle\to\mathbb{R}$ is the dual of $b$.

#### Strict Lie 2-algebra model 

**Proposition** The string Lie 2-algebra given above is equivalent to the infinite-dimensional Lie 2-algebra coming from the [[differential crossed module]]

$$
  \hat \Omega \mathfrak{g} \to P \mathfrak{g}
$$

of the universal central extension of the [[loop Lie algebra]] mapping into the path Lie algebra, which acts on the former in the evident way.

This is proven in [BCSS](#BCSS).



### As a homotopy fiber {#AsHomotopyFiber}

Up to equivalence, the string Lie 2-algebra is the [[homotopy fiber]] of the cocycle $\mu : \mathfrak{so}(n) \to \mathbf{b}^2 \mathfrak{u}(1)$, hence is the canonical $\mathbf{b} \mathfrak{u}(1)$-[[principal ∞-bundle]] over $\mathfrak{so}(n)$.

Here we take by definition the [[(∞,1)-category]] of [[∞-Lie algebroid]]s to be that [[presentable (∞,1)-category|presented]] by the opposite (after passing to [[Chevalley-Eilenberg algebra]]s) of the [[model structure on dg-algebra]]s. In terms of dg-algebras, the cocycle is dually a morphism

$$
  CE(\mathfrak{so}(n)) \leftarrow CE(\mathbf{b}^2 \mathfrak{u}(1)) : \mu
$$ 

and the [[homotopy fiber]] in question is dually modeled by the [[homotopy pushout]] 

$$
  \array{
    && 0
    \\
    && \uparrow
    \\
    CE(\mathfrak{so}(n)) &\stackrel{\mu}{\leftarrow}&
    CE(\mathbf{b}^2 \mathfrak{u}(1))
  }
  \,.
$$

By the general rules for computing [[homotopy pushout]]s, this may be computed by an ordinary [[pushout]] if we choose a  [[resolution]] of $CE(\mathbf{b}^2 \mathfrak{u}(1)) \to 0$ by a cofibration and ensure that all three objects in the pushout diagram are cofibrations.

For the resolution we take the standard one by the CE-algebra of the $\mathbf{b}^2 \mathfrak{u}(1)$-[[universal principal ∞-bundle]] $\mathbf{e b} \mathfrak{u}(1)$, which is the dg-algebra

$$
  CE(\mathbf{e b} \mathfrak{u}(1)) = (\wedge^\bullet( \langle b\rangle \oplus \langle c\rangle ), d)
$$

where $b$ is a generator of degree 2, $c$ one of degree 3 and the differential is given by

$$
  d b = c
$$

and 

$$
  d c = 0
  \,.
$$

The morphism $CE(\mathbf{b}^2 \mathfrak{u}(1)) \to CE(e b \mathfrak{u}(1))$ is the one that identifies the two degree-3 generators.

Now $CE(\mathbf{b}^2 \mathfrak{u}(1))$ and $CE(\mathbf{e b} \mathfrak{u}(1))$ are [[Sullivan algebra]]s, hence are cofibrant objects in the [[model structure on dg-algebra]]s. The dg-algebra $CE(\mathfrak{g})$ is not quite a Sullivan algebra, but almost: it is a [[semifree dga]] and only fails to have the filtering property on the differential.  This is sufficient for computing the desired [[homotopy fiber]], as discussed at <a href="http://ncatlab.org/nlab/show/infinity-Lie+algebra+cohomology#Extensions">∞-Lie algebra cohomology -- Extensions</a>.


One observes now that 

$$
  \array{
    CE(\mathfrak{string}) &\leftarrow& CE(\mathbf{e b} \mathfrak{u}(1))
    \\
    \uparrow && \uparrow
    \\
    CE(\mathfrak{so}(n)) &\leftarrow& CE(\mathbf{b}^2 \mathfrak{u}(1))
  }
$$

is a [[pushout]] diagram.  Dually, this exhibits $\mathfrak{string}$ as the [[(∞,1)-pullback]]

$$
  \array{
    \mathfrak{string}(n) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathfrak{so}(n) &\stackrel{\mu}{\to}& \mathbf{b}^2 \mathfrak{u}(1)
  }
  \,.
$$

And this may be taken to be the abstract definition of the string Lie 2-algebra.

By the general logic of [[fiber sequence|fiber sequences]] this implies that also

$$  
  \mathbf{b} \mathfrak{u}(1) \to \mathfrak{string} \to \mathfrak{so}(n)
$$

is a fiber sequence. By analogous reasoning as before, we see that this is modeled by the ordinary pushout

$$
  \array{
    CE(\mathbf{b} \mathfrak{u}(1)) &\leftarrow& *
    \\
    \uparrow && \uparrow
    \\
    CE(\mathfrak{string}) &\leftarrow& CE(\mathfrak{g})
  }
  \,.
$$

This is indeed a homotopy pushout even without resolving the point, because $CE(\mathfrak{string}) \leftarrow CE(\mathfrak{g})$ is already a cofibration, being the pushout of a cofibration by the above.

## Generalizations

More generally, for $\mathfrak{g}$ an [[L-infinity-algebra|∞-Lie algebra]] and $\mu \in CE(\mathfrak{g})$ an $\infty$-Lie algebra cocycle (a closed element in the [[Chevalley?Eilenberg algebra]] of $\mathfrak{g}$) of degree $k$, there is a corresponding shifted central extension

$$
  0 \to \mathbf{b}^{k-2} \mathfrak{u}(1) \to \mathfrak{g}_\mu  \to \mathfrak{g} \to 0
  \,.
$$

For instance the [[supergravity Lie 3-algebra]] is such an extension of the [[super Poincare Lie algebra]] by a [[super Lie algebra]] 4-cocycle.



## References

In one incarnation or other the String Lie 2-algebra has been considered in literature of [[dg-algebra]]s, but its [[Lie theory|Lie theoretic]] interpretation as a Lie 2-algebra has been made fully explicit only in

* [[John Baez]], [[Alissa Crans]], Higher-dimensional Algebra V: Lie 2-algebras, _Theory and Applications of Categories_ **12** (2004), 492-528.  ([web](http://www.tac.mta.ca/tac/volumes/12/15/12-15abs.html))
([arXiv:math.QA/0307263](http://arxiv.org/abs/math.QA/0307263))

In 

* [[Andre Henriques]], _Integrating $L_\infty$-algebras_ ([arXiv:0603563](http://arxiv.org/abs/math/0603563))

the string Lie 2-algebra is integrated to the [[string 2-group]] using the general abstract method described at [[Lie integration]]. 

In

* [[John Baez]], [[Alissa Crans]], [[Urs Schreiber]] and [[Danny Stevenson]], From loop groups to 2-groups, _Homotopy, Homology and Applications_ **9** (2007), 101-135.  ([arXiv:math.QA/0504123](http://arxiv.org/abs/math.QA/0504123)) 
  {#BCSS}

the equivalent strict model given by a differential crossed module is found, which is then integrated termwise as ordinary Lie algebras to a [[crossed module]] of Frechet-Lie groups, hence to a Lie [[strict 2-group]] model of the String Lie 2-group.

The string Lie 2-algebra is also considered in a certain context in 

* Sati, Schreiber, Stasheff, _$L_\infty$-algebra connections_

where also the relation to the [[supergravity Lie 3-algebra]] and other structures is discussed.

The super-$L_\infty$-version of the string $L_\infty$-algebra was considered in

* [[John Baez]], [[John Huerta]], _Division Algebras and Supersymmetry II_ ([arXiv:1003.3436](http://arxiv.org/abs/1003.3436)).

See also [[division algebra and supersymmetry]].

[[!redirects string Lie 2-algebra]]