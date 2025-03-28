
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Serre long exact sequence_ of a [[Serre fibration]] is a [[long exact sequences]] of [[ordinary cohomology]]/[[ordinary homology]] groups associated with a [[Serre fibration]] with sufficiently highly connected base and fibers.
It arises as a special case of the information contained in the corresponding [[Serre spectral sequence]].


## Statement

+-- {: .num_prop #SerreLongExactSequenceForHighlyConnectedBaseAndFiber}
###### Proposition

Let 

$$
  \array{
    F &\overset{i}{\longrightarrow}& X
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    && B 
  }
$$

be a [[Serre fibration]] such that 

1. the base space $B$ is $(n_1-1)$-[[n-connected topological space|connected]] for $n_1 \geq 2$;

1. the [[fiber]] $F$ is $(n_2-1)$-connected, for $n_1 \geq 1$;

then for every [[abelian group]] $A$ there is a [[long exact sequence]] of [[ordinary homology]] groups of the form

$$
  H_{n_1 + n_2 - 1}(F,A)
    \overset{i_\ast}{\longrightarrow}
  H_{n_1 + n_2 - 1}(X,A)
    \overset{p_\ast}{\longrightarrow}
  H_{n_1 + n_2 - 1}(B,A)
    \overset{\tau}{\longrightarrow}
  H_{n_1 + n_2 - 2}(F,A)
    \overset{i_\ast}{\longrightarrow}
  \cdots
    \overset{i_\ast}{\longrightarrow}
  H_1(X,A)        
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the homology [[Serre spectral sequence]] of the given fibration

$$
  E_2 = H_q(B, H_p(F,A)) \;\Rightarrow\; H_\bullet(X,A)
  \,.
$$

By the connectedness assumptions and the [[Hurewicz theorem]], then 

$$
  H_{0 \lt \bullet \lt n_1}(B,-) = 0
$$

and

$$
  H_{0 \lt \bullet \lt n_2}(F,-) = 0
$$

and hence the only possibly non-vanishing groups on the second page of the spectral sequence (hence on every higher page) in total degree $k \leq n_1 + n_2 - 1$ are $E^r_{k,0}$ and $E^r_{0,k}$. 

On the second page these groups are

$$
 E^2_{k,0} \simeq H_k(B,H_0(F,A)) \simeq H_k(B,A)
$$

$$
  E^2_{0,k} \simeq H_0(B,H_k(F,A)) \simeq H_k(F,A)
$$

by the fact that both $B$ and $F$ are connected by assumption.

Now, since the differentials on the $r$th page have bidegree $(-r,r+1)$, it follows that the only possibly non-vanishing differential on the $k$th page for $k \leq n_1 + n_2$ is

$$
  \partial_k
  \;\colon\;
  E^k_{k,0}
   \longrightarrow
  E^k_{0,k-1}
  \,.
$$

This being so, it follows that the above non-vanishing groups on the $E^2$-page in total degree $k$ remain intact up to these pages, hence that

$$
  E^k_{k,0} \simeq H_k(B,A)
  \;\;\;\;\;
    \,,
  \;\;\;\;\;
  E^k_{0,k-1} \simeq H_{k-1}(F,A)
  \,.
$$

Moreover, by convergence of the spectral sequence there are [[exact sequences]] of the form

$$
  0  
    \to 
  E^\infty_{k,0}
    \longrightarrow
  E^k_{k,0}
   \overset{\partial_k}{\longrightarrow}
  E^k_{0,k-1}
   \longrightarrow
  E^\infty_{0,k-1}
    \to
  0
  \,,
$$

hence, by the previous statement, of the form

$$
  0  
    \to 
  E^\infty_{k,0}
    \longrightarrow
  H_k(B,A)
   \overset{\partial_k}{\longrightarrow}
  H_{k-1}(F,A)
   \longrightarrow
  E^\infty_{0,k-1}
    \to
  0
  \,,
$$

Finally, by convergence and the [[filtering]] condition, the only non-vanishing filter contributions to $H_k(X,A)$ in degree $k \leq n_1 + n_2 - 1$ are in filtering degree 0 and $k$, and so projection to filtering degree $k$ gives a [[short exact sequence]] of the form

$$
  0 
    \to
  E^\infty_{0,k}
    \longrightarrow
  H_k(X,A)
    \longrightarrow
  E^\infty_{k,0}
    \to 
  0
  \,.
$$

Splicing together the exact sequences thus obtained yields the long exact sequence in question:

$$
  \array{
    \cdots
     &\to&
    H_k(F,A)
      && \longrightarrow &&
    H_k(X,A)
      && \longrightarrow &&
    H_k(B,A)
      &\overset{}{\longrightarrow}&
    H_{k-1}(F,A)
     &\to&
    \cdots
    \\
    &&
    & 
    \searrow
     && \nearrow
    &
    & \searrow && \nearrow
    \\
    &&
    &&
    E^\infty_{0,k}
    &&
    && E^\infty_{k,0}
  }
$$


=--

## Examples and Applications

+-- {: .num_prop }
###### Proposition

For $X$ an [[n-connected topological space]], then for $k \leq 2n$ there are [[isomorphisms]]

$$
  H_k(X) \simeq H_{k-1}(\Omega X)
$$

between the [[ordinary homology]] of $X$ in degree $k$ and the ordinary homology of the [[loop space]] of $X$ in degree $k-1$.

=--


+-- {: .proof}
###### Proof

The Serre long exact sequence from prop. \ref{SerreLongExactSequenceForHighlyConnectedBaseAndFiber} applied to the based [[path space]] [[Serre fibration]] of $X$

$$
  \Omega X \longrightarrow Path_\ast(X) \longrightarrow X
$$

is of the form

$$
  H_{2n}(\Omega X)
    \overset{i_\ast}{\longrightarrow}
  H_{2n}(Path_\ast(X))
    \overset{p_\ast}{\longrightarrow}
  H_{2n}(X)
    \overset{\tau}{\longrightarrow}
  H_{2n-1}(\Omega X)
    \overset{i_\ast}{\longrightarrow}
  \cdots
    \overset{i_\ast}{\longrightarrow}
  H_1(X)        
  \,.
$$

Since $Path_\ast(X)$ is [[contractible topological space|contractible]], every third group in this sequence vanishes, and hence exactness gives the isomorphisms

$$
  \tau \colon H_k(X) \simeq H_{k-1}(\Omega X)
$$

for $k \leq 2n$. 

=--


## Related concepts

* [[Serre spectral sequence]]

* [[Thom-Gysin sequence]]

* [[long exact sequence in cohomology]]

* [[long exact sequence of homotopy groups]]

## References

* {#Kochmann96} [[Stanley Kochmann]], prop. 3.2.1 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#McCleary01} [[John McCleary]], example 5.D of_A User's Guide to Spectral Sequences_, Cambridge University Press (2001)

[[!redirects Serre long exact sequences]]

[[!redirects Serre exact sequence]]
[[!redirects Serre exact sequences]]