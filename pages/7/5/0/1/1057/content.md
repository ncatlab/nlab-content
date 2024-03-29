
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##  Definition 

A **strong monomorphism** in a [[category]] $C$ is a [[monomorphism]] which is right [[orthogonality|orthogonal]] to any [[epimorphism]].  The dual notion is, of course, [[strong epimorphism]].


## Remarks 

* If $C$ has [[coequalizers]], then any morphism which is right orthogonal to epimorphisms must automatically be a monomorphism.

* If $C$ has [[kernel pairs]] and [[coequalizers]] of kernel pairs, then any morphism which is right orthogonal to epimorphisms must automatically be a monomorphism.

* Every [[regular monomorphism]] is strong. The converse is true if $C$ is [[regular category| co-regular]].

* Every strong monomorphism is [[extremal monomorphism|extremal]]; the converse is true if $C$ has [[pushouts]].



## Examples 

* A nice example of strong monomorphisms in a category are the subspace inclusions in the category of [[diffeological spaces]].  In this setting, any subset $Y$ of a diffeological space $X$ is again a diffeological space.  If smooth, the inclusion $\iota:Y \rightarrow X$ is always a monomorphism, but it is a strong monomorphism if and only if $Y$ has "enough" plots, that is if $\varphi: U\rightarrow Y$ is a plot if and only if the composite $\iota\varphi: U\rightarrow X$ is a plot.

* Let $C$ be the category whose objects are the integers $\mathbf{Z}$, and whose morphisms are generated from arrows
$$ s_i, t_i : i \to i+1 $$ 
subject to the relations
$$ s\circ s = s\circ t = t\circ s = t\circ t.$$
Then the only epimorphisms and monomorphisms in $C$ are the identities, thus every map is right orthogonal to all epimorphisms but only the identities are strong monomorphisms.

## Properties

+-- {: .num_prop #PushoutOfStrongMonomorphismInQuasitopos}
###### Proposition
**pushout of [[strong monomorphism]] in [[quasitopos]]**

Suppose that $(\mathrm{T},\mathcal{C})$ is either

* ([[monomorphism]],[[topos]]), or
* ([[strong monomorphism]],[[quasitopos]])

Suppose that 
$$\array{
O_{0,1} & \to & O_{1,1} \\
\downarrow m &&\downarrow h  \\
O_{0,0} & \to & O_{1,0}
}$$
is a [[commutative diagram]] in $\mathcal{C}$ such that 

* * $m$ is $\mathrm{T}$ in $\mathcal{C}$
* * the diagram is a pushout in $\mathcal{C}$


Then 

* * $h$ is $\mathrm{T}$ in $\mathcal{C}$
* * the diagram is a pullback in $\mathcal{C}$

=--

See at _[[quasitopos]]_ [this lemma](quasitopos#PushoutOfStrongMonos). Note that the result for quasitoposes immediately implies the result for toposes, since all monomorphisms $i: A \to B$ in a topos are [[regular monomorphism|regular]] ($i$ being the equalizer of the arrows $\chi_i, t \circ !: B \to \Omega$ in 

$$\array{
 & & 1 \\ 
 & \mathllap{!} \nearrow & \downarrow \mathrlap{t} \\ 
B & \underset{\chi_i}{\to} & \Omega
}$$ 

where $\chi_i$ is the classifying map of $i$) and therefore strong. 





[[!redirects strong monomorphisms]]