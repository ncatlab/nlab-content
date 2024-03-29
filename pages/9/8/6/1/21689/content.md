
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Let $G$ be a [[group]], $N$ an [[abelian group]] and $(-)\cdot (-) \colon G \times N \to N$ an [[action]] of $G$ on $N$ by [[linear maps]], thus making $N$ a [[module]] over $G$. 

Then this is called a _nilpotent module_ if the [[sequence]] of abelian subgroups 

$$
  \Gamma_0 N 
    \supset 
  \Gamma_1 N
    \supset   
  \Gamma_2 N
    \supset
  \cdots   
  \,,
$$

given [[recursion|recursively]] by 

$$
  \begin{aligned}
  \Gamma_0 N & \coloneqq\; N
  \\
  \Gamma_{k+1} N 
    & \coloneqq\; 
  \big\{
     g \cdot n - n
     \;\vert\;
     g \in G,\;
     n \in \Gamma_k N 
  \big\}
  \,,
  \end{aligned}
$$ 

terminates, in that there is $k_{max} \in \mathbb{N}$ with 
$\Gamma_{k_{max}}N = 0$.

## Related concepts

* [[nilpotent group]]

* [[nilpotent topological space]]

* [[nilpotent Lie algebra]]

* [[nilpotent element]]

\linebreak

* [[rational homotopy theory]]

  * [[Sullivan model]]

  * [[rational fiber lemma]]

## References

* [[Peter Hilton]], _Nilpotency in group theory and topology_, Publicacions de la Secció de Matemàtiques Vol. 26, No. 3 (1982), pp. 47-78 ([jstor:43741908](https://www.jstor.org/stable/43741908))




[[!redirects nilpotent modules]]
