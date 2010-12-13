

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## In a monoidal category

### Definition

+-- {: .un_defn}
###### Definition

An object $A$ in a [[monoidal category]] $C$ is **dualizable** if it has an [[adjunction|adjoint]] when regarded as a [[morphism]] in the one-object [[delooping]] [[bicategory]] $\mathbf{B}C$ corresponding to $C$.  Its adjoint in $\mathbf{B}C$ is called its **dual** in $C$ and often written as $A^*$.

=--

If $C$ is [[braided monoidal category|braided]] then left and right adjoints in $\mathbf{B}C$ are equivalent; otherwise one speaks of $A$ being **left dualizable** or **right dualizable**.  

+-- {: .un_remark}
###### Remark

nfortunately, conventions on left and right vary and sometimes contradict their use for adjoints.  But if we define right duals to be the same as right adjoints in $\mathbf{B}C$, then a right dual of $A$ is an object $A^*$ equipped with a **unit** (or *coevaluation*)
$$i: I \to A^* \otimes A $$
and **counit** (or *evaluation*)
$$e : A \otimes A^* \to I $$
satisfying the 'triangle identities' familiar from the concept of [[adjunction]].

=--

+-- {: .un_defn}
###### Definition

If every object of $C$ has a left and right dual, then $C$ is called a [[rigid monoidal category]] or an [[autonomous monoidal category]].  If it is additionally symmetric, it is called a [[compact closed category]].  

=--

See [[category with duals]] for more discussion.


### Properties

Dualizable objects support a good abstract notion of [[trace]].

## In a symmetric monoidal $(\infty,n)$-category

+-- {: .un_defn}
###### Definition

An [[object]] in a [[symmetric monoidal (∞,n)-category]] $C$ is called **dualizable** if it is so as an object in the ordinary [[symmetric monoidal category|symmetric monoidal]] [[homotopy category]] $Ho(C)$.

=--

This appears as ([Lurie, def. 2.3.5](#Lurie)).


+-- {: .un_remark}
###### Remark

This means that an object in $C$ is dualizable if there exists unit and counit 1-morphism that satisfy the [[triangle identity]] up to [[homotopy]]. The definition does not demand that this homotopy is [[coherent]] (that it satisfies itself higher order relations up to higher order [[k-morphism]]s).

If the structure morphisms of the adjunction of a dualizable object _have_ themselves all adjoints, then the object is called a [[fully dualizable object]].

=--


+-- {: .un_remark}
###### Remark

As before, we may equivalently state this after [[delooping]] the monoidal structure and passing to the $(\infty,n+1)$-category $\mathbf{B}C$. Then $C$ has duals for objects precisely if $\mathbf{B}C$ has all adjoints.

=--

## References

The notion of duals in a symmetric monoidal $(\infty,n)$-category is due to section 2.3 of

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_


[[!redirects dual object]]
[[!redirects dual objects]]
[[!redirects dualizable object]]
[[!redirects dualizable objects]]
[[!redirects dualisable object]]
[[!redirects dualisable objects]]