
| | [[type theory]] | [[category theory]] |
|--|--|--|
|  | [[syntax]] | [[semantics]] |
|  |  [[natural deduction]] |  [[universal construction]] | 
|  | **[[dependent sum type]]** | **[[dependent sum]]** |
| [[type formation]] | $\frac{\vdash\: A \colon Type \;\;\;\;\; x \colon A \;\vdash\; B(x)\colon Type}{\vdash \; \left(\sum_{x \colon A} B\left(x\right)\right) \colon Type}$ | $\left(A \in \mathcal{C}, \array{ B \\ \downarrow^{\mathrlap{p_1}} \\ A} \; \in \mathcal{C}/A \right) \Rightarrow \left( B \in \mathcal{C}\right)$ |
| [[term introduction]] | $\frac{\vdash\: a \colon A \;\;\;\;\; \vdash\; b \colon B(a)}{\vdash (a,b) \colon \sum_{x \colon A} B\left(x\right) }$ | $\array{ Q &\stackrel{(a,b)}{\to}& B \\ & {}_{\mathllap{a}}\searrow & \\ && A }$ |
| [[term elimination]] | $\frac{\vdash\; t \colon \left(\sum_{x \colon A} B\left(x\right)\right)}{\vdash\; p_1(t) \colon A\;\;\;\;\; \vdash\; p_2(t) \colon B(p_1(t))}$ | $\array{ Q &\stackrel{t}{\to}& B \\ &  & \downarrow^{\mathrlap{p_1}} \\ && A }$ |
| [[computation rule]] | $p_1(a,b) = a\;\;\;\; p_2(a,b) = b$ | $\array{ Q &\stackrel{(a,b)}{\to}& B \\ & {}_{\mathllap{a}}\searrow & \downarrow^{\mathrlap{p_1}} \\ && A }$ | 


