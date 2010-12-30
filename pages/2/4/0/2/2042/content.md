
# The property (sup)
* table of contents
{: toc}

## Idea

The property (sup) is an optional property of an [[abelian category]], introduced in [[Des catégories abéliennes]], by [[Pierre Gabriel]].


## Definition

An [[abelian category]] has __property (sup)__ if:

+-- {: .un_defn}
###### Definition (sup)

For any ascending chain $\Omega$ of [[subobjects]] of a fixed object $M$, the [[supremum]] of $\Omega$ exists; and, for any subobject $L\hookrightarrow M$, the canonical morphism
$$
sup\{L\cap P | P\in \Omega\}\to (sup \Omega) \cap L
$$
is an [[isomorphism]]. 
=--


## Examples

Gabriel's property (sup) is satisfied by any [[Grothendieck category]] (in some expositions it is listed as a part of the definition), e.g. the category of all [[modules]] over a fixed [[ring]] $R$, and the category of [[sheaf|sheaves]] of [[abelian groups]] on a fixed [[topological space]] $X$. 

According to the Appendix B of the Thomason--Trobaugh contribution to [[Grothendieck Festschrift]], it is not known whether the category $Qcoh_Y$ of [[quasicoherent sheaf|quasicoherent sheaves]] over an arbitrary scheme $Y$ is a Grothendieck category (although this is known for a large class), but it is an elementary fact that it does satisfy Gabriel's property (sup). If an abelian category is [[noetherian category|noetherian]] it clearly satisfies the property (sup).


[[!redirects property sup]]
[[!redirects property (sup)]]
[[!redirects Gabriel's property (sup)]]
