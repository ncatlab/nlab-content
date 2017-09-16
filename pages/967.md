A [[locally small category]] $C$ is **total** if its [[Yoneda embedding]] $C\to [C^{op},Set]$ has a [[adjoint functor|left adjoint]].  If $C^{op}$ is total, $C$ is called **cototal**.

The definition above requires some set-theoretic assumption to ensure that the [[functor category]] $[C^{op},Set]$ exists, but it can be rephrased to say that the [[colimit]] of $Id_C:C\to C$ [[weighted limit|weighted]] by $W$ exists, for any $W:C^{op}\to Set$.  This version has an evident generalization to [[enriched category|enriched]] categories.

Total categories satisfy a very satisfactory [[adjoint functor theorem]]: any colimit-preserving functor from a total category to a locally small category has a right adjoint.

Any category which is [[monad|monadic]] over [[Set]] is total, as is any category admitting a [[topological functor|topological functor]] to [[Set]].

# References

* G. M. Kelly, _A survey of totality for enriched and ordinary categories_.
