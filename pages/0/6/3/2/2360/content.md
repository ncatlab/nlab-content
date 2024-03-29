
> under construction -- needs attention

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

For usual ([[commutative ring|commutative]]) [[rings]], [[Grothendieck]] introduced the notion of a [[prime spectrum of a commutative ring|prime spectrum]]. In order to accommodate not only [[polynomials]] but also [[formal power series]], it is convenient to consider [[completion of a ring|completions]] and [[topological rings]]. Order $n$ [[nilpotent elements]] in an ordinary ring compare to completions as truncations of general power series and geometrically represent certain $n$-th [[infinitesimal space|infinitesimal]] neighborhood. Completions represent certain pro-objects in the category of rings. Adic completion corresponds to have all infinitesimal neighborhoods at once. 
 
A _formal spectrum_ is a generalization of prime spectrum to adic noetherian rings, therefore containing information on all infinitesimal neighborhoods, corresponding to the ideal of completion. 

## Definition

> see for instance ([Strickland 00, def. 4.13](#Strickland00))

Assume $R$ is a  [[commutative ring]] and $I \subset R$ is an ideal, such that its powers make a fundamental system of neighborhoods of zero of a complete Hausdorff topology (we say that $R$ is an separated complete ring in the $I$-[[adic topology]]).

The **formal spectrum** $Spf R$ of $(R,I)$ is the [[inductive limit]] of the [[prime spectrum of a commutative ring|prime spectra]]

$$
  Spf(R) :=colim_n Spec (R/I^n)
  \,.
$$

where the connecting morphisms are the closed nilpotent immersions $Spec(R/I^n)\hookrightarrow Spec(R/I^{n+1})$ of [[affine schemes]] and the [[colimit]] is taken in the [[category]] of [[topologically ringed space|topologically ringed spaces]]. 

Regarding that all affine schemes $X_n := Spec(R/I^n)$ for $n\geq 1$ have the same underlying topological space $\chi$ because nilpotents in $I^n$ do not affect the underlying reduced scheme, so does $Spf R = (\chi,\mathcal{O}_\chi)$. With our assumptions on $I$-[[adic topology]], in fact $\chi$ contains all closed points of $Spec R$ and any open subset of $Spec R$ containing $\chi$ is the whole of $Spec R$.  The structure sheaf $\mathcal{O}_\chi$ has the ring of sections $\mathcal{O}_\chi(U) = lim_n \mathcal{O}_{X_n}(U)$ where the limit is taken in the category of topological rings, and $\mathcal{O}_{X_n}(U)$ have the discrete topology. For example, the ring of global sections is $\mathcal{O}_\chi(\chi) = \hat R$.

A formal spectrum is an example of a [[formal scheme]]. Formal schemes in general form certain subcategory of the category of ind-schemes. 

The formal spectrum of a separated complete topological $I$-adic ring $R$ depends just on the underlying topology on $R$ and not on a choice of the ideal $I$ generating this topology.

## Related concepts

* [[formal disk]]

## References


* standard references are [[EGA]], Hartshorne

* [[Luc Illusie]], _Grothendieck existence theorem in formal geometry_, in [[FGA explained]] (draft: [pdf](http://cdsagenda5.ictp.it//askArchive.php?categ=a0255&id=a0255s3t3&ifd=15021&down=1&type=lecture_notes))

Discussion more from a [[topos theory]] perspective is in section 4.2 of

* {#Strickland00} [[Neil Strickland]], _Formal schemes and formal groups_, [math.AT/0011121](http://arxiv.org/abs/math.AT/0011121)

For the case of [[formal group laws]] see also

* _[[A Survey of Elliptic Cohomology - formal groups and cohomology]]_


[[!redirects formal spectra]]

