+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}



## Definition 

If $G$ is a [[topological group]], then the **identity component** is the [[connected space|connected component]] of the [[identity element]] $e$ in $G$. 

## Basic results 

+-- {: .un_prop}
###### Proposition 
The identity component $G_0$ is a [[closed set|closed]] [[normal subgroup]] of $G$. 
=--

+-- {: .proof} 
###### Proof 
It is clearly closed (indeed, any connected component is closed). If $g, h \in G_0$, then $g h$ is in the same connected component as $g$ (since $h$ is in the same connected component as $e$ and left multiplication by $g$ is a [[homeomorphism]]), which in turn is in the same connected component as $e$. Using similar reasoning, if $g$ is in the connected component as $e$, then $e$ is in the same connected component as $g^{-1}$. Hence $G_0$ is a subgroup. 

If $\phi$ is any [[automorphism]] of $G$, then $\phi(G_0) = G_0$. (Indeed, $\phi(G_0)$ is a connected set containing $e$ and therefore $\phi(G_0) \subseteq G_0$. Replacing $\phi$ by its [[inverse]] $\phi^{-1}$, we similarly have $\phi^{-1}(G_0) \subseteq G_0$ and therefore $G_0 \subseteq \phi(G_0)$.) Applying this to [[inner automorphism|inner automorphisms]] $\phi$, we conclude that $G_0$ is a normal subgroup of $G$. 
=-- 

* **Remark:** $G_0$ need not be [[open set|open]] in $G$; for example, for the group of $p$-[[p-adic integer|adic integers]], $G_0$ is the (non-open) [[singleton]] $\{e\}$. However, if $G$ is [[locally connected space|locally connected]], for example if $G$ is a [[Lie group]], then $G_0$ is open (and therefore also [[clopen]]. In this case, $G/G_0$ is discrete (because $G \to G/G_0$ is an open map, implying that the identity and therefore every point in $G/G_0$ is open). 

+-- {: .un_prop}
###### Proposition  
The group $G/G_0$, equipped with the [[quotient space|quotient space topology]], is a [[Hausdorff space|Hausdorff]] [[topological group]]. 
=-- 

+-- {: .proof} 
###### Proof 
Given the fact that $p \colon G \to G/G_0$ is an [[open map|open]] [[surjection]], the [[product]] $p \times p \colon G \times G \to G/G_0 \times G/G_0$ is also an open surjection and therefore a quotient map. It follows easily from the [[universal property]] of quotient maps that the multiplication $G \times G \to G$ therefore descends to a continuous multiplication $G/G_0 \times G/G_0 \to G/G_0$, so that $G/G_0$ is a topological group. 

Because a topological group is a [[uniform space]], the Hausdorff condition follows from a weaker [[separation axiom]] such as $T_1$ (points are closed). It suffices that the identity of $G/G_0$ be closed. Its [[complement]] $C$ is the image under $p$ of the complement of $G_0$ in $G$ (just by examining [[coset]] decompositions), which is open. Since $p$ is an open map, it follows that $C$ is open, so that $\{e\}$ is closed, as desired. 
=-- 
