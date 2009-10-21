<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

# Contents #

* automatic table of contents
{:toc}


A _string structure_ on a [[manifold]] is a higher version of a [[spin structure]]. A string structure on a [[manifold]]  with [[spin structure]] given by a [[Spin group]]-[[principal bundle]] to which the [[tangent bundle]] is [[associated bundle|associated]] is a lift $\hat g$ of the classifying map $g : X \to \mathcal{B} Spin(n)$ through the  third nontrivial step $\mathcal{B}String(n) \to \mathcal{B}String(n)$ in the [[Whitehead tower]] of $O(n)$ to a [[String group]]-[[principal bundle]]:

$$
  \array{
    && \mathcal{B}String(n)
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathcal{B}Spin(n)
  }
$$

A lift one further step through the Whitehead tower is a [[Fivebrane structure]].

This has generalizations to the smooth context, where instead of the topological String-group one uses the [[String Lie 2-group]].

## Definition ##

Let $X$ be an $n$-dimensional manifold. 
Its tangent [[bundle]] is canonically associated to a $O(n)$-principal bundle, which is in turn classified by a map

$$
  X \to B O(n)
$$

from $X$ to the [[classifying space]] of the group $O(n)$.

* A **String structure** on $X$ is the choice of a lift of this map a few steps through the [[Whitehead tower]] of $O(n)$.

* The manifold "is string" if such a lift exists.

This means the following:

* there is a canonical map $w_1 : B O(n) \to B\mathbb{Z}_2$ from the [[classifying space]] of $O(n)$ to that of $\mathbb{Z}_2 = \mathbb{Z}/2\mathbb{Z}$ that represents the generator of the cohomology $H^1(B O(n), \mathbb{Z}_2)$. The classifying space of the group $SO(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B SO(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B O(n) &\stackrel{w_1}{\to}& \mathbb{B}\mathbb{Z}_2
   }
  $$
  Namely using the [[homotopy hypothesis]] (which is a theorem, recall), we may identify $B O(n)$ with the one object [[groupoid]] whose space of morphisms is $O(n)$ and similarly for $ B \mathbb{Z}_2$. Then the map in question is the one induced from the group homomorphism that sends orientation preserving elements in $O(n)$ to the identity and orientation reversing elements to the nontrivial element in $\mathbb{Z}_2$.

  * an **[[orientation]]** on $X$ is a choice of lift of the structure group through $B SO(n) \to B O(n)$
  $$
   \array{
    && B SO(n)
    \\
    & {}^{orientation}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B O(n)
   }
   \,.
  $$

* there is a canonical map $w_2 : B SO(n) \to B^2 \mathbb{Z}_2$ representing the generator of $H^2(B SO(n), \mathbb{Z}_2)$. The classifying space of the group $Spin(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B Spin(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B SO(n) &\stackrel{w_2}{\to}& \mathbb{B}^2\mathbb{Z}_2
   }
  $$

  * a **[[spin structure]]** on an oriented manifold $X$ is a choice of lift of the structure group through $B Spin(n) \to B SO(n)$
  $$
   \array{
    && B Spin(n)
    \\
    & {}^{spin structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B SO(n)
   }
   \,.
  $$

* there is a canonical map $B Spin(n) \to B^3 U(1)$ The classifying space of the group $String(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B String(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B Spin(n) &\stackrel{\frac{1}{2}p_1}{\to}& \mathbb{B}^3 U(1)
   }
  $$

  * a **string structure** on an oriented manifold $X$ is a choice of lift of the structure group through $B String(n) \to B Spin(n)$
  $$
   \array{
    && B String(n)
    \\
    & {}^{string structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B Spin(n)
   }
   \,.
  $$

* there is a canonical map $B String(n) \to B^7 U(1)$ The classifying space of the group $Fivebrane(n)$ is the [[generalized universal bundle|homotopy pullback]]
  $$
   \array{
    B Fivebrane(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B String(n) &\stackrel{\frac{1}{6}p_2}{\to}& \mathbb{B}^7 U(1)
   }
  $$

  * a **[[fivebrane structure]]** on an string manifold $X$ is a choice of lift of the structure group through $B Fivebrane(n) \to B String(n)$
  $$
   \array{
    && B Fivebrane(n)
    \\
    & {}^{fivebrane structure}\nearrow& \downarrow 
    \\
    X &\stackrel{}{\to}& B String(n)
   }
   \,.
  $$


## Description in terms of classes on the total space ##

One can reformulate an

* [[orientation]]-
 
* [[spin structure|Spin]]-

* [[string structure|String]]-

* [[fivebrane structure|Fivebrane]]-

structure in terms of the existence of a certain class on the total space of the given bundle.

We write this out for the case of string structures, all other cases work entirely analogously.


Let $X$ be an oriented Spin manifold and let $P \to X$ be the corresponding $Spin(n)$-bundle. Notice that this, like any principal bundle (see [[generalized universal bundle]], [[principal bundle]] and [[principal infinity-bundle]]) is the [[homotopy limit|homotopy pullback]] 

$$
  \array{
    P &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{}{\to}& B Spin(n)
  }
$$
of the point along the classifying map from $X$ to the [[classifying space]] $B Spin(n)$.

In other words, there is a [[fibration sequence]]

$$
  \cdots 
  \to
  (\Omega B Spin = Spin(n))
  \to
  P
  \to 
  X 
  \to
  B Spin(n)
  \,.
$$

If now $X$ does admit a String structure, i.e. a decomposition of $X \to B Spin(n)$ into a map $X \to B String(n) \to B Spin(n)$ then we obtain the following diagram, where each square is a [[homotopy limit|homotopy pullback]]

$$
  \array{
    String &\to& \hat P &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Spin &\to& P &\to&  B^2 U(1) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& X &\to& B String(n) &\to& B Spin(n)
  }
$$

The map $P \to B^2 U(1)$ appears by decomposing the homotopy pullback of the point along $X \to B Spin(n)$ into a homotopy pullback first along $B String(n) \to B Spin(n)$ and then along $X \to B String(n)$ using the given String structure. The rest of the diagram is constructed in order to prove the following:

* The class in $H^3(P, \mathbb{Z})$ represented by $P \to B^2 U(1)$ has the property that restricted to the fibers of the $Spin(n)$-principal bundle $P$ it becomes the generating class in $H^3(Spin(n), \mathbb{Z})$.

**Proof**. 

Here $\hat P \to X$ denotes the $String(n)$-principal bundle classified by $X \to B String(n)$.

This uses 

* the fact that pasting compositites of homotopy pullbacks are again homtopy pullbacks.

* the fact that the homotopy pullback of the point to itself produces the [[loop space object]], e.g.
  $$
    \array{
      \Omega B Spin(n) \simeq Spin(n) &\to& {*}
      \\
      \downarrow && \downarrow
      \\
      {*} &\to& B Spin
    }
  $$


## References ##

The relevance of String structures (like that of Spin structures half a century before) was recognized in the physics of spinning strings, therefore the name.

String stuctures had originally been mostly discussed in terms of their transgressions to loop spaces

* Killingback, Witten 

  * blog entry on [String(n)](http://golem.ph.utexas.edu/string/archives/000572.html)

later it was reformulated in terms of the classes down on base space just mentioned in

* Stolz, Teichner, [What is an elliptic object](http://math.ucr.edu/home/baez/qg-winter2007/Oxford.pdf).

The relation between the two pictures is analyzed for instance in

* Asada ...

For discussion of String-structures using 3-classes on total spaces see for instance the work by Corbett Redden and Konrad Waldorf described at 

* [[Oberwolfach Workshop, June 2009 -- Friday, June 12]]


[[!redirects String structure]]
[[!redirects String-structure]]
[[!redirects string-structure]]