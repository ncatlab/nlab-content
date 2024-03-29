
> This entry is about conditional convergence of [[spectral sequences]] in [[homological algebra]] and [[stable homotopy theory]]. For conditional convergence of [[series]] in [[real analysis]] and [[functional analysis]], see *[[conditional convergence]]*. 

---

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[algebraic topology]], _conditional convergence_ refers to a more general kind of convergence of [[spectral sequences]] than actual ("strong") convergence ([def.](spectral+sequence#Convergence)). It is the right concept of convergence for spectral sequences that are not concentrated in the first or third quadrant.

Notably an $E$-[[Adams spectral sequence]]  is in general only conditionally convergent (to the $E$-[[nilpotent completion]]), unless finiteness conditions are imposed

## Definition

Given a [[spectral sequence]] [induced](exact+couple#SpectralSequencesFromExactCouples) from an unrolled [[exact couple]] of the form

$$
  \array{
     \cdots 
       &\stackrel{}{\longrightarrow}& 
     \mathcal{D}^{3,\bullet} 
       &\stackrel{i_2}{\longrightarrow}& 
     \mathcal{D}^{2,\bullet} 
       &\stackrel{i_1}{\longrightarrow} & 
     \mathcal{D}^{1,\bullet} 
       &\stackrel{i_0}{\longrightarrow}& 
     \mathcal{D}^{0,\bullet}
     \\
     && 
     \downarrow^{\mathrlap{}}  &{}_{\mathllap{k_2}}\nwarrow & 
     {}^{\mathllap{j_2}}\downarrow &{}_{\mathllap{k_1}}\nwarrow &
     {}^{\mathllap{j_1}}\downarrow &{}_{\mathllap{k_0}}\nwarrow
     & {}_{\mathllap{j_0}}\downarrow
     \\
     && \mathcal{E}^{3,\bullet} && \mathcal{E}^{2,\bullet} 
     && \mathcal{E}^{1,\bullet} && \mathcal{E}^{0,\bullet}
   }
$$

then it is said to **converge conditionally** to $\mathcal{D}^{0,\bullet}$ if, when regarding $\{\mathcal{D}^{s,\bullet}\}$ as a  [[filtering]] for $\mathcal{D}^{0,\bullet}$ it is _exhaustive_ and _complete_, in that:

1. $\underset{\longleftarrow}{\lim}_s \mathcal{D}^{s,\bullet} = 0$ (the [[limit]] over the filtering vanishes);

1. $\underset{\longleftarrow}{\lim}^1_s \mathcal{D}^{s,\bullet} = 0$ (the [[lim^1]] over the filtering vanishes).


([Boardman 99, def. 5.10](#Boardman99), see also [Rognes 12, def. 2.20](#Rognes12))


The point is that: Given a spectral sequence $\{E_r^{\bullet,\bullet}, d_r\}_r$ as above, that converges conditionally, then sufficient condition that it converges strongly ([def.](spectral+sequence#Convergence)) is that also the [[lim^1]] over its pages vanishes:

$$
  \underset{\longleftarrow}{\lim}^1_r E_r = 0
$$

([Boardman 99, theorem 7.3](#Boardman99), see also [Rognes 12, theorem 2.24](#Rognes12))


## References

Due to 

* {#Boardman99} [[Michael Boardman]], _Conditionally convergent spectral sequences_, 1999 ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/boardman-conditionally-1999.pdf))

Lecture notes include

* {#Rognes12} [[John Rognes]], p 44 of _The Adams spectral sequence_, 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

[[!redirects conditionally convergent spectral sequence]]