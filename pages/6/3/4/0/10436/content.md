+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Blakers-Massey theorem_ in [[homotopy theory]] states that for $f_1$ and $f_2$ two maps out of the same [[codomain]] which are $n_1$-[[n-connected morphism|connective]] and $n_2$-connective, respectively, then the canonical map from the [[codomain]] into the [[homotopy pullback]] of their [[homotopy pushout]]

$$
  \array{
    X &\stackrel{f_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{f_2}} & \searrow
    \\
    Y_2 && Y_2 \underset{Y_2 \underset{X}{\coprod} Y_1}{\times} Y_1
  }
$$

is $(n_1 + n_2 - 1)$-connective.

In the original statement of the theorem ([Blakers-Massey 51](#BlakersMassey51)) this was considered for the [[homotopy theory]] of [[topological spaces]], hence for [[homotopy types]]/[[∞-groupoids]] &#180;but the statement holds true in all [[(∞,1)-toposes]] (Rezk) and in fact in [[homotopy type theory]] ([Lumsdaine-Finster-Licata 13](#LumsdaineFinsterLicata13)), hence also for "[[geometric homotopy types]]".

## References

The original statement of the theorem is due to 

* A. L. Blakers, W. S. Massey, _The homotopy groups of a triad I_ , Annals of Mathematics 53: 161&#8211;204, (1951)
  {#BlakersMassey51}

The general version of the theorem in [[homotopy type theory]] and

* [[Peter LeFanu Lumsdaine]], [[Eric Finster]], [[Dan Licata]], ...
  {#LumsdaineFinsterLicata13}