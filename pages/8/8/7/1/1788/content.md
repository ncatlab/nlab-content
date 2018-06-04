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
