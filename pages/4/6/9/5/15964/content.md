
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
([Fourman 75, def. 3.6](#Fourman75))
A morphism

$$
  g \colon \mathbb{R}_D^{n_1} \longrightarrow \mathbb{R}_D^{n_2}
$$

in the topos $\mathbf{H}$ is called a __standard function__, precisely if

1. it is a [[continuous function]] in the internal sense that

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

We will furthermore consider __smooth standard functions__, meaning standard functions that satisfy the internalized ordinary definition of [[smooth function]] (i.e. $C^\infty$).

We define an [[equivalence relation]] on $\mathbb{R}_D^n$ by taking two elements to be equivalent if there are smooth standard functions taking them into each other:

$$
  \vdash 
  (r \simeq s)
  \coloneqq
  \underset{{f,g } \atop {smooth \; standard\;functions}}{\exists}
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
([Fourman 75, def. 4.1](#Fourman75))
A __smooth structure of dimension $n$__ on a topos $\mathbf{H}$ is an equivalence class for the above equivalence relation on $\mathbb{R}_D^n$.  In other words, the object of smooth structures of dimension $n$ is the quotient of $\mathbb{R}_D^n$ by this equivalence relation.
=--


+-- {: .num_defn}
###### Definition
([Fourman 75, def. 4.4](#Fourman75))
Given a smooth structure $S$ of dimension $n$ on the topos $\mathbf{H}$ according to def. \ref{SmoothStructureDimN}, then the __smooth real number object__ is the [[subobject]]

$$
  \mathbb{R}_S \hookrightarrow \mathbb{R}_D
$$

defined internally as the set of all images of points in $S\subseteq \mathbb{R}_D^n$ under smooth standard functions $\mathbb{R}_D^n \to \mathbb{R}_D$.  In symbols, it is given by

$$
  \mathbb{R}_S
  \coloneqq
  \left\{
    x \in \mathbb{R}_D
    \;|\;
    \underset{{smooth \; standard\;funct.}\atop{\mathbb{R}_D^n \stackrel{f}{\to} \mathbb{R}_D}}{\exists}
    \underset{s \in S}{\exists}
    (x = f(s))  
  \right\}
  \,.
$$

=--

Note that any function constant at a Cauchy real is standard.  Therefore, every Cauchy real is a smooth real.


## Examples

+-- {: .num_example}
###### Example
([Fourman 75, example 4.3 1](#Fourman75))
Let $X$ be a [[smooth manifold]] of [[dimension]] $n$, with [[sheaf topos]] $\mathbf{H} \coloneqq Sh(X)$.  As shown at [[real numbers object]], $\mathbb{R}_D$ is then the sheaf of *continuous* real-valued functions on $X$.

Let $S\subseteq \mathbb{R}_D^n$ be the sheaf of local [[coordinate systems]], i.e. $S(U)$ is the set of real-valued functions $U\to \mathbb{R}^n$ that are smooth and are locally diffeomorphisms onto their images.  Then $S$ is a smooth structure on $Sh(X)$ of dimension $n$, according to def. \ref{SmoothStructureDimN}.

The corresponding object $\mathbb{R}_S$ of smooth reals is the sheaf of *smooth* real-valued functions $X\to \mathbb{R}$.  Note that since $X$ is locally connected, the Cauchy real numbers object $\mathbb{R}_C$ in $Sh(X)$ is the sheaf of locally constant real-valued functions, so $\mathbb{R}_S$ sits strictly in between $\mathbb{R}_C$ and $\mathbb{R}_D$.

=--

+-- {: .num_example}
###### Example
Let $h:1\to \mathbb{R}_D^n$ be any global section of $\mathbb{R}_D^n$.  Then the equivalence class of $h$, under the above equivalence relation, is a smooth structure.  In particular, if $h$ is a tuple of Cauchy real numbers (such as $0$), then so is every point in $S$, and thus $\mathbb{R}_S = \mathbb{R}_C$.  This gives the "discrete" smooth structure on $\mathbf{H}$.

For $\mathbf{H}=Sh(X)$, such a global section is a continuous map $h:X\to \mathbb{R}^n$, and this gives the smooth structure "cogenerated by" $h$, in that it makes $h$ smooth and only those other functions that must be smooth if $h$ is.  The case when $h$ is a Cauchy real corresponds to $h:X\to \mathbb{R}^n$ being locally constant, in which case all smooth functions are locally constant; this is the "minimal" smooth structure on a topological space $X$.
=--


## References

* {#Fourman75} [[Michael Fourman]], _Comparaison des R&#233;els d'un Topos - Structures Lisses sur un Topos El&#233;mentaire_ , Cah. Top. G&#233;om. Diff. Cat. **16** (1975) pp.233-239. ( _Colloque Amiens 1975 proceedings_ ) (p. 18-24 in [NUMDAM](http://www.numdam.org/item?id=CTGDC_1975__16_3_217_0)))
