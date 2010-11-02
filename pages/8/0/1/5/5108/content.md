##Idea##


In modal logic, the relational signature of the [[relational structures]] being described by a given logic are sometimes called a  **modal similarity type**.  

+--
{: .un_def}
######Definition######
A modal similarity type is given by a pair $\tau = (O,\rho)$ where $O$ is a (usually non-empty) set and $\pho : O \to \mathbb{N}$ is a function.  The elements of $O$ are called the (labels for) **modal operators** and, if $\Delta \in O$, then $\rho(\Delta)$ indicates the **arity** of the modal operator $\Delta$, i.e. the number of arguments to which $\Delta$ is applied, so that, if $\rho(\Delta)= n$, the label $\Delta$ stands will stand for an $n$-ary relation on a given set.
=--

A _modal similarity type_ thus determines a **single sorted** relational [[signature (in logic)|signature]], $\Sigma$ where, in the notation used in the page on [[signatures in logic]], $Rel(\Sigma) = O$ and $ar: Rel(\Sigma) \to S^*$ is just  $\rho$.

##References##

General books on modal logics include

* P. [[Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.