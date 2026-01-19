
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


\tableofcontents


## Idea

The _IPC-property_ ("inductive limit product commutation property") is a technical condition on a [[category]] $A$ which ensures that [[presheaves]] with values in $A$ have a good notion of [[sheafification]].

## Definition

A [[category]] $A$ is said to satisfy the **IPC-property** if

* it admits [[small limit|small]] [[products]] and [[filtered category|filtered]] [[colimits]];

* for 

  * every [[indexed set]] $\{I_s\}_{s \in S}$ of [[small category|small]] [[filtered categories]] and

  * for any [[indexed set]] $\{\alpha_s \colon I_s \to A\}$ of [[functors]]

  * indexed by a [[small set]] $S$ 

  the canonical [[morphism]]

  $$
    colim \left(
      \prod_s I_s 
      \xrightarrow
        { k \mapsto \prod_s \alpha_s(\pi_s(k)) }
      A
    \right)
    \longrightarrow
    \prod_s colim \alpha_s
  $$

  is an [[isomorphism]].

## References


* {#KashiwaraSchapira2006} [[Masaki Kashiwara]], [[Pierre Schapira]]; Def. 3.1.10 in in: *[[Categories and Sheaves]]*, Grundlehren der Mathematischen Wissenschaften __332__, Springer (2006) &lbrack;[doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)&rbrack;

It is invoked for [[sheafification]] in section 17.4 there.


