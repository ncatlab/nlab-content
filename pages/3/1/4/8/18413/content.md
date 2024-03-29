
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
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

Generally, a _topological interval_ is a ([[bounded set|bounded]]) [[interval]] in the [[real line]] (an [[open interval]] $(a,b)$ or a [[closed interval]] $[a,b]$ or a [[half-open interval]] $(a,b]$ or $[a,b)$) equipped with the [[subspace topology]] of the [[Euclidean space|Euclidean]] [[metric topology]].

Specifically in the context of [[topological homotopy theory]], the _standard topological [[interval object]]_ is the [[closed interval]] $[0,1]$ equipped with the [[continuous functions]] 

1. $const_0 \;\colon\; \ast \to [0,1]$

1. $const_1 \;\colon\; \ast \to [0,1]$

which include the [[point space]] as the two endpoints, respectively.

Together with the unique function $[0,1] \to \ast$ this yields the factorization of the [[codiagonal]] on the [[point space]]

$$
  \nabla_{\ast}
  \;\colon\;
  \ast \sqcup \ast \overset{(const_0,const_1)}{\longrightarrow} [0,1] \overset{\exists!}{\longrightarrow} \ast
$$

which exhibits an example of an _[[interval object]]_ in the general sense of [[model category]] theory with respect to the [[classical model structure on topological spaces]].

## Induced constructions

### Topological cylinder

For $X$ a [[topological space]], then the [[product topological space]] $X \times [0,1]$ with the topological interval is the _standard topological [[cylinder]]_ over $X$. Via the above inclusion functions, this inherits a factorization of the [[codiagonal]] of $X$ (the canonical continuous function out of the [[disjoint union space]] of $X$ with itself to $X$):

$$
  \nabla_X
  \;\colon\;
  X \sqcup X
   \overset{(id_X \times const_0, id_X \times const_1)}{\longrightarrow}
  X \times [0,1]
   \overet{pr_1}{\longrightarrow}
  X
  \,.
$$


Accordingly, with respect to the [[classical model structure on topological spaces]] this is an example a of _[[cylinder object]]_.

### Left homotopy

Given $X,Y$ two [[topological spaces]] and $f,g \;\colon\; X \longrightarrow Y$ two [[continuous functions]],then a **[[left homotopy]]**

$$
  \eta \colon f \,\Rightarrow_L\, g
$$

is a [[continuous function]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$


out of the [[product topological space]] of $X$ with the topological interval, such that this fits into a [[commuting diagram]] of the form

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://www.ncatlab.org/nlab/files/AHomotopy.jpg" width="400">
</div>


$$
  \array{
     X
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{f}}
     \\
     X \times I &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{g}}
     \\
     X
  }
  \,.
$$

(graphics grabbed from J. Tauber [here](http://jtauber.com/blog/2005/07/01/path_homotopy/))

### Path space

For $X$ a [[topological space]], then its _path space_ is the [[mapping space]] $X^{[0,1]}$, out of the topological interval into $X$, i.e. the set of [[continuous function]] $\gamma \;\colon\; [0,1] \to X$ equipped with the [[compact-open topology]]. 

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

### Freyd's characterization 

The topological interval $[0, 1]$ may be characterized by a [[coalgebra for an endofunctor|coalgebraic]] definition first identified by [[Freyd]]: 

Let $Top_{\ast, \ast}$ be the [[category]] of [[topological spaces]] $X$ equipped with a [[pair]] $x_0, x_1$ of distinct points, for example $I = ([0, 1]; 0, 1)$. Let $F \colon Top_{\ast, \ast} \to Top_{\ast, \ast}$ be the [[functor]] defined on [[objects]] by 

$$
  F(X; x_0, x_1) = (X \vee X, y_0, y_1)
  \,,
$$ 

where $X \vee X$ denotes the [[quotient space]] of the [[disjoint union space]] $X \sqcup X$ formed by identifying the element $x_1$ of the first copy of $X$ with $x_0$ of the second copy of $X$, where $y_0$ is identified with $x_0$ of the first copy, and $y_1$ is identified with $x_1$ of the second copy. 

For $I = ([0, 1]; 0, 1)$ there is an evident identification $F(I) = ([0, 2]; 0, 2)$, and moreover there is an $F$-[[coalgebra of an endofunctor|coalgebra]] structure $I \to F(I)$ given by "multiplication by $2$". 

+-- {: .num_theorem} 
###### Theorem 
**(Freyd)** 

The topological interval $I = ([0, 1], 0, 1)$ is the [[terminal coalgebra of an endofunctor|terminal F-coalgebra]]. 


=-- 

For more information, see [[coalgebra of the real interval]], which shows in particular how the interval structure of $[0, 1]$ may be defined by coinduction. 

[[!redirects topological intervals]]
