
#Contents#
* table of contents
{:toc}

##Idea##

A **wheeled graph** in the sense of ([HRY](#HRY)) is a generalization of the notion of a [[directed pseudograph]]. What differentiates a wheeled graph from a [[directed pseudograph]] is the notion of an "exceptional cell," which should be thought of as a set of half edges which are not adjacent to any vertex. 

The basic idea behind a wheeled graph is that it is a set of vertices with directed edges between them but also edges that leave and enter the graph. It can also have loops and even edges that are not adjacent to any vertex (called **exceptional edges**, see [[generalized graph]] for more). Moreover, a wheeled graph $G$ is equipped with a coloring, i.e. there is a function $Vt(G)\overset{\kappa}\to \mathcal{C}$ from the vertices of $G$ to a set of colors. Since wheeled operads have inputs and outputs, this makes them suitable for modeling [[PROPs]] and [[properads]]. 

The term "wheeled" refers to the fact that a [[generalized graph]] $G$ might have directed loops in it. These can be in the form of vertices with loops, closed directed paths in $G$, or "exceptional loops" that have no vertices at all (see the examples below). Sometimes, we will be interested in wheel-free graphs, which are wheeled graphs without wheels (though they are not, crucially, just [[graphs]].)  

This entry relies on notation defined in [[generalized graph]]. 

## Definitions ##
 The following is the fifth item of Definition 2.5 of [HRY](#HRY):

+-- {: .num_defn }
###### Definition

A wheeled graph is a [[generalized graph]] equipped with a coloring, a direction and a listing (see [here](https://ncatlab.org/nlab/show/generalized+graph#properties) for definitions of these properties). 
 
=--

## Extra Structure 

Wheeled graphs can have a number of attributes. Most of the following are self-explanatory though stating them in the terminology of [[generalized graph]] as [HRY]{#HRY} does, can be tedious: 

* One of these, confusingly, is being **wheel-free**. In other words, a wheeled graph which is wheel-free is a generalized graph with a coloring, a direction and a listing, but without any loops (either ordinary or exceptional) or directed paths with identical initial and terminal vertex. 

* A wheeled graph is **connected** if it is a single exceptional edge, a single exceptional loop,  or has empty exceptional cell, is non-empty and between any two vertices there is an edge.

* A wheeled graph is **simply connected** if it is connected, is not an exceptional loop, and contains no cycles. 

* A wheeled graph is a **unital tree** if it is simply connected and each vertex has exactly one output flag.

* A wheeled graph is a **linear graph** if it is a linear tree in which each vertex has exactly one input flag. 


Using these definitions we can define the following sets:

* Define $Gr_c^{\circlearrowleft}$ to be the set of connected wheeled graphs.

* Define $Gr_c^{\uparrow}$ to be the set of connected wheel-free graphs. 

* Define $Gr_{di}^{\uparrow}$ to be the set of simply connected wheel-free graphs.

* Define $UTree$ and $ULin$ to be the sets of unital trees and linear graphs, respectively. 

Note that $UTree$ and $ULin$ are effectively the object sets of the category of [[trees]] and the [[simplex category]] respectively. 

## Examples

1. The most elementary wheeled graph (which is also of course an ordinary [[graph]] and a [[quiver]]) is the empty wheeled graph which has the [[empty set]] as its set of flags and as such no vertices or edges. 
1. Any [[quiver]] can be realized as a wheeled graph in an obvious way.
1. There is a graph $I$ with $Flag(I)=\{e_{-1},e_1\}$, $\iota(e_i)=e_i$, $\kappa(e_i)=c$, $\delta(e_i)=i$. This is the **$c$-colored exceptional edge**. It can be represented schematically by 
$$
\uparrow_c.
$$
1. There is a graph $W$ which is identical to $I$ except that $\iota(f_{-1})=f_1$ and $\iota(f_1)=f_{-1}$. This is the **$c$-colored exceptional loop**. The involution $\iota$ can be thought of as "spinning" the loop. It can be represented schematically by
$$
\circlearrowleft_c.
$$

## Related concepts

* [[graph]]

* [[quiver]]

* [[generalized graph]]

* [[PROP]]

* [[properad]]

## References




* [[Philip Hackney]], [[Marcy Robertson]] and [[Donald Yau]]. _Infinity Properads and Infinity Wheeled Properads_,  Lecture Notes in Mathematics, 2147. Springer, Cham, 2015. [(arxiv version)](http://arxiv.org/pdf/1410.6716v2.pdf)
{#HRY} 


