
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

Given a sequence of [[short exact sequences]] of the form

$$
  0
    \to 
  X_n 
    \overset{i_n}{\longrightarrow}
  Y_n
    \overset{p_n}{\longrightarrow}
  X_{n+1}
    \to
  0
$$

for $n \in \mathbb{Z}$, then their **splicing** is the horizontal [[composition|composite]] sequence

$$
  \array{
    \cdots
     && \overset{}{\longrightarrow} &&
    Y_{n-1}
     && \longrightarrow &&
    Y_n
     && \longrightarrow &&
    Y_{n+1}
     && \longrightarrow &&
    \cdots
    \\
    &&
    &&
    & {}_{\mathllap{p_{n-1}}}\searrow && \nearrow_{\mathrlap{ i_n } }
    &&
    {}_{\mathllap{p_n}}\searrow 
      && 
    \nearrow_{\mathrlap{ i_{n+1} }}
    \\
    &&
    &&
    &&
    X_n
    &&
    &&
    X_{n+1}
  }
$$

which is, evidently, a [[long exact sequence]].

More generally, there is splicing of interlocking systems of [[long exact sequences]]. See at _[Exact couple of a tower of fibrations](exact+couple#ExactCoupleOfATowerOfFibrations)_.

## Related entries

* [[Adams spectral sequence]]

