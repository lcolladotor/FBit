


This week started the English Composition I: Achieving Expertise course (<span class="showtooltip" title="(2013). Coursera.  https://www.coursera.org/ [Online.
last-accessed: 2013-03-21 03:47:13]. 
https://www.coursera.org/course/composition."><a href="https://www.coursera.org/course/composition">Comer, 2013</a></span>) that I have been looking forward to. 

I am not sure yet how long I will last, but I hope to enjoy it as much as I can. Plus, it should help me with my posting and other writing areas. While I last in the course, I plan to publish my writings in the blog too. So you will hopefully see me be more active here.

As it is important to cite when writing, I have also figured out how to do so automatically in Rmd files. For that I learnt how to use __knitcitations__ from the GitHub instructions (<span class="showtooltip" title="cboettig (2013). knitcitations. 
https://github.com/cboettig/knitcitations [Online. last-accessed:
2013-03-21 03:19:44]. 
https://github.com/cboettig/knitcitations."><a href="https://github.com/cboettig/knitcitations">knitcitations</a></span>) and a explanatory post (<span class="showtooltip" title="Boettiger C (2013). knitcitations. 
http://www.carlboettiger.info/2012/05/30/knitcitations.html
[Online. last-accessed: 2013-03-21 02:15:41]. 
http://www.carlboettiger.info/2012/05/30/knitcitations.html."><a href="http://www.carlboettiger.info/2012/05/30/knitcitations.html">Boettiger, 2013</a></span>).

__knitcitations__ is great, but it kind of struggles with some pages. That is why I modified my template in [FBit](https://github.com/lcolladotor/FBit) by writing my own citing function for pages where `citep` fails. Here is the code:


```r
## I made my own citing function since citep() doesn't work like I want to
## with urls that are not really pages themselve like part of a GitHub
## repo.
mycitep <- function(x, short, year = substr(date(), 21, 24), tooltip = TRUE) {
    tmp <- citep(x)
    res <- gsub("></a>", paste0(">", short, "</a>"), tmp)
    if (tooltip) {
        res <- gsub("\\?\\?\\?\\?", year, res)
    }
    res
}

## You already saw an inline working example in the post itself.
```






- Carl Boettiger,   (2013) knitcitations.  *Lab Notebook*  [http://www.carlboettiger.info/2012/05/30/knitcitations.html](http://www.carlboettiger.info/2012/05/30/knitcitations.html)
-  cboettig,  knitcitations.  *GitHub*  [https://github.com/cboettig/knitcitations](https://github.com/cboettig/knitcitations)
-  Coursera.  *Coursera*  [https://www.coursera.org/course/composition](https://www.coursera.org/course/composition)

