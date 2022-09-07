# Career Statement

---
title: "Career statement"
output: html_document
date: "2022-08-31"
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

```{r cars}
summary(cars)
```

## Including Plots

You can also embed plots, for example:

```{r pressure, echo=FALSE}
plot(pressure)
```

```{r}
install.packages("DiagrammeR")
library(DiagrammeR)
install.packages("diagram")
library(diagram)


DiagrammeR::mermaid("
                    graph TB
                    a(RUTH)-->b
                    b == Link text ==> Values
                    Ruth ==another link text ==> Goal
                    subgroup one
                    Value --> d{Skill}
                    Value --> Unqiue
                    end
                    subgraph two
                    Goal == link text==> 2022
                    Goal == another link text ==> 5yrs
                    Goal == link text==> 10yrs
                   5yrs --> i{text}
                    5yrs -->j
                    end
                    10yrs ->tab1 -> tab2 -> tab3;
                    subgraph one 
                    2022 -->d(text)
                    2022 -->e((text))
                    2022 -->f[text]
                    2022 -->g[text]
                  
                    end
                    style Goal fill:#f9f,stroke:#333,stroke-width:4px
                    style Skill fill:#f9f,stroke:#333,stroke-width:2px 
                    style 2022 fill:#ccf,stoke:#f66,stroke-width:2px,stroke-dasharray:5, 5
                    ")
```
# node definitions with substituted label text
# edge definitions with the node IDs
```{r}
library(DiagrammeR)
grViz("digraph flowchart {
```{r}
```{r}

```

```
     
      node [fontname = Helvetica, shape = rectangle]        
      tab1 [label = '@@1'] 
      tab2 [label = '@@2']
      tab3 [label = '@@3']
      tab4 [label = '@@4']
      tab5 [label = '@@5']
      tab6 [label = '@@6']
tab1 -> tab2 -> tab3;
tab3 -> tab6;
tab2 -> tab4 -> tab5
      }

      [1]: 'List 3 key career goals that you would like to achieve in the next 5 years'
      [2]: 'Explain how they would contribute to your 10 year plan'
      [3]: 'Which one(s) do you intend to achieve in 2022'
      [4]: ' What is your monthly goal/ objective while there?'
      [5]: 'What are the key skills you would like to gain from the experience?'
      [6]: 'What will make you stand out in a company?'
      ")
```
#
```{r}
openplotmat()
 
# create the coordinates
pos <- coordinates(c(1,3,3,3,3))
pos

class(pos)
plot(pos, type = 'n')
text(pos)
par(mar = rep(1, 4))
openplotmat()
pos <- coordinates(c(1,3,3,3,3))
openplotmat(main = "textbox shapes")
rx <- 0.1
ry <- 0.05
pos <- coordinates(c(1, 1, 1, 1, 1, 1, 1,1 ), mx = -0.2)
pos
plot()
textdiamond(mid = pos[1,], radx = rx, rady = ry, lab = PYTHON[1], cex = 2, shadow.col = "lightblue")
textellipse(mid = pos[2,], radx = rx, rady = ry, lab = R[2], cex = 2, shadow.col = "blue")
texthexa(mid = pos[3,], radx = rx, rady = ry, lab = SAP[3], cex = 2, shadow.col = "darkblue")
textmulti(mid = pos[4,], nr = 7, radx = rx, rady = ry, lab = KINGDOM[4], cex = 2, shadow.col = "red")
textrect(mid = pos[5,], radx = rx, rady = ry, lab = QGIS[5], cex = 2, shadow.col = "darkred")
textround(mid = pos[6,], radx = rx, rady = ry, lab = A.EXCELL[6], cex = 2, shadow.col = "black")
textparallel(mid = pos[7,], radx = rx, rady = ry, lab = PETREL[7], cex = 2, theta = 40, shadow.col = "black")
textempty(mid = pos[8,], lab = LETTERS[8], cex = 2, box.col = "yellow")



pos[ ,1] <- pos[ ,1] + 0.5
pos
text(pos[ ,1],pos[ ,2], c("textdiamond", "textellipse", "texthexa",
                          "textmulti", "textrect", "textround",
                          "textparallel", "textempty"))
```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.


