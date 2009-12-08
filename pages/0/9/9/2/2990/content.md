
#Contents#
* automatic table of contents goes here
{:toc}

## In Top

### Definition

Given a [[continuous map]] $f:X\to Y$ of [[topological space]]s, one can define its **mapping cylinder** as a [[pushout]] 

$$\array{
X&\stackrel{f}\to& Y \\
\sigma_0\downarrow && \downarrow f_*(\sigma_0)\\
X\times I &\stackrel{(\sigma_0)_* (f)}\to & Cyl(f)
}$$

where $I = [0,1]$ (the [[unit interval]]) and $\sigma_0:X\to X\times I$ is given by $x\mapsto (x,0)$. By tradition, homotopy theorists sometimes use the inverted (upside-down) mapping cylinder where $\sigma_0$ is replaced by $\sigma_1:x\mapsto (x,1)$. Of course the two mapping cylinders are [[homeomorphism|homeomorphic]] so it is matter of convention which one to use, of course, compatibly with other constructions depending on the orientation of $I$. 

Set-theoretically, the mapping cylinder is usually represented by the quotient space $(X\times I \coprod Y)/{\sim}$ where $\sim$ is the smallest [[equivalence relation]] identifying $(x,0)\sim f(x)$ for all $x\in X$. 

### Properties

As any other pushout, the mapping cylinder has a universal property: for any space $Z$ and mapping $g_1:X\times I\to Z$, $g_2:Y\to Z$ such that $g_1(x,0)=g_2(f(x))$ for all $x\in X$, there is a unique $k:Cyl(f)\to Z$, such that the composition $X\times I\to Cyl(f)\stackrel{k}\to Z$ equals $g_1$ and the composition $Y\to Cyl(f)\stackrel{k}\to Z$ equals $g_2$.

+-- {: .un_theorem}
###### Theorem
Let $f:X\to Y$ be any continuous map.
The canonical map $j:=f_*(\sigma_0):Y\to Cyl(f)$ is a homotopy equivalence. In fact its homotopy inverse can be chosen a deformation retraction. 
=--

Proof. We exhibit $j$ as a homotopy equivalence by constructing its homotopy inverse $\tilde{f}$ given by $\tilde{f}:[x,t]\mapsto f(x)$, where $[x,t]$ is a class of  $(x,t)\in X\times I$ and $\tilde{f}([y])=[y]$ for $y\in Y$.
Clearly this map is well-defined and 
$\tilde{f}\circ j = \id_Y$. On the other hand, 
$(j\circ\tilde{f})[x,t] = [f(x)]$. Homotopy
$H:\mathrm{Cyl}(f)\times I\to Y$ is given by
$$
H([x,t],\tau) = [x,t(1-\tau)], \,\,\,H([y],\tau)=[y].
$$
It is easy to see that $H(-,0) = \id_{Cyl(f)}$,
$H(-,1)=[-,0]=[f(-)]$ hence $j\circ\tilde{f}\sim id_{Cyl(f)}$.

+-- {: .un_theorem}
###### Theorem
A continuous map $i:A\to X$ is a [[Hurewicz cofibration]] iff there is a [[retraction]] $r:X\times I\to Cyl(f)$ for the canonical map $X\times I \to Cyl(f)$.
=--

+-- {: .un_theorem}
###### Theorem
A continuous map $f:X\to Y$ is a [[homotopy equivalence]] iff $X = X\times\{0\}$ is a [[deformation retract]] of the cylinder $Cyl(f)$.
=--

+-- {: .un_theorem}
###### Theorem
For any $f:X\to Y$, the composition 

$$X\stackrel{\sigma_1}\to X\times I\stackrel{(\sigma_0)_* (f)}\to Cyl(f)$$ 

is a [[Hurewicz cofibration]]. Furthermore, the map $r:Cyl(f)\to Y$ determined by $r([x,t])= f(x)$ (for all $x\in X$ and $t\in I$) and $r([y])=y$ (for $y\in Y$) is well defined and a homotopy equivalence. 

The composition $r\circ (\sigma_0)_* (f)\circ \sigma_1 = f$, hence this is a decomposition of a continuous map into a cofibration followed by a homotopy equivalence.
=--

## Related entries

See also [[mapping cone]].