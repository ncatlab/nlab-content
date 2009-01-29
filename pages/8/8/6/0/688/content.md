
The term _categorical trace_ usually refers to the concept introduced in 

* Nora Ganter and Mikhail Kapranov, _Representation and character theory in 2-categories_ ([arXiv](http://arxiv.org/abs/math.KT/0602510), [blog](http://golem.ph.utexas.edu/string/archives/000757.html)) 


#Definition#

Let $C$ be a [[2-category]] and $F : B \to B$ a 1-[[endomorphism]] on one of its objects. Then the **categorical trace** $Tr(F)$ of $F$ is the collection of 2-morphisms from the identity $Id_B$ on $B$ into $B$
$$
  Tr(F) = Hom_C(Id_B, F)
  \,.
$$


#Examples#

* For $C = KV2Vect$, the 2-category of Kapranov-Voevodsky [[2-vector space]]s, a 1-endomorphism $Vect^n \stackrel{F}{\to} Vect^n$ is an $n \times n$-matrix $(V_{i j})_{i,j}$ of vector spaces $V_{i j} \in Vect$. The categorical trace on that is the direct sum of the diagonal entries, $Tr(F) = \oplu_{i} V_{i i}$. Hence under the decategorification functor from $KV2Vect$ to vectors and matrices with entries in $\mathbb{N}$, this becomes the ordinary trace of matrices.

#Remarks#

* The categorical trace is closely related to the [[span trace]].