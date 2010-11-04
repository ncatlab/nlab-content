[[!redirects Lindenbaum_Tarski algebra]]

#Contents#
* table of contents
{:toc}
##The Lindenbaum-Tarski algebra of a normal modal logic##  
   
Associated to any [[normal modal logic]], $\Lambda$ in $\mathcal{L}_\omega(n)$ (and more 
generally) is an algebra $\mathfrak{A}^\Lambda_\omega$,which is a [[algebraic models for modal logics|BAO]] of type $n$, 
i.e. $n$ (modal) operators, $m_i$.  This is called the **Lindenbaum-Tarski algebra** of $\Lambda$, and is a quotient of the [[term algebra]] of  $\mathcal{L}_\omega(n)$, i.e. of the free universal algebra of type $n$ formed by the $\mathcal{L}_\omega(n)$-formulae using the connectives $\vee$, $\wedge$, $\neg$, $\bot$, $\top$, and the $\Diamond_i$.  The Lindenbaum-Tarski algebra is formed from this free algebra by using the congruence $\simeq_\Lambda$, where 

$$\phi \simeq_\Lambda\psi  if and only if  {\vdash}_\Lambda \phi\leftrightarrow \psi.$$  
  
(Recall the usual rules of notation: $\phi \to \psi$ is $\neg\phi\vee\psi$; 
$\phi\leftrightarrow \psi$ is $(\phi\to \psi)\wedge (\psi\to\phi)$; and 
${\vdash}_\Lambda \phi $ means $\phi \in \Lambda$.)  
 
 
 The elements of $\mathfrak{A}^\Lambda_\omega$ are the equivalence 
classes:
  
$$||\phi|| = \{\psi \mid \vdash_\Lambda \phi\leftrightarrow \psi\},$$
 
with the operations 

   *  $||\phi|| + ||\psi|| = ||\phi \vee \psi||$;

   *  $||\phi|| \cdot ||\psi||= ||\phi \wedge \psi||$;

   *  $||\phi||^- = ||\neg\phi||$;
 
   *  $0 =||\bot||$; 

   *  $1 = ||\top||$;

 and

   *  $m_i||\phi|| = ||\Diamond_i\phi|| .$$
 
As we assumed that $\Lambda$ was normal, the normality schemata:

 $(K)$: $\Diamond(\psi \vee \chi)\to \diamond \psi\vee \diamond \chi$; 

 $(N)$, in the form, $\neg \Diamond_i(\bot)$

and monotonicity :
 
if $\psi \to \chi \in \Lambda$ then $\Diamond_i \psi \to \Diamond_i \chi \in \Lambda$. 


 imply
+--
{: . un_lem}
######Lemma######
$m_i$ is a normal operator.
=--
######Proof######
We first note that $\vdash_\Lambda \Diamond(\psi\vee \phi) \leftrightarrow \Diamond_i \psi \vee \Diamond_i \phi$, then the result follows by simply writing down what is required and staring at it for a moment!


##Canonical models##
The Lindenbaum-Tarski algebra for a modal logic, $\Lambda$,   gives rise a canonical Kripke model. This has the set of $\Lambda$-[[maximal consistent]] formulae as its set of states.