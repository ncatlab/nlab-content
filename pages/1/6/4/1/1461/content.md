
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _strict morphism_ is a [[morphism]] for which the notion of [[regular image]] and [[regular coimage]] coincide.


Compare with [[strict epimorphism]].

## Definition

### In a category with limits and colimits 

Let $C$ be a category with finite [[limits]] and [[colimits]]. Let $f : c \to d$ be a [[morphism]] in $C$.

Recall that the [[regular image]] of $f$ is the [[limit]] 

$$
  Im f \simeq lim( d \rightrightarrows d \sqcup_c d )
  \,,
$$

i.e. the [[equalizer]] of $d \rightrightarrows d \sqcup_c d$,

while the [[regular coimage]] is the [[colimit]]

$$
  Coim f \simeq colim( c \times_d c \rightrightarrows c)
  \,.
$$

By the various universal properties, there is a unique morphism 

$$
  u : Coim f \to Im f
$$

such that

$$
  \array{
      c &\stackrel{f}{\to}& d
      \\
      \downarrow && \uparrow
      \\
      Coim f &\stackrel{u}{\to}& Im f
  }
  \,.  
$$

The morphism $f$ is called a **strict morphism** if $u$ is an [[isomorphism]].



## Examples

Examples of categories in which _every_ morphism is strict include

* [[Set]];
* the category $Mod(R)$ of [[modules]] over a [[ring]] $R$;
* the category $PSh(C) = [C^{op},Set]$ of [[presheaf|presheaves]] on any [[small category]] $C$;
* any [[abelian category]];
* any [[topos]].

[[!redirects strict morphisms]]