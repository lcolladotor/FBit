


This is a test post since I want to improve upon Jeffrey Horner's [strategy for posting R code in Tumblr](http://jeffreyhorner.tumblr.com/post/25943954723/blog-with-r-markdown-and-tumblr-part-ii). The only minor improvement I wanted to try out is hosting the images directly on the web. I mean, right now the images won't show in RSS readers. I'm not doing anything new at all, just using the imgur_upload function in [knitr](http://yihui.name/knitr/).

This is part of my plan to write paper posts. I already created the GitHub repo [FBit](https://github.com/lcolladotor/FBit) which should host any future posts I make with knitr.

For now, I'm testing the post template from [FBit template](https://github.com/lcolladotor/FBit/blob/master/R-post-template/R-post-template.Rmd)



```r
library(ggplot2)
qplot(hp, mpg, data = mtcars) + geom_smooth()
```

![plot of chunk carplot](http://i.imgur.com/zfg0Gih.png) 


You can also visualize the test [here](http://htmlpreview.github.com/?https://github.com/lcolladotor/FBit/blob/master/test-template/test-template.html)
