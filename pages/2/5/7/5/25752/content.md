
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


\tableofcontents

\section{Definition}

\begin{definition}\label{PointedRModule}
Let $R$ be a ([[commutative ring|commutative]]) [[ring]]. Then a **pointed $R$-module** is an $R$-[[module]] $M$ equipped with the further choice of an [[element]] $1 \in M$. 
A [[homomorphism]] of pointed modules is a homomorphism of the [[underlying]] modules which preserves the choice of the extra points.
\end{definition}

If $R$ is a [[field]], then pointed $R$-modules are also called **pointed $R$-vector spaces**. 

If $R$ is the [[integers]] then pointed $R$-modules are also called **[[pointed abelian groups]]**.


\begin{remark}
Equivalently, a pointed $R$-module (Def. \ref{PointedRModule}) is an $R$-[[module]] $M$ equipped with an $R$-[[linear map]] $R \to M$ (which is fixed by its [[image]] of $1 \in R$). Since $R$ is the [[tensor unit]] for the [[tensor product of modules]] in the [[monoidal category]] [[Mod|$R \mathrm{Mod}$]] of $R$-modules and $R$-linear maps, this means that pointed $R$-modules are equivalently [[pointed object in a monoidal category|pointed objects in the monoidal-categorical sense]] (in addition to their [[underlying]] [[sets]] being [[pointed set|pointed objects in the set-theoretic sense]]). Accordingly, the category of pointed modules is equivalently the [[coslice category]] $R Mod^{R/}$ of [[Mod|$R \mathrm{Mod}$]] under (the [[underlying]] $R$-module of) $R$.
\end{remark}

\section{Related concepts}

* [[module]]

* [[pointed abelian group]]

* [[pointed object in a monoidal category]]

* [[functorial aspects of the GNS representation]]




[[!redirects pointed module]]
[[!redirects pointed modules]]

[[!redirects category of pointed modules]]

[[!redirects pointed vector space]]
[[!redirects pointed vector spaces]]

[[!redirects category of pointed vector spaces]]