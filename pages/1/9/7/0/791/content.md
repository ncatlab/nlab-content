A homotopy 2-type is the class of spaces whose homotopy groups vanish above dimension 2. 

Such homotopy types are classified up to weak homotopy type by [[crossed module]]s of groupoids. 

These are the 2-truncated versions  of [[crossed complex]]es. So such a $C$  consists of a morphism   

$$\delta: C_2 \to C_1$$  

of [[groupoid]]s with object set $C_0$ such that $C_2$ is totally disconnected, i.e. is a family of groups $C_2(x), x \in C_0$. Further the groupoid $C_1$ operates on this family of groups so that (using right operations) if $a: x \to y$ in $C_1$ and $u \in C_2(x)$ then $u^a \in C(y)$; and the usual rules for an operation are satisfied, namely $(uv)^a=u^av^a$, $u^1=u$, $(u^a)^b=u^{ab}$ when these are defined. Further the two basic crossed module rules hold:

CM1) $\delta(u^a)= a^{-1} (\delta u) a $;

CM2) $ v ^{-1} uv = u ^{\delta v} $; 

for all $a \in C_1, u,v \in C_2$ when the rules make sense. 

Such a crossed module may be extended to a crossed complex $sk^2 C$ by adding trivial elements in dimensions higher than 2. Hence there is a simplicial [[nerve]] $N^\Delta C$ which in dimension $n$ is 

$$ Crs(\Pi (\Delta^n_*), sk^2 C).  $$ 

The geometric realisation of this is the [[classifying space]] $BC$. Its first and second homotopy groups at $x \in C_0$ are the cokernel and kernel of $\delta: C_2(x) \to C_1(x,x)$. It components are those of the groupoid $C_1$.  All other homotopy groups  are trivial. 

If $X$ is a CW-complex then there is a bijection of homotopy classes

$$ [X,BC] \cong [\Pi X_*, sk^2 C],$$

and hence there is a map $X \to B(cotr^2 \Pi X_*)$ inducing isomorphisms of homotopy groups in dimensions 1 and 2. 

Here the cotruncation $cotr^n D$ of a general crossed complex $D$ agree with $D$ up to dimension $(n-1)$, is $Cok \delta_{n+1}$ in dimension $n$, and is trivial in higher dimensions. 

It is in this sense that crossed modules of groupoids classify weak homotopy 2-types. 

The category $Crs^2$ of such crossed modules of groupoids is equivalent to that of strict [[2-groupoid]]s. Further, $Crs^2$ is [[monoidal closed]]:

$$Crs^2(C \otimes D, E) \cong Crs^2(C, CRS^2(D,E))$$

 and with a unit interval object $I$ so that (left) homotopies are determined as morphisms $Crs^2(I \otimes D,E)$ or as elements of $CRS^2(D,E)_1$.  



##Homotopy 2-types via simplicial group(oid)s##
As a crossed module give rise to an internal groupoid in the category of groups (or groupoids), we can take the nerve of that structure and get a simplicial group (or [[simplicially enriched category|simplicially enriched groupoid]]). From a simplicial group(oid), $G$, one can define a simplicial set called the classifying space $\overline{W}G$ of the simplicial group, $G$, for which construction see [[simplicial group]]. We thus can start with a crossed module $C$ form a simplicial group and then take $\overline{W}$ of that to get another model of $BC$.
