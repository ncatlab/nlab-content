+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A more general concept of [[metric space]]. 

## Definition ##

A __premetric space__ is a [[set]] $S$ with a ternary [[relation]] $(-)\sim_{(-)}(-)\colon S \times \mathbb{R}_+ \times S \to \Omega$, where $\mathbb{R}_+$ represent the positive [[real numbers]] in $\mathbb{R}$ and $\Omega$ is the set of [[truth values]]. 

## Uniform premetrics ##

A premetric $(-)\sim_{(-)}(-)\colon S \times \mathbb{R}_+ \times S \to \Omega$ is **[[uniform space|uniform]]** if

1. for every positive real number $\epsilon \in \mathbb{R}_+$ and $a \in S$, $a \sim_\epsilon a$

2. for every positive real number $\epsilon \in \mathbb{R}_+$, there exists a positive real number $\eta \in \mathbb{R}_+$ such that for every $a \in S$, $b \in S$, and $c \in S$, if $a \sim_\eta b$ and $b \sim_\eta c$, then $a \sim_\epsilon c$. 

3. For every positive real number $\epsilon \in \mathbb{R}_+$, there exists a positive real number $\eta \in \mathbb{R}_+$ such that for every $a \in S$ and $b \in S$, if $a \sim_\eta b$, then $b \sim_\epsilon a$. 

4. There exists a positive real number $\epsilon \in \mathbb{R}_+$ and elements $a \in S$ and $b \in S$ such that $a \sim_\epsilon b$. 

5. If there are positive real numbers $\epsilon \in \mathbb{R}_+$ and $\eta \in \mathbb{R}_+$, then there is a positive real number $\delta \in \mathbb{R}_+$ such that for every element $a \in S$ and $b \in S$, if $a \sim_\delta b$, then $a \sim_\epsilon b$ and $a \sim_\eta b$. 

6. If there is a positive real number $\epsilon \in \mathbb{R}_+$, then there is a positive real number $\eta \in \mathbb{R}_+$ such that for all $a \in S$ and $b \in S$, if $a \sim_\epsilon b$, then $a \sim_\eta b$. 

## Pseudometric spaces ##

A premetric $(-)\sim_{(-)}(-)\colon S \times \mathbb{R}_+ \times S \to \Omega$ is a **[[pseudometric space|pseudometric]]** if there is a function $\rho:S \times S \to \mathbb{R}_{\geq 0}$ such that 

1. For every positive real number $\epsilon \in \mathbb{R}_+$ and $a \in S$, $a \sim_\epsilon a$

2. For every positive real number $\epsilon \in \mathbb{R}_+$, $a \in S$ and $b \in S$, $a \sim_\epsilon b$ if and only if $b \sim_\epsilon a$. 

3. For every positive real number $\delta \in \mathbb{R}_+$, $\eta \in \mathbb{R}_+$ and for every element $a \in S$, $b \in S$, and $c \in S$, $a \sim_\delta b$ and $b \sim_\eta c$ if and only if $a \sim_{\delta + \eta} c$. 

4. For every positive real number $\epsilon \in \mathbb{R}_+$ and every element $a \in S$ and $b \in S$, $a \sim_\epsilon b$ if and only if $\rho(a, b) \lt \epsilon$

## Rational premetric spaces ##

Sometimes the positive [[rational numbers]] $\mathbb{Q}_{+}$ are used instead of $\mathbb{R}_{+}$, such as in the construction of the [[Cauchy real numbers]] and the [[HoTT book real numbers]]. While these are also called "premetrics" in the literature, we shall call these **rational premetrics** and the associated spaces **rational premetric spaces**, to distinguish from the real premetrics above. 

In fact, any Archimedean [[Tarski group]] would work to define premetrics and premetric spacces. 

## See also ##

* [[Cauchy structure]]

* [[metric space]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

[[!redirects premetric]]
[[!redirects premetrics]]
[[!redirects premetric spaces]]

[[!redirects rational premetric]]
[[!redirects rational premetrics]]
[[!redirects rational premetric space]]
[[!redirects rational premetric spaces]]