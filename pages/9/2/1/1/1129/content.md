
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

Let $C$ be a [[category]] and $J \subset Mor(C)$ a [[class]] of [[morphism]]s in $C$.  

+-- {: .un_example}
###### Example

Frequently $J$ is the class of all [[monomorphism]]s or a related class.  

This is notably the case for  $C$ is a [[category of chain complexes]] equipped with the injective [[model structure on chain complexes]] and $J$ is its class of cofibrations.

=--

+-- {: .un_def}
###### Definition


An object $I$ in $C$ is **$J$-injective** if all diagrams of the form

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

If $J$ is the class of all [[monomorphism]]s, we speak merely of an **injective object**.  

We say that a category $C$ has **enough injectives** if every object admits a monomorphism into an injective object.


=---

The dual notion is a [[projective object]].

+-- {: .un_remark}
###### Remark


If $C$ has a [[terminal object]] $*$ then these extensions are equivalently 
lifts

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

and hence the $J$-injective objects are precisely those that have the [[left lifting property]] against the class $j$.

=--

+-- {: .un_remark}
###### Remark

If $C$ is a [[locally small category]] then $I$ is $J$-injective precisely if the [[hom-functor]]

$$
  Hom_C(-,I) : C^{op} \to Set
$$

takes morphisms in $J$ to [[epimorphism]]s in [[Set]].

=--



### In abelian categories 

The term _injective object_ is used most frequently in the context that $C$ is an [[abelian category]].  

+-- {: .un_lemma}
###### Observation


For $C$ an [[abelian category]] the class $J$ of monomorphisms is the same as the class of morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is [[exact sequence|exact]].  

=--

+-- {: .proof}
###### Proof

By definition of [[abelian category]] every monomorphism $A \hookrightarrow B$ is a [[kernel]], hence a [[pullback]] of the form

$$
  \array{
    A &\to& 0
    \\
    \downarrow && \downarrow
    \\
    B &\to& C
  }
$$

for $0$ the [[zero object]]. By the <a href="http://ncatlab.org/nlab/show/pullback#Pasting">pasting law</a> for pullbacks we find that also the left square in 

$$
  \array{
    0 &\to& A &\to& 0
    \\
    \downarrow && \downarrow && \downarrow
    \\
    0 &\to& B &\to& C
  }
$$

is a pullback, hence $0 \to A \to B$ is exact.

=--

+-- {: .un_corollary}
###### Corollary

An [[object]] $I$ of an abelian category $C$ is then **injective** if it satisfies the following equivalent conditions:

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

=--

### In chain complexes

See [[homotopically injective object]] for a relevant generalization to categories of chain complexes, and its relationship to ordinary injectivity.


## Examples

### Injective modules

Let $R$ be a [[commutative ring]] and  $C = R Mod$ the category of $R$-[[module]]s.

**Proposition** (Baer's criterion)
{#Baer}

An object $N \in R Mod$ is injective precisely if for $I$ any left $R$-ideal regarded as an $R$-module, any morphism $g : I \to N$ in $C$ can be extended to all of $R$ along the inclusion $I \hookrightarrow R$.

### Injective abelian groups

Let $C = \mathbb{Z} Mod \simeq $ [[Ab]]  be the abelian category of abelian groups. 

Using [Baer's criterion](#Baer) one finds that

**Proposition** An abelian group $A$ is injective precisely if it is a [[divisible group]], in that for all [[integer]]s $n \in \mathbb{N}$ we have $n G = G$.

So in particular the group of [[rational number]]s $\mathbb{Q}$ is injective in [[Ab]], as is the additive group of [[real number]]s $\mathbb{R}$ and generally that underlying any [[field]]. The additive group underlying any [[vector space]] is injective. The [[quotient]] of any injective group by any other group is injective.

_Not_ injective in [[Ab]] is for instance the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ for $n \gt 1$.

### Existence of enough injectives

* Every [[topos]] has enough injectives.  In fact, every [[power object]] can be shown to be injective, and every object embeds into its power object by the "singletons" map.

* At least assuming some form of the [[axiom of choice]], the category of [[abelian groups]] has enough injectives.  Full AC is much more than required, however; [[small violations of choice]] suffices.

* As soon as the category of abelian groups has enough injectives, so does the [[abelian category]] of [[modules]] over some [[ring]] $R$.  To see this, observe that the forgetful functor $U\colon R Mod \to AbGp$ has both a [[left adjoint]] $R_!$ ([[extension of scalars]] from $\mathbb{Z}$ to $\mathbb{R}$) and a right adjoint $R_*$ ([[coextension of scalars]]).  Since it has a left adjoint, it is [[exact functor|exact]], and so its right adjoint $R_*$ preserves injective objects.  Thus given any $R$-module $M$, we can embed $U(M)$ in an injective abelian group $I$, and then $M$ embeds in $R_*(I)$.

* The category of abelian [[sheaves]] on any small [[site]] also has enough injectives.  (This is in stark contrast to the situation for projectives, which generally do not exist in categories of sheaves.)  A proof of this can be found in [[Peter Johnstone]]'s book *Topos Theory*, p261.

* Combining the last fact with the penultimate one (which relativizes to any topos), we find that the category of modules over any [[sheaf of rings]] on any small site also has enough injectives.  This slick proof of this important fact was pointed out by Colin McLarty in an email to the categories list dated 10 Oct 2010.


## References

A general discussion can be found in 

* Kashiwara-Schapira, _[[Categories and Sheaves]]_

The general notion of injective objects is in section 9.5, the case of injective complexes in section 14.1.

Using tools from the theory of [[accessible categories]], injective objects are discussed in

* [[Jiri Rosicky]], _Injectivity and accessible categories_ ([ps](http://www.math.muni.cz/~rosicky/papers/acc5.ps))

[[!redirects injective objects]]