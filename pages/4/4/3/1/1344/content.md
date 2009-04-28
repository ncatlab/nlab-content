#Definition#

The **category of simplices** of a [[simplicial set]] $X_\bullet : \Delta^{op} \to Set$ is the [[category of elements]] of the [[presheaf]] $X_\bullet$. 

#Remarks#

We spell this out in detail:

The category of simplices is the [[comma category]] $(Y,X_\bullet)$, where $Y$ is the [[Yoneda embedding]], hence the functor $Y : [n] \to \Delta^n$ 

The [[object]]s of the category of simplices are therefore morphisms $c : \Delta^n \to X_\bullet$ from the standard simplicial [[simplex]] $\Delta$ to $X_\bullet$, hence are $n$-cells of $X_\bullet$, while morphisms $c \to c'$ are morphisms $f : \Delta^n \to \Delta^{n'}$ in the [[simplex category]] $\Delta$ such that

$$
  \array{ 
    \Delta^n &&\stackrel{f}{\to}&& \Delta^{n'}
    \\
    & {}_{c}\searrow && \swarrow_{c'}  
    \\
    && X_\bullet
  }
  \,.
$$