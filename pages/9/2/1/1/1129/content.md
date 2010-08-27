
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* toc
{: toc}

## Definition

There is a very general notion of _injective objects_ in a [[category]] $C$, and a sequence of refinements as $C$ is equipped with more [[stuff, structure, property|structure and property]], in particular for $C$ an [[abelian category]] [[additive and abelian categories|or a relative]] thereof.

### General definition 

Let $C$ be a [[category]] and $J$ a collection of morphisms in $C$.  Frequently $J$ is the class of all [[monomorphism]]s or a related class.  An object $I$ in $C$ is **$J$-injective** if all diagrams

$$
  \array{
    X &\to& I
    \\
    {}^{\mathllap{j \in J}}\downarrow 
    \\
    Z
  }
$$

admit an extension

$$
  \array{
    X &\to& I
    \\
    {}^{\mathllap{j \in J}}\downarrow & \nearrow_{\mathrlap{\exists}}
    \\
    Z
  }
  \,.
$$

If $C$ has a [[terminal object]] $*$ this can be thought of as a lift

$$
  \array{
    X &\to& I
    \\
    {}^{\mathllap{j \in J}}\downarrow & \nearrow_{\mathrlap{\exists}}
    &
    \downarrow
    \\
    Z
    &\to&
    *
  }
$$

as for [[weak factorization system|factorization systems]].

If $C$ is a [[locally small category]] then $I$ is $J$-injective precisely if the [[hom-functor]]

$$
  Hom_C(-,I) : C^{op} \to Set
$$

takes morphisms in $J$ to [[epimorphism]]s in [[Set]].

If $J$ is the class of all monomorphisms, we speak merely of an **injective object**.  We say that a category $C$ has **enough injectives** if every object admits a monomorphism into an injective object.

The dual notion is a [[projective object]].


### In abelian categories 

The term _injective object_ is used most frequently in the context that $C$ is an [[abelian category]].  In this case the class $J$ of monomorphisms is the same as the class of morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is [[exact sequence|exact]].  An [[object]] $I$ of an abelian category $C$ is then **injective** if it satisfies the following equivalent conditions:

* the [[hom-functor]] $Hom_C(-, I) : C^{op} \to Set$ is [[exact functor|exact]];

* for all [[morphism]]s $f : X \to Y$ such that $0 \to X \to Y$ is [[exact sequence|exact]] and for all $k : X \to I$, there exists $h : Y \to I$ such that $ h\circ f = k$.

$$
  \array{
    0 &\to& X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{\mathrlap{k}} & \swarrow_{\mathrlap{\exists h}}
    \\
    &&
    I 
  }
  \,.
$$

### In chain complexes

See [[homotopically injective object]] for a relevant generalization to categories of chain complexes, and its relationship to ordinary injectivity.


## Examples

### Injective modules

Let $R$ be a [[commutative ring]] and  $C = R Mod$ the category of $R$-[[module]]s.

**Proposition** (Baer's criterion)
{#Baer}

An object $N \in R Mod$ is injective precisely if for $I$ any left $R$-ideal regarded as an $R$-module, and morphism $g : I \to N$ in $C$ can be extended to all of $R$ along the inclusion $I \hookrightarrow R$.

### Injective abelian groups

Let $C = \mathbb{Z} Mod \simeq $ [[Ab]]  be the abelian category of abelian groups. 

Using [Baer's criterion](#Baer) one finds that

**Proposition** An abelian group $A$ is injective precisely if it is a [[divisible group]], in that for all [[integer]]s $n \in \mathbb{N}$ we have $n G = G$.

So in particular the group of [[rational number]]s $\mathbb{Q}$ is injective in [[Ab]], as is the additive group of [[real number]]s $\mathbb{R}$ and generally that underlying any [[field]]. The additive group underlying any [[vector space]] is injective. The [[quotient]] of any injective group by any other group is injective.

_Not_ injective in [[Ab]] is for instance the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ for $n \gt 1$.

### Existence of enough injectives

* Every [[topos]] has enough injectives.  In fact, every [[power object]] can be shown to be injective, and every object embeds into its power object by the "singletons" map.

* At least assuming some form of the [[axiom of choice]], the category of [[abelian groups]] has enough injectives.  Full AC is much more than required, however; [[small violations of choice]] suffices.  The abelian category of [[modules]] over some [[ring]] is similar.

* The category of abelian [[sheaves]] on any small [[site]] also has enough injectives.  This is in stark contrast to the situation for projectives, which generally do not exist in categories of sheaves.


## References

Much of this discussion can be found in 

* Kashiwara-Schapira, _[[Categories and Sheaves]]_

The general notion of injective objects is in section 9.5, the case of injective complexes in section 14.1.
