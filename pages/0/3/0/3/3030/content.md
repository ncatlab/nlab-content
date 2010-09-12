
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


* [[group cohomology]]

  * **nonabelian group cohomology**, [[groupoid cohomology]]

* [[group extension]]

* [[Lie group cohomology]] 

  * [[∞-Lie groupoid cohomology]]

***


This entry largely discusses [[Schreier theory]] of nonabelian [[group extension]]s -- but from the [[nPOV]].


#Contents#
* automatic table of contents goes here
{:toc}


## Idea and Definition

By the [[category theory|general nonsense]] of [[cohomology]], the _abelian_ [[group cohomology]] in degree $k \in \mathbb{N}$ of a [[group]] $G$ with coefficients in an abelian group $K$ is the set of equivalence classes of [[morphism]]s

$$
  H^n(G,K) = \{ \mathbf{B}G  \to \mathbf{B}^n K \}_\sim
$$

in the [[(∞,1)-category]] [[? Grpd]], from the [[delooping]] $\mathbf{B}G$ of $G$ to the $n$-fold delooping $\mathbf{B}^n K$ of $K$.

However, if the group $K$ is not abelian, then its $n$-fold delooping does not exist for $n \geq 2$, so accordingly the above does not give a prescription for cohomology of $G$ with coefficients in a nonabelian group $K$ in degree greater than 1 (and in degree 1 group cohomology it is not very interesting).

But for nonabelian $K$ there are higher groupoids that _approximate_ the non-existing higher deloopings. Nonabelian group cohomology is the [[cohomology]] of $\mathbf{B}G$ with coefficients in such approximations.

More precisely, notice that for $n=2$ and $K$ abelian, the $n$-fold [[delooping]] $\mathbf{B}^2 K$ is the strict [[2-groupoid]] whose corresponding [[crossed complex]] is

$$
  [\mathbf{B}^2 K]
  = 
  \left(
    K \to {*} \stackrel{\to}{\to} {*}
  \right)
  \,.
$$

But for every [[group]] $K$ there is also its [[2-group|automorphism 2-group]] $AUT(K)$. Its delooping corresponds to the [[crossed complex]]

$$
  [\mathbf{B} AUT(K)]
  =
  \left(
    K \stackrel{\delta = Ad}{\to} Aut(K) \stackrel{\to}{\to}
    {*}
  \right)
  \,,
$$

where the boundary map $\delta$ is the one that sends an element $k \in K$ to the automorphism $Ad(k) : k' \mapsto k k' k^{-1}$.

So this looks much like $\mathbf{B}^2 K$ (when that exists) only that it has more elements in degree 1.

Accordingly, what is called nonabelian group cohomology of $G$ with coefficients in $K$ is the set of equivalence classes of morphisms

$$
  H^2_{nonab}(G,K) := \{ \mathbf{B}G \to \mathbf{B}AUT(K) \}_\sim
  \,.
$$

Notice that when $K$ has nontrivial [[automorphism]]s, this differs in general from the ordinary degree 2 abelian group cohomology even if $K$ is abelian.

It is a familiar fact that abelian group cohomology classifies (shifted) central [[group extension]]s. This is really nothing but the statement that to a morphism $\mathbf{B}G \to \mathbf{B}^n K$ we may associate its [[fibration sequence]]

$$
  \array{
    \mathbf{B}^{n-1} K& \to&\mathbf{B}\hat G &\to& {*}
    \\
    \downarrow &&\downarrow && \downarrow 
    \\
    {*}& \to& \mathbf{B}G &\to& \mathbf{B}^n K
  }
$$

(where both squares are [[homotopy pullback]] squares). In particular, for $n = 2$ we get ordinary central extensions

$$
  \mathbf{B}K \to \mathbf{B}\hat G \to \mathbf{B}B
  \,.
$$

which may be looped to yield exact sequences of morphisms of groups

$$
  K \to \hat G \to B
  \,.
$$

In [[Schreier theory]] one notices that similarly nonabelian group cohomology in degree 2 classifies nonabelian [[group extension]]s, i.e. sequences

$$
  K \to \hat G \to G
  \,.
$$

As we shall discuss below, by following the [[category theory|abstract nonsense]] as described above, nonabelian degree 2 cocycles really classify something slightly richer, namely exact sequences of groupoids

$$
  Aut(K)//K \to Aut(K)//\hat G \to {*}//G
  \,,
$$

where the double slashes denote [[action groupoid]]s (and ${*}//G = \mathbf{B}G$).


In the existing literature -- which does not usually present the picture quite in the way we are doing here -- nonabelian group cohomology is rarely considered beyond degree 2. But the picture does straightforwardly generalize. For instance degree 3 nonabelian cohomology of $G$ with coefficients in $K$ may be taken to be the [[cohomology]] of $\mathbf{B}G$ with coefficients in the 3-groupoid $\mathbf{B}AUT(AUT(K))$.

$$
  H^3_{nonab}(G,K) = \{\mathbf{B}G \to \mathbf{B}AUT(AUT(K))\}_\sim
  \,.
$$

And so on.


## Details

We work out in detail what nonabelian group cocycles, such as morphisms

$$
  \mathbf{B}G \to \mathbf{B}AUT(K)
$$

correspond to in terms of claassical group data, using the relation between [[strict 2-group]]s and [[crossed module]]s that is spelled out in detail at [strict 2-group -- in terms of crossed modules](http://ncatlab.org/nlab/show/strict+2-group#InTermsOfCrossedModules).

For making the translation we follow the **convention LB** there.


### Degree 2 cocycles

+-- {: .un_prop}
###### Proposition

Degree 2 cocycles of nonabelian group cohomology on $G$ with coefficients in $K$ are given by the following data:

* a map $\psi : G \to Aut(K)$;

* a map $\chi : G \times G \to K$

* subject to the constraint that for all $g_1, g_2 \in G$ we have

  $$
    \psi(g_1 g_2)
    = 
    Ad(\chi(g_1, g_2)) \psi(g_2) \psi(g_1)  
    \,.
  $$

* and subject to the cocycle condition that for all $g_1, g_2, g_3 \in G$ we have

  $$
   \chi(g_1 g_2, g_3) \psi(g_3)(\xi(g_1,g_2))
   = 
   \chi(g_1, g_2 g_3) \chi(g_2, g_3)
  $$

=--

+-- {: .proof}
###### Proof

Use the identification of $\mathbf{B}AUT(K)$ with its [[crossed module]] $(A \stackrel{Ad}{\to} Aut(K))$ in the _convention L B_ as described at [strict 2-group -- in terms of crossed modules](http://ncatlab.org/nlab/show/strict+2-group#InTermsOfCrossedModules) to translate the relevant diagrams -- which are of the sort spelled out in great detail at [[group cohomology]]: the first three items of the above describe the maps

$$
  (\psi, \chi) : 
  \left(
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_1}}\nearrow &
       \Downarrow^{\mathrlap{=}}&
       \searrow^{\mathrlap{g_2}}
       \\
       \bullet &&\stackrel{g_1 g_2}{\to} && \bullet
    }
  \right)
  \;\;\;
  \mapsto
  \;\;\;
  \left(
    \array{
       && \bullet
       \\
       & {}^{\mathllap{\psi(g_1)}}\nearrow &
       \Downarrow^{\mathrlap{\chi(g_1,g_2)}}&
       \searrow^{\mathrlap{\psi(g_2)}}
       \\
       \bullet &&\stackrel{\psi(g_1 g_2)}{\to} && \bullet
    }
  \right)
  \,.
$$

The cocycle condition is the fact that this assignment has to make all tetrahedras commute (since there are only trivial [[k-morphism]]s with $k \geq 3$ in $\mathbf{B}AUT(K)$):

$$
  \array{
    \bullet &&\stackrel{\psi(g_2)}{\to}&& \bullet
    \\
    \uparrow 
    &
      \Downarrow{}^{\mathrlap{\chi(g_1, g_2)}}
    &&& \downarrow
    \\
    {}^{\mathllap{\psi(g_1)}}\uparrow
    &&{}^{\mathllap{\psi(g_1 g_2)}}\nearrow&&
    \downarrow^{\mathrlap{\psi(g_3)}}
    \\
    \uparrow &&&
     {}^{\mathllap{\chi(g_1 g_2, g_2)}}\Downarrow 
   & \downarrow
    \\
    \bullet &&\stackrel{\psi(g_3)}{\to}&&
    \bullet
  }
  \;\;\;\;\;\;\;\;
  =
  \;\;\;\;\;\;\;\;
  \array{
    \bullet &&\stackrel{\psi(g_2)}{\to}&& \bullet
    \\
    \uparrow 
    &&&
      {}^{\mathllap{\chi(g_2, g_3)}}
    \Downarrow    
& \downarrow
    \\
    {}^{\mathllap{\psi(g_1)}}\uparrow
    &&\searrow^{\mathrlap{\psi(g_2 g_3)}}&&
    \downarrow^{\mathrlap{\psi(g_3)}}
    \\
    \uparrow &
     \Downarrow{}^{\mathrlap{\chi(g_1 , g_2 g_3)}} 
    &&& \downarrow
    \\
    \bullet &&\stackrel{\psi(g_3)}{\to}&&
    \bullet
  }
$$

=--

+-- {: .un_remark}
###### Remark

Precisely the same kind of "twisted" cocycles appear as the cocycles of nonabelian [[gerbe]]s and [[principal 2-bundle]]s: for a $K$-gerbe these are cocycles with coefficients in $\mathbf{B}AUT(K)$ but on a domain that is the [[discrete groupoid]] given by the given base space.

=--

### Extensions classified by degree 2-cocycles

The following statement is classically the central statement of [[Schreier theory]]. We state and prove it in the abstract nonsense context of general [[cohomology]], where the things classified by a cocycle are nothing but its [[homotopy fiber]]s.

+-- {: .un_prop}
###### Proposition

Cohomology classes of nonabelian 2-cocycles $(\psi, \chi) :  \mathbf{B}G \to \mathbf{B}AUT(K)$ are in bijection  with equivalence classes of extensions

$$
  K \to \hat G \to G
$$

=--



+-- {: .proof}
###### Proof

In fact, we claim a bit more: we claim that the [[fibration sequence]] to the left defined by the cocycle $(\psi, \chi) : \mathbf{B}G \to \mathbf{B}AUT(K)$ is

$$
  \cdots
  \to
  Aut(K)
  \to 
  Aut(K)//K
  \to 
  Aut(K)//\hat G
  \to
  \mathbf{B}G
  \stackrel{(\psi,\xi)}{\to}
  \mathbf{B}AUT(K)
  \,,
$$

where 

$$
  \hat G := K \times_{(\psi,\chi)} G
$$

is the twisted product of $K$ with $G$, using the maps $\chi$ and $\psi$, i.e. the group whose underlying set is the cartesian [[product]] $K \times G$ with multiplication given by

$$
  (k_1, g_1) (k_2, g_2) = 
  \left(
    \chi(g_1,g_2) \psi(g_2)(k_1) k_2 
    \;\;  , \;\;
    g_1 g_2
  \right)
  \,.
$$

To see this, we compute the [[homotopy pullback]] 

$$
  \array{
    Aut(K)//\hat G & \to & {*}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{(\psi,\chi)}{\to}&
    \mathbf{B}AUT(K)
  }
$$

as the ordinary [[pullback]]

$$
  \array{
    Aut(K)//\hat G & \to & \mathbf{E}AUT(K)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{(\psi,\chi)}{\to}&
    \mathbf{B}AUT(K)
  }
$$

as described at [[generalized universal bundle]]. ($\mathbf{E}AUT(K)$ is the universal $AUT(K)$-[[principal 2-bundle]]).

Recall from the discussion there that a morphism in $\mathbf{AUT}(K)$ is a triangle

$$
  \array{
     && \bullet
     \\
     & {}^{\mathllap{\alpha}}\swarrow
     &{}^\mathrlap{k}\swArrow& 
     \searrow^{\mathrlap{\beta}}
     \\
     \bullet 
     &&\stackrel{\gamma}{\to}&&
     \bullet
  }
$$

in $\mathbf{B}AUT(K)$, and composition of morphisms is pasting of these triangles along their vertical edges. 2-morphisms in $\mathbf{E}AUT(K)$ are given by paper-cup pasting diagrams of such triangles in $\mathbf{B}AUT(K)$



Accordingly, the [[pullback]] $\mathbf{B}G \times_{(\psi,\xi)} \mathbf{E}AUT(K)$ has

* objects are elements of $Aut(K)$ (this is the bit not seen in the classical picture of [[Schreier theory]], as that doesn't know about [[groupoid]]s);

* morphisms are pairs 

  $$
    (k,g)
    \;\;\;
    :=
    \left(
    \array{
      && \bullet
      \\
      & {}^{\mathllap{\alpha}}\swarrow
      &{}^\mathrlap{k}\swArrow& 
      \searrow^{\mathrlap{\beta}}
      &&&&& \in \mathbf{AUT(K)}
      \\
      \bullet 
      &&\stackrel{\psi(g)}{\to}&&
      \bullet
      \\
      \\
      \bullet 
      &&\stackrel{g}{\to}&&
      \bullet    
      &&&& \in \mathbf{B}G
    }
    \right)
  $$

* 2-morphisms (though of as 2-[[simplex]]es) take two 
  such triangles $(k_1, g_1)$ and $(k_2, g_2)$ to the pair $(k', g_1, g_2)$, where $k'$ is given by the pasting diagram

  $$
    \array{
      && \bullet
      \\
      &\swarrow& \downarrow & \searrow
      \\
      \downarrow &\Downarrow^{\mathrlap{k_1}}& 
      \bullet &{}^{\mathllap{k_2}}\Downarrow& \downarrow
      \\
      \downarrow 
      & \nearrow &\Downarrow^{\mathrlap{\chi(g_1, g_2)}}
      & \searrow & \downarrow
      \\
      \bullet && \stackrel{}{\to}
      &&
      \bullet
    }
    \,.
  $$

Translating these diagrams into forumas using the _convention LB_ as described at [strict 2-group -- in terms of crossed modules](http://ncatlab.org/nlab/show/strict+2-group#InTermsOfCrossedModules) yields the given formulas.

=--

### Homotopies between 2-cocycles {#Homotopy2Cocycle}


Given two 2-cocycles

$$
  (\psi_1, \chi_1), (\psi_2, \chi_2)
  : 
  \mathbf{B}G
  \to 
  \mathbf{B}AUT(K)
$$

a homotopy (coboundary) between them is a [[transfor|transformation]]

$$
  \lambda : (\psi_1, \chi_1) \Rightarrow (\psi_2, \chi_2)
  \,.
$$

Its components 

$$
  \lambda
  : 
  (\bullet \stackrel{g}{\to} \bullet)
  \;\;
  \mapsto
  \;\;
  \left(
   \array{
     \bullet &\stackrel{\psi_1(g)}{\to}& \bullet
     \\
     {}^{\mathllap{\lambda(\bullet)}}
     \downarrow &{}^{\mathllap{\lambda(g)}}\swArrow& 
     \downarrow^{\mathrlap{\lambda(\bullet)}}
     \\
     \bullet &\stackrel{\psi_2(g)}{\to}& \bullet 
   }
  \right)
$$

are given in terms of group elements by 

* $\lambda(\bullet) \in Aut(K)$

* $\{\lambda(g) \in K | g \in G\}$

such that

\[
  \lambda(\bullet) \psi_1(g)
  =
  Ad(\lambda(g)) \psi_2(g) \lambda(\bullet)
  \,.
\]

The naturality condition on this datat is that 
for all $g_1, g_2 \in G$ we have

$$
  \array{
    && \bullet
    \\
    & {}^{\mathllap{\psi_1(g_1)}}\nearrow 
    &\Downarrow^{\chi_1(g_1,g_2)}& 
    \searrow^{\mathrlap{\psi_1(g_2)}}
    \\
    \bullet &&\stackrel{\psi_1(g_2 g_1)}{\to}&& \bullet
    \\
    {}^{\mathllap{\lambda(\bullet)}}\downarrow &&
    {}^{\mathllap{\lambda(g_1, g_2)}}\swArrow
    && 
    \downarrow^{\mathrlap{\lambda(\bullet)}}
    \\
    \bullet
    &&\stackrel{\psi_2(g_2 g_1)}{\to}&&
    \bullet
  }
  \;\;\;\;\;\;\;\;
  =
  \;\;\;\;\;\;\;\;
  \array{
    & {}^{\mathllap{\psi_1(g_1)}}\nearrow
    &\downarrow& \searrow^{\mathrlap{\psi_1(g_1)}}
    \\
    \downarrow 
    &{}^{\lambda(g_2)}\swArrow
     &
     \downarrow^{\mathrlap{\lambda(\bullet)}}
    &{}^{\lambda(g_2)}\swArrow& 
    \downarrow
    \\
    {}^{\mathllap{\lambda(\bullet)}}\downarrow
     & 
     {}^{\mathllap{\psi_2(g_1)}}
     \nearrow &
     \Downarrow^{\chi_2(g_1,g_2)}
     & \searrow^{\mathrlap{\psi_2(g_2)}}
     &
     \downarrow^{\mathrlap{\lambda(\bullet)}}
    \\
    \bullet &&\stackrel{\psi_2(g2 g_1)}{\to}&&
    \bullet
  }
$$

In terms of the _conventionl LB_ at [strict 2-group -- in terms of crossed modules](http://ncatlab.org/nlab/show/strict+2-group#InTermsOfCrossedModules), this is equivalent to the equation

\[
  \label{homotopy}
  \lambda(g_2 g_1) \; 
  \rho(\lambda(\bullet))(\chi_1(g_1,g_2))
  =
  \chi_2(g_1, g_2) 
  \;
  \rho(\psi_1(g_2))(\lambda(g_2))  
  \;
  \lambda(g_2)
  \,.
\]

Compare this to the discussion of [2-coboundaries of extensions](http://ncatlab.org/nlab/show/group+extension#2Coboundaries) at [[group extension]].

## Nonabelian Lie algebra cohomology

When the groups in question are [[Lie group]]s, there is an [[infinitesimal object|infinitesimal]] version of nonabelian group cohomology:

* [[nonabelian Lie algebra cohomology]]

See there for details.

[[!redirects nonabelian group cohmology]]
