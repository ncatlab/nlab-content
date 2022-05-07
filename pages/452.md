
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Content#
* table of contents
{:toc}

## Idea

The concept of _crossed modules_  of groups ([Whitehead 41](#Whitehead41), [Whitehead 49](#Whitehead49)) is a basic concept in [[homotopical algebra]] and [[homological algebra]]: It is (from the [[nPOV]]) a convenient way of encoding a [[strict 2-group]] $G$ in terms of a [[homomorphism]] $\partial : G_2 \to G_1$ of two ordinary [[groups]].

From other points of view it is:

*  like the inclusion of a [[normal subgroup]], but isn\'t an inclusion in general;

*  like a [[module]] with a twisted 'multiplication';

*  like an [[action]] by [[automorphisms]] on a group;

*  a [[crossed complex]] concentrated in degrees $1$ and $2$;

*  a nonabelian [[chain complex|chain-complex]] of length 2;

*  a [[Moore complex]] of certain [[simplicial groups]].

Historically, crossed modules were among the first examples of [[higher dimensional algebra]] to be studied.

## Definition

### Diagrammatic definition


\begin{defn}\label{DiagrammaticDefinition}
A **crossed module of groups** is

* a [[pair]] of [[groups]] $G_2, G_1$,

* a [[group homomorphism]]

  $$
    G_2 
      \overset{
        \delta
       }{
         \longrightarrow
       }
    G_1
  $$ 

* a [[group homomorphism]] from $G_1$ to the [[automorphism group]] of $G_2$:

  $$
    G_1 
      \overset{
        \alpha
      }{
        \longrightarrow
      } 
      Aut(G_2)
      \,,
  $$ 

  which we may equivalently regard as a [[function]]

  $$
    \alpha 
     \;\colon\;
     G_1 \times G_2 
       \longrightarrow 
     G_2
   $$ 

   (out if the [[Cartesian product]] of underlyings [[sets]]/[[objects]])

   that satisfies the $G_1$-[[action]] property and is such that for every $g_1 \in G_1$ it is a group [[automorphism]] of $G_2$;

such that the following [[commuting diagram|diagrams commute]]:

$$
  \array{
    G_2 \times G_2
    &&
      \overset{
        \delta \times Id
      }{
        \longrightarrow
      }
    &&
    G_1 \times G_2
    \\
    & 
    {}_{\mathllap{Ad}}
    \searrow 
    && 
    \swarrow_{\mathrlap{\alpha}}
    \\
    &&
    G_2
  }
$$


and

$$
  \array{
    G_1 \times G_2 
    &
      \stackrel{
        \alpha
      }{
        \longrightarrow
      }
    & 
    G_2
    \\
    \big\downarrow^{
      \mathrlap{Id \times \delta}
    } 
    && 
    \big\downarrow^{
      \mathrlap{\delta}
    }
    \\
    G_1 \times G_1 
    &
      \stackrel{
        Ad
      }{
        \longrightarrow
      }
    & 
    G_1    
    \,,
  }
$$
where $Ad$ denotes the [[adjoint action]] of $G_2$ on itself.
\end{defn}

\begin{remark}
The diagrammatic Def. \ref{DiagrammaticDefinition} makes sense  [[internalization|internal]] to any [[cartesian monoidal category]] $\mathcal{C}$:

* for $\mathcal{C}=$ [[Sets]] we get bare crossed modules of [[discrete groups]];

* for $\mathcal{C}=$ [[SmoothManifolds]] we get crossed modules of [[Lie groups]];

  if one allows [[infinite-dimensional manifolds]] here then this subsumes crossed modules of [[Kac-Moody groups]] such as appear in models for the [[String 2-group]].

\end{remark}


Alternatively, one can take another tack, and define crossed module objects in categories that support enough structure without using internal groups, the most general case of which, in practice, are [[semiabelian categories]]. There one considers the objects to behave 'like groups' in the sense that the category they form looks very much like the category of groups. Janelidze ([Janelidze 2003](#Janelidze_03)) defined the notion of internal crossed module in a semiabelian category (so that in the prototypical example of the category of groups, they reduce to the above notion). 

A key result, also due to ([Janelidze 2003](#Janelidze_03)) and generalising the Brown-Spencer theorem from the case of ordinary crossed modules, is the following:

+-- {: .num_theorem}
###### Theorem
**(Janelidze's Brown-Spencer theorem).**
Let $C$ be a [[semiabelian category]]. Then the category $XMod(C)$ of crossed modules in $C$ is equivalent to the category $Gpd(C)$ of internal groupoids in $C$.
=--

Here the notion of [[internal groupoid]] is the usual diagrammatic notion.

### Definition in terms of equations

The two [[diagrams]] can be translated into [[equations]], which may often be helpful.

*   If we write the effect of acting with $g_1\in G_1$ on $g_2\in G_2$ as ${}^{g_1}g_2$, then the second diagram translates as the equation:
    $$\delta({}^{g_1}g_2) = g_1\delta(g_2)g_1^{-1}.$$
In other words, $\delta$ is equivariant for the action of $G_1$. 

*   The first diagram is slightly more subtle.  The group $G_2$ can act on itself in two different ways, (i) by the usual conjugation action, ${}^{g_2}g^\prime_2=g_2g^\prime_2g_2^{-1} $ and (ii) by first mapping $g_2$ down to $G_1$ and then using the action of that group back on $G_2$.  The first diagram says that the two actions coincide. Equationally this gives:
$${}^{\delta(g_2)}g^\prime_2 = g_2g^\prime_2g_2^{-1}.$$
This equation is known as the **Peiffer rule** in the literature.
Another way to interpret it is to rewrite it slightly:
$${}^{\delta(g_2)}g^\prime_2 g_2 = g_2g^\prime_2$$
The Peiffer rule can thus be seen as a 'twisted commutativity law' for $G_2$.

### Morphisms {#Morphisms} 

For $G$ and $H$ two [[strict 2-group]]s coming from crossed modules $[G]$ and $[H]$, a morphism of strict 2-groups $f : G \to H$, and hence a morphism of crossed modules $[f] : [G] \to [H]$ is a [[2-functor]]

$$
  \mathbf{B}f : \mathbf{B}G \to \mathbf{B}H
$$

between the corresponding [[delooping|delooped]] [[2-groupoid]]s. Expressing this in terms of a diagram of the ordinary groups appearing in $[G]$ and $[H]$ yields a diagram called a [[butterfly]]. See there for more details.



## Examples

* For $H$ any group, its [[automorphism]] crossed module is 

  $$
    AUT(H) := (G_2 = H, G_1 = Aut(H), \delta = Ad, \alpha = Id)
   \,.
  $$ 

  Under the equivalence of crossed modules with [[strict 2-group]]s this corresponds to the [[automorphism 2-group]] 
 
  $$
    Aut_{Grpd}(\mathbf{B}H)
  $$ 

  of [[automorphism]]s in the category [[Grpd]] of [[groupoid]]s on the one-object [[delooping]] [[groupoid]] $\mathbf{B}H$ of $H$.

*  Almost the canonical example of a crossed module is given by a group $G$ and a [[normal subgroup]] $N$ of $G$.  We take $G_2 = N$, and $G_1 = G$ with the action $\alpha$ being the [[conjugation action]], whilst $\delta$ is the given inclusion, $N \hookrightarrow G$. 

  This is 'almost canonical', since if we replace the groups by simplicial groups $G_.$ and $N_.$, then $(\pi_0(G_.),\pi_0(N_.),\pi_0(inc))$ is a crossed module, and given any crossed module, $(C,P,\delta)$, there is a simplicial group $G_.$ and a normal subgroup $N_.$, such that the construction above gives the given crossed module up to isomorphism.

* Another standard example of a crossed module is $M \to ^0 P$ where $P$ is a group and $M$ is a $P$-module. Thus the category of modules over groups embeds in the category of crossed modules. 

* If $\mu: M \to P$ is a crossed module with cokernel $G$, and $M$ is abelian, then the operation of $P$ on $M$ factors through $G$. In fact such crossed modules in which both $M$ and $P$ are abelian should not be sneezed at! A good example is $\mu: C_2 \times C_2 \to C_4$ where $C_n$ denotes the cyclic group of order $n$, $\mu$ is injective on each factor, and $C_4$ acts on the product by the twist.  This crossed module has a [[classifying space]] $X$ with fundamental and second homotopy groups $C_2$ and non trivial $k$-invariant in $H^3(C_2, C_2)$, so $X$ is not a product of [[Eilenberg-MacLane space]]s.  However the crossed module is an algebraic model and so one one can do algebraic constructions with it. It  gives in some ways a better feel for the space than the $k$-invariant. The [[higher homotopy van Kampen theorem]] implies that   the above $X$ gives the 2-type of the [[mapping cone]] of the map of [[classifying space]]s $BC_2 \to BC_4$. 


* Suppose $F\stackrel{i}{\to}E\stackrel{p}{\to}B$ is a [[fibration sequence]]

  of [[pointed object|pointed spaces]], thus $p$ is a [[fibration]] in the [[model structure on topological spaces|topological sense]] (lifting of paths and homotopies of paths will suffice), $F = p^{-1}(b_0)$, where $b_0$
  is the basepoint of $B$.  The fibre $F$ is pointed at $f_0$, say, and $f_0$
  is taken as the basepoint of $E$ as well.

    There is an induced map on [[homotopy group]]s

    $$\pi_1(F) \stackrel{\pi_1(i)}{\longrightarrow} \pi_1(E)$$ 

    and if $a$ is a loop in $E$ based at $f_0$, and $b$ a loop in $F$ based at $f_0$, then the composite path corresponding to $a b a^{-1}$ is [[homotopy|homotopic]] to one wholly within $F$.  To see this, note that $p(a b a^{-1})$ is [[null homotopic loop|null homotopic]].  Pick a [[homotopy]] in $B$ between it and the constant map, then lift that homotopy back up to $E$ to one starting at $a b a^{-1}$.  This homotopy is the required one and its other end gives a well defined element ${}^a b \in \pi_1(F)$ (abusing notation by confusing paths and their homotopy classes).  With this action $(\pi_1(F), \pi(E), \pi_1(i))$ is a crossed module.  This will not be proved here, but is not that difficult.  (Of course,  secretly, this example is 'really' the same as the previous one since a fibration of [[simplicial group]]s is just morphism that is an [[epimorphism]] in each degree, and the [[fibration sequence|fibre]] is thus just a [[simplicial group|normal simplicial subgroup]]. What is fun is that this generalises to 'higher dimensions'.)  

* A particular case of this last example can be obtained from the inclusion of a subspace $A\to X$ into a pointed space $(X,x_0)$, (where we assume $x_0\in A$).  We can replace this inclusion by  a homotopic fibration, $\overline{A}\to X$ in 'the standard way', and then find that the fundamental group of its fibre is $\pi_2(X,A,x_0)$. 

A deep theorem of J.H.C. Whitehead is that the crossed module 

 $$\delta: \pi_2(A \cup \{e^2_\lambda\}_{\lambda \in \Lambda},A,x) \to \pi_1(A,x)$$

 is the [[free crossed module]]  on the characteristic maps of the $2$-cells. One utility of this is that it enables the  expression of  nonabelian chains and boundaries ideas in dimensions $1$ and $2$: thus for the standard picture of a Klein Bottle formed by identifications from a square $\sigma$ the formula 

$$\delta \sigma = a+b-a +b $$

makes sense with $\sigma$ a generator of a free crossed module; in the usual abelian chain theory we can write only $\partial \sigma =2b$, thus losing information. 

Whitehead's proof of this theorem used knot theory and transversality. The theorem is also a consequence of the $2$-dimensional Seifert-van Kampen Theorem, proved by Brown and Higgins, which states that the functor
 
$\Pi_2$: (pairs of pointed spaces) $\to$ (crossed modules) 

preserves certain colimits (see reference below).  


This last example was one of the first investigated by Whitehead and his proof appears also in a little book by [[Hilton]]; see also [[Nonabelian algebraic topology]], however the more general result of Brown and Higgins determines also the group $\pi_2(X \cup CA,X,x)$ as a crossed $\pi_1(X,x)$ module, and then Whitehead's result is the case with $A$ is a wedge of circles. 



## Related concepts 

* [[group]]

* [[2-group]], **crossed module**, [[differential crossed module]]

* [[3-group]], [[2-crossed module]] / [[crossed square]], [[differential 2-crossed module]]

* [[n-group]]

* [[∞-group]], [[simplicial group]], [[crossed complex]], [[hypercrossed complex]]



## References
 {#References}

The second axiom for a crossed module first appeared as footnote 35 on p. 422 of Whitehead's paper:

* {#Whitehead41} [[J.H.C. Whitehead]], On adding relations to homotopy groups. Ann. of Math. (2) 42 (1941) 409–428. 

Section 16 of the following paper 

*  {#Whitehead49} [[J. H. C. Whitehead]],  _Combinatorial Homotopy II_, Bull. Amer. Math. Soc., 55 (1949), 453--496.

proved a key result on "Free crossed modules". An exposition of this proof is in

* [[R. Brown]], _On the second relative homotopy group of an adjunction space: an exposition of a theorem of J.H.C. Whitehead_,   J. London Math. Soc._ (2) 22 (1980) 146-152 ([doi:10.1112/jlms/s2-22.1.146](https://doi.org/10.1112/jlms/s2-22.1.146))

see also

* [[Peter J. Hilton]], _An Introduction to Homotopy Theory_, Cambridge University Press 1953. 

Note that the geometric core of the proof uses [[knot theory]] and transversality arguments which come from the "previous paper" of Whitehead:


*  _On adding relations to  homotopy groups_, Annals of Math., 42 (1941) 400-428. 
 
The following paper 

* [[Ronnie Brown]], [[Philip Higgins]], _On the connections between the second relative homotopy groups of some related spaces_,  _Proc. London Math.  Soc._ (3) 36 (1978) 193-212.

showed that the theorem of Whitehead on free crossed modules from CH II Sec 16 is a special case of a 2-dimwensional Van Kampen type Theorem for the homotopy crossed modules  (over groupoids) of open unions of "connected" triples $(X,A,S$ of spaces where $S$ is a set of base points. However the proof of the main theorem uses the relation of crossed modules not to cat$^1$-groups but to "double groupoids with connections", also proved with Spencer. full details and references re  in Part I of: 


* [[Ronnie Brown]], [[Philip Higgins]], and R. Sivera, _[[Nonabelian Algebraic Topology]]: Filtered spaces, Crossed Complexes, Cubical Homotopy Groupoids_, EMS Tracts in Mathematics, Vol. 15, (2011). 

See also 

* [[Ronnie Brown]], _Groupoids and crossed objects in algebraic topology_,  Homology, Homotopy and Applications, 1 (1999) 1-78.

* {#Janelidze_03} [[George Janelidze]], _Internal crossed modules_, Georgian Mathematical Journal **10** (2003) pp 99-114. ([EuDML](https://eudml.org/doc/51553))


For wider uses of crossed modules in other algebraic contexts see for example 

* A. S-T. Lue, _Cohomology of groups relative to a variety_, J. Algebra 69 (1) (1981) 155–174.

[[!redirects crossed modules]]
