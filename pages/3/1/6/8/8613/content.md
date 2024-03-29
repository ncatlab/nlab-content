| | [[type theory]] | [[category theory]] |
|--|--|--|
|  | [[syntax]] | [[semantics]] |
|  |  [[natural deduction]] |  [[universal construction]] | 
|  | **[[function type]]** | **[[internal hom]]** |
| [[type formation]] | $\frac{\vdash\: X \colon Type \;\;\;\;\; \vdash\; A\colon Type}{\vdash \; \left(X \to A\right) \colon Type}$ | <img src=""/> |
| [[term introduction]] | $\frac{x \colon X \;\vdash\; a(x) \colon A}{\vdash (x \mapsto a\left(x\right)) \colon \left(X \to A\right) }$ | <img src=""/> |
| [[term elimination]] | $\frac{\vdash\; f \colon \left(X \to A\right)\;\;\;\; \vdash \; x \colon X}{\;\;\;\vdash\; f(x) \colon A}$ |  <img src=""/> |
| [[computation rule]] | $(y \mapsto a(y))(x) = a(x)$ |  <img src=""/> | 
