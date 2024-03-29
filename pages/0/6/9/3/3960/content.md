
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[topology]] the _path space_ of a [[topological space]] $X$ is a _topological space of all continuous [[paths]]_ in $X$.

In [[topological homotopy theory]] the path space construction serves to exhibit [[homotopies]] in the guise of _[[right homotopies]]_. This situation generalizes to many other [[model categories]] and one speaks more generally of _[[path space objects]]_ in this case.
 
For exposition in the context of [[point-set topology]] see at _[[Introduction to Topology -- 1]] around [this example](Introduction+to+Topology+--+1#PathSpace)_.

For exposition in the context of [[topological homotopy theory]] see at _[[Introduction to Homotopy Theory]]_ around [this definition](Introduction+to+Homotopy+Theory#TopologicalPathSpace).

## Definition

For $X$ a [[topological space]], then its _path space_ is the [[mapping space]] $X^{[0,1]}$, out of the [[topological interval]] into $X$, i.e. the set of [[continuous functions]] $\gamma \;\colon\; [0,1] \to X$ equipped with the [[compact-open topology]]. 

The two endpoint inclusions $\ast \colon [0,1]$ and the unique projection $[0,1] \to \ast$ induce continuous functions

$$
  X
    \overset{}{\longrightarrow}
  X^{[0,1]}
   \overset{X^{(const_0,const_1)}}{\longrightarrow}
  X \times X
$$

(inclusion of constant paths and endpoint evaluation of paths).

## Properties

### Relation to loop space

The [[fiber product]] of the projection with the [[diagonal]] on $X$ is the [[free loop space]] $\mathcal{L}X$ of $X$:


$$
  \array{
    \mathcal{L}X &\longrightarrow& X^{[0,1]}
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{X^{(const_0,const_1)}}}
    \\
    X &\underset{\Delta_X}{\longrightarrow}& X \times X
  }
$$

If $X$ is equipped with a choice of basepoint $x \colon \ast \to X$ (making it a [[pointed topological space]]), then the further [[fiber product]] with this basepoint inclusion is the based [[loop space]] $\Omega_x X$:


$$
  \array{
    \Omega_x X &\longrightarrow& \mathcal{L}X &\longrightarrow& X^{[0,1]}
    \\
    \downarrow &(pb)& \downarrow &(pb)& \downarrow^{\mathrlap{X^{(const_0,const_1)}}}
    \\
    \ast &\underset{x}{\longrightarrow}& X &\underset{\Delta_X}{\longrightarrow}& X \times X
  }
$$



## Related concepts

* [[loop space]]

* [[path groupoid]];

* [[fundamental groupoid]];

* [[topological complexity]]

* [[path space object]]

* [[identity type]]


[[!redirects path space]]
[[!redirects path spaces]]
