---
output:
  md_document:
    variant: markdown
---

Get data
--------

Get data from file and check it out.

``` {.r}
tempfil = read.table("T1-9b.dat",header=FALSE)
head(tempfil)
```

    ##    V1    V2    V3    V4   V5   V6   V7     V8
    ## 1 ARG 11.57 22.94 52.50 2.05 4.25 9.19 150.32
    ## 2 AUS 11.12 22.23 48.63 1.98 4.02 8.63 143.51
    ## 3 AUT 11.15 22.70 50.62 1.94 4.05 8.78 154.35
    ## 4 BEL 11.14 22.48 51.45 1.97 4.08 8.82 143.05
    ## 5 BER 11.46 23.05 53.30 2.07 4.29 9.81 174.18
    ## 6 BRA 11.17 22.60 50.62 1.97 4.17 9.04 147.41

``` {.r}
# create matrix from data frame (removing factor column)
X = as.matrix(tempfil[2:8])
```

Magma colors
------------

In the figure \ref{figure_vol} you got an amazing image of a volcano.

``` {.r}
library(graphics)
library(viridis)
image(volcano, col = viridis(200, option = "A"))
```

![figure caption is this what it is!
\label{figure_vol}](1-example1_files/figure-markdown/unnamed-chunk-3-1.png)

LaTeX coding
------------

Let’s try a first example. Here’s a dummy equation:
$$a^2 + b^2 = c^2$$

and 
$$ \mathsf{Data = PCs} \times \mathsf{Loadings} $$
better is
\\[ \mathbf{X} = \mathbf{Z} \mathbf{P^\mathsf{T}} \\]
and this is quite nice,
$$ \mathbf{X}\_{n,p} = \mathbf{A}\_{n,k} \mathbf{B}\_{k,p} $$
.

\begin{equation}
\label{eq-abc}
a + b = c
\end{equation}
and see equation \ref{eq-abc}. Or for example: see \autoref{eq-abc}.

\begin{equation}
y_{ij} = b_{ij} + \beta_{0} + \beta_{1}
\end{equation}
Test test $\mathbb{1}$ test.

Internationalization
--------------------

Detta är en text på svenska med åäö, dvs ÖÄÅ. Undrar hur det fungerar!
