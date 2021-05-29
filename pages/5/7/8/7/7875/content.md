
# Contents
* tabe of contents
{: toc}

## Idea

In the context of [[arithmetic]], _carrying_ is part of the operation of representing [[addition]] of [[natural numbers]] by digits with respect to a base.

## In terms of commutative algebra 

Given the [[rig]] of natural numbers $\mathbb{N}$, there exists a [[free object|free]] commutative $\mathbb{N}$-algebra $\mathbb{N}[b]$ on one generator $b$ called the base. Since multiplication in a [[commutative algebra]] is [[power-associative]], there exists a right $\mathbb{N}$-[[action]] on $\mathbb{N}[b]$ $(-)^{(-)}:\mathbb{N}[b]\times\mathbb{N}\to\mathbb{N}[b]$ called the power, and every element in $\mathbb{N}[b]$ could be written as a [[polynomial]]

$$p = \sum_{n=0}^{k} a(n) b^n$$

When the algebra is quotiented out by the relation $b \sim 10$, the resulting [[quotient object|quotient algebra]] is [[isomorphic]] to the original rig of natural numbers $\mathbb{N}$. This means that every natural number could be expressed a polynomial with base ten, 

$$p = \sum_{n=0}^{k} a(n) 10^n$$

There is a [[canonical]] such polynomial, one where all natural numbers in the [[sequence]] $a(n) \lt 10$ in the polynomial. Carrying arises from adding two canonical polynomials, when the sum $a_1(n) + a_2(n) \geq 10$ and the polynomial is no longer canonical; in order to make the polynomial canonical again, one would have to take the sum $a_1(n) + a_2(n)$ [[modulo]] 10 and add 1 to the sum $a_1(n+1) + a_2(n+1)$ in the next power of ten. This means there ought to be another representation of the digits in terms of integers modulo 10. 

## In terms of cohomology

Write $\mathbb{Z}/10$ for the [[abelian group]] of [[addition]] of [[integers]] modulo 10. In the following we identify the elements as

$$
  \mathbb{Z}/{10} = \{0,1,2, \cdots, 9\}
  \,,
$$

as usual.

Being an abelian group, every [[delooping]] [[n-groupoid]] $\mathbf{B}^n (\mathbb{Z}/{10})$ exists. 

Carrying is a 2-[[cocycle]] in the [[group cohomology]], hence a morphism of [[infinity-groupoids]]

$$
  c : \mathbf{B} (\mathbb{Z}/{10}) \to \mathbf{B}^2 (\mathbb{Z}/{10})
  \,.
$$

It sends

$$
  \array{
    && \bullet
    \\
    & {}^{\mathllap{a}}\nearrow 
     &\Downarrow^=& 
    \searrow^{\mathrlap{b}}
    \\
    \bullet &&\stackrel{a+b mod 10}{\to}&&
  }
  \;\;\;
  \mapsto
  \;\;\;
  \array{
    && \bullet
    \\
    & {}^{\mathllap{id}}\nearrow 
     &\Downarrow^{c(a,b)}& 
    \searrow^{\mathrlap{id}}
    \\
    \bullet &&\stackrel{id}{\to}&& \bullet
  }
  \,,
$$

where 

$$
  c(a,b) = 
  \left\{
    \array{
       1 & a + b \geq 10
       \\
       0 & a + b \lt 10
       \,.
    }
  \right.
$$

The [[central extension]] classified by this 2-cocycle, hence the [[homotopy fiber]] of this morphism is $\mathbb{Z}/{100}$

$$
  \array{
    \mathbf{B} (\mathbb{Z}/{100}) &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B} (\mathbb{Z}/{10}) &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^2 (\mathbb{Z}/{10})
  }
  \,.
$$

That now carries a 2-cocycle

$$
  \mathbf{B} (\mathbb{Z}/{100}) \to \mathbf{B}^2 (\mathbb{Z}/{10})
  \,,
$$

and so on. 

$$
  \array{
    \vdots
    \\
    \downarrow 
    \\
    \mathbf{B} (\mathbb{Z}/{1000})
    &\stackrel{c}{\to}&
    \mathbf{B}^2 (\mathbb{Z}/{10})
    \\
    \downarrow 
    \\
    \mathbf{B} (\mathbb{Z}/{100})
    &\stackrel{c}{\to}&
    \mathbf{B}^2 (\mathbb{Z}/{10})
    \\
    \downarrow 
    \\
    \mathbf{B} (\mathbb{Z}/{10})
    &\stackrel{c}{\to}&
    \mathbf{B}^2 (\mathbb{Z}/{10})
  }
$$

This tower can be viewed as a sort of "[[Postnikov tower]]" of $\mathbb{Z}$ (although it is of course not a Postnikov tower in the usual sense).  Note that it is not "convergent": the limit of the tower is the ring of $10$-[[p-adic numbers|adic integers]] $\mathbb{Z}_{10}$.  This makes perfect sense in terms of carrying: the $10$-adic integers can be identified with "decimal numbers" that can be "infinite to the left", with addition and multiplication defined using the usual carrying rules "on off to infinity".


## References

* [[Dan Isaksen]], _A cohomological viewpoint on elementary school arithmetic_, The American Mathematical Monthly, Vol. 109, No. 9. (Nov., 2002), pp. 796-805. ([jstor](http://links.jstor.org/sici?sici=0002-9890%28200211%29109%3A9%3C796%3AACVOES%3E2.0.CO%3B2-2))
