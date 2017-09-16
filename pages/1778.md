
Cech cohomology is less a special kind of [[cohomology]] than a special algorithm for _computing_ cohomology classes.

On the other hand, while the algorithm always produces results that look like cohomology classes, these actually are the abstractly defined cohomology classes only under certain assumptions. Historically Cech cohomology has often been understood as being defined as whatever that algorithm computes, and theorems would be proven that determine under which conditions such "Cech cohomology" coincides with cohomology defined by other means, where "by other means" traditionally is: "in terms of right derived functor definition of [[abelian sheaf cohomology]]".

From the discussion at [[abelian sheaf cohomology]] we know that the right derived functor definition computes the hom-set in the [[homotopy category of an (infinity,1)-category|homotopy category]] of an [[(infinity,1)-topos]] $\mathbf{H}$ that may alternatively be computed as a colimit over resolutions of the domain object

$$
  H(X,A)
  := 
  \pi_0 \mathbf{H}(X,A)
  = colim_{Y \stackrel{\in W \cap F}{\to} X} 
  C_H(Y,A)/_{homotopy}
$$

where the colimit is over all acyclic fibrations $Y \stackrel{\in W \cap }{\to} X$ in an appropriate [[model category]] $C_H$ that [[presentable (infinity,1)-category|presents]] $\mathbf{H}$. For $\mathbf{H}$ an [[infinity-stack]] [[(infinity,1)-topos]] this $C_H$ is a [[model structure on simplicial presheaves]] and the acyclic fibrations $Y \stackrel{\in W \cap F}{\to} X$ for $X$ an ordinary space are the [[hypercover]]s.

Now, for some coefficient objects $A$ it is sufficient to take the colimit here not over all [[hypercover]]s, but just over [[Cech cover]]s. The resulting formula

$$
  H(X,A)
  = colim_{Y \stackrel{Cech cover}{\to} X} 
  C_H(Y,A)/_{homotopy}
$$

is then called the formula for **Cech cohomology** on $X$ with values in $A$.

Here a Cech cover is a simplicial presheaf that arises from an ordinary covering map $U \to X$ of $X$ by another space $U$ as the corresponding [[Cech nerve]] simplicial presheaf

$$
 \begin{aligned}
  Y := \left( 
    \cdots
    U \times_X U \times_X U
    \stackrel{\to}{\stackrel{\to}{\to}}
    U \times_X U \stackrel{\to}{\to} U 
  \right)
  \simeq
  hocolim_{[k] \in \Delta} U^{\times_X k}
 \end{aligned}
  \,.
$$

See [[descent for simplicial presheaves]] for more on the manipulations involved here.

To amplify, a general [[hypercover]] would start in degree 0 with a $U$ as above, but then in the next degree would have a cover $V \to U \times_X U$ of the fiber product, and so on, each fiber product in turn being covered by another space.

If $Y$ is not simply a Cech cover but also not the most general hypercover in that this iterative choice of further covering stops in degree $n$, then one also speaks of **Cech cover of level $n$** and of the corresponding cohomology formula as **higher Cech cohomology**. See for instance the reference by Tibor Beke below.

# Examples #

We start with describing the " _nonabelian_ " Cech cohomology, i.e. the plain unwrapping of the above definition, before assuming that our coefficient object is [[abelian sheaf cohomology|abelian]] and before applying the [[Moore complex]] functor that sends the following simplicial computation to the maybe more familiar one in [[chain complex]]es.

The reasoning parallels that described at [[descent]] to some extent, but is maybe still worthwhile repeating here.

So let $C$ be some [[site]] and let $SSh(C)$ the category of [[simplicial presheaf|simplicial (pre)sheaves]] on $C$. Let $C(U)$ be the Cech nerve for a cover $\pi : U \to X$ of some simplicial presheaf $X$ and let $A$ be any other simplicial presheaf that serves as the coefficient object.

Using [[end]] and [[coend]] notation we compute the required hom

$$
 \begin{aligned}
    SSh(C(U), A)
    &
    \simeq
    SSh( \int^{[k] \in Delta} \Delta^k \cdot C(U)_k, A )
    \\
    &
    \simeq
    \int_{[k] \in Delta} SSh(\Delta^k \cdot C(U)_k, A )   
    \\
    &
    \simeq
    \int_{[k] \in Delta} SSet(\Delta^k , SSh(C(U)_k,A) )   
    \\
    &
    \simeq
    \int_{[k] \in Delta} SSet(\Delta^k , A(U \times_X \cdots \times_X U) )   
 \end{aligned}
  \,.
$$

An object in this last expression -- an $A$-valued cocycle on $X$ relative to $U$ -- is a diagram in [[SSet]] of the form

$$
  \array{
    \vdots && \vdots
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^2
    &\stackrel{f}{\to}&
    A(U \times_X U \times_X U)
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^1
    &\stackrel{g}{\to}&
    A(U \times_X U)
    \\
    \uparrow
    &&
    \uparrow
    \\
    \Delta^0
    &\stackrel{a}{\to}&
    A(U)
  }
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

This is a **Cech-cocycle** on $X$ with values in $A$ relative to $U$.

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

## Nonabelian 1-cocycles: principal bundles ##

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

* a $\mathbf{B}G$-Cech cocycle is

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

* a $\mathbf{B}G$-Cech coboundary is
  
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

Remembering that the Cech cohomology is the colimit over refinement of covers over cohomology classes defined this way, one sees the standard

+-- {: .un_theorem }
###### Theorem

Cech cohomology with coefficients in $\mathbf{B}G$
(as above) classies $G$-[[principal bundle]]s

$$
  colim_{U \stackrel{Cech cover}{\to} X}
  SSh(C(U), \mathbf{B}G)/_{homtopy}
  \simeq
  G Bund(X)/_\sim
$$

=--


## Nonabelian 1-cocycles: gerbes and principal 2-bundles ##


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

One finds that a Cech-cocycle now is
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
    \alpha(g_{i j}|_{U_{i j k l}})(f_{j k l})
    \cdot
    f_{i j k}|_{U_{i j k l}}
  $$

This is a **nonabelian Cech 2-cocycle**.

Reading off the formulas for the coboundaries is
left as an excercise for the reader.

For the specical case the 

$$
  (G_2 \to G_1) = (G \to Aut(G))
$$

this is the nonabelian cohomology classifying
[[gerbe]]s.



#References#

* Tibor Beke, _Higher Cech theory_ ([journal](http://www.math.uiuc.edu/K-theory/0646/) [pdf](http://www.math.uiuc.edu/K-theory/0646/cech.pdf))

