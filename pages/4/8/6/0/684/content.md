#Definition#

##Free loop space object##

In a category with [[interval object]] the 
**free loop space object** is the part of the [[path object]] $B^I = [I,B]$ which consists of closed paths, namely the [[pullback]]
$$
  \array{
    \Lambda B &\to& [I,B]
    \\
    \downarrow && \downarrow^{d_0 \times d_1}
    \\
    B &\stackrel{Id \times Id}{\to}& B \times B
  }
  \,.
$$

This is the same as the image of the [[co-span co-trace]] $cotr(I)$  of the interval object (which is the interval object closed to a loop!,  see the examples at [[co-span co-trace]]) in $B$:

$$
  \left[
  \array{
     && cotr(I)
     \\
     & \nearrow && \nwarrow
     \\
     pt &&&& I
     \\
     & {}_{Id \sqcup Id}\nwarrow && \nearrow_{in \sqcup out}
     \\
     && pt \sqcup pt
  }
  \;\;\;\;,\;\;\;\;
  B
  \right]
  \;,\;\;\;\;
  \simeq
  \;,\;\;\;\;
  \array{
     && \Lambda B
     \\
     & \swarrow && \searrow
     \\
     B &&&& [I,B]
     \\
     & {}_{Id \times Id}\searrow && \swarrow_{d_0 \times d_1}
     \\
     && B \times B
  }
$$


##Based loop space object##

If $B$ is a [[pointed object]] with point $pt \stackrel{pt_B}{\to} B$ then the **based loop space object** of $B$ is the pullback $\Omega_{pt} B$ in

$$
  \array{
    \Omega_{pt}B &\to& [I,B]
    \\
    \downarrow && \downarrow^{d_0 \times d_1}
    \\
    pt
    &\stackrel{pt_B \times pt_B}{\to}&
    B \times B
  }
  \,.
$$

###Remarks

* $\Omega_{pt}B$ is the fiber of the [[generalized universal bundle]] $\mathbf{E}_{pt}B \to B$.

* the based loop space object $\Omega_{pt} B$ is the pullback of the free loop space object $\Lambda B$ to the point
$$
  \array{
    \Omega_{pt} B &\to& \Lambda B
    \\
    \downarrow && \downarrow
    \\
    pt &\stackrel{pt_B}{\to}& B 
  }
  \,.
$$



#Remarks#

* The loop space object $B$ can be regarded as the homotopy trace on the identity span on $B$, as described at [[span trace]].

* The free loop space object inherits the structure of an [[A-infinity category]] from that of the [[path object]] $[I,B]$. 

#Examples#

* Let $C =$ [[Top]] with the standard [[interval object]]. Then for $B= X$ a topological space $\Lambda B = \Lambda X$ is the ordinary free loop space of $X$.

* Let $C = $ [[Grpd]] with the standard interval object $I = \{a \stackrel{\simeq}{\to} b\}$ and let $\mathbf{B}G$ be the one-object groupoid corresponding to a group $G$, then
$$
  \Lambda \mathbf{B}G = G//_{Ad}G
$$
is the [[action groupoid]] of $G$ acting on itself by its adjoint action. Notice the example at [[co-span co-trace]] which says that the cotrace on $I$ is $cotr(I) = \mathbf{B}\mathbb{Z}$, and indeed
$$
  \Lambda \mathbf{B}G =  [\mathbf{B}\mathbb{Z}, \mathbf{B}G]  
  \,.
$$
The role of this $\Lambda \mathbf{B}G$ as a loop object is amplified in particular in
   * Simon Willerton, _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv](http://arxiv.org/abs/math.QA/0503266))
   * Bruce Bartlett, _On unitary 2-representations of finite groups and topological quantum field theory_ ([arXiv](http://arxiv.org/abs/0901.3975))

* On the other hand, the _based_ loop object of $\mathbf{B}G$ is just $G$:
$$
  \Omega \mathbf{B}G = G
  \,.
$$
