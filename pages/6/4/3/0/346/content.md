#Idea#

A category $C$ is _closed_ if for any pair $a, b$ of object the collection of morphisms from $a$ to $b$ can be regarded as forming itself an object of $C$.

So far, we only discuss [[closed monoidal category|closed monoidal categories]]. However, there is also a definition of **closed category** that does not require the category to already be monoidal.  A monoidal structure $\otimes$, if it exists, can then be universally characterized as a _left_ adjoint to the internal-hom, dual to the above characterization of internal-homs as right adjoints to $\otimes$.  See Eilenberg-Kelly, referenced below.

While this is less fashionable, in some cases it is more obvious what the correct internal-homs are than what the correct tensor product is, so the latter was originally defined as an adjoint to the former.  This is the case for the [[Gray tensor product]] and was probably the case for [[abelian group]]s as well.

* Samuel Eilenberg and Max Kelly, _Closed categories_.  Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).