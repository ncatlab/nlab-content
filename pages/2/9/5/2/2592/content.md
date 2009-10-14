
#Contents#
* automatic table of contents goes here
{:toc}



#In a lined topos#

+-- {: .query}

Not just to make this entry interesting for the $n$Lab, but also because I might actually need this for an application, I'd like to give a discussion of the orthogonal group and of the [[general linear group]] inside an arbitrary [[lined topos]]. What can one say?

=--


Let $(\mathcal{T}, R)$ be a [[lined topos]].

Then for $n \in \mathbb{N}$ the _orthogonal group_ $O(n)$ is the subgroup of the [[automorphism]] group $Aut_{\mathcal{T}}(R^n)$ of the $n$-fold [[product]] $R^n$ of the line $R$ in $\mathcal{T}$.



# Whitehead tower and higher orientation structures#

The [[Whitehead tower]] of the orthogonal group plays an important role in appliications related to [[quantum physics]]. 

The first steps are

$$
  \cdots \to Fivebrane(n)
  \to String(n) \to Spin(n)
  \to SO(n)
  \to O(n)
$$

[[Fivebrane group]] $\to$ [[String group]] $\to$ [[Spin group]] $\to$ [[special orthogonal group]] $\to$ orthogonal group.


Given a [[manifold]] $X$, lifts of the structure map $X \to \mathcal{B}O(n)$ of the $O(n)$-[[principal bundle]] to which the [[tangent bundle]] is [[associated bundle|associated]] through this tower define, respectively

* [[orientation]]

* [[Spin structure]]

* [[String structure]]

* [[Fivebrane structure]]

on $X$.