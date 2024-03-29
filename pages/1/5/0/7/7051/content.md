
# Fundamental vector fields and differential forms
* table of contents
{: toc}

## Definitions

Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}\cong T_e G$, $M$ a $C^1$-[[differentiable manifold]] and
$$
\nu\colon G \times M\to M
$$
a left $C^1$-[[differentiable map|differentiable]] [[action]]. For every $m \in M$, denoted by $\nu_m\colon G\to M$ the $C^1$-differentiable map $\nu_m\colon g\mapsto \nu(g,m)$. If $A \in \mathfrak{g}$, the $C^1$-differentiable [[vector field]] on $M$ given by 
$$
(\chi_A)_m = (T_{1_G}\nu_m)(A),\,\,\,\,m\in M,
$$ 
sometimes also denoted $A^\sharp$, is called the __fundamental vector field__ corresponding to $A$. If $s\colon I\to G$ is a curve around $s(0) = 1_G$ representing $A$, then $(\chi_A)_m$ is represented by $t \mapsto s(t) m$. 

Analogously, one can define the fundamental vector field for the right actions.

There is a dual notion as well. Given a right $C^1$-differentiable $G$-manifold $E$, a $C^1$-differentiable $1$-[[differential 1-form|form]] $\omega$ with values in $\mathfrak{g}$,  
$$
\omega \in \Gamma (T^* E\otimes\mathfrak{g})
$$
is called the __fundamental differential form__ corresponding to $A$, if for all $p\in E$, $\omega_p(\chi_A) = A$. 


## Applications

The fundamental vector fields are important in study of differentiable actions and particularly useful in the basic study of [[Ehresmann connections]]. Indeed, the connection form is a fundamental form ("1st Ehresmann condition"), and there is a characterization of those fundamental forms which are connection forms ("2nd Ehresmann condition").


[[!redirects fundamental vector field]]
[[!redirects fundamental vector fields]]

[[!redirects fundamental form]]
[[!redirects fundamental forms]]
[[!redirects fundamental differential form]]
[[!redirects fundamental differential forms]]
[[!redirects fundamental differentiable form]]
