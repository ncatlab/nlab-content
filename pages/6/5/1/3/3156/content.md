#Contents#
* automatic table of contents goes here
{:toc}

##Basic idea##

**Natural weak factorization systems** (NWFS) are algebraizations of [[weak factorization system]]s (WFS). The elements in the left and right classes of morphisms are replaced by coalgebras and algebras, respectively, for a certain [[comonad]] and [[monad]] on the [[arrow category]]. This comonad and monad also determine the functorial factorization and give natural coalgebra and algebra structures to the left and right factors.

##Preliminaries##

Recall a **functorial factorization** on a category $K$ is a functor $E : K$<sup>[2]</sup> &rarr; $K$<sup>[3]</sup> that is a section to the composition functor $d_1$, induced by the inclusion functor $d^1 : [2] \rightarrow [3]$ between the ordinal categories.

Explicitly, $E$ factors a morphism $(u,v) : f \Rightarrow g$ in $K^{[2]}$ as

$$
  \array{
    \cdot &\stackrel{u}{\to}& \cdot
    \\
    \downarrow^f
    &&
    \downarrow^g
    \\
   \cdot &\stackrel{v}{\to}& \cdot    
  } \array{ & & } \stackrel{E}{\mapsto} \array{ &&}
  \array{
    \cdot &\stackrel{u}{\to}& \cdot
    \\
    \downarrow^{Lf}
    &&
    \downarrow_{Lg}
    \\
    \cdot  & \stackrel{E(u,v)}{\to} & \cdot 
   \\ \downarrow^{Rf} && \downarrow_{Rg} \\
   \cdot &\stackrel{v}{\to}& \cdot    
  }
$$

There are two other injective functors $d^0, d^2 : [2] \rightarrow [3]$ whose image misses the object that appears as their superscript. When we compose $E$ with $d_2$ and $d_0$, we obtain endofunctors of $K^{[2]}$, which we call $L$ and $R$. 

There are obvious natural transformations $1 \Rightarrow R$ and $L \Rightarrow 1$ whose components are given by the data of the functorial factorization $E$. We say $L$ and $R$ are **pointed** endofunctors, with these natural transformations in mind.

##Definition##

A NWFS on a category $K$ consists of a pair $(L,R)$ where $L$ is a comonad and $R$ is a monad, whose underlying pointed endofunctors arise from a functorial factorization $E$. Some authors (Garner) also require that the canonical natural transformation $LR \Rightarrow RL$, whose domain and codomain components are given by the comultiplication and multiplication maps, is a distributive law of the comonad over the monad. This amounts to the requirement that a pentagon involving the comultiplication and multiplication maps commutes.

We refer to the $L$-coalgebras as the **left class** of the NWFS and the $R$-algebras as the **right class**. When we forget the algebra structures, we obtain classes of maps in $K$. The retract closures of these classes form a WFS called the **underlying WFS** of this NWFS.

Given a lifting problem 
$$
  \array{
    \cdot &\stackrel{u}{\to}& \cdot
    \\
    \downarrow^f
    &&
    \downarrow^g
    \\
   \cdot &\stackrel{v}{\to}& \cdot    
  }$$
where $f$ is a $L$-coalgebra and $g$ is an $R$-algebra, the functorial factorization, coalgebra, and algebra structures can be combined to define a solution, which proves that the left class has the left lifting property with respect to the right class. We leave the details as an exercise.

##Interesting features##

* The right class of a NWFS is closed under any limits that exist in $K^{[2]}$, because the forgetful functor to the underlying category of arrows creates all limits which exist. Note that it does not follow that the right class of the underlying WFS is closed under limits in the arrow category, because first, it is possible that some elements of the right class will not have an $R$-algebra structure, and second, not every map in the arrow category between $R$-algebras is necessarily an $R$-algebra map.

* Algebras for the monad of a NWFS can be composed canonically, as can the coalgebras for the comonad. The composition law for the algebras uses the comultiplication natural transformation, and dually for the coalgebras.

* A NWFS $(L,R)$ on $K$ induces a levelwise NWFS on any diagram category $K^A$. Note that its underlying WFS will not be similarly "levelwise". (Indeed, a WFS does not typically induce a levelwise WFS on a diagram category.)

##Small object argument##

There is a modification of the [[small object argument]], due to Richard Garner, which produces **cofibrantly generated** NWFS. Importantly, Garner's small object argument allows the generators to be a small category over the arrow category $K^{[2]}$, rather than simply a set of arrows. As a result, there are WFS which are not cofibrantly generated in the classical sense, but which can be exhibited as the underlying WFS of a cofibrantly generated NWFS.

## References

* Grandis and Tholen, "Natural weak factorization systems"

* Richard Garner, "Understanding the small object argument", [arXiv](http://arxiv.org/abs/0712.0724).

* Emily Riehl, "Natural weak factorization systems in model structures", [arXiv](http://arxiv.org/abs/0910.2733).
