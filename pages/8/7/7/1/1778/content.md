
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#&#268;ech cohomology#
* table of contents
{:toc}


## Idea ##

### General idea
 {#GeneralIdea}


&#268;ech cohomology is a tool, or an algorithm, which, when it applies, computes [[abelian sheaf cohomology]] (of some $X$ with [[coefficients]] in some $A$) by use of [[coverings]] and systems of [[coefficients]] on the covering and all its non-empty finite intersections. More generally, it applies also to [[nonabelian cohomology]] and may hence for instance (in degree 1) be used to compute classes of [[principal bundles]] and generally (in higher degree) those of [[principal ∞-bundles]]. Quite generally &#268;ech cohomology is the way to express the intrinsic [[cohomology]] of [[(∞,1)-sheaf]] [[(∞,1)-toposes]] by mapping out of [[Cech nerves]] of [[covers]].

Hence &#268;ech cohomology is more an algorithm for computing [[cohomology]] (see also at _[[Čech methods]]_) than a cohomology theory in itself. In particular it applies (when it applies) to all sorts of [[coefficient]] [[sheaves]]/[[stacks]]/[[∞-stacks]] $A$.

When no further qualification of the coefficients $A$ is given then one usually has in mind by default either that $A = \mathbb{Z}$ is the group of [[integers]] (or a [[delooping]] thereof, in which case one computes [[ordinary cohomology]] by Cech methods) or, if working on a [[ringed space]]/[[ringed topos]]/[[structured (∞,1)-topos]] that $A = \mathcal{O}^\times$ is the [[group of units]] in the [[structure sheaf]].

Notice that there are technical conditions on a [[site]] and a [[cover]] to ensure that the result of the Cech cohomology algorithm really coincides with the more abstractly defined [[abelian sheaf cohomology]] -- and generally with the [[hom-spaces]] in the given [[(∞,1)-topos]]. (Technically the condition is that the [[Cech nerve]] is a [[cofibrant resolution]] in a [[model structure on simplicial presheaves]] for which the coefficient sheaf is a [[fibrant object]]). If these conditions do not apply, then the definition of Cech cohomology groups still works as such, but typically no longer qualifies as a "cohomology theory", axiomatically. They are just some groups. Strictly speaking one should maybe not use the term "Cech cohomology" in such cases, but beware that some authors do.

### More technical idea

From the discussion at [[abelian sheaf cohomology]] we know that the [[right derived functor]] definition computes the hom-set in the [[homotopy category of an (infinity,1)-category|homotopy category]] of an [[(infinity,1)-topos]] $\mathbf{H}$ that may alternatively be computed as a [[colimit]] over [[resolutions]] of the [[domain]] object

$$
  H(X,A)
  \coloneqq
  \pi_0 \mathbf{H}(X,A)
  = colim_{Y \stackrel{\in W \cap F}{\longrightarrow} X} 
  C_H(Y,A)/_{homotopy}
$$

where the colimit is over all acyclic fibrations $Y \stackrel{\in W \cap F}{\longrightarrow} X$ in an appropriate [[model category]] $C_H$ that [[presentable (infinity,1)-category|presents]] $\mathbf{H}$. For $\mathbf{H}$ an [[infinity-stack]] [[(infinity,1)-topos]] this $C_H$ is a [[model structure on simplicial presheaves]] and the acyclic fibrations $Y \stackrel{\in W \cap F}{\to} X$ for $X$ an ordinary space are the [[hypercovers]].

Now, for some coefficient objects $A$ it is sufficient to take the colimit here not over all [[hypercovers]], but just over [[Čech covers]]. The resulting formula

$$
  H(X,A)

  = colim_{Y \stackrel{\mathop{&#268;ech} cover}{\to} X} 
  C_H(Y,A)/_{homotopy}
$$

is then called the formula for **&#268;ech cohomology** on $X$ with values in $A$.

Here a [[Čech cover]] is a simplicial presheaf that arises from an ordinary covering map $U \to X$ of $X$ by another space $U$ as the corresponding [[Čech nerve]] simplicial presheaf

$$
 \begin{aligned}
  Y := \left( 
    \cdots
    U \times_X U \times_X U
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    U \times_X U \stackrel{\longrightarrow}{\longrightarrow} U 
  \right)
  \simeq
  hocolim_{[k] \in \Delta} U^{\times_X k}
 \end{aligned}
  \,.
$$

See [[descent for simplicial presheaves]] for more on the manipulations involved here.

To amplify, a general [[hypercover]] would start in degree 0 with a $U$ as above, but then in the next degree would have a cover $V \to U \times_X U$ of the fiber product, and so on, each fiber product in turn being covered by another space.

If $Y$ is not simply a [[Čech cover]] but also not the most general [[hypercover]] in that this iterative choice of further covering stops in degree $n$, then one also speaks of **&#268;ech cover of level $n$** and of the corresponding cohomology formula as **higher &#268;ech cohomology**. See for instance the reference by Tibor Beke below.



## General ("nonabelian") &#268;ech cohomology 
 {#NonabelianCechCohomology}

We start with describing the general " _nonabelian_ " &#268;ech cohomology (compare the terminology and remarks at [[cohomology]] and [[nonabelian cohomology]]), i.e. the plain unwrapping of the above definition, before assuming that our coefficient object is [[abelian sheaf cohomology|abelian]] and before applying the [[Moore complex]] functor that sends the following simplicial computation to the maybe more familiar one in [[chain complexes]].

The reasoning parallels that described at [[descent]] to some extent, but is maybe still worthwhile repeating here.

So let $C$ be some [[site]] and let $SSh(C)$ the category of [[simplicial presheaf|simplicial (pre)sheaves]] on $C$. Let $C(U)$ be the &#268;ech nerve for a cover $\pi : U \to X$ of some simplicial presheaf $X$ and let $A$ be any other simplicial presheaf that serves as the coefficient object.

Using [[end]] and [[coend]] notation we compute the required hom

$$
 \begin{aligned}
    SSh(C(U), A)
    &
    \simeq
    SSh( \int^{[k] \in \Delta} \Delta^k \cdot C(U)_k, A )
    \\
    &
    \simeq
    \int_{[k] \in \Delta} SSh(\Delta^k \cdot C(U)_k, A )   
    \\
    &
    \simeq
    \int_{[k] \in \Delta} SSet(\Delta^k , SSh(C(U)_k,A) )   
    \\
    &
    \simeq
    \int_{[k] \in \Delta} SSet(\Delta^k , A(U \times_X \cdots \times_X U) )   
    \\
    &
    \simeq
    \int_{[k] \in \Delta} SSet(\Delta^k , \prod_{i_0, \cdots, i_k} A(U_{i_0 i_1, \cdots ,i_k}) )   
 \end{aligned}
  \,.
$$

Here in the last line we have assumed that $U = \sqcup_i U_i$ for $\{U_i \to X\}$ an open cover of some space $X$ and we abbreviate as usual with
$
  U_{i_0, i_1, \cdots, i_k}
$ the $(k+1)$-fold intersections 
$\cap_{0 \leq r \leq k} U_{i_r}$.

An object in this last expression -- an $A$-valued cocycle on $X$ relative to $U$ -- is a collection of morphisms in [[SSet]] of the form

$$
  \left(
  \array{
    \vdots && \vdots
    \\
    \Delta^2
    &\stackrel{f}{\longrightarrow}&
    \prod_{i j k} A(U_{i j k})
    \\
    \Delta^1
    &\stackrel{g}{\longrightarrow}&
    \prod_{i j}A(U_{ i j})
    \\
    \Delta^0
    &\stackrel{a}{\longrightarrow}&
    \prod_i A(U_i)
  }
  \right)
$$

that make all diagrams of the form

$$
  \array{
    \vdots && \vdots
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^2
    &\stackrel{f}{\longrightarrow}&
    \prod_{i j k} A(U_{i j k})
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^1
    &\stackrel{g}{\to}&
    \prod_{i j}A(U_{ i j})
    \\
    \uparrow^{\delta_{\cdot}}
    &&
    \uparrow^{A(d_{C(U)})_\cdot}
    \\
    \Delta^0
    &\stackrel{a}{\to}&
    \prod_i A(U_i)
  }
$$

commute. Here the vertical morphism on the right, when one traces their origin through the derivation above, are the various inclusion and restriction maps of elements of $A$ evaluated on a $k$-fold intersection to some other intersection.

For instance the three possible vertical maps at the
bottom have components on the cartesian factors given by

$$
  A(d_1)|_{U_i} := (-)|_{U_{i j}}
  :
  A(U_i)  
  \to 
  A(U_{i j})
$$

and

$$
  A(d_0)|_{U_i} := (-)|_{U_{i j}}
  :
  A(U_j)  
  \to 
  A(U_{i j})
$$

and 

$$
  A(s_0)|_{U_{i i}}
  :
  A(U_{i i})  
  \to 
  A(U_{i })
  \,.
$$


This picks

* an object $a \in A(U)$

* a morphism $g : \pi_1 ^* a \to \pi_2^* a in A(U \times_X U)$

* a 2-morphism 
  $$ 

    \array{
      && \pi_{2}^* a
      \\
      & {}^{\pi_{12}^* g}\nearrow &\Downarrow^{f}& \searrow^{\pi_{23}^* g}
      \\
      \pi_{1}^* a
      &&\stackrel{\pi_{13}^* g}{\to}&&
      \pi_3^* a
    }
  $$
  in $A(U \times_X U \times_X U)$

* etc.

If we follow tradition and write 

* $U = \sqcup_i U_i$;

* and $U \times_X U = \sqcup_{i j} U_{i j} := \sqcup_{i j} U_i \cap U_j$

* etc

this is

* an collection of objects $(a_i \in A(U_i))$

* a collection of morphisms 
  $(g_{i j} : a_i|_{U_{ij}} \to a_{j}|_{U_{i j}} 
  in A(U_{i j}))$

* a collection of 2-morphisms 
  $$ 
   \left(
    \array{
      && a_{j}|_{U_{i j k}}
      \\
      & {}^{g_{ij}|_{U_{i j k}}}\nearrow 
      &\Downarrow^{f_{i j k}}& 
       \searrow^{g_{j k}|_{U_{i j k}}}
      \\
      a_i|_{U_{i j k}}      
       &&\stackrel{g_{i k}|_{U_{i j k}}}{\to}&&
      a_k|_{U_{i j k}}
    }
   \right)
  $$
  in $A(U_{i j k})$

* etc.

This is a **&#268;ech-cocycle** on $X$ with values in $A$ relative to $U$.

A **transformation/homotopy/coboundary** between two such cocycles is a cylinder over these diagrams, i.e. 

* a collection of morphism
  $ h_i : a_i  \to a'_i  in A(U_i)$;

* a collection of 2-morphism
  $$
    \array{
      a_i|_{U_{i j}} 
       &\stackrel{g_{i j}}{\to}&
      a_j|_{U_{i j}}
      \\
      \;\;\;\downarrow^{h_i|_{U_{i j}}} 
      &\Downarrow^{a_{i j}}& 
      \;\;\;\downarrow^{h_j|_{U_{i j}}}
      \\
      a'_i|_{U_{i j}} 
       &\stackrel{g_{i j}}{\to}&
      a'_j|_{U_{i j}}      
    }
  $$
  on $U_{i j}$

* a collection of 3-morphisms
  $$
    \array{
      && a_j|_{U_{i j k}}
      \\
      & {}^{g_{ij}|_{U_{i j k}}}\nearrow
      &\Downarrow^{f_{i j k}}& 
      \searrow^{g_{j k}|_{U_{i j k}}}
      \\
      a_i|_{U_{i j k}} 
       &&\stackrel{g_{i k}}{\to}&&
      a_k|_{U_{i j k}}
      \\
      \;\;\;\downarrow^{h_i|_{U_{i j}}} 
      &&\Downarrow^{a_{i k}}&& 
      \;\;\;\downarrow^{h_j|_{U_{i j}}}
      \\
      a'_i|_{U_{i j k}} 
       &&\stackrel{g_{i k}}{\to}&&
      a'_k|_{U_{i j k}}      
    }
    \;\;
    \;\;
    \;\;
    \;\;
    \;\;
    \stackrel{\rho_{i j k}}{\Rightarrow}
    \;\;
    \;\;
    \;\;
    \;\;
    \;\;
    \array{
      && a_j|_{U_{i j k}}
      \\
      & 
      {}^{g_{ij}|_{U_{i j k}}}\nearrow
      &\Downarrow^{a_{i j}\cdot a_{j k}|_{U_{i j k}}}& 
      \searrow^{g_{j k}|_{U_{i j k}}}
      \\
      a_i|_{U_{i j k}} 
       && a'_j|_{U_{i j k}} &&
      a_k|_{U_{i j k}}    
      \\
      \downarrow^{h_{i}|_{U_{i j k}}}
      &
        {}^{g'_{i j}|_{U_{i j k}}}\nearrow 
      &
       \Downarrow^{f'_{ijk}}
      &
        \searrow^{g'_{j k}|_{U_{i j k}}} 
      &
      \downarrow^{h_{k}|_{U_{i j k}}} 
      \\
      a'_i|_{U_{i j k}}
      &&\stackrel{g'_{i k}|_{U_{i j k}}}{\to}&&
      a'_k|_{U_{i j k}}
    }
  $$

We now plug in some concrete coefficient object 
$n$-types for low $n$ and reproduce some concrete formulas
from this.

### Nonabelian 1-cocycles: principal bundles 

For $G$ a [[group]] let 
$\mathbf{B} G$ by abuse of notation denote 

* first of all the corresponding
[[delooping|delooped]] [[groupoid]], 

* then the corresponding [[nerve]] 

* then finally the corresponding simplicial sheaf that for each object $U$ assigns the [[nerve]] for the group $Hom(U,G)$:

  $$
    \mathbf{B}G : U \mapsto
    \left\{
      \array{
        \mathbf{B}G(U)_0 = Hom(U,{*}) = {*}
        \\
        \mathbf{B}G(U)_1 = Hom(U,G)
        \\
        \mathbf{B}G(U)_2 = Hom(U,G)\times Hom(U,G)
        \\
        \vdots
      }     
    \right.
  $$

The above then says that 

* a $\mathbf{B}G$-&#268;ech cocycle is

  * a collection of $G$-valued functions 

     $$
       (g_{ij} \in Hom(U_{i j}, G))
     $$
  
  * a collection of identities between $G$-valued functions

    $$
      g_{ij}|_{U_{i j k }} 
       \cdot
      g_{j k}|_{U_{i j k }}
      =
      g_{i k}|_{U_{i j k }}
    $$

* a $\mathbf{B}G$-&#268;ech coboundary is
  
  * a collection of $G$-valued functions

    $$
      (h_i \in Hom(U_i , G))
    $$

  * a collection of identites between $G$-valued functions

    $$
      g_{ij} \cdot h_j|_{U_{i j}}
      = 
      h_i|_{U_{i j}} \cdot g'_{j k}
      \,.
    $$

Remembering that the &#268;ech cohomology is the colimit over refinement of covers over cohomology classes defined this way, one sees the standard

+-- {: .num_theorem }
###### Theorem

&#268;ech cohomology with coefficients in $\mathbf{B}G$
(as above) classies $G$-[[principal bundles]]

$$

  colim_{U \stackrel{\mathop{&#268;ech} cover}{\to} X}
  SSh(C(U), \mathbf{B}G)/_{homtopy}
  \simeq
  G Bund(X)/_\sim
$$

=--


### Nonabelian 2-cocycles: gerbes and principal 2-bundles


In one degree higher the general [[homotopy n-type|homotopy 2-type]] coefficient object is modeled using a strict [[2-group]] $H$ coming from a [[crossed module]]
$G_2 \stackrel{\delta}{\to} G_1$.

The [[nerve]] of the corresponding [[delooping|delooped]]
[[2-groupoid]], regarded immediately as a simplicial sheaf starts out like

$$
  \mathbf{B}(G_2 \to G_1)
  :
  U 
  \mapsto
  \left\{
    \array{
       \mathbf{B}(G_2 \to G_1)(U)_{0}
       = 
       Hom(U, G_1)
       \\
       \mathbf{B}(G_2 \to G_1)(U)_{1}
       = 
       Hom(U, G_1) \times Hom(U, G_1)
       \times Hom(U, G_2)
       \\

       \vdots
    }
  \right.
  \,.
$$

One finds that a &#268;ech-cocycle now is
(see also the diagrams at [[group cohomology]] for this)

* a collection of functions 

  $$
    (g_{i j} \in Hom(U_{i j}, G_1))
  $$

* a collection of functions
  
  $$
    (f_{i j k }\in Hom(U_{i j k}, G_2) )
  $$

* a collection of identities  

  $$
    \delta(f_{i j k}|_{U_{i j k}})
    g_{i j}|_{U_{i j k}}
    g_{j k}|_{U_{i j k}}
    =
    g_{i k}|_{U_{i j k}}  
  $$

* and a collection of identities

  $$
    f_{i k l}|_{U_{i j k l}}
    \cdot
    f_{i j k}|_{U_{i j k l}}
    =
    f_{i j l}|_{U_{i j k l}}
    \cdot
    \alpha(g_{i j}|_{U_{i j k l}})(f_{j k l}|_{U_{i j k l}}),
    $$

where $\alpha:G_1\to Aut(G_2)$ is the homomorphism associated with the crossed-module description of the 2-group.

This is a **nonabelian &#268;ech 2-cocycle**.

Reading off the formulas for the coboundaries is
left as an excercise for the reader.

For the specical case the 

$$
  (G_2 \to G_1) = (G \to Aut(G))
$$

this is the nonabelian cohomology classifying

[[gerbes]].


## Abelian &#268;ech cohomology 
 {#AbelianCechCohomology}

In much of the literature _&#268;ech cohomology_ denotes exclusively the abelian case, which we now describe.

In the special case that the coefficient [[simplicial presheaf]] $A$ is in the image of the [[nerve]] operation 

$$
  N : Ch_+ \to sAb \to SSet
$$

on [[chain complexes]] with values in [[simplicial sets]] that happen to be abelian [[simplicial groups]], the computation of &#268;ech cocycles may be entirely pulled back to the world of [[homological algebra]] by making use of the [[Dold-Kan correspondence]] that provides an [[adjoint equivalence]] between simplicial sets with values in abelian groups and non-negatively graded chain complexes.


### Definition
 {#AbelianCechCohomologyDefinition}
 
 

We discuss the [[double complex]] which gives the traditional definition of Cech cohomology with coefficients in [[sheaves of abelian groups]].

Let 

* $X$ be a [[topological space]];

* $A_\bullet = (\cdots \stackrel{\partial}{\to} A_2 \stackrel{\partial}{\to} A_1 \stackrel{\partial}{\to} A_0)$ be a [[chain complex]] of [[abelian sheaves]] on $X$ (i.e. on the [[category of open subsets]] $S \colon Op(X)$ of $X$, regarded as a [[site]] with the usal [[covering]] [[Grothendieck topology]]);

* $\{U_i \to X\}$ be an [[open cover]] of $X$.

We write 

$$
  U_{i_0,\cdots i_k}
  \coloneqq
  U_{i_0}
  \underset{X}{\times}
  U_{i_1}
  \underset{X}{\times}
  \cdots  
  \underset{X}{\times}
  U_{i_k}
$$

for the $k$-fold intersections of these open subsets. Given an inclusion of open subsets $U_1 \to U_2$ and given any group element $a\in A_\bullet(U_2)$ we write $a|_{U_1}$ for its restriction along this map.

More generally, we may allow $S$ to be any [[site]]. For simplicity of the following formulas assume that $S$ has [[finite products]] (which in the case that $S$ is a [[category of open subsets]] are the [[fiber products]] above.) Then $A_\bullet$ is a chain complex of [[abelian sheaves]] on that site. 

+-- {: .num_defn #CechComplex}
###### Definition
**(&#268;ech complex)**


The **&#268;ech cochain complex** $C^\bullet((X,\{U_i\}),A_\bullet)$ 
of $X$ with respect to the cover $\{U_i \to X\}$ and with [[coefficients]] in $A_\bullet$ is in degree $k \in \mathbb{N}$ given by the [[abelian group]]

$$
  C^k((X,\{U_i\}),A_\bullet)
  \coloneqq
  \oplus_{{l,n} \atop {k = n-l}}
  \oplus_{i_0, i_1, \cdots, i_n}
  A_l(U_{i_0, \cdots, i_n})
$$

which is the [[direct sum]] of the values of $A_\bullet$ on the given intersections as indicated; and whose [[differential]] 

$$
  d
  \colon
  C^{k}((X,\{U_i\}),A_\bullet)
  \longrightarrow
  C^{k+1}((X,\{U_i\}),A_\bullet)
$$

is defined componentwise (see at [[matrix calculus]] for conventions on maps between [[direct sums]]) by

$$
  \begin{aligned}
    (d a)_{i_0, \cdots, i_{k+1}} 
    & \coloneqq 
    (\partial_A a + (-1)^k \delta a)_{i_0, \cdots, i_{k+1}} 
    \\
    & \coloneqq
    \partial_A a_{i_0, \cdots, i_{k+1}}
    +
    (-1)^k
    \sum_{0 \leq j \leq k+1} (-1)^{j}
    a_{i_0, \cdots, i_{j-1}, i_{j+1}, \cdots, i_{k+1}} 
    |_{U_{i_0, \cdots, i_{k+1}}}
  \end{aligned}
$$

where on the right the sum is over all components of $a$ obtained via the canonical restrictions obtained by discarding one of the original $(k+1)$ subscripts.

The **Cech cohomology** groups of $X$ with coefficients in $A_\bullet$ __relative to the given cover__ are the [[chain homology]] groups of the Cech complex

$$
  H_{Cech}^k((X,\{U_i\}), A_\bullet)
  \coloneqq
  H^k(C^\bullet((X,\{U_i\}),A_\bullet))
  \,.
$$

The **Cech cohomology** groups as such are the [[colimit]] ("[[directed limit]]") of these groups over refinements of covers

$$
  H^k_{Cech}(X, A_\bullet)
  \coloneqq
  \underset{\longrightarrow}{\lim}_{\{U_i \to X\}}
  H_{Cech}^k((X,\{U_i\}), A_\bullet)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Often Cech cohomology is considered for the case that $A_\bullet$ is concentrated in a single degree, in which case the first term in the sum defining the differential in def. \ref{CechComplex} disappears. 
When $A_\bullet$ is not concentrated in a single degree, then for emphasis and following terminology of _[[hypercohomology]]_ 
one may speak of the **&#268;ech hypercomplex** computing **&#268;ech hypercohomology**.

=--


+-- {: .num_remark}
###### Remark

The Cech chain complex in def. \ref{CechComplex} is the [[total complex]] of the [[double complex]] whose vertical differential is that of $A_\bullet$ and whose horizontal differential is the _Cech differential_ $\delta$ given by alternating sums over restrictions along patch inclusions

$$
  \array{
     \vdots && \vdots
     \\
     \downarrow^{\mathrlap{\partial_A}}
     &&
     \downarrow^{\mathrlap{\partial_A}}
     \\
     \oplus_i A_1(U_i)
     &\stackrel{\delta}{\longrightarrow}&
     \oplus_{i_1, i_2} A_1(U_{i_1, i_2})
     &\stackrel{\delta}{\longrightarrow}&
     \cdots
     \\
     \downarrow^{\mathrlap{\partial_A}}
     &&
     \downarrow^{\mathrlap{\partial_A}}
     \\
     \oplus_i A_0(U_i)
     &\stackrel{\delta}{\longrightarrow}&
     \oplus_{i_1, i_2} A_0(U_{i_1, i_2})
     &\stackrel{\delta}{\longrightarrow}&
     \cdots
  }
$$

=--


### Relation to nonabelian &#268;ech cohomology
 {#RelationAbelianNonabelian}


We discuss how the abelian Cech complex of def. \ref{CechComplex} arises as a special case of the simplicial nonabelian cocycle complex of general nonabelian Cech cohomology [above](#NonabelianCechCohomology), under the [[Dold-Kan correspondence]].


+-- {: .num_remark}
###### Remark


It may be helpful to keep the following pictures in mind to match the signs to the orientations of simplices.

In dimension one we have:

$$
  (0 \to 1)
  \;\;\;

  \mapsto
  \;\;\;
  (a_0 \stackrel{a_{0 1}}{\to} a_1)
  \;\;\;
  \leftrightarrow
  \;\;\;
  (a_1 = a_0 + d_A a_{01})
$$

In dimension 2 we have:

$$
  \array{
    && 1
    \\
    & \nearrow &\Downarrow& \searrow
    \\
    0 &&\to&& 2
  }
  \;\;\;
  \mapsto
  \array{
    && a_1
    \\
    & {}^{a_{0 1}}\nearrow &\Downarrow^{a_{0 1 2}}
    & \searrow^{a_{1 2}}
    \\
    a_0 &&\stackrel{a_{0 2}}{\to}&& a_2
  }
  \;\;\;
  \leftrightarrow
  (a_{0 2} = a_{0 1} + a_{1 2} + d a_{0 1 2})
  \,.
$$

Here the relation on the right is the 
[[Dold-Kan correspondence]] relating coboundaries in the
complex $A_\bullet$ to simplices .

=--

+-- {: .num_remark}
###### Remark

The following derivation of abelian &#268;ech cohomology from nonabelian &#268;ech cohomology restricted to nerves of chain complexes needs of the [[Dold-Kan correspondence]] only that it is an [[adjunction]], not that it is an [[adjoint equivalence]]. 

=--


+-- {: .num_prop }
###### Proposition (recovering abelian &#268;ech cohomology)

Let $A_\bullet$ be a sheaf with values in $Ch_+$
and write $N(A_\bullet)$ for the corresponding
simplicial sheaf under the [[nerve]] operation
of the [[Dold-Kan correspondence]].

Then the general (nonabelian) &#268;ech cohomology
of $N(A_\bullet)$ as defined above coincides
with the cohomology of the &#268;ech complex of
$A_\bullet$:

$$
  H(X, N(A_\bullet))
  \simeq
  colim_U H_0(C(U,A_\bullet))
  \,.
$$

=--

+-- {: .proof}
###### Proof

The underlying idea is to use the 
adjunction of the [[Dold-Kan correspondence]]
to move the nerve operation $N(A_\bullet)$ 
on the right to the
free abelian chain complex operation 
$C_bullet(F(C(U)))$
on the 
[[Čech cover]] simplicial sheaf $C(U)$ and then 
use the [[Yoneda lemma]] to evaluate $A_\bullet$
on $N_\bullet(F(C(U)))$. The result is the 
&#268;ech complex of $A_\bullet$. 
Cocycles and homotopies/coboundaries
are in bijection on both sides.

Spelled out in full detail this looks a bit more lengthy,
but is nothing but this simple idea.

Before starting the computation notice the following
observation on the image of the [[Čech cover]]
$C(U)$ under the [[Dold-Kan correspondence]]:

For $Y = C(U)$ a [[Čech cover]] on a sieve 
$\{U_i \to X\}_{i \in I}$, and for $W$ any test object,
the non-degenerate $n$-simplices in $C(U)(W)$ are the

$$
  U_{i_0, i_1, \cdots, i_n}(W)
$$ 

with all indices pairwise different, $i_k \neq i_l$. 

Accordingly the free abelian simplicial group-valued
sheaf $F(C(U))$ is for each $W$ and $n$ the 
free abelian group generated from these 
$U_{i_0, i_1, \cdots, i_n}(W)$ with pairwise distinct elements, i.e. that given by
formal interger combinations of these element.

In turn, the normalized [[Moore complex]] sheaf

$$
  N_\bullet(F(C(U))) 
$$

assigns to a test domain $W$ the complex that in
each degree is the free abelian group on these 
elements.




With this in hand,
we compute the set of $N(A_\bullet)$-valued cocycles on $U$ as follows:

$$
  \begin{aligned}
    Hom_{SPSh}(C(U), N(A_\bullet))
    &\simeq
    \int_W Hom_{SSet}( C(U)(W) , N(A_\bullet)(W) )
    \\
    & \simeq
    \int_W Hom_{SSet}( C(U)(W) , N(A(W)_\bullet) )    
    \\
    & \simeq
    \int_W Hom_{SAb}( F(C(U)(W)) , N(A(W)_\bullet) )    
    \\
    & \simeq
    \int_W Hom_{Ch_+}( N_\bullet(F(C(U)(W))) ,
         A(W)_\bullet )    
    \\
    & \simeq
    \int_W \int_{n}  
       Hom_{Ab}( N_n(F(C(U)(W)), A(W)_n ) 
    \\
    & \simeq
       \int_{n}
       \int_W   
       Hom_{Ab}( N_n(F(C(U)(W)), A(W)_n )  
    \\
    & \simeq
       \int_{n}
       \int_W  
       Hom_{Set}( \coprod_{i_0, i_1, \cdots, i_k} 
       U_{i_0,i_1, \dots, i_n}(W) , A(W)_n )  )
    \\
    & \simeq
    \int_{n}
       \prod_{i_0, i_1, \cdots, i_n} 
       A(U_{i_0,i_1, \dots, i_n})_n  
    \\
    & =
    ker d_{C(U, A_\bullet)} \subset C(U,A_\bullet)_0
  \end{aligned}
  \,.
$$

Here

* The first step is the definition of morphism of [[presheaf|presheaves]] using the [[end]] notation;

* the second step is the definition of the [[nerve]] of of [[chain complexes]] applied to chain complex valued sheaves;

* the third step uses that the free simplicial abelian group functor is [[left adjoint]] to the forgetful one that remembers the underlying simplicial set;

* the fourth step then uses the [[Dold-Kan correspondence]], or actually just that the normalized [[Moore complex]] functor is [[left adjoint]] to the [[nerve]] of [[chain complexes]];

* the fifth step expresses the set of morphisms of [[chain complexes]] as an [[end]] (being itself a [[natural transformation]]);

* the sixth step uses the [[Fubini theorem]] of [[enriched category theory]] to commute the two [[ends]];

* the seventh step uses that the chain complex in the left argument is generated freely on elements of a set to rewrite the hom of abelian groups into one of sets;

* this finally allows to apply the [[Yoneda lemma]] in step eight

* and in step nine, by inspection, one notices that the result thus obtained is the set of 0-cycles in the &#268;ech complex $C(U,A_\bullet)$ as previously defined.

An entirely analogous argument shows that dividing out homotopies is respected. 

One starts by observing that the cohomology coboundaries are given by homotopies in the hom-simplicial set, i.e. by

$$
  Hom_{SPSh}(C(U) \times \Delta^1, N(A_\bullet))
  \,.
$$

With this one goes in the above computation.
After applying the 
[[Dold-Kan correspondence|Dold-Kan adjunction]]
we now have on the left in the integrand the term

$$
  N_\bullet(F(C(U)(W) \times \Delta^1))
  \,.
$$

Using first that the free simplicial group functor is monoidal and then that the normalized [[Moore complex]]
functor is lax monoidal (as described at 
[[Dold-Kan correspondence]])

> what to do about laxness versus pseudoness??

we get a morphism to that from 

$$
  N_\bullet(F(C(U)(W))) \otimes  N_\bullet(F(\Delta^1))
  \,.
$$

Using that the normalized Moore complex is 
isomorphic to the Moore complex divided by the part
generated by degenerate cells, 
on the right we identify the [[interval object]] complex

$$
   (  \cdots \to 0 \to I  \stackrel{1 \oplus -1}{\to} I \oplus I)
  \,.
$$

To see that one just needs to observe that the normalized [[Moore complex]] of the 1-[[simplex]] serves as an [[interval object]] in chain complexes.


=--

### Relation to abelian sheaf cohomology

For $A$ a complex of sheaves, there is a canonical morphism

$$
  \check{H}(X,A) \to H(X,A)
$$

from the &#268;ech cohomology to the full (hypercompleted) cohomology, which is [[abelian sheaf cohomology]] in the case that $A$ is in the image of the [[Dold-Kan correspondence|Dold-Kan map]] from [[chain complexes]]. Using the description of abelian sheaf cohomology in terms of morphisms out of hypercovers described at the beginning of this entry, this morphism is the obvious one coming from the inclusion of [[Čech covers]] into all [[hypercovers]].

+-- {: .num_theorem }
###### Theorem 

If $X$ is a [[paracompact space]] the canonical morphism

$$
  \check{H}(X,A) \to H(X,A)
$$

from &#268;ech cohomology to [[abelian sheaf cohomology]] is an isomorphism from every $A \in Sh(X, Ch_+)$.

=--

+-- {: .proof}
###### Proof

Recalled as theorem 1.3.13 in 

* Brylinski, _Loop spaces, characteristic classes and geometric quantization_ 

=--

When $X$ is not paracompact, we still have the following condition under which &#268;ech cohomology computes [[abelian sheaf cohomology]]-.


For $A$ a complex of sheaves, there is a canonical morphism

$$
  H_0(C(U,A)_\bullet) \to H(X,A)
$$


from the cohomology of the &#268;ech complex with respect to a cover $U$ with coefficients in $A$ to the [[abelian sheaf cohomology]] of $X$ with values in $A$. Using the description of abelian sheaf cohomology in terms of morphisms out of hypercovers described at the beginning of this entry, this morphism is the obvious one coming from the inclusion of [[Čech covers]] into all [[hypercovers]].

+-- {: .num_theorem }
###### Theorem 

Let $A$ be a complex of sheaves on $X$ concentrated
in a single degree $p \geq 0$, 
and let $\{U_i \to X\}$ be a [[cover]]
such that the $A$-cohomology of all intersections vanishes, 

$$
 \forall U_{i_0 , \cdots, i_k} H(U_{i_0, \cdots, i_k},A) = 0
$$

Then the canonical morphism

$$
  H_0(C(U,A)_\bullet) \to H(X,A)
$$

is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

One considers the spectral sequence associated with the &#268;ech double complex. Details are on page 28 of

* Brylinski, _Loop spaces, characteristic classes and geometric quantization_ 

=--




### Examples ###

We now list examples for abelian &#268;ech cohomology expressed in terms of the &#268;ech complex described above.



#### Line bundles ####

Let $G = U(1)$ be the circle group, an abelian
group. The [[nerve]] $N(\mathbf{B}G)$ 
of its [[delooping]] $\mathbf{B}G$ is the 
[[bar construction]] of $G$. This is equivalently
the nerve of the [[chain complex]] 

$$
  U(1)[1]
  := ( \cdots \to 0 \to U(1) \to 0 )
  \,.
$$

Equivalently we get the corresponding simplicial sheaves
and complexes of sheaves, eg

$$
  U(1)[1] : W \mapsto 
  ( \cdots \to 0 \to Hom(W,U(1)) \to 0 )
  \,.
$$

So given a cover $\{U_i \to X\}$ a &#268;ech cocycle is a collection

$$
  c = ( \{g_{i j} \in U(1)[1](U_{i j})\}|_{i,j})
$$

such that the &#268;ech differential evaluated on it

$$
  \begin{aligned}
    (d_{C(U,U(1)[1])} c)_{i j k}
    &=
    g_{j k}|_{U_{i j k}} - g_{i k}|_{U_{i j k}} 
    + g_{i j}|_{U_{i j k}} )
  \end{aligned}
$$

vanishes:

$$
  g_{i j}|_{U_{i j k}} + g_{j k}|_{U_{i j k}} = g_{i k}|_{U_{i j k}}
$$

for all $i, j, k$.

Here now we write plus signs for the operation in the abelian group $U(1)$ which above we have written by juxtaposition or using a dot. So up to notation for the group operation this is

$$
  g_{i j} g_{j k} = g_{i k}
$$

on $U_{i j k}$ as before in the nonabelian case of
&#268;ech cocycles for
$U(1)$-[[principal bundles]].

Here and from now on we shall notationally suppress the restriction maps $(-)|_{U_{i_0, i_1, \cdots, i_n}}$
as they are unambiguously obviuous in every case.


#### Line bundle gerbes 


Similarly by shifting $U(1)$ ever higher in chain degree,
one finds &#268;ech cocycles for [[bundle gerbes]], bundle 2-gerbes, etc.

A &#268;ech cocycle for 

$$
  U(1)[2]
  := ( \cdots \to 0 \to U(1) \to 0 \to 0 )
  \,.
$$

is 

$$
  c = ( \{g_{i j k} \in U(1)[2](U_{i j k})\}|_{i,j, k})
$$

such that on $U_{i,j,k,l}$ we have

$$
  g_{i j k} - g_{i j l} + g_{i k l} - g_{j k l} = 0
$$

which in the nonabelian context would be written as

$$
  g_{i j k} g_{i k l} = g_{i j l} g_{j k l}
  \,.
$$



#### &#268;ech-Deligne cohomology 

When refining the complexes of sheaves $U(1)[n]$
to the [[Deligne cohomology|Deligne complex]]

$$
  U(1)[n] \hookrightarrow \mathbb{Z}(n+1)_D^\infty
$$

and then evaluating &#268;ech cohomology with coefficients
in the Deligne complex, we obtain the formulas for
&#268;ech-Deligne cohomology.



* For $n = 1$ a cocycle is a collection
  $$
    ( A_i \in \Omega^1(U_i), 
      g_{i j} \in C^\infty(U_{i j}, U(1)) )
  $$
  such that for all $i, j$
  $$
    d log g_{i j} + A_i - A_j -  = 0
  $$
  and for all $i,j ,k$
  $$
    g_{i j} g_{j k} = g_{i k} 
    \,.
  $$
  Such cocycles classify $U(1)$-[[principal bundles]]
  with [[connection on a bundle|connection]].


  These $n=1$ &#268;ech-Deligne cocycles appear naturally in the study of the [[electromagnetic field]].

* For $n = 2$ a cocycle is a collection
  $$
    ( B_i \in \Omega^2(U_i), 
      A_{i j} \in \Omega^1(U_{i j}), 
      g_{i j k} \in C^\infty(U_{i j k}, U(1)) )
  $$
  such that for all $i, j$
  $$
    d A_{i j} + B_i - B_j = 0
  $$
  and for all $i,j ,k$
  $$
    A_{i j} - A_{i k} + A_{j k} + d log g_{i j k} = 0
  $$
  and for all $i, j, k ,l$

  $$
    g_{i j k} g_{i k l} = g_{i j l} g_{j k l}    
    \,.
  $$
  Such cocycles classify $U(1)$-[[bundle gerbes]]
  with connection.




## Related entries

* For discussion of the isomorphism between isomorphism classes of [[topological vector bundles]] and Cech cohomology on [[topological spaces]] with coefficients in continuous functions with values in the [[general linear group]] see [there](topological+vector+bundle#TransitionFunctionsAndCechCohomology).


## References 

A classical reference is

* Godement _Topologie alg&#233;brique et th&#233;orie de faisceaux_

A historical survey (of some aspects) is in 

* [[David Edwards]], Harold M. Hastings, _Cech Theory: Its past, present, and future_, Rocky Mountain J. Math. Volume 10, Number 3 (1980), 429-468. ([Euclid](http://projecteuclid.org/euclid.rmjm/1250128825))

A motivational introdcuction from within [[complex analytic geometry]] is in 

* Michael Weiss, _The Search for a Global Primitive -- Cech Cohomology with Coecients in a Sheaf_ ([pdf](http://files.meetup.com/4699592/cech-ipad.pdf))

A discussion of &#268;ech cohomology in the wider context of [[cohomology]] particularly realized in terms of the [[model structure on simplicial presheaves]] and with an emphasis on the shades of notions between [[Čech cover]] and [[hypercover]] is

* [[Tibor Beke]], _Higher &#268;ech theory_ ([journal](http://www.math.uiuc.edu/K-theory/0646/), [pdf](http://www.math.uiuc.edu/K-theory/0646/cech.pdf))

Abelian &#268;ech cohomology is discussed in some detail in section I.3 of 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_ 


A discussion of the [[model structure on simplicial presheaves]] with an eye towards the distinction between &#268;ech and hyperlocalization is in 

* [[Daniel Dugger]], _Sheaves and Homotopy theory_ ([web](http://math.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

(But beware that, while providing useful insights, these are unfinished abandoned notes that seem to have some gaps right at this point.)

A long list of reasons why higher &#268;ech cohomology might 
is after all better behaved than its [[hypercompletion]] where a cycle is with respect to an arbitrary [[hypercover]] is in section 6.5.4, **Descent versus Hyperdescent** of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The relation between smooth and continuous Cech cohomology is discussed in

* Christoph M&#252;ller, [[Christoph Wockel]], _Equivalences of smooth and continuous principal bundles with infinite-dimensional structure groups_, Advances in Geometry. Volume 9, Issue 4, Pages 605&#8211;626 (2009)

[[!redirects {?}ech cohomology]]
[[!redirects ?ech cohomology]]
[[!redirects ?ech cohomology]]
[[!redirects Cech cohomology]]