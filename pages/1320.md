Given a pair of [[adjoint functors]] $F:C\to D: U$, $F\dashv U$, with unit $\eta:Id_C\to UF$ and counit $\epsilon:FU\to Id_D$ one constructs a [[monad]] $\mathbf{T}=(T,\mu,\eta)$ setting $T=UF:C\to C$, $\mu = U\epsilon F: TT= UFUF\to UF=T$. Consider the [[Eilenberg-Moore category]] $C^{\mathbf{T}}$ of $T$-algebras ($T$-modules) in $C$. Clearly $U(\epsilon_M):TUM=UFUM\to UM$ is a $T$-action. In fact there is a canonical __comparison functor__ $K^{\mathbf{T}}:D\to C^{\mathbf{T}}$ given on objects by $K(M)=(UM,U(\epsilon_M))$.

A [[functor]] $U:D\to C$ is **monadic** if it has a [[left adjoint]] $F:C\to D$ and the comparison functor $K^{\mathbf{T}}: D\to C^{\mathbf{T}}$ is an [[equivalence of categories]].  In other words, up to equivalence, monadic functors are precisely the [[forgetful functor]]s defined on Eienberg-Moore categories for monads. A __category__ $D$ is __monadic__ over a category $C$ if there is a functor $U:D\to C$ which is monadic. 


Various version of the Beck's [[monadicity theorem]] (old-fashioned name of some schools: tripleability theorem) give sufficient, and sometimes necessary, conditions for a given functor to be monadic.

[[!redirects monadic]]
[[!redirects monadic category]]
[[!redirects tripleability theorem]]