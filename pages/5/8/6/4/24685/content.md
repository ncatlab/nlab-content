+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Congruences
* table of contents
{: toc}

## Definition

In a [[finitely complete category]] $C$, a **setoid object** is an object $X$ with an [[internalization|internal]] [[pseudo-equivalence relation]] on $X$. This means that it consists of a an object $X$, an object $R$, and morphisms $p_1:R \to X$ and $p_2:R \to X$, equipped with the following [[morphisms]]: 

* internal [[reflexive relation|reflexivity]]: $r \colon X \to R$ which is a [[section]] both of $p_1$ and of $p_2$, i.e., $p_1 r = p_2 r = 1_X$;

* internal [[symmetric relation|symmetry]]: $s \colon R \to R$ which interchanges $p_1$ and $p_2$, i.e., $p_1\circ s = p_2$ and $p_2\circ s = p_1$;

* internal [[transitive relation|transitivity]]: $t: R \times_X R \to R$ which factors the left/right projection map $R \times_X R \to X \times X$ through $R$, i.e., the following diagram commutes
  $$\array{
    && R \\  
    & {}^{\mathllap{t}}\nearrow & \downarrow \\
    R \times_X R & \stackrel{(p_1 q_1,p_2 q_2)}\rightarrow & X \times X
  }
  $$
where $q_1$ and $q_2$ are the projections defined by the [[pullback | pullback diagram]]
  $$\array{
    R \times_X R & \stackrel{q_2}\rightarrow & R
    \\
    \downarrow^{\mathrlap{q_1}} && \downarrow^{\mathrlap{p_1}}
    \\
    R & \stackrel{p_2}\rightarrow & X
  }
  $$

## See also

* [[setoid]]
* [[congruence]]
* [[category object]]

[[!redirects internal pseudo-equivalence relation]]
[[!redirects internal pseudo-equivalence relations]]
[[!redirects internal setoid]]
[[!redirects internal setoids]]
[[!redirects setoid object]]
[[!redirects setoid objects]]