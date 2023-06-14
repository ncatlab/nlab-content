
The following "operators" come out much too large in some systems:

$$
  \int f
  \;\;\;\;
  \int X
$$

***

The following over/underlines recently come out tiny when viewed in  

* Chrome, Edge and Opera 

while they still come out as expected in 

* Firefox 

(at least on the systems we tried in discussion [here](https://nforum.ncatlab.org/discussion/12362/twisted-arrow-1category/?Focus=110459#Comment_110459)):

* "`$\overline{ThisShouldRenderWithALooongOverline}$`" 

  renders as: 

  "$\overline{ThisShouldRenderWithALooongOverline}$"

* "`$\overline{ThisShouldRenderWithALooongUnderline}$`" 

  renders as: 

  "$\underline{ThisShouldRenderWithALooongUnderline}$"

Specifically, the rendering with Chrome, Edge and Opera looks (except for horizontal positioning) like that of the `\bar` command:

* "`$\bar{ThisShouldRenderWithATinyOverline}$`" 

  renders as: 

  "$\bar{ThisShouldRenderWithATinyOverline}$"

