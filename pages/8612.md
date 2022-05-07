
| | [[type theory]] | [[category theory]] |
|--|--|--|
|  | [[syntax]] | [[semantics]] |
|  |  [[natural deduction]] |  [[universal construction]] | 
|  | **[[dependent product type]]** | **[[dependent product]]** |
| [[type formation]] | $\displaystyle\frac{\vdash\: X \colon Type \;\;\;\;\; x \colon X \;\vdash\; A(x)\colon Type}{\vdash \; \left(\prod_{x \colon X} A\left(x\right)\right) \colon Type}$ | $\left( \array{ A^{\phantom{p_1}} \\ \downarrow^{p_1} \\ X_{\phantom{p_1}}} \in \mathcal{C}\right) \Rightarrow \left( \prod_{x\colon X} A\left(x\right) \in \mathcal{C}\right)$ |
| [[term introduction]] | $\displaystyle\frac{x \colon X \;\vdash\; a\left(x\right) \colon A\left(x\right)}{\vdash (x \mapsto a\left(x\right)) \colon \prod_{x' \colon X} A\left(x'\right) }$ | <img src=""/> |
| [[term elimination]] | $\displaystyle\frac{\vdash\; f \colon \left(\prod_{x \colon X} A\left(x\right)\right)\;\;\;\; \vdash \; t \colon X}{\vdash\; f(t) \colon A(t)}$ |  <img src=""/> |
| [[computation rule]] | $(y \mapsto a(y))(x) = a(x)$ |  <img src=""/> | 


