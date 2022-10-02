# Contents
* table of contents
{: toc}

## Idea

A symbol in [[mathematics]] and [[computer science]] to indicate that a particular variable is being assigned a value or that a particular symbol is being defined.  

## In type theory

The assignment operator $\coloneqq$ is defined in type theory by the following rules:

$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A\; \mathrm{type}}$$

$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv a:A}$$

This is commonly used to define types and terms in type theory, and in particular abbreviations in type theory. 

For example, suppose one wants to define a type $B$ to be $A$. Then given any derivation 
$$\frac{\mathcal{D}}{\Gamma \vdash A \; \mathrm{type}}$$
one could extend the derivation tree with 
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash B \coloneqq A \; \mathrm{type}}$$

From the rules of the assignment operator it follows that $B$ is a type and $B$ is definitionally equal to $A$. 

## See also

* [[definitional equality]]

## References

The assignment operator is defined (not by name) in Remark 2.2.1 in:

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)