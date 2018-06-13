Test.



$$
  \begin{aligned}
    [\mathcal{D}, \mathcal{V}]( G,\, Ran_p F  )
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    [ G(d) ,\, (Ran_p F)(d), \, ]
    \\
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    \left[ G(d) 
      ,\, 
       \underset{c\in \mathcal{C}}{\int}
       [\mathcal{D}(d,p(c)), F(c)] 
    \right]
    \\
    & \simeq
    \underset{d \in \mathcal{D}}{\int}
    \underset{c\in \mathcal{C}}{\int}
    \left[  
      G(d) \otimes \mathcal{D}(d,p(c)),\, F(c)
    \right]
    \\
    & \simeq
    \underset{c\in \mathcal{C}}{\int}
    \left[  
      \overset{d \in \mathcal{D}}{\int}
      G(d) \otimes \mathcal{D}(d,p(c)),\, F(c)
    \right]
    \\
    & \simeq
    \underset{c \in \mathcal{D}}{\int}
    \left[   
      G(p(c)),\, F(c)
    \right]
    \\
    & \simeq
    [\mathcal{C}, \mathcal{V}]( p^\ast G , F )
  \end{aligned}
$$




#centered table test


## uncentered

|   column header 1 | column header 2 |
|-------------------|-----------------|
|   item            | item            |


## centered

+-- {: .cent}
   |   column header 1 | column header 2 |
   |-------------------|-----------------|
   |   item            | item            |
=--


the above table is wrapped with `+-- {: .cent}`

to get this to actually center I added a CSS rule via with the Firefox extension Stylus

`div.cent table {margin-left: auto; margin-right: auto}`

|   column header 1 | column header 2 |
|-------------------|-----------------|
|   item            | item            |
{: style='margin:auto; color: blue'}
