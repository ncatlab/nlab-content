

#Contents#
* automatic table of contents goes here
{:toc}

## Statement

**Pontryagin duality** is the statement that there is an [[contravariant functor|contravariant]] [[adjoint equivalence|adjoint]] self-[[equivalence of categories|equivalence]] on the [[category]] of [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] [[topological space|topological]] [[abelian group]]s induced by homming into the circle group $S^1$. That is to say, the [[functor]] $hom(-, S^1): LocCompAb^{op} \to Set$ lifts to a functor 

$$hom(-, S^1): LocCompAb^{op} \to LocCompAb$$ 

with [[left adjoint]]

$$hom(-, S^1)^{op}: LocCompAb \to LocCompAb^{op}$$ 

for which the unit 

$$\eta_G: G \to hom(hom(G, S^1), S^1): a \mapsto (f \mapsto f(a))$$ 

and the counit, i.e., the same arrow read in reverse in the [[opposite category]], are [[isomorphism]]s. 

This contravariant self-equivalence restricts to an equivalence 

$$hom(-, S^1): CompAb^{op} \to Ab$$ 

where the [[codomain]], the category of abelian groups, embeds as discrete abelian groups in $LocCompAb$; it also restricts to an equivalence 

$$hom(-, S^1): Ab^{op} \to CompAb$$

The topological group $hom(G,S^1)$ is called the **character group** of $A$, and is usually denoted $\hat{G}$. 

## Applications

Pontryagin duality underlies the abstract framework of [[Fourier analysis]] on locally compact Hausdorff abelian groups $G$: [[Fourier duality]] on $G$ stipulates a [[Hilbert space]] isomorphism 

$$\mathcal{F}_G: L^2(G, d\mu) \to L^2(\hat{G}, d\hat{\mu})$$ 

where $d\mu$ is a suitable choice of [[Haar measure]] on $G$, and $d\hat{\mu}$ is a suitable choice of Haar measure on the dual group. Fourier duality is compatible with Pontryagin duality in the sense that $\mathcal{F}_{\hat{G}}$ is the inverse of $\mathcal{F}_G$. 


[[!redirects Pontrjagin duality]]