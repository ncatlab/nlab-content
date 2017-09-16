#Definition#

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
  
    * Crucial is this condition for the _outer horns_ $\Lambda^n_0$ and $\Lambda^n_n$, where it says that the above works not only when edges are composable, but also when they mit with their sources or their targets. For 
instance for the horn $\Lambda^2_2$ the picture is
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

A _quasi-fibration_ or _weak Kan fibration_ of simplicial sets is defined as above, but with the lifting property only imposed in _inner horns_: $\Lambda^n_k$ with $0 \lt k \lt (n-1)$, not the _outer horns_ $\Lambda^n_0$ and $\Lambda^n_n$.

This weakened condition then says that _composition_ of cells may be lifted through the quasi-fibration, but not necessarily [[inverse|inversion]] of 1-cells.


#Relation to other concepts#

* Kan fibrations and quasi-fibrations are fibrations in two common [[model structure on simplicial sets|model structures on simplicial sets]].

* Recall that the [[horn]] $\Lambda^k[n]$ is the boundary of the $n$-[[simplex]] $\Delta^n$ with one face removed. If in the above definiion one replaces horns with the full boundaries of simplices, one obtaines the definition of a [[hypercover]], the acyclic fibrations in the classical [[model structure on simplicial sets]].

* A simplicial set $X$ for which the unique morphism $X \o pt$ to the [[terminal object|terminal simplicial set]] is a Kan fibration is called a [[Kan complex]].

* A simplicial set $X$ for which the unique morphism $X \to pt$ to the [[terminal object|terminal simplicial set]] is a quasi-fibration/weak Kan fibration is called a [[quasi-category]].
