An **isofibration** is a [[functor]] $p:E\to B$ such that for any [[object]] $e\in E$ and any [[isomorphism]] $\phi:p(e) \cong b$, there exists an isomorphism $\psi:e \cong e'$ such that $p(\psi)=\phi$.  

$$
  \array{
    e &\stackrel{\exists \psi \in p^{-1}(\phi)}{\to} & \exists e'&&& E 
    \\
     &&&&&  \downarrow^p
    \\
    p(e) &\stackrel{\phi}{\to} & b &&& B
  }
  \,.
$$

If $p$ is a [[forgetful functor]], then being an isofibration says that whatever stuff $p$ forgets can be "transported along isomorphisms."

Isofibrations have a number of good properties.  For example, any strict [[pullback]] of an isofibration is also a [[2-categorical limit|bicategorical pullback]].  Any [[Grothendieck fibration]] or opfibration is an isofibration, but not conversely.

The isofibrations are the _fibrations_ in the [[folk model structure]] on [[Cat]].  More generally, the fibrations in folk model structures on various types of higher categories are usually some generalization of isofibrations.  For example, the fibrations in the Lack model structure on 2-Cat have "equivalence lifting" and "local isomorphism lifting," and the fibrations in the Joyal model structure for [[quasi-category|quasicategories]] have "equivalence lifting" at all levels.

