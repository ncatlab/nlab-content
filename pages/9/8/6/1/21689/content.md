
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
     n \in \Gamma_n N 
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

[[!redirects nilpotent module]]
