#Lie's three theorems#

There is an obvious functor
$$
  diff : LieGroups \to LieAlgebras
$$
which sends every Lie group to its Lie algebra and every homomorphism of Lie groups to the corresponding homomorphism of Lie algebras. 

Lie's three theorems establish the following properties of this functor.

  1. **Lie's first theorem** is today regarded as lacking a good notion of differentiable manifold;

  2. **Lie's second theorem.** 
     If $G$ and $H$ are Lie groups 
     with Lie algebras $g = diff(G)$ and $h = diff(H)$;
      such that $G$ is simply connected;
      and if $f : g \to h$ is a morphism of Lie algebras;
      then there is a unique morphism $F : G \to H$ of Lie groups lifting $g$, i.e. such that $f = diff(F)$.  

  3. **Lie's third theorem.** **$diff$ is surjective on objects**: to every Lie algebra  $g$ there is a Lie group $G$ such that $g = diff(G)$. Moreover, there exists such $G$ which is simply connected.

##Remarks##

###Restriction to simply connected Lie groups.###

Let $LieGroups_{simpl}$ be the [[full subcategory]] of $LieGroups$ on simply connected Lie groups. Then the above implies that restricted to $LieGroups_{simpl}$ the functor $diff$ becomes a [[k-surjectivity|surjective equivalence]] of categories

#Generalization of Lie's theorems to Lie groupoids#

The generalization of these theorems to [[Lie groupoid|Lie groupoids]] is discussed pages 3-5 of 


Crainic and Fernandes, _Integrability of Lie brackets_ ([arXiv](http://arxiv.org/abs/math.DG/0105033v1))




#Generalization of Lie's theorems to stacky Lie groupoids#

The generalization of Lie's theorems from Lie groups to to [[Lie theory for stacky Lie groupoids|stacky Lie groupoids]] is discussed
in Chenchang Zhu, _Lie II theorem for Lie algebroids via stacky Lie groupoids_, ([arXiv](http://arxiv.org/abs/math/0701024)).

# General context#

For the general context see [[Lie theory]].
