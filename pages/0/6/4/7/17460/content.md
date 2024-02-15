This page concerns:

* Alessandra Capotosti:

  \linebreak

  **From String structures to Spin structures on loop spaces**

  \linebreak

  Ph.D. thesis, 

  Universit&#224; degli Studi Roma Tre, Rome, April 2016

  \linebreak

  [thesis pdf](http://www.matfis.uniroma3.it/Allegati/Dottorato/TESI/capotosti/PhD%20Thesis%202016%20A%20Capotosti.pdf), [[Capotosti-FromStringStructures.pdf:file]] 

   talk slides [[Capotosti-FromStringStruc-Slides.pdf:file]]

on [[differential string structures]].

**Summary**

This thesis derives the [[transgression]] map of [[String structures]] on an $n$-dimensional [[smooth manifold]] $X$ ($n \geq 3$) to [[Spin structures]] on its [[loop space]] from the existence of a natural morphism of [[smooth infinity-stacks|smooth $\infty$-stacks]] 
$$
  \mathbf{B}Spin 
    \longrightarrow 
  \mathbf{B}^2\big(\mathbf{B}U(1)_{conn}\big)
$$
refining the [[first fractional Pontryagin class]] (following [[schreiber:Cech Cocycles for Differential characteristic Classes|Fiorenza, Schreiber and Stasheff 2012]]). This transgression map has been known for a while in the Physics literature, and a completely rigorous proof has
been then given by [[Konrad Waldorf]] in a series of papers. 

Recall that a [[Spin manifold]] $X$ is endowed with a [[String
structure]] if the map $X \overset{f_{T X}}\rightarrow B Spin(n) \overset{\frac{1}{2}p_1}\rightarrow K(\mathbb{Z}, 4)$ is homotopically trivial, where $f_{T X}$ denotes the classifying map for the [[tangent bundle]] of $X$. In this case, the
map $f_{TX}$ can be lifted to a map $X \to B String(n)$, where $B String(n)$ is defined as the [[homotopy
fiber]] of $\frac{1}{2}p_1$. By taking the [[based loop space]] of $B String(n)$ one obtains the topological [[String group]]:
$String(n) = \Omega BString(n)$.

Let now $\mathcal{L}X$ be
the [[free loop space]] of the Spin manifold $X$ and let $\mathcal{L}Spin(n)$ be the [[loop group]] of the [[Spin group]]. Since the
Spin group $Spin(n)$ is [[connected topological space|connected]], the loop space of the Spin manifold $X$ is naturally an
$\mathcal{L}Spin(n)$-manifold (an [[infinite-dimensional manifold|infinite dimensional one]]), i.e., the tangent bundle $T (\mathcal{L}X)$ is naturally associated with an $\mathcal{L}Spin(n)$-bundle over $\mathcal{L}X$ (see [Waldorf 2011, Lemma 5.1](#smooth+loop+space#Waldorf11)  and [Spera & Wurzbacher 2007](smooth+loop+space#SperaWurzbacher07)). 

The loop group $\mathcal{L}Spin(n)$ has a universal [[central extension]]
$$
1 \to U (1) \to\widetilde{\mathcal{L}Spin(n)} \to LSpin(n) \to 1
$$
 and one defines a Spin structure on $\mathcal{L}X$ as a lift of the [[structure group]] of the
tangent bundle $T (\mathcal{L}X)$ of $\mathcal{L}X$ from $\mathcal{L}Spin(n)$ to $\widetilde{\mathcal{L}Spin(n)}$, i.e., as a lift of the tangent
bundle morphism $T (\mathcal{L}X) \,\colon\, \mathcal{L}X \to B\mathcal{L}Spin(n)$ to a morphism 
$$
\mathcal{L}X \to B\widetilde{\mathcal{L}Spin(n)}.
$$
Notice how a Spin structure on a loop space is not, strictly speaking a Spin structure, i.e., it
is not a morphism to $BSpin(dim \mathcal{L}X)$. On the other hand, since $\mathcal{L}X$ is infinite dimensional,
such a notion would be meaningless.

It is well known in the theoretical physics [[folklore]] that a String structure on $X$ is essentially
the same thing as a Spin structure on $\mathcal{L}X$. In a series of articles
Konrad Waldorf has given a rigorous proof of this statement, proving that there is a natural
transgression map
$$
\{\text{String structures on}\;X\} \to \{\text{Spin structures on}\;\mathcal{L}X\},
$$
which induces a bijection at the level of isomorphism classes
$$
\{\text{String structures on}\;X\}/\sim \to \{\text{Spin structures on}\;\mathcal{L}X\}/\sim,
$$
as soon as $X$ is [[compact topological space|compact]] and [[simply connected topological space|simply connected]].

In this Thesis it is shown how the transgression map considered by Waldorf is naturally obtained
from general constructions in the [[(infinity,1)-category|$\infty$-category]] of [[smooth infinity-stacks|smooth infinity-stack]]. It should however be stressed that this abstract derivation of the transgression map does not come with a proof that one gets a bijection on equivalence classes when $X$ is compact and simply connected, and the latter result need to be proved by ad hoc methods. 

The crucial point in the stacky construction of the transgression map is the existence
of a natural morphism of smooth stacks
$$
 \mathbf{B}Spin 
    \longrightarrow 
 {\mathbf{B}}^2\big(\mathbf{B}U(1)_{conn}\big)
$$
refining the [[first fractional Pontryagin class]]. This morphism of smooth stacks appears implicitly in [Waldorf 2016](smooth+loop+space#Waldorf16) in the form of a multiplicative [[bundle gerbe]] [[connection on a bundle gerbe|with connection]] over the [[Spin group]], and as such plays
an essential role in Waldorf’s proof. In particular, the central extension $\widetilde{\mathcal{L}Spin}$ considered in the Thesis is what Waldorf calls a *fusion extension* of $\mathcal{L}Spin$. 

But once the canonical
multiplicative gerbe with connection over $B Spin$ is regarded as a morphism of [[smooth infinity-stack|smooth $\infty$-stacks]], everything else follows by very general reasoning. For instance, the fact that $\widetilde{\mathcal{L}Spin}$ is a fusion extension of $\mathcal{L}Spin$ is encoded into the natural [[homotopy fiber sequence]] of smooth stacks
$$
  \array{ 
    \mathbf{B}\widetilde{\mathcal{L}Spin} 
    & \rightarrow & 
    \ast  
    \\
    \big\downarrow && \big\downarrow 
    \\
    \mathbf{B}\mathcal{L}Spin 
    &\rightarrow& 
    \mathbf{B}^2 U(1) 
  }
$$
induced by the morphism $\mathbf{B}Spin \to {\mathbf{B}}^2\big({\mathbf{B}}U(1)_{conn}\big)$ and by the [[holonomy]] morphism. Also, in the Thesis is provided a direct proof of the existence of the morphism $\mathbf{B}Spin \rightarrow {\mathbf{B}}^2\big({\mathbf{B}}U(1)_{conn}\big)$ which
does not rely on Waldorf’s result and is instead based on the differential refinement of the
first fractional Pontryagin class
$$
  \frac{1}{2} \hat{\mathbf{p}}_1 
  \colon 
  \mathbf{B}Spin_{conn} \to \mathbf{B}^3 U(1)_{conn}
$$
constructed in [[schreiber:Cech Cocycles for Differential characteristic Classes|Fiorenza, Schreiber and Stasheff 2012]].

## Related entries

* [[stringor bundle]]


category: reference

[[!redirects Alessandra Capotosti]]

