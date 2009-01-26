##Definition##


Given a [[simplicial group]] $G$, the **Moore complex**, $({NG},\partial )$,  of $G$ is the non-Abelian chain complex defined by 
$$
NG_n=\bigcap_{i=1}^{n}Ker\,d_i^n 
$$
with $\partial _n:NG_n\rightarrow NG_{n-1}$ induced from $d_0^n$ by
restriction. 

*Note* there is no assumption that the $NG_n$ are Abelian.

##Conventional remarks##

* There is an alternative 'dual' form of this with $\bigcap_{i=10}^{n-1}Ker\,d_i^n$ and with the boundary /  differential $\partial$ induced by the last face map $d^n_n$. The theories run parallel but the fact there are two valid forms can be confusing for the formulae for various derived structures. 


*  The notation $NG$ is quite widely used in the literature but can get confused with that sometimes used for the nerve functor, so care is needed.


##Discussion##
If an element $g \in G_n$ is in the Moore complex then all but its zeroth face is trivial. In dimension 1, this means that $g$ is a 1-simplex that 'starts' at the identity element of $G_0$. If this $g$ is in the kernel of the boundary map $\partial _1: NG_1\rightarrow NG_{0}$, then $g$ will be a loop at that identity. If it is $\partial x$ for some $x\in NG_2$, then $x$ intuitively provides a homotopy between $g$ and the identity element.  This motivates the following definition:

###Definition###
The **n$^{th}$ homotopy group**, $\pi _n$(G), of $G$ is the $n^{th}$ homology of the Moore complex of $G$, i.e.,  
$$
\pi _n({G})  \cong  H_n( {NG},\partial ),   = \big( \bigcap_{i=0}^n Ker\,d_i^n\big)/d_{0}^{n+1}\big(\bigcap_{i=1}^{n+1} Ker\,d_i^{n+1}\big). 
$$

Note that $\partial NG_{n+1}\triangleleft  NG_n$.