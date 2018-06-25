# test centering a `<p>` of 2 images

## 2 images in a row

[[adjunction-up-string.png:pic]]  [[adjunction-down-string.png:pic]]

## with ` $\phantom{AAAAAA}$` spacing between them

[[adjunction-up-string.png:pic]]  $\phantom{AAAAAA}$  [[adjunction-down-string.png:pic]]

## with `$\quad\quad\quad \quad$` spacing

[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]

##  quad spaced with `  {: style='margin:auto}` on following line

[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='margin:auto'}

## above wrapped in a `<div>` created with `+-- {: .standout}` 

+-- {: .standout}
[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='margin:auto'}
=--

## above  followed by ` {: style='width:100%'}`

+-- {: .standout}
[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='margin:auto'}
=--
{: style='width:100%}



## above wrapped in a plain`<div>` created with `+-- {: style='width:100%'}`
` 

+-- {: style='width:100%'}
[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='margin:auto}
=--


## above with `text-align:center` on both inner and outer
` 

+-- {: style='width:100%;text-align:center'}
[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='margin:auto;text-align:center'}
=--


## above with `text-align:center` on inner
` 

+-- {: style='width:100%'}
[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='margin:auto;text-align:center'}
=--

## above with `text-align:center` on outer
` 

+-- {: style='width:100%;text-align:center'}
[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='margin:auto;text-align:center'}
=--


## no div wrapping, just `{: style='text-align:center'}` following the list
` 

[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]
{: style='text-align:center'}



## above with an extra span? element at end of list
` 

[[adjunction-up-string.png:pic]]  $\quad\quad\quad \quad$  [[adjunction-down-string.png:pic]]  $foo$
{: style='text-align:center'}



## does ` $\phantom{AAAAAA}$` spacing not work?

[[adjunction-up-string.png:pic]]  $\phantom{AAAAAA}$  [[adjunction-down-string.png:pic]]
{: style='text-align:center'}


## end




