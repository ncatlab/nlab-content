
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Bohr compactification_ is a kind of [[compactification]] of a [[topological group]] to one that is [[compact topological space|compact]] [[Hausdorff topological space|Hausdorff]].

## Definition and existence 

Let $i: CHGrp \to TopGrp$ denote the full embedding of the category of compact Hausdorff topological groups into the category of all topological groups. Let $G$ be a topological group. 

+-- {: .num_defn} 
###### Definition 
The *Bohr compactification* $Bohr(G)$ is a representing object for the functor $TopGrp(G, i-): CHGrp \to Set$. 
=-- 

+-- {: .num_theorem} 
###### Theorem 
The Bohr compactification exists for any topological group $G$. 
=-- 

+-- {: .proof} 
###### Proof 
We verify that the hypotheses of the general [[adjoint functor theorem]] are satisfied. Certainly $CHGrp$ is complete, and $i: CHGrp \to TopGrp$ preserves small limits since products and equalizers in $CHGrp$ are formed just as they are in $TopGrp$. We must now show there is a small solution set, i.e., a [[weakly initial set]] for the comma category $G \downarrow i$. 

Let $I = [0, 1]$ be the unit [[interval]] with its standard topology. There is a canonical map $u_G: G \to I^{Top(G, I)}$ where $u: id \to M$ is the unit of the monad $M = I^{Top(-, I)}$ on $Top$; note $u_X$ is a closed embedding if $X$ is compact Hausdorff (see the discussion [here](http://ncatlab.org/nlab/show/compactum#StoneCechCompactification)). We claim that the collection of closed subspaces of $I^{Top(G, I)}$ that come equipped with topological group structures is a solution set. Indeed, for an arbitrary CH group $K$ and continuous homomorphism $f: G \to K$, the closure of the image $\widebar{f(G)}$ is a compact Hausdorff subgroup of $K$ through which $f$ factors (according to the lemma that follows), and this is a closed subspace of $M(f)^{-1}(u_K)$ in the pullback diagram 

$$\array{
M(f)^{-1}(u_K) & \hookrightarrow & I^{Top(G, I)} \\ 
\downarrow & & \downarrow_{M(f)} \\ 
K & \underset{u_K}{\hookrightarrow} & I^{Top(K, I)}
}$$ 

and therefore $\widebar{f(G)}$ occurs as a closed subspace of $I^{Top(G, I)}$, as claimed. 
=-- 

+-- {: .num_lemma} 
###### Lemma 
If $H$ is a topological group and $J \subseteq H$ is a subgroup, then the topological closure $\widebar{J} \subseteq H$ is also a subgroup. (The same is true for any finitary algebraic theory in place of the theory of groups.) 
=-- 

+-- {: .proof} 
###### Proof 
For $X, Y$ arbitrary topological spaces and subsets $A \subseteq X$, $B \subseteq Y$, it is elementary that $\widebar{A \times B} = \widebar{A} \times \widebar{B}$. Hence for any operation $m: H^n \to H$ that $J$ is closed under, $\widebar{J}^n = \widebar{J^n}$ is contained in $m^{-1}(\widebar{J})$ (by continuity of $m$), so that $m$ restricts to an operation $\widebar{J}^n \to \widebar{J}$ as required. 
=-- 

+-- {: .num_remark} 
###### Remark 
The Bohr compactification admits a more elegant construction if $G$ is a topological *abelian* group: if $S = S^1$ is the unit [[circle]], then $Bohr(G)$ may be taken to be the closure of the image of $G$ under the canonical map $G \to S^{TopAb(G, S)}$. The argument is that it suffices to consider only compact Hausdorff abelian groups $K$, where $K$ embeds as a closed subgroup of $S^{TopAb(K, S)}$ by [[Pontryagin duality]]; using a pullback similar to the above, the argument is easily completed. The description simplifies further if $G$ is a locally compact Hausdorff abelian group; here $Bohr(G)$ is the Pontryagin dual of the discretization of the Pontryagin dual of $G$. 
=-- 

## Example 

A MathOverflow question from 2011 asks whether, for $G$ a compact Hausdorff group, can $\mathbb{Z}$ appear as a quotient of $G$ *considered as an abstract group*? 

A truly simple answer was [given](http://mathoverflow.net/questions/80966/morphism-from-a-compact-group-to-z#) by Sean Eberhard using the Bohr compactification, as follows. A quotient $p: G \to \mathbb{Z}$ admits a section $i: \mathbb{Z} \to G$ which extends to the Bohr compactification $\widehat{i}: Bohr(\mathbb{Z}) \to G$. The composite $p \widehat{i}: Bohr(\mathbb{Z}) \to \mathbb{Z}$ is still surjective as its restriction along the unit $\mathbb{Z} \to Bohr(\mathbb{Z})$ is the identity. According to the remark above, $Bohr(\mathbb{Z})$ is the Pontryagin dual of the discrete group $S^1 \cong \mathbb{R}_{disc} \oplus \mathbb{Q}/\mathbb{Z}$, so $Bohr(\mathbb{Z}) \cong \mathbb{R}_{disc}' \oplus (\mathbb{Q}/\mathbb{Z})'$. Now the Pontryagin dual of a discrete torsionfree group such as $\mathbb{R}_{disc}$ is divisible (more generally, if $Q$ is an injective module over a commutative ring and $F$ is flat, then $\hom(F, Q)$ is also injective), so the restriction of $p \widehat{i}: Bohr(\mathbb{Z}) \to \mathbb{Z}$ to the summand $\mathbb{R}_{disc}'$ is zero. But the restriction to the other summand $(\mathbb{Q}/\mathbb{Z})' \cong \widehat{\mathbb{Z}} = \prod_p \mathbb{Z}_p^\wedge$ is also zero, as the further restriction to $\mathbb{Z}_2^\wedge$ is zero by 3-divisibility, and the restriction to $\prod_{p \neq 2} \mathbb{Z}_p^\wedge$ is zero by 2-divisibility. 

## Related concepts

* [[compactification]]

* [[one-point compactification]]

* [[Stone-Cech compactification]]

* [[end compactification]]

* [[Kaluza-Klein compactification]]

## References

* Wikipedia, _[Bohr compactification](http://en.wikipedia.org/wiki/Bohr_compactification)_

[[!redirects Bohr compactifications]]