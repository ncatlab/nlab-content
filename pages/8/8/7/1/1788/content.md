
| $\phantom{A}$[[nLab:geometry]]$\phantom{A}$  | $\phantom{A}$[[nLab:category]]$\phantom{A}$ | $\phantom{A}$[[nLab:dual category]]$\phantom{A}$ |  $\phantom{A}$[[nLab:algebra]]$\phantom{A}$ |
|--------------------|--|------------------|---|
| $\phantom{A}$[[nLab:topology]]$\phantom{A}$ | $\phantom{A}$$\phantom{NC}TopSpaces_{H,cpt}$$\phantom{A}$ | $\phantom{A}$$\overset{\text{<a href="https://ncatlab.org/nlab/show/Gelfand+duality">Gelfand duality</a>}}{\simeq} TopAlg^{op}_{C^\ast, comm}$$\phantom{A}$ | $\phantom{A}$[[nLab:commutative C*-algebra|comm. C*-algebra]]$\phantom{A}$ |
| $\phantom{A}$[[nLab:noncommutative topology|noncomm. topology]]$\phantom{A}$ | $\phantom{A}$$NCTopSpaces_{H,cpt}$$\phantom{A}$ | $\phantom{A}$$\overset{\phantom{\text{Gelfand duality}}}{\coloneqq} TopAlg^{op}_{C^\ast}$$\phantom{A}$ | $\phantom{A}$general [[nLab:C*-algebra]]$\phantom{A}$ | 
| $\phantom{A}$[[nLab:algebraic geometry]]$\phantom{A}$ |  $\phantom{A}$$\phantom{NC}Schemes_{Aff}$$\phantom{A}$ | $\phantom{A}$$\overset{\text{<a href="https://ncatlab.org/nlab/show/affine+scheme#AffineSchemesFullSubcategoryOfOppositeOfRings">almost by def.</a>}}{\hookrightarrow} \phantom{Top}Alg^{op}_{fin} $$\phantom{A}$ |$\phantom{A}$[[nLab:finitely generated algebra|fin. gen.]]$\phantom{A}$ <br/>  $\phantom{A}$[[nLab:commutative algebra]]$\phantom{A}$ |
| $\phantom{A}$[[nLab:noncommutative algebraic geometry|noncomm. algebraic]]$\phantom{A}$ <br/> $\phantom{A}$[[nLab:noncommutative algebraic geometry|geometry]]$\phantom{A}$ |  $\phantom{A}$$NCSchemes_{Aff}$$\phantom{A}$ | $\phantom{A}$$\overset{\phantom{\text{Gelfand duality}}}{\coloneqq} \phantom{Top}Alg^{op}_{fin, red}$$\phantom{A}$ | $\phantom{A}$[[nLab:finitely generated algebra|fin. gen.]] <br/>$\phantom{A}$[[nLab:associative algebra]]$\phantom{A}$$\phantom{A}$|
| $\phantom{A}$[[nLab:differential geometry]]$\phantom{A}$ |  $\phantom{A}$$SmoothManifolds$$\phantom{A}$ | $\phantom{A}$$\overset{\text{<a href="https://ncatlab.org/nlab/show/embedding+of+smooth+manifolds+into+formal+duals+of+R-algebras">Milnor's exercise</a>}}{\hookrightarrow} \phantom{Top}Alg^{op}_{comm}$$\phantom{A}$ | $\phantom{A}$[[nLab:commutative algebra]]$\phantom{A}$ |
| $\phantom{A}$[[nLab:supergeometry]]$\phantom{A}$ | $\phantom{A}$$\array{SuperSpaces_{Cart} \\ \\ \mathbb{R}^{n\vert q}}$$\phantom{A}$ | $\phantom{A}$$\array{ \overset{\phantom{\text{Milnor's exercise}}}{\hookrightarrow} & Alg^{op}_{\mathbb{Z}_2 \phantom{AAAA}}  \\ \mapsto & C^\infty(\mathbb{R}^n) \otimes \wedge^\bullet \mathbb{R}^q }$$\phantom{A}$ | $\phantom{A}$[[nLab:supercommutative superalgebra|supercommutative]]$\phantom{A}$<br/>$\phantom{A}$[[nLab:superalgebra]]$\phantom{A}$  |
| $\phantom{A}$[[nLab:formal moduli problem|formal]] [[nLab:higher differential geometry|higher]]$\phantom{A}$ <br/> $\phantom{A}$[[nLab:supergeometry]]$\phantom{A}$ <br/> $\phantom{A}$([[nLab:super L-∞ algebra|super Lie theory]])$\phantom{A}$ | $\phantom{A}\array{ Super L_\infty Alg_{fin} \\ \mathfrak{g} }\phantom{A}$ | $\phantom{A}\array{ \overset{ \phantom{A}\text{<a href="https://ncatlab.org/nlab/show/L-infinity-algebra#ReformulationInTermsOfSemifreeDGAlgebra">Lada-Markl</a>}\phantom{A}   }{\hookrightarrow} & sdgcAlg^{op} \\ \mapsto & CE(\mathfrak{g}) }\phantom{A}$ | $\phantom{A}$[[nLab:differential graded-commutative superalgebra|differential graded-commutative]]$\phantom{A}$ <br/> $\phantom{A}$[[nLab:superalgebra]] <br/> $\phantom{A}$ ("[[nLab:D'Auria-Fre formulation of supergravity|FDAs]]")  |


[[sets]]

[[SimplicialSetsIdea.jpg:file]]

<img src="https://ncatlab.org/nlab/files/SimplicialSetsIdea.jpg" width="600">

| $\phantom{AA}$[[nLab:left homotopy]]$\phantom{AA}$ | $\phantom{AA}$[[nLab:right homotopy]]$\phantom{AA}$ |
|------------------------|-------------------------|
| $ \phantom{AAAA} \array{ X \\ {}^{\mathllap{(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{f}} \\ X \times I &\stackrel{\eta}{\longrightarrow}& Y \\ {}^{\mathllap{(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{g}} \\ X } \phantom{AA}$ | $ \phantom{AA}  \array{ && X \\ & {}^{\mathllap{f}}\nearrow & \Big\uparrow{}^{\mathrlap{ \Maps(\delta_0,X) }} \\ X &\overset{\widetilde \eta}{\rightarrow}& Maps(I,X) \\ &{}_{\mathllap{g}}\searrow& \Big\downarrow{}^{ \mathrlap{Maps( \delta_1, X ) } } \\ && X } \phantom{AAAA}$ | 


$$
  \array{
    && X
    \\
    & {}^{\mathllap{f}}\nearrow & \Big\uparrow{}^{\mathrlap{ \Maps(\delta_0,X) }}
    \\
    X &\overset{\widetilde \eta}{\rightarrow}& Maps(I,X)
    \\
    &{}_{\mathllap{g}}\searrow& \Big\downarrow{}^{ \mathrlap{Maps( \delta_1, X ) } }
    \\
    && X
  }
$$


<img src="https://ncatlab.org/nlab/files/GeometryOfGeneralizedSpaces.jpg" width="700"/>


| $\phantom{A}$[[nLab:geometry]]$\phantom{A}$  | $\phantom{A}$[[nLab:category]]$\phantom{A}$ | $\phantom{A}$[[nLab:dual category]]$\phantom{A}$ |  $\phantom{A}$[[nLab:algebra]]$\phantom{A}$ |
|--------------------|--|------------------|---|
| $\phantom{A}$[[nLab:topology]]$\phantom{A}$ | $\phantom{A}$$\phantom{NC}TopSpaces_{H,cpt}$$\phantom{A}$ | $\phantom{A}$$\overset{\text{<a href="https://ncatlab.org/nlab/show/Gelfand+duality">Gelfand duality</a>}}{\simeq} TopAlg^{op}_{C^\ast, comm}$$\phantom{A}$ | $\phantom{A}$[[nLab:commutative C*-algebra|comm. C*-algebra]]$\phantom{A}$ |
| $\phantom{A}$[[nLab:noncommutative topology|noncomm. topology]]$\phantom{A}$ | $\phantom{A}$$NCTopSpaces_{H,cpt}$$\phantom{A}$ | $\phantom{A}$$\overset{\phantom{\text{Gelfand duality}}}{\coloneqq} TopAlg^{op}_{C^\ast}$$\phantom{A}$ | $\phantom{A}$general [[nLab:C*-algebra]]$\phantom{A}$ | 
| $\phantom{A}$[[nLab:algebraic geometry]]$\phantom{A}$ |  $\phantom{A}$$\phantom{NC}Schemes_{Aff}$$\phantom{A}$ | $\phantom{A}$$\overset{\phantom{\text{Gelfand duality}}}{\simeq} \phantom{Top}Alg^{op}_{fin, red, comm} $$\phantom{A}$ |$\phantom{A}$[[nLab:finitely generated algebra|fin. gen.]] [[nLab:reduced ring|reduced]]$\phantom{A}$ <br/>  $\phantom{A}$[[nLab:commutative algebra]]$\phantom{A}$ |
| $\phantom{A}$[[nLab:noncommutative algebraic geometry|noncomm. algebraic geometry]]$\phantom{A}$ |  $\phantom{A}$$NCSchemes_{Aff}$$\phantom{A}$ | $\phantom{A}$$\overset{\phantom{\text{Gelfand duality}}}{\coloneqq} \phantom{Top}Alg^{op}_{fin, red}$$\phantom{A}$ | $\phantom{A}$[[nLab:finitely generated algebra|fin. gen.]] [[nLab:reduced ring|reduced]] <br/>$\phantom{A}$[[nLab:associative algebra]]$\phantom{A}$$\phantom{A}$|
| $\phantom{A}$[[nLab:differential geometry]]$\phantom{A}$ |  $\phantom{A}$$SmoothManifolds$$\phantom{A}$ | $\phantom{A}$$\overset{\text{<a href="https://ncatlab.org/nlab/show/embedding+of+smooth+manifolds+into+formal+duals+of+R-algebras">Milnor's exercise</a>}}{\hookrightarrow} \phantom{Top}Alg^{op}_{comm}$$\phantom{A}$ | $\phantom{A}$[[nLab:commutative algebra]]$\phantom{A}$ |
| $\phantom{A}$[[nLab:supergeometry]]$\phantom{A}$ | $\phantom{A}$$\array{SuperSpaces_{Cart} \\ \\ \mathbb{R}^{n\vert q}}$$\phantom{A}$ | $\phantom{A}$$\array{ \overset{\phantom{\text{Milnor's exercise}}}{\hookrightarrow} & Alg^{op}_{\mathbb{Z}_2 \phantom{AAAA}}  \\ & C^\infty(\mathbb{R}^n) \otimes \wedge^\bullet \mathbb{R}^q }$$\phantom{A}$ | $\phantom{A}$[[nLab:supercommutative superalgebra|supercommutative]]$\phantom{A}$<br/>$\phantom{A}$[[nLab:superalgebra]]$\phantom{A}$  |