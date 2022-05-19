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

1. for every real number $\epsilon \in \mathbb{R}_+$ and $a \in S$, $a \sim_\epsilon a$

2. for every real number $\epsilon \in \mathbb{R}_+$, there exists an real number $\eta \in \mathbb{R}_+$ such that for every $a \in S$, $b \in S$, and $c \in S$, if $a \sim_\eta b$ and $b \sim_\eta c$, then $a \sim_\epsilon c$. 

3. For every real number $\epsilon \in \mathbb{R}_+$, there exists a real number $\eta \in \mathbb{R}_+$ such that for every $a \in S$ and $b \in S$, if $a \sim_\eta b$, then $b \sim_\epsilon a$. 

4. There exists a real number $\epsilon \in \mathbb{R}_+$ and elements $a \in S$ and $b \in S$ such that $a \sim_\epsilon b$. 

5. If there are real numbers $\epsilon \in \mathbb{R}_+$ and $\eta \in \mathbb{R}_+$, then there is a real number $\delta \in \mathbb{R}_+$ such that for every element $a \in S$ and $b \in S$, if $a \sim_\delta b$, then $a \sim_\epsilon b$ and $a \sim_\eta b$. 

6. If there is an real number $\epsilon \in \mathbb{R}_+$, then there is an real number $\eta \in \mathbb{R}_+$ such that for all $a \in S$ and $b \in S$, if $a \sim_\epsilon b$, then $a \sim_\eta b$. 

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