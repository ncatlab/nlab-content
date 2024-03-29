Type preservation is an important property of a type system and operational semantics. Informally, an operational semantics $t \longrightarrow t\prime$ preserves types if the evaluation of $t$ does not change its type.

More formally, if $\Gamma \vdash t : A$ and $t \longrightarrow t\prime$, then $\Gamma \vdash t\prime : A$.