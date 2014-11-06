
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
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

A [[topos]] can be viewed as a generalization of a [[topological space]].  A _smooth structure on a topos_ is a corresponding generalization of the notion of [[smooth manifold]], in that to put a smooth structure on $Sh(X)$, for a topological space $X$, is (at least closely related to) putting the structure of a smooth manifold on $X$.  However, since it is phrased internally with reference to the (Cauchy and Dedekind) [[real numbers objects]], it is applicable to any topos.

## Definition

Given a [[topos]] $\mathbf{H}$, write

* $\mathbb{N} \in \mathbf{H}$ for its [[natural numbers object]];

* $\mathbb{R}_{C} \in \mathbf{H}$ for its [[Cauchy real numbers object]];

* $\mathbb{R}_{D} \in \mathbf{H}$ for its [[Dedekind real numbers object]];

* $\mathbb{R} \in $ [[Set]] for the external [[real numbers]].

There are canononical [[subobject]] inclusions

$$
  \mathbb{N} \hookrightarrow \mathbb{R}_C \hookrightarrow \mathbb{R}_D
  \,.
$$

+-- {: .num_defn #StandardFunction}
###### Definition

A morphism

$$
  g \colon \mathbb{R}_D^{n_1} \longrightarrow \mathbb{R}_D^{n_2}
$$

in the topos $\mathbf{H}$ is called a _standard function_, precisely if

1. it is a [[continuous function]] in that

   $$
     \underset{\epsilon \gt 0}{\forall} 
     \underset{\delta \gt 0}{\exists}
     \underset{\vec x, \vec y \in \mathbb{R}_D^{n_1}}{\forall}
     \left(   
       \left(
         \underset{i}{max} {\vert x_i - y_i \vert}
         \lt \delta
       \right)
       \Rightarrow
       \left(
         \underset{i}{max} {\vert g(\vec x)_i - g(\vec y)_i \vert}
         \lt \delta
       \right)
     \right)
   $$

1. it respects the sub-object of Cauchy reals, in that

   $$
     \underset{\vec x \in \mathbb{R}_C^{n_1}}{\forall} 
     \left(
        g(\vec x) \in \mathbb{R}_{C}^{n_2}
     \right)
     \,.
   $$

=--

This is ([Fourman 75, def. 3.6](#Fourman75)).

Define an [[equivalence relation]] on $\mathbb{R}_D^n$ by taking to elements to be equivalent if there are standard functions, def. \ref{StandardFunction}, taking them into each other:

$$
  (r \simeq s)
  \coloneqq
  \underset{f,g \; standard\;functions}{\exists}
  \left( 
     \left(
       f(r) = s
     \right)
        \wedge
     \left(
       g(s) = r
     \right)
  \right)
  \,.
$$


+-- {: .num_defn #SmoothStructureDimN}
###### Definition
A _smooth structure of dimension $n$_ on a topos $\mathbf{H}$ is a [[subobject]] 

$$
  S \hookrightarrow \mathbb{R}_D^n
$$

such that

$$
  \underset{\vec s \in S}{\exists}
  \underset{\vec x \in \mathbb{R}_D^n}{\forall}
  \left(
     \left(\vec x \in S\right)
     \Leftrightarrow
     \left(\vec x \simeq \vec s\right)
  \right)
  \,.
$$

=--

This is ([Fourman 75, def. 4.1](#Fourman75)).

## Examples

+-- {: .num_example}
###### Example

For $X$ a [[smooth manifold]] of [[dimension]] $n$, with [[sheaf topos]] $\mathb{H} \coloneqq Sh(X)$, then the [[sheaf]] $S$ of local [[coordinate systems]]
is a smooth structure on $Sh(X)$ (of dimension $n$, presumeably), according to def. \ref{SmoothStructureDimN}.

=--

This is ([Fourman 75, example 4.3 1)](#Fourman75)).

## References

* {#Fourman75} [[Michael Fourman]], _Comparaison des Re&#233;ls d'un Topos - Structures Lisses sur un Topos El&#233;mentaire_ , Cah. Top. G&#233;om. Diff. Cat. **16** (1975) pp.233-239. ( _Colloque Amiens 1975 proceedings_ ) (p. 18-24 in [NUMDAM](http://www.numdam.org/item?id=CTGDC_1975__16_3_217_0)))