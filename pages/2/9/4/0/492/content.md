#Definition#

A Kan fibration is one of the notions of [[fibrations of simplicial sets]].

A _Kan fibration_ is a [[morphism]] $\pi : Y \to X$ of [[simplicial set|simplicial sets]] with the [[weak factorization system|lifting property]] for all [[horn]] inclusions.

This means that for 

$$
 \array{
   \Lambda^k[n] &\to& Y
   \\
   \downarrow && \downarrow^\pi
   \\
   \Delta^n &\to& X
 }
$$

a commuting square, there always exists a lift

$$
 \array{
   \Lambda^k[n] &\to& Y
   \\
   \downarrow &\nearrow& \downarrow^\pi
   \\
   \Delta^n &\to& X
 }
 \,.
$$

#Illustration#

Kan fibrations are combinatorial analogs of [[Serre fibration|Serre]] [[fibration]]s  of [[topological space]]s.  In fact, under the [[Quillen equivalence]] of the standard [[model structure on topological spaces]] and the standard [[model structure on simplicial sets]], Kan fibrations map to Serre fibrations.

Recall the shape of the [[horn]]s in low dimension. 

* -**$n=1$**- The horns $\Lambda^1_0$ and $\Lambda^1_1$ of the 1-[[simplex]] are just copies of the 0-[[simplex]] $\Delta^0$ regarded as the left and right endpoint of $\Delta^1$. For $n= 1$ the above condition says that for $\pi : Y \to X$ a Kan fibration we have
  $$
    \array{
       Y &\ni &
       y
       \\
      \downarrow^\pi
       \\
       X &\ni& \pi(y) &\stackrel{\forall f}{\to}& x
    }
    \;\;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;\;  
    \array{
       Y &\ni&
       y &\stackrel{\exists \hat f}{\to}& \exists \hat x
       \\
       \downarrow^\pi
       \\
       X &\ni& \pi(y) &\stackrel{f = \pi(\hat f)}{\to}& x = \pi(x)
    }
  $$
  corresponding to the lifting diagram
  $$
   \array{
     \Lambda_1^1 &\stackrel{y}{\to}& Y
     \\
     \downarrow &{}^{\hat f}\nearrow& \downarrow^\pi
     \\
     \Delta^1 &\stackrel{f}{\to}& X
   }
   \,.
  $$

* -**$n=2$**- the horn $\Lambda^2_1$ consists of the 
two top sides of a triangle. For this the Kan condition 
says that for any two composable 1-cells in $Y$ that
have a "composite up to a 2-cell" in $X$, there exists
a corresponding "composite up to a 2-cell" in $Y$ that
projects down to the one in $X$:

  $$
  \array{
    &&&&& y_2
    \\
    &&&& \nearrow && \searrow
    \\
    Y &\ni& & y_1 &&&& y_3
    \\
    \downarrow^\pi 
    \\
    X &\ni& &&& \pi(y_2)
    \\
    &&& & \nearrow &\Downarrow^{\forall h}& \searrow
    \\
    &&& \pi(y_1) &&\to&& \pi(y_2)
  }
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  \array{
    &&&&& y_2
    \\
    &&&& \nearrow &\Downarrow^{\exists \hat h}& \searrow
    \\
    Y &\ni& & y_1 &&\stackrel{\exists}{\to}&& y_3
    \\
    \downarrow^\pi 
    \\
    X &\ni& &&& \pi(y_2)
    \\
    &&& & \nearrow &\Downarrow^{h = \pi(\hat h)}& \searrow
    \\
    &&& \pi(y_1) &&\to&& \pi(y_2)
  }
  $$
  This corresponds to the lifting diagram
  $$
   \array{
     \Lambda_2^1 &\stackrel{y}{\to}& Y
     \\
     \downarrow &{}^{\hat h}\nearrow& \downarrow^\pi
     \\
     \Delta^2 &\stackrel{h}{\to}& X
   }
   \,.
  $$
  
  * Crucial is this condition for the _outer horns_ $\Lambda^n_0$ and $\Lambda^n_n$, where it says that the above works not only when edges are composable, but also when they meet just at  their sources or their targets. For instance for the horn $\Lambda^2_2$ the picture is
    $$
    \array{
      &&&&& y_2
      \\
      &&&& && \searrow
      \\
      Y &\ni& & y_1 &&\to&& y_3
      \\
      \downarrow^\pi 
      \\
      X &\ni& &&& \pi(y_2)
      \\
      &&& & \nearrow &\Downarrow^{\forall h}& \searrow
      \\
      &&& \pi(y_1) &&\to&& \pi(y_2)
    }
    \;\;\;\;\;\;
    \Rightarrow  
    \;\;\;\;\;\;
    \array{
      &&&&& y_2
      \\
      &&&& {}^\exists\nearrow &\Downarrow^{\exists \hat h}
      &    \searrow
      \\
      Y &\ni& & y_1 &&\stackrel{\exists}{\to}&& y_3
      \\
      \downarrow^\pi 
      \\
      X &\ni& &&& \pi(y_2)
      \\
      &&& & \nearrow &\Downarrow^{h = \pi(\hat h)}& \searrow
      \\
      &&& \pi(y_1) &&\to&& \pi(y_2)
    }
    $$
    This corresponds to the lifting diagram
    $$
     \array{
       \Lambda_2^2 &\stackrel{y}{\to}& Y
       \\
       \downarrow &{}^{\hat h}\nearrow& \downarrow^\pi
       \\
       \Delta^2 &\stackrel{h}{\to}& X
     }
     \,.
    $$


#Quasi-fibration#

A **quasi-fibration** or **weak Kan fibration** or **inner Kan fibration** of simplicial sets is defined as above, but with the lifting property only imposed in _inner horns_: $\Lambda^n_k$ with $0 \lt k \lt (n-1)$, not the _outer horns_ $\Lambda^n_0$ and $\Lambda^n_n$.

This weakened condition then says that _composition_ of cells may be lifted through the quasi-fibration, but not necessarily [[inverse|inversion]] of 1-cells.

# Left and right Kan fibration #

Similarly, a **left Kan fibration** is one that has the lifting property for all horns except possibly the last one.
and a **right Kan fibration** is one that has the lifting property for all horns except possibly the first one.


#Properties#

+-- {: .un_theorem}
###### Theorem

The morphisms $f : X \to Y$ of Kan complexes that are both Kan fibrations as well as [[model structure on simplicial sets|weak equivalences]] in that they induce isomorphisms on all [[simplicial homotopy group]]s (i.e. the **acyclic fibrations** of Kan complexes) are precisely the morphisms that have the [[weak factorization system|right lifting property]] with respect to all [[boundary of a simplex|boundary inclusions]] $\partial \Delta^n \hookrightarrow \Delta^n$:
  $$
    \array{
      \partial \Delta[n] &\to& X
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^f 
      \\
      \Delta[n] &\to& Y
    }
    \,.
  $$

=--

+-- {: .proof}
###### Proof

A proof is in chapter I of

* Goerss-Jardine, _Simplicial homotopy theory_. Explicitly, it is theorem 7.10 [here](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi).

=--

+-- {: .un_cor}
###### Corollary

Kan fibrations and acyclic Kan fibrations are both stable under [[pullback]].

=--

+-- {: .proof}
###### Proof

Because every class of morphisms defined by a [[weak factorization system|right lifting property]] is stable under pullback.

=--

**Remark** From this it follows readily that [[Kan complex]]es form a Brownian [[category of fibrant objects]].


Let $C, D$ be ordinary [[nLab:groupoid|groupoid]]s and $N(C)$, $N(D)$ their ordinary [[nLab:nerve|nerve]]s. We'd like to show in detail that 

+-- {: .un_theorem}
###### Theorem

A [[nLab:functor|functor]] $F : C \to D$ is 

* [[nLab:k-surjective functor|k-surjective]] for all $k$ and hence a surjective [[nLab:equivalence of categories|equivalence of categories]] precisely if under the [[nLab:nerve|nerve]] $N(F) : N(C) \to N(D)$ it induces an acyclic fibration of Kan complexes;

=--

+-- {: .proof}
###### Proof

We know that both $N(C)$ and $N(D)$ are Kan complexes. By the above theorem it suffices to show that $N(f)$ being a surjective equivalence is the same as having all lifts

$$
  \array{
    \delta \Delta[n] &\to& N(C)
    \\
    \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
    \\
    \Delta[n] &\to& N(D)
  }
  \,.
$$


We check successively what this means for increasing $n$:

* $n= 0$. In degree 0 the boundary inclusion is that of the empty set into the [[nLab:point|point]] $\emptyset \hookrightarrow {*}$. The lifting property in this case amounts to saying that every point in $N(D)$ lifts through $N(F)$. 
  $$
    \array{
      \emptyset &\to& N(C)
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \Leftrightarrow
    \array{
      && N(C)
      \\
      &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \,.
  $$
  This precisely says that $N(F)$ is surjective on 0-cells and hence that $F$ is surjective on objects.

* $n=1$. In degree 1 the boundary inclusion is that of a pair of points as the endpoints of the interval
  $\{\circ, \bullet\} \hookrightarrow \{\circ \to \bullet\}$. The lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ all elements in $Hom(F(a),F(b))$ are hit. Hence that $F$ is a [[nLab:full functor|full functor]].

* $n=2$. In degree 2 the boundary inclusion is that of the triangle as the boundary of a filled triangle. It is sufficient to restrict attention to the case that the map $\partial \Delta[2] \to N(C)$ sends the top left edge of the triangle to an identity. Then the lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ the map $F_{a,b} : Hom(a,b) \to Hom(F(a),F(b))$ is injective. Hence that $F$ is a [[nLab:faithful functor|faithful functor]].
  $$
    \left(
    \array{
      && a 
      \\
      & {}^{Id_a}\nearrow && \searrow^{f}
      \\
      a &&\stackrel{g}{\to}&& b
    }
    \right)
    \stackrel{N(F)}{\mapsto}
    \left(
    \array{
      && a 
      \\
      & {}^{Id_a}\nearrow &\Downarrow^=& \searrow^{F(f)}
      \\
      a &&\stackrel{F(g)}{\to}&& b
    }
    \right)
  $$


=--






#Relation to other concepts#

* Kan fibrations and quasi-fibrations are fibrations in two common [[model structure on simplicial sets|model structures on simplicial sets]].

* Recall that the [[horn]] $\Lambda^k[n]$ is the boundary of the $n$-[[simplex]] $\Delta^n$ with one face removed. If in the above definition one replaces horns with the full boundaries of simplices, one obtaines the definition of a [[hypercover]], the acyclic fibrations in the classical [[model structure on simplicial sets]].

* A simplicial set $X$ for which the unique morphism $X \to pt$ to the [[terminal object|terminal simplicial set]] is a Kan fibration is called a [[Kan complex]].

* A simplicial set $X$ for which the unique morphism $X \to pt$ to the [[terminal object|terminal simplicial set]] is a quasi-fibration/weak Kan fibration is called a [[quasi-category]].

* Just as the underlying simplicial set of a [[simplicial group]] is a [[Kan complex]] (see algorithm at [[simplicial group]]), so also given any simplicial morphism $f : G\to H$ of simplicial groups for which in each dimension, $n$, the homomorphism $f_n : G_n \to H_n$ is an [[epimorphism]], then the underlying simplicial map of simplicial sets is a Kan fibration. (Apart from a careful choice of section in each dimension, the proof can be constructed from the algorithm given in [[simplicial group]].)

* A morphism of simplicial sets that has the left [[lifting property]] with respect to all Kan fibrations is called an [[anodyne morphism]].


[[!redirects left Kan fibration]]
[[!redirects inner Kan fibration]]
[[!redirects right Kan fibration]]
[[!redirects weak Kan fibration]]
[[!redirects left fibration]]
[[!redirects inner fibration]]
[[!redirects right fibration]]
[[!redirects weak fibration]]
