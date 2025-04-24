
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



> This entry largely discusses *[[Schreier theory]]* of nonabelian [[group extensions]] -- but from the [[nPOV]].


#Contents#
* table of contents
{:toc}


## Idea and Definition

As [[group cohomology]] of a group $G$ is the cohomology of its [[delooping]] $\mathbf{B}G$, so _nonabelian group cohomology_ is the corresponding [[nonabelian cohomology]].

By the [[category theory|general abstract]] definition of [[cohomology]], the _[[abelian group|abelian]]_ [[group cohomology]] in degree $n \in \mathbb{N}$ of a [[group]] $G$ with coefficients in an abelian group $K$ is the set of 
[[equivalence classes]] of [[morphisms]]

$$
  H^n(G,K) 
  \;\simeq\; 
  \big\{ \mathbf{B}G  \to \mathbf{B}^n K \big\}_{/\sim}
$$

in the [[(∞,1)-category]] [[∞Grpd]], from the [[delooping]] $\mathbf{B}G$ of $G$ to the $n$-fold delooping $\mathbf{B}^n K$ of $K$.

However, if the group $K$ is not abelian, then its $n$-fold delooping does not exist for $n \geq 2$, so accordingly the above does not give a prescription for cohomology of $G$ with coefficients in a nonabelian group $K$ in degree greater than 1 (and in degree 1 group cohomology is not very interesting, though see at *[[crossed homomorphism]]*).

But for nonabelian $K$ there are higher groupoids that "approximate" the non-existing higher deloopings, in some sense. Nonabelian group cohomology is the [[cohomology]] of $\mathbf{B}G$ with coefficients in such approximations.

More in detail, notice that for $n=2$ and $K$ abelian, the $n$-fold [[delooping]] $\mathbf{B}^2 K$ is the strict [[2-groupoid]] whose corresponding [[crossed complex]] is

$$
  [\mathbf{B}^2 K]
  = 
  \left(
    K \to {*} 
     \rightrightarrows {*}
  \right)
  \,.
$$

But for every [[group]] $K$ there is also its [[2-group|automorphism 2-group]] $AUT(K)$. Its delooping corresponds to the [[crossed complex]]

$$
  [\mathbf{B} AUT(K)]
  =
  \big(
    K 
    \xrightarrow
      {\delta = Ad}
     Aut(K) 
   \rightrightarrows
    {*}
  \big)
  \,,
$$

where the boundary map $\delta$ is the one that sends an element $k \in K$ to the [[inner automorphism]] ([[adjoint action]])  $Ad(k) \,\colon\, k' \mapsto k k' k^{-1}$.

So this looks much like $\mathbf{B}^2 K$ (when that exists) only that it has more elements in degree 1.

Accordingly, what is called nonabelian group cohomology of $G$ with coefficients in $K$ is the set of equivalence classes of morphisms

$$
  H^2_{nonab}(G,K) 
    \;\coloneqq\; 
  \big\{ \mathbf{B}G \to \mathbf{B}AUT(K) \big\}_{/\sim}
  \,.
$$

Notice that when $K$ has nontrivial [[automorphisms]], this differs in general from the ordinary degree=2 abelian group cohomology even if $K$ is abelian.

It is a familiar fact that abelian group cohomology classifies (shifted) [[central extension|central]] [[group extensions]]. Abstractly, this is really nothing but the statement that to a morphism $\mathbf{B}G \to \mathbf{B}^n K$ we may associate its [[homotopy fiber]], making the [[fiber sequence]]

$$
  \array{
    \mathbf{B}^{n-1} K
      &\longrightarrow&
    \mathbf{B}\hat G &\to& {*}
    \\
    \big\downarrow &&\downarrow && \big\downarrow 
    \\
    {*} 
      &\longrightarrow& 
    \mathbf{B}G &\to& \mathbf{B}^n K
  }
$$

(where both squares are [[homotopy pullback]] squares). In particular, for $n = 2$ we get ordinary [[central extensions]]

$$
  \mathbf{B}K \to \mathbf{B}\hat G \to \mathbf{B}B
  \,,
$$

which may be looped to yield [[exact sequences]] of groups

$$
  K \longrightarrow \hat G \longrightarrow B
  \,.
$$

In [[Schreier theory]] one notices that, similarly, nonabelian group cohomology in degree=2 classifies nonabelian [[group extensions]], i.e. sequences

$$
  K \longrightarrow \hat G \longrightarrow G
  \,.
$$

As we shall discuss below, along the lines of the abstract discussion above, nonabelian degree=2 cocycles really classify something slightly richer, namely exact sequences of groupoids

$$
  Aut(K) \sslash K 
    \longrightarrow
  Aut(K) \sslash \hat G
   \longrightarrow
  {*}\sslash G
  \,,
$$

where the double slashes denote [[homotopy quotients]] (presented as [[action groupoids]], and so ${*}\sslash G = \mathbf{B}G$ is the [[delooping groupoid]]).


In the existing literature --- which does not usually present the picture quite in the way we are doing here --- nonabelian group cohomology is rarely considered beyond degree$=2$. But the picture does straightforwardly generalize. For instance degree$=3$ nonabelian cohomology of $G$ with coefficients in $K$ may be taken to be the cohomology of $\mathbf{B}G$ with coefficients in the [[3-groupoid]] $\mathbf{B}AUT\big(AUT(K)\big)$.

$$
  H^3_{nonab}(G,K) 
  \;\coloneqq\; 
  \Big\{
    \mathbf{B}G \to \mathbf{B}AUT\big(AUT(K)\big)
  \Big\}_{/\sim}
  \,,
$$

and so on.


## Details

We work out in detail what nonabelian group cocycles, such as morphisms

$$
  \mathbf{B}G 
    \longrightarrow
  \mathbf{B}AUT(K)
$$

correspond to in terms of classical group data, using the relation between [[strict 2-groups]] and [[crossed modules]] that is spelled out at *[strict 2-group -- in terms of crossed modules](strict+2-group#InTermsOfCrossedModules)*.

For making the translation we follow the **convention LB** there.


### Degree=2 cocycles


\begin{proposition}
Degree$=2$ cocycles of nonabelian group cohomology on $G$ with coefficients in $K$ are given by the following data:

1. a map $\psi \,\colon\, G \to Aut(K)$;

1. a map $\chi \,\colon\, G \times G \to K$

subject to 

1. the constraint that for all $g_1, g_2 \in G$ we have

   $$
     \psi(g_1 g_2)
     = 
     Ad\big(\chi(g_1, g_2)\big) \psi(g_2) \psi(g_1)  
     \,.
   $$

1. the cocycle condition that for all $g_1, g_2, g_3 \in G$ we have

  $$
   \chi(g_1 g_2, g_3) 
   \cdot 
   \psi(g_3)\big(\chi(g_1,g_2)\big)
   \,=\, 
   \chi(g_1, g_2 g_3) \cdot \chi(g_2, g_3)
   \,.
  $$

\end{proposition}

\begin{proof}
Use the identification of $\mathbf{B}AUT(K)$ with its [[crossed module]] $\big(A \overset{Ad}{\to} Aut(K)\big)$ in the "convention L B" as described at *[strict 2-group -- in terms of crossed modules](strict+2-group#InTermsOfCrossedModules)* to translate the relevant diagrams -- which are of the sort spelled out in great detail at *[[group cohomology]]*: The first three items of the above encode a map of [[2-morphisms]]


\begin{tikzcd}[
  row sep=15pt,
  column sep=22pt
]
  &
  \bullet
    \ar[ddr, "{ g_2 }"]
  \ar[dd, equals, shorten <=10pt, shorten >=7pt]
  &
  &&
  &
  \bullet
  \ar[ddr, "{ \psi(g_2) }"]
  \ar[dd, Rightarrow, shorten <=10pt, shorten >= 7pt,
    "{ \chi(g_1, g_2) }"{description}
  ]
  \\
  &&& 
  \longmapsto
  &
  \\
  \bullet
    \ar[rr, "{ g_1 g_2 }"{swap}]
    \ar[uur, "{ g_1 }"]
  &{}&
  \bullet
  &&
  \bullet
  \ar[uur, "{ \psi(g_1) }"]
  \ar[rr, "{ \psi(g_1 g_2) }"{swap}]
  &{}&
  \bullet
\end{tikzcd}

and the cocycle condition encodes that this assignment makes all [[tetrahedra]] commute (since there are only trivial [[k-morphisms]] with $k \geq 3$ in $\mathbf{B}AUT(K)$):

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

\end{proof}

\begin{remark}
Precisely the same kind of "twisted" cocycles appear as the cocycles of nonabelian [[gerbes]] and [[principal 2-bundles]]: for a $K$-gerbe these are cocycles with coefficients in $\mathbf{B}AUT(K)$ but on a domain that is the [[discrete groupoid]] given by the given base space.
\end{remark}

### Extensions classified by degree=2 cocycles

The following statement is classically the central statement of [[Schreier theory]]. We state and prove it in terms of [[delooping]]  [[2-groupoids]], where the object classified by a cocycle is nothing but its [[homotopy fiber]].

+-- {: .un_prop}
###### Proposition

Cohomology classes of nonabelian 2-cocycles $(\psi, \chi) :  \mathbf{B}G \to \mathbf{B}AUT(K)$ are in bijection  with equivalence classes of extensions

$$
  K \to \hat G \to G
  \mathrlap{\,.}
$$

=--



+-- {: .proof}
###### Proof

In fact, we claim a bit more: we claim that the [[fibration sequence]] to the left which is induced by the cocycle $(\psi, \chi) \,\colon\, \mathbf{B}G \to \mathbf{B}AUT(K)$ is

$$
  \cdots
    \longrightarrow
  Aut(K)
    \longrightarrow
  Aut(K) \sslash K
    \longrightarrow
  Aut(K) \sslash \hat G
    \longrightarrow
  \mathbf{B}G
    \overset{(\psi,\xi)}{\to}
  \mathbf{B}AUT(K)
  \,,
$$

where 

$$
  \hat G \,\coloneqq\, K \times_{(\psi,\chi)} G
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
    Aut(K)\sslash\hat G & \to & {*}
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
    Aut(K)\sslash\hat G & \to & \mathbf{E}AUT(K)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{(\psi,\chi)}{\to}&
    \mathbf{B}AUT(K)
  }
$$

as described at [[generalized universal bundle]]. ($\mathbf{E}AUT(K)$ is the universal $AUT(K)$-[[principal 2-bundle]]).

Recall from the discussion there that

* [[1-morphisms]] in $\mathbf{E}AUT(K)$ are triangular [[2-morphism]]

  $$
    \array{
       && \bullet
       \\
       & 
       {}^{\mathllap{\alpha}}\swarrow
       & 
       {}^\mathrlap{k}\swArrow& 
       \searrow^{\mathrlap{\beta}}
       \\
       \bullet 
       &&\stackrel{\gamma}{\to}&&
       \bullet
    }
  $$

  in $\mathbf{B}AUT(K)$, and [[composition]] of morphisms is [[pasting diagram|pasting]] of these triangles along their vertical edges

* [[2-morphisms]] in $\mathbf{E}AUT(K)$ are given by paper-cup [[pasting diagrams]] of such triangles in $\mathbf{B}AUT(K)$.



Accordingly, the [[pullback]] $\mathbf{B}G \times_{(\psi,\xi)} \mathbf{E}AUT(K)$ has

* [[objects]] are elements of $Aut(K)$ (this is the bit not seen in the classical picture of [[Schreier theory]], as that doesn't know about [[groupoids]]);

* [[1-morphisms]] $\alpha \to \beta$ are pairs 

  \[
    \label{MorphismsOfWidehatG}
    (k,g)
    \;\;\;
    \coloneqq
    \left(
    \array{
      && \bullet
      \\
      & {}^{\mathllap{\alpha}}\swarrow
      &{}^\mathrlap{k}\swArrow& 
      \searrow^{\mathrlap{\beta}}
      &&&&& \in \mathbf{B}AUT(K)
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
  \]

* [[2-morphisms]] (thought of as 2-[[simplices]]) take pairs of such triangles, $(k_1, g_1)$ and $(k_2, g_2)$, to the pair $(k', g_1 g_2)$, where $k'$ is given by the pasting diagram

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

Translating these diagrams into formulas using the _convention LB_ as described at *[strict 2-group -- in terms of crossed modules](strict+2-group#InTermsOfCrossedModules)* yields the claimed expressions.

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
  \,\colon\,
  (\bullet \stackrel{g}{\to} \bullet)
  \;\;
  \mapsto
  \;\;
  \;\;
  \left(
  \;\;\;\;
   \array{
     \bullet 
       &\overset{\psi_1(g)}{\longrightarrow}& 
     \bullet
     \\
     {}^{\mathllap{\lambda(\bullet)}}
     \big\downarrow 
       &\;{}^{\mathllap{\lambda(g)}}\!\swArrow& 
     \big\downarrow^{\mathrlap{\lambda(\bullet)}}
     \\
     \bullet &\overset{\psi_2(g)}{\longrightarrow}& \bullet 
   }
  \;\;\;\;
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

In terms of the _conventionl LB_ at [strict 2-group -- in terms of crossed modules](strict+2-group#InTermsOfCrossedModules), this is equivalent to the equation

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

Compare this to the discussion of [2-coboundaries of extensions](group+extension#2Coboundaries) at [[group extension]].

## Nonabelian Lie algebra cohomology

When the groups in question are [[Lie groups]], there is an [[infinitesimal object|infinitesimal]] version of nonabelian group cohomology:

* [[nonabelian Lie algebra cohomology]]

See there for details.

## Related concepts

* [[non-abelian cohomology]]

* [[group cohomology]]

  * **nonabelian group cohomology**, [[groupoid cohomology]]

* [[group extension]]

* [[Lie group cohomology]] 

  * [[∞-Lie groupoid cohomology]]

## References

Non-abelian group cohomology in degree 1, as the set of [crossed-conjugation](crossed+homomorphism#AdjointActionOnCrossedHomomorphisms)-[[equivalence classes]] of [[crossed homomorphisms]]: 

* [[Philippe Gille]], [[Tamás Szamuely]], Def. 2.3.2 in: *Central Simple Algebras and Galois Cohomology*, Cambridge University Press  2006 ([doi:10.1017/CBO9780511607219](https://doi.org/10.1017/CBO9780511607219), [pdf](http://www.math.ens.fr/~benoist/refs/Gille-Szamuely.pdf))

* {#Milne17} [[James Milne]], Sec. 3.k (27.a of the [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf)) in: *Algebraic Groups*, Cambridge University Press 2017  ([doi:10.1017/9781316711736](https://doi.org/10.1017/9781316711736), [webpage](http://www.jmilne.org/math/Books/iag.html), [pdf](https://www.jmilne.org/math/CourseNotes/iAG200.pdf))


* [[Groupprops]], *[First cohomology set with coefficients in a non-abelian group](https://groupprops.subwiki.org/wiki/First_cohomology_set_with_coefficients_in_a_non-abelian_group)*


[[!redirects non-abelian group cohomology]]


