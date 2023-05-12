
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

\section{Idea}

In [[modal type theory]], *left division* refers to an operation on [[contexts]] used to define the [[syntax|syntactical]] [[inference rules]] for [[modalities]], and is an alternative to [[split contexts]] or [[context locks]] for that purpose. Left division is a [[left adjoint]] to post-composition of modalities. 


\section{Comparison with split context and context locks}

The [[introduction rules]] for a [[modal operator]] $\mu L$ is syntactically given by 

| [[split context]] | [[context lock]] | [[left division]] |
|---|---|---|
| $\frac{\Gamma \vdash a \colon A}{\Gamma \vert \Delta \vdash a^L \colon \mu L(A)}$ | $\frac{\Gamma, \mathrm{lock}_\mu \vdash a \colon A}{\Gamma \vdash a^L \colon \mu L(A)}$ | $\frac{\Gamma/\mu \vdash a \colon A}{\Gamma \vdash a^L \colon \mu L(A)}$ |

\section{Related concepts}

* [[modality]]

* [[modal type theory]]


* [[split context]]
* [[context lock]]

\section{References}

* [[Andreas Nuyts]], *Contributions to Multimode and Presheaf Type Theory* (2020) &lbrack;[pdf](https://lirias.kuleuven.be/retrieve/581985)&rbrack;

* [[Mike Shulman]], *Semantics of multimodal adjoint type theory* ([arXiv:2303.02572](https://arxiv.org/abs/2303.02572)) 

[[!redirects left division]]

