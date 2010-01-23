<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

>entry left in unfinished state as I have to run now, please feel free to polish


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

We describe the notion of cohomology of a [[chain complex]], the cochain cohomology of its dual [[cochain complex]], from the [[nPOV]] on [[cohomology]], as discussed there.

A [[chain complex]] in non-negative degree is, under the [[Dold-Kan correspondence]] a [[homological algebra]] model for a particularly nice [[topological space]] or [[∞-groupoid]]: namely one with an abelian group structure on it.
Accordingly, an unbounded (arbitrary) [[chain complex]] is a model for a [[spectrum]] with abelian group structure. 

One consequence of this embedding

$$
  N : Ch_+ \to \infty Grpd
$$

induced by the Dold-Kan [[nerve]] is that it allows to think of [[chain complexes]] as objects in the [[(∞,1)-topos]] [[∞Grpd]] or equivalently [[Top]]. Every [[(∞,1)-topos]] comes with a notion of [[homotopy]] and [[cohomology]] and so such abstract notions get induced on chain complexes.

Of course there is an independent, age-old definition of [[homology]] of chain complexes and, by dualization, of cohomology of cochain complexes. 

This entry describes how these standard definition of chain homology and cohomology follow from the general [[(∞,1)-topos]] nonsense described at [[cohomology]] and [[homotopy]]. 

The main statement is that

* the na&iuml;ve [[homology]] groups of a [[chain complex]] are really its [[homotopy groups]], in the abstract sense (i.e. with the chain complex regarded as a model for a space/$\infty$-groupoid);

* the na&iuml;ve cohomology groups of a cochain complex are really the abstract [[cohomology groups]] of the dual [[chain complex]].

## Preliminaries 

Before discussing chain homology and cohomology, we fix some terms and notation.

### Eilenberg-MacLane objects 

In a given [[(∞,1)-topos]] there is a notion of [[homotopy]] and [[cohomology]] for every (co-)coefficient object $A$ ($B$).

The particular case of [[chain complex]] [[homology]] is only the special case induced from coefficients given by the corresponding [[Eilenberg-MacLane objects]].

Assume for simplicity here and in the following that we are talking about non-negatively graded chain complexes of vector spaces over some field $k$. Then for every $n \in \mathbb{N}$ write

$$
  \begin{aligned}
    \mathbf{B}^n k &:=
    ( 
      \cdots
      \to 
      \mathbf{B}^n k_n
      \to  
      \cdots 
       \to \stackrel{\partial}{\to} \mathbf{B}^n k_1 
      \stackrel{\partial}{\to} \mathbf{B}^n k_0)
    \\
    &=
    (  \cdots \to k \to \cdots \to 0 \to 0 )
  \end{aligned}
$$

for the $n$th [[Eilenberg-MacLane object]]. 

Notice that this is often also denoted $k[n]$ or $k[-n]$ or $K(k,n)$.


### Homotopy and cohomology 

With the [[Dold-Kan correspondence]] understood, embedding
chain complexes into [[∞-groupoids]], for any chain complexes $X_\bullet$, $A_\bullet$ and $B_\bullet$ we obtain 

* the $\infty$-groupoid

  $$
    \mathbf{H}_{\infty Grpd}(X_\bullet, A_\bullet)
  $$

  whose 
  * objects are the $A$-valued [[cocycle]]s on $X$;
  * morphisms are the coboundaries between these [[cocycle]]s;
  * 2-morphisms are the coboundaries between coboundaries
  * etc.
  and where the elements of $\pi_0 \mathbf{H}(X_\bullet,A_\bullet)$ are the cohomology classes

* the $\infty$-groupoids

  $$
    \mathbf{H}_{\infty Grpd}(B_\bullet, X_\bullet)
  $$

  whose 
  * objects are the $B$-co-valued cycles on $X$;
  * morphisms are the boundaries between these cycles;
  * 2-morphisms are the boundaries between boundaries
  * etc.
  and where the elements of $\pi_0 \mathbf{H}(B_\bullet,X_\bullet)$ are the homotopy classes


## Chain homology as homotopy 

For $X_\bullet := V_\bullet$ any [[chain complex]] 
and $H_n(V_\bullet)$ its ordinary chain [[homology]] in degree $n$, we have

$$
  H_n(V_\bullet) \simeq 
  \pi_0 \mathbf{H}(\mathbf{B}^n k_\bullet, V_\bullet)
  \,.
$$

A cycle $c : \mathbf{B}^n k_\bullet \to V_\bullet$ 
is a chain map

$$
  \array{
    \cdots 
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    k
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    \cdots
    \\
    && \downarrow
    && \downarrow^{c_n}
    && \downarrow
    \\
    \cdots 
    &\stackrel{\partial}{\to}&
    V_{n+1}
    &\stackrel{\partial}{\to}&
    V_n
    &\stackrel{\partial}{\to}&
    V_{n-1}
    &\stackrel{\partial}{\to}&
    \cdots        
  }
$$

Such chain maps are clearly in bijection with those elements $c_n \in V_n$ that are in the kernel of
$V_n \stackrel{\partial}{\to} V_{n-1}$
in that $\partial c_n = 0$.

A boundary $\lambda : c \to C'$ is a chain homotopy

$$
  \array{
    \cdots 
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    k
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    \cdots
    \\
    && &
    {}^{\lambda_n}\swarrow
    \\
    \cdots 
    &\stackrel{\partial}{\to}&
    V_{n+1}
    &\stackrel{\partial}{\to}&
    V_n
    &\stackrel{\partial}{\to}&
    V_{n-1}
    &\stackrel{\partial}{\to}&
    \cdots        
  }
$$

such that $c' = c + \partial \lambda$.

...


## Cohomology of cochain complexes 

The ordinary notion of cohomology of a [[chain complex|cochain complex]]
is the special case of cohomology in the 
[[stable (∞,1)-category|stable (∞,1)-]] [[category of chain complexes]].

For $V^\bullet$ a cochain complex let 

$$
  \begin{aligned}
      X &:= V_\bullet = (V^\bullet)^*
      \\
      &=
      (\cdots \to X_{n+1} \stackrel{\partial}{\to}
      X_n \stackrel{\partial}{\to} X_{n-1} \to \cdots)
      \\
      & :=
      (\cdots \to V_{n+1} \stackrel{\partial}{\to}
      V_n \stackrel{\partial}{\to} V_{n-1} \to \cdots)
  \end{aligned}
$$

be the corresponding dual [[chain complex]]. Let

$$
  \begin{aligned}
     A  &:=  \mathbf{B}^n I 
     \\
     &=
     (\cdots \to A_{n+1}  \to A_n \to A_{n-1} \to \cdots )
     \\
      & =
     (\cdots \to 0  \to I \to 0 \to \cdots )
  \end{aligned}
$$ 

be the [[chain complex]] with the 
tensor unit (the [[ground field]], say) in degree $n$ and
trivial elsewhere. Then 
$$
  \begin{aligned}
    \mathbf{H}(X,A)
    &=
    Ch(V_\bullet, \mathbf{B}^n I)
  \end{aligned}
$$

has 

* as objects chain morphisms 
  $c : V_\bullet \to \mathbf{B}^n I$
  $$
    \array{
      \cdots &\to& V_{n+1} &\stackrel{\partial}{\to}& 
      V_{n} 
      &\stackrel{\partial}{\to}& V_{n-1} 
      &\to& 
      \cdots
      \\
      &&  \downarrow^{c_{n+1}}
      && \downarrow^{c_{n}}
      && \downarrow^{c_{n-1}}
      \\
      \cdots &\to& 0 &\stackrel{\partial}{\to}& 
      I 
      &\stackrel{\partial}{\to}& 0 
      &\to& 
      \cdots  
    }
    \,.
  $$
  These are in canonical bijection with 
  the elements in the kernel of $d_{n}$ of the dual
  cochain complex $V^\bullet = [V_\bullet,I]$.

* as morphism chain homotopies $\lambda : c \to c'$

  $$
    \array{
      \cdots &\to& V_{n+1} &\stackrel{\partial}{\to}& 
      V_{n} 
      &\stackrel{\partial}{\to}& V_{n-1} 
      &\to& 
      \cdots
      \\
      && 
      && 
      &{}^{\lambda}\swarrow& 
      \\
      \cdots &\to& 0 &\stackrel{\partial}{\to}& 
      I 
      &\stackrel{\partial}{\to}& 0 
      &\to& 
      \cdots  
    }
    \,.
  $$

Comparing with the general definition of cocycles and coboudnaries from above, one confirms that

* the **cocycles** are the chain maps
  $$
    V_\bullet \to I[n]_\bullet
  $$

* the **coboundaries** are the chain homotopies between these chain maps.

* the **coboundaries of coboundaries** are the second order chain homotopies between these chain homotopies.

* etc.

## References 

* [[John Baez]] and [[Mike Shulman]], _Lectures on $n$-Categories and Cohomology_ ([pdf](http://math.ucr.edu/home/baez/cohomology.pdf), [[Lectures on n-Categories and Cohomology|nLab]])

  * See, in particular, the discussion beginning at the bottom of page 24.


> [[Urs Schreiber]]: this is a nice reference, but does it really help on the above discussion?

## Discussion

+--{: .query}

> concerning the statement at the very beginning, there was once this exchange here:

[[David Roberts]]: Should this be _of the homotopy type of an abelian topological group_? Or an $E_\infty$-algebra?

[[Urs Schreiber|Urs]]: I thought the statement (at least the strictest version of what that statement can be) of the [[Dold-Kan correspondence]] is that non-negatively graded chain complexes of abelian groups are equivalent to simplicial sets internal to abelian groups. Since these are necessarily Kan complexes, I phrased this as "$\infty$-groupoids with abelian group structure" (strict abelian group structure, that is). 

So these in particular have the homotopy type of an abelian group, and in particular are special cases of $E_\infty$-spaces, but are much more restrictive, in that there is on the nose a strict abelian group structure around.

That's what I am thinking. But let me know if I am mixed up. And please feel free to improve on the presentation here as you see the need. I don't have time for this entry right now, will try to come back to it later.

=--


[[!redirects chain homology]]
[[!redirects cochain homology]]
[[!redirects chain cohomology]]
[[!redirects cochain cohomology]]