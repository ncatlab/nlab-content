
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The "retract argument" is a simple but frequently useful standard lemma in discussion of [[weak factorization systems]]. It asserts that if a [[morphism]] factors as the [[composition]] of two factors such that it is has the left or right [[lifting property]] against its second or first factor, respectively, then it is a [[retract]] (as an [[object]] of the [[arrow category]]) of the respective other factor.

The retract argument is frequently used in the verification of the [[axioms]] of [[model category]] structures. 

## Statement

+-- {: .num_lemma #RetractArgument}
###### Lemma
**(retract argument)**

Consider a [[composition|composite]] [[morphism]]

$$
  f \;\colon\; X\stackrel{i}{\longrightarrow} A \stackrel{p}{\longrightarrow} Y
  \,.
$$

Then:

1. If $f$ has the [[left lifting property]] against $p$, then $f$ is a [[retract]] of $i$.

1. If $f$ has the [[right lifting property]] against $i$, then $f$ is a [[retract]] of $p$.

=--

+-- {: .num_remark #RetractsOfMorphisms}
###### Remark

Here by a _retract_ of a [[morphism]] $X \stackrel{f}{\longrightarrow} Y$ in some [[category]] $\mathcal{C}$ is meant a [[retract]] of $f$ as an object in the [[arrow category]] $\mathcal{C}^{\Delta[1]}$, hence a morphism $A \stackrel{g}{\longrightarrow} B$ such that in $\mathcal{C}^{\Delta[1]}$ there is a factorization of the identity on $g$ through $f$

$$
  id_g \;\colon\;
  g \longrightarrow f \longrightarrow g
  \,.
$$

This means equivalently that in $\mathcal{C}$ there is a [[commuting diagram]] of the form

$$
  \array{
    id_A \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}}
    \\
    id_B \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof 
(of lemma \ref{RetractArgument})

We discuss the first statement, the second is [[formal duality|formally dual]].

Write the factorization of $f$ as a [[commuting square]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A 
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By the assumed [[lifting property]] of $f$ against $p$ there exists a diagonal filler $g$ making a [[commuting diagram]] of the form

$$
  \array{
    X &\stackrel{i}{\longrightarrow}& A 
    \\
    {}^{\mathllap{f}}\downarrow &{}^{\mathllap{g}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &= & Y
  }
  \,.
$$

By rearranging this diagram a little, it is equivalent to 

$$
  \array{
    & X &=& X 
    \\
    & {}^{\mathllap{f}}\downarrow 
     &&
    {}^{\mathllap{i}}\downarrow 
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$

Completing this to the right, this yields a diagram exhibiting the required retract according to remark \ref{RetractsOfMorphisms}:

$$
  \array{
    id_X \colon & X &=& X &=& X
    \\
    & {}^{\mathllap{f}}\downarrow 
     &&
    {}^{\mathllap{i}}\downarrow 
     &&
     {}^{\mathllap{f}}\downarrow
    \\
    id_Y \colon & Y &\underset{g}{\longrightarrow}& A &\underset{p}{\longrightarrow}&
    Y
  }
  \,.
$$


=--
