
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An ordinary [[vielbein]]/[[orthogonal structure]] is a [[reduction of structure groups|reduction of the structure group]] of the [[tangent bundle]] of a [[smooth manifold]] from the [[general linear group]] $GL_n$ to its [[maximal compact subgroup]], the [[orthogonal group]].

Accordingly, whenever we have a [[reduction of structure groups]] along the inclusion $H \hookrightarrow G$ of a [[maximal compact subgroup]], we may speak of a _generalized vielbein_. 

## Definition

Let $G$ be a [[Lie group]] and let $H \hookrightarrow G$ be the inclusion of a [[maximal compact subgroup]]. Write 

$$
  i : \mathbf{B}H \to \mathbf{B}G
$$ 

for the induced morphism of [[smooth infinity-groupoid|smooth]] [[moduli stacks]] of [[principal bundles]].

Notice that 

1. these form a bundle

  $$
    \array{
      G/H &\to& \mathbf{B}H
      \\
      && \downarrow^{\mathrlap{i}}
      \\
      && \mathbf{B}G
    }
  $$

  exhibiting the [[coset]] $G/H$ as the [[homotopy fiber]] of $i$;

1. under [[geometric realization]] $i$ becomes an [[weak homotopy equivalence|equivalence]] 

   $$
     {\vert i\vert}  : {\vert \mathbf{B} H\vert} = B H \simeq B G = {\vert \mathbf{B}G\vert}
   $$

Then for $X$ a [[smooth manifold]] or more generally a [[smooth infinity-groupoid]] equiped with a map $g : X \to \mathbf{B}G$ an _$i$-generalized vielbein_ is a lift $e$ in

$$
  \array{
     && \mathbf{B}H
     \\
     & {}^{\mathllap{e}}\nearrow & \downarrow^{\mathrlap{i}}
     \\
     X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

The [[moduli space]] of $i$-generalized vielbeing relative $g$ is the [[twisted cohomology]]

$$
  \mathbf{H}_{/\mathbf{B}G}(g,i)  
  \,.
$$

## Properties

* Locally on $X$ the moduli space of generalized vielbeins is the [[coset]] $G/H$.


## Examples

* The ordinary notion of [[vielbein]] is obtained for

  $$
    \array{
       GL_n/O(n) &\to& \mathbf{B}O(n)
       \\
       && \downarrow
       \\
       && \mathbf{B}GL_n
    }
    \,.
  $$

* in the context of [[generalized complex geometry]] one considers generalized vielbeins arising from reduction along $O(n)\times O(n) \to O(n,n)$ of the [[generalized tangent bundle]]

  $$
    \array{
       O(n)\backslash O(n,n)/O(n) &\to& \mathbf{B}(O(n) \times O(n))
       \\
       && \downarrow
       \\
       && \mathbf{B}O(n,n)
    }
    \,.
  $$
  

* in the context of [[exceptional generalized geometry]] one considers vielbeins arising from reduction along $H_n \to E_n$ for $E_n$ an [[exceptional Lie group]].

## Related concepts

* [[super-vielbein]]

## References

For instance

* [[Ralph Blumenhagen]], Pascal du Bosque, [[Falk Hassler]], [[Dieter Lüst]]: section 5.1 of: *Generalized Metric Formulation of Double Field Theory on Group Manifolds*, J. High Energ. Phys. **2015** 56 (2015) &lbrack;[arXiv:1502.02428](https://arxiv.org/abs/1502.02428), <a href="https://doi.org/10.1007/JHEP08(2015)056">doi:10.1007/JHEP08(2015)056</a>&rbrack;


See also the section _[Fields](geometry+of+physics#Fields)_ at 

* _[[geometry of physics]]_

[[!redirects generalized vielbeins]]
