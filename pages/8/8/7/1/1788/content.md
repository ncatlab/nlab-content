
+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***


I would like to understand the following question in 
an $\infty$-topos / in homotopy type theory:

given an object $V$ with an action by a group $G$, and given another object $X$. How can we naturally construct $[V,X]\sslash G$, the quotient of the space of maps $V \to G$ by $G$ acting by precomposition?

This seems basic, but I am being a bit dense, maybe. 

I am suspecting that this object is $\sum_{\mathbf{B}G}[V\sslash G, X \times \mathbf{B}G]_{\mathbf{B}G}$. At least this exbits some $G$-action, so if it's not the one I am after then a second question I have: which $G$ action is this?

More in detail:

I write $\mathbf{H}$ for my $\infty$-topos, as usual.

The $G$-action on $V$ is exhibited by a fiber sequence

$$
  \array{ 
     V &\to& V \sslash G
     \\
     && \downarrow
     \\
     && \mathbf{B}G 
  }
  \,.
$$

Similarly we get the fiber sequence

$$
  \array{
     Q
     &\to&  \sum_{x : \mathbf{B}G} [V \sslash G , X \times \mathbf{B}G ]_{/\mathbf{B}G}
     \\
     && \downarrow
     \\
     && \mathbf{B}G
  }
$$

where $Q$ is the stand-in notation for whatever the fiber of the morphism on the right is. This exhibits an action of $G$ on Q. 

What is $Q$? 

So I can say what $\flat Q$ is, the type of global points of $Q$, by this line of reasoning:

$$
  \begin{aligned}
     \flat Q & \simeq
     \flat [ pt_{\mathbf{B}G} , 
     [V\sslash G, X \times \mathbf{B}G]_{\mathbf{B}G} ]_{/\mathbf{B}G}
     \\
     & \simeq \flat [ pt_{\mathbf{B}G} \times_{\mathbf{B}G} V\sslash G, X \times \mathbf{B}G ]_{\mathbf{B}G}
     \\
     & \simeq \flat [
        V , X \times \mathbf{B}G ]_{\mathbf{B}G}
     \\
     & \simeq
     \flat [V,X]
  \end{aligned}
  \,.
$$

That matches my initial guess that $Q \simeq [V,X]$. 

I am currently hesitant as to how to proceed in the first step above without the $\flat$s. It seems clear, but I need to think about it more. 


But so it looks like this gives a canonical construction of a $G$-action on $[V,X]$. Can we also check that indeed it is the expected action by pre-composition with the $G$-action on $V$?

For a $G$-action on $V$, its invariants are $\Gamma_{\mathbf{B}G}(V\sslash G)$. So maybe I can check what $\Gamma_{\mathbf{B}G}( \sum_{\mathbf{B}G} [V\sslash G, X \times \mathbf{B}G]_{\mathbf{B}G} )$ is. I compute:

$$
  \begin{aligned}
    \Gamma_{\mathbf{B}G}( \sum_{\mathbf{B}G} [V\sslash G, X \times \mathbf{B}G]_{\mathbf{B}G} )
    & \simeq
      \flat [ \mathbf{B}G , [V\sslash G, X \times \mathbf{B}G]_{\mathbf{B}G}]_{\mathbf{B}G}
    \\
    & \simeq
     \flat [ \mathbf{B}G \times_{\mathbf{B}G}  V \sslash G, X \times \mathbf{B}G]_{\mathbf{B}G}
    \\
    & \simeq
      \flat [ V \sslash G  , X \times \mathbf{B}G]_{\mathbf{B}G}
    \\
    & \simeq \flat[ V \sslash G, X ]
  \end{aligned}
$$

which is the right answer, I suppose, the maps $V \to X$ that are invariant under precomposing the $G$-action on $V$.

That's how far I got for the moment. Will further mull over this.



***


category: meta
_
[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects שנה טובה]]
[[!redirects Featured math : Quora]]
