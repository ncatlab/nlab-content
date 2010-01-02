* toc
{: toc}

#Definition#

There is a very general notion of _injective objects_ in a category $C$, and a sequence of refinements as $C$ is equipped with more [[stuff, structure, property|structure and property]], in particular for $C$ an [[abelian category]] [[additive and abelian categories|or a relative]].

## General definition ##

Let $C$ be a [[category]] and $J$ a collection of morphisms in $C$.  Frequently $J$ is the class of all [[monomorphism]]s or a related class.  An object $I$ in $C$ is **$J$-injective** if all diagrams

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} 
    \\
    Z
  }
$$

admit an extension

$$
  \array{
    X &\to& I
    \\
    \downarrow^{j \in J} & \nearrow_{\exists}
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
    \downarrow^{j \in J} & \nearrow_{\exists}
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


## In abelian categories ##

The term _injective object_ is used most frequently in the context that $C$ is an [[abelian category]].  In this case the class $J$ of monomorphisms is the same as the class of morphisms $f : X \to Y$ such that $0 \to X \stackrel{f}{\to} Y$ is [[exact sequence|exact]].  An [[object]] $I$ of an abelian category $C$ is then **injective** if it satisfies the following equivalent conditions:

* the [[hom-functor]] $Hom_C(-, I) : C^{op} \to Set$ is [[exact functor|exact]];

* for all [[morphism]]s $f : X \to Y$ such that $0 \to X \to Y$ is [[exact sequence|exact]] and for all $k : X \to I$, there exists $h : Y \to I$ such that $ h\circ f = k$.

$$
  \array{
    0 &\to& X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^k & \swarrow_{\exists h}
    \\
    &&
    I 
  }
  \,.
$$

## In chain complexes

See [[homotopically injective object]] for a relevant generalization to categories of chain complexes, and its relationship to ordinary injectivity.


# Examples

* Every [[topos]] has enough injectives.  In fact, every [[power object]] can be shown to be injective, and every object embeds into its power object by the "singletons" map.

* At least assuming some form of the [[axiom of choice]], the category of [[abelian groups]] has enough injectives.  Full AC is much more than required, however; [[small violations of choice]] suffices.  The abelian category of [[modules]] over some [[ring]] is similar.

* The category of abelian [[sheaves]] on any small [[site]] also has enough injectives.  This is in stark contrast to the situation for projectives, which generally do not exist in categories of sheaves.


#References#

Much of this discussion can be found in 

* Kashiwara--Schapira, [[Categories and Sheaves]]

The general notion of injective objects is in section 9.5, the case of injective complexes in section 14.1.
