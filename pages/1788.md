
\begin{tikzcd}
    \mathrm{Ho}
    \Big(
      \big(
        \mathrm{dgcAlg}^{\geq 0 }_{\color{blue}\mathbb{Q}}
      \big)^{\mathrm{op}}_{\mathrm{proj}}
    \Big)
    \ar[
      dd,
      "{
        \mathbb{R}
        \big(
          (-) \otimes_{\mathbb{Q}} \mathbb{R}
        \big)
      }"{right}
    ]
    &&
    \;\;
    \mathrm{Ho}
    \big(
      \mathrm{sSets}_{\mathrm{Qu}}
    \big)^{\mathrm{fin}_{\mathbb{Q}}}
    \ar[
      ll,
      "
        \mathbb{L}
        \Omega^\bullet_{\mathrm{P}{\color{blue}\mathbb{Q}}\mathrm{LdR}}
      "{above}
    ]
    \ar[
      dd,-,
      shift right=1pt
    ]
    \ar[
      dd,-,
      shift left=1pt
    ]
    \\
    \\
    \mathrm{Ho}
    \Big(
    \big(   
      \mathrm{dgcAlg}^{\geq 0}_{\color{blue}\mathbb{R}}
    \big)^{\mathrm{op}}_{\mathrm{proj}}
    \Big)
    &&
    \;\;
    \mathrm{Ho}
    \big(
      \mathrm{sSets}_{\mathrm{Qu}}
    \big)^{\mathrm{fin}_{\mathbb{Q}}}
    \ar[
      ll,
      "
        \mathbb{L}
        \Omega^\bullet_{\mathrm{P}{\color{blue}\mathbb{R}}\mathrm{LdR}}
      "{below}
    ]
\end{tikzcd}


\linebreak

For $\mathbf{H}$ an $\infty$-topos
and $G \in Groups(\mathbf{H})$,
one would expect that 

(1)
group objects 
$\Gamma /\!\!/ G \,\in\, \mathrm{Groups}\big( \mathbf{H}_{/\mathbf{B}G} \big)$
in the slice over the delooping of $G$

are equivalent to 

(2) group objects $\Gamma \,\in\, \mathrm{Groups}(\mathbf{H})$
equipped with an action of $G$ by group automorphisms.

A construction $(2)\Rightarrow (1)$ is in Prop. 2.102 on [p. 35](https://ncatlab.org/schreiber/files/orbi210607.pdf#page=35) of *[[schreiber:Proper Orbifold Cohomology|Proper Orbifold Cohomology]]*.

The following are some thoughts on how to go about $(1) \Rightarrow (2)$, but not conclusive yet.

The following pasting diagram shows something slightly weaker:

  \begin{tikzcd}
    &
    G 
    \ar[r]
    \ar[
      d,
      "{(e,\mathrm{id})}"{left}
    ]
    \ar[
      dr,
      phantom,
      "\mbox{\tiny\rm(d)}"
    ]
    &
    \ast
    \ar[d]
    \\
    G
    \ar[r]
    \ar[d]
    \ar[
      dr,
      phantom,
      "\mbox{\tiny\rm(d)}"
    ]
    &
    \Gamma \times G
    \ar[
      r,
      "\mathrm{pr}_1"{description}
    ]
    \ar[
      d,
      "\rho"{description}
    ]
    \ar[
      dr,
      phantom,
      "{\mbox{\tiny (c)}}"
    ]
    & 
    \Gamma
    \ar[d]
    \ar[rr]
    \ar[
      drr,
      phantom,
      "{\mbox{\tiny (b)}}"
    ]
    &&
    \ast
    \ar[d]
    \\
    \ast
    \ar[r]
    &
    \Gamma
    \ar[d]
    \ar[r]
    \ar[
      dr,
      phantom,
      "{\mbox{\tiny (b)}}"
    ]
    &
    \Gamma /\!\!/ G
    \ar[rr]
    \ar[d]
    \ar[
      drr,
      phantom,
      "\mbox{\tiny\rm(a)}"
    ]
    &&
    \mathbf{B}G
    \mathrlap{
      \;
      \simeq
      \Gamma /\!\!/ (\Gamma \rtimes G)
    }
    \ar[d]
    \\
    &
    \ast
    \ar[r]
    &
    \mathbf{B}G
    \ar[rr]
    &&
    \underset{\mathbf{B}G}{\sum} \mathbf{B} (\Gamma /\!\!/ G)
    \mathrlap{
      \;
      \simeq
      \mathbf{B}(\Gamma \rtimes G)
    }
    \ar[d]
    \\ 
    &&&&
    \mathbf{B}G
    &
    {\phantom{AAAAAAAAAA}}
  \end{tikzcd}

Here:

(a) is the homotopy pullback that exhibits $\Gamma /\!\!/ G$
as a group object in the slice over $\mathbf{B}G$;

(b) is the homotopy pullback that exhibits $\Gamma /\!\!/ G$
as the homotopy quotient of a $G$-action on $\Gamma$;

(c) is the homotopy fiber product which exhibits
the shear map equivalence of 
$\Gamma$ as a principal $G$-bundle over $\Gamma /\!\!/ G$;

(d) is a homotopy pullback implied from this by the pasting law.

While we can't seem to conclude group structure on $\Gamma$ directly, 
we see that $\Gamma \times G$ carries a group structure,
to be denoted $\Gamma \rtimes G$, whose delooping is 
the bottom right object.


Moreover, 
$G \xrightarrow{(e,\mathrm{id})} \Gamma \times G$ is
exhibited as a homomorphism of group objects.


Also, we see that 
$G \xrightarrow{(e,\mathrm{id})} \Gamma \times G \xrightarrow{\rho} \Gamma$
are $G$-equivariant maps for $G$ acting by right multiplication on itself.
This implies that $\rho$ is the given $G$-action, 

So we are beginning to see that $\Gamma \!\sslash\! G \in Groups\big( \Gamma \rtimes G\big)$ is equivalent to a  "semidirect product $\infty$-group"
$\Gamma \rtimes G$. 

But can we make explicit that the action of $G$ on $\Gamma$ is by group automorphisms? This would require constructing a homotopy fiber sequence of the form

$$
  \array{
    \mathbf{B}\Gamma
    &\longrightarrow&
    \mathbf{B}(\Gamma \rtimes G)
    \\
    && \big\downarrow
    \\
    && \mathbf{B}G
  }
$$

How to see this homotopy fiber from the above diagram (or from some other consideration)?


\linebreak
\linebreak
