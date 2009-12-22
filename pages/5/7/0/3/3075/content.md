<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
***
[[!include homotopy - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The _mapping cocone_, also called the _mapping path space_, of a morphism $f : A \to C$, with $C$ a [[pointed object]], is a particular [[model category]] realization of the [[homotopy fiber]] of $f$, i.e. of the [[homotopy pullback]]

$$
  \array{
    Cocone(f) &\to& A
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    {*} &\to& C
  }
$$

of the point along $f$.

The concept is [[duality|dual]] to that of [[mapping cone]]. 

Mapping co-cones are realized in terms of _mapping cocyclinders, as described below. These typically play the role of [[generalized universal bundle]]s.

## Definition

Under sufficiently nice conditions (...spell out...), the [[homotopy pullback]]

$$
  \array{
    Cocone(f) &\to& A
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    {*} &\to& C
  }
$$

may be computed as the ordinary [[limit]] over the diagram

$$
  \array{
    && && A
    \\
    &&&& \downarrow^{\mathrlap{f}}
    \\
    &&C^I &\to& C
    \\
    && \downarrow
    \\
    {*} &\to& C
  }
  \,,
$$

where $C^I$ is a [[path space object]] of $C$. This, in turn, may be computed as two consecutive ordinary [[pullback]]s. The first one

$$
  \array{
    && \mathbf{E}_f C &\to& A
    \\
    && \downarrow && \downarrow^{\mathrlap{f}}
    \\
    &&C^I &\to& C
    \\
    && \downarrow
    \\
    {*} &\to& C
  }
$$

yields the **mapping cocylinder** $\mathbf{E}_f C$. This is the kind of object discussed at [[generalized universal bundle]]. The second pullback then produces the mapping cocone

$$
  \array{
    Cocone(f)  &\to& \mathbf{E}_f C &\to& A
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{f}}
    \\
     &&C^I &\to& C
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& C
  }
  \,.
$$

## Examples


### Principal bundles

In the category [[Top]] of [[topological space]]s, let $G$ be group and $\mathcal{B}G$ its [[classifying space]], and let $f : X \to \mathcal{B}G$ be a morphism. Then 

* the mapping coylinder of ${* }\to \mathcal{B}G$ is the universal $G$-bundle;

* the mapping cocone of $X \to \mathcal{B}G$ is the $G$-principal bundle $P \to X$ classified by $f$:

  $$
    \array{
      P  &\to& \mathcal{E} G &\to& {*}
      \\
      \downarrow && \downarrow && \downarrow^{}
      \\
       &&(\mathcal{B}G)^I &\to& \mathcal{B}G
      \\
      \downarrow && \downarrow
      \\
      X &\stackrel{f}{\to}& \mathcal{B}G
    }
    \,.
  $$

## Note on terminology {#Terminology}

Whitehead complained about the term _cocone_ back in the old days, because of the seeming (though false) double dualization, so he used _mapping path space_ . This practice was followed by his school (in most of US for example). But he himself was not confident in that terminology. For example there is a table in his book where he lists the dual notions and at the place where mapping cocone/mapping path space should fit he puts just the symbol for the construction while on the dual side he puts the whole name. Similarily for the mapping cocylinder.

Somebody -- maybe [[Samuel Eilenberg]] -- (-- check --) suggested to Whitehead to use _ne_ insteaad of _cocone_ , jokingly cancelling one _co_ against the other, as if both expressed abstract [[duality]].

Postnikov uses the term _mapping cocylinder_ , while for on Whitehead's complaint he comments: 

> we do not see a particular criminal in the cocone terminology, but will anyway not use it.


[[!redirects mapping cocylinder]]
[[!redirects mapping path space]]