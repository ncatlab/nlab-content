#Definition#

In a category with [[interval object]] the 
free **loop space object** is the part of the [[path object]] $B^I = [I,B]$ which consists of closed paths, namely the [[pullback]]
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

#Remarks#

* The loop space object $B$ can be regarded as the homotopy trace on the identity span on $B$, as described at [[span trace]].

* The free loop space object inherits the structure of an [[A-infinity category]] from that of the [[path object]] $[I,B]$. 

#Examples#

* Let $C = Groupd$ with the standard interval object $I = \{a \stackrel{\simeq}{\to} b\}$ and let $\mathbf{B}G$ be the one-object groupoid corresponding to a group $G$, then
$$
  \Lambda \mathbf{B}G = G//_{Ad}G
$$
is the [[action groupoid]] of $G$ acting on itself by its adjoint action.

