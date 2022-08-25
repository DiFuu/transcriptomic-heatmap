#FINAL HEATMAPS
library("gplots")

#Read the data and convert to .txt
library(readxl)

ERF2 <- read_excel("ERF2.xlsx", 1)
write.table(ERF2, "ERF2.txt",sep="\t")
ERF6 <- read_excel("ERF6.xlsx", 1)
write.table(ERF6, "ERF6.txt",sep="\t")
ERF104 <- read_excel("ERF104.xlsx", 1)
write.table(ERF104, "ERF104.txt",sep="\t")

#We read the file
genedata2 <- read.table("ERF2.txt",header=T, row.names = "Gene")
attach(genedata2)

data2 <- genedata2[,-1]
data2 <- as.matrix(data2)

genedata6 <- read.table("ERF6.txt",header=T, row.names = "Gene")
attach(genedata6)

data6 <- genedata6[,-1]
data6 <- as.matrix(data6)

genedata104 <- read.table("ERF104.txt",header=T, row.names = "Gene")
attach(genedata104)

data104 <- genedata104[,-1]
data104 <- as.matrix(data104)

#HEATMAPS

library("gplots")

heatmap.2(data2, scale = "row", col = bluered(100), 
          trace = "none", density.info = "none", Colv = FALSE,
          colsep=c(3:3, 6:6, 9:9), rowsep=9:9)

heatmap.2(data6, scale = "row", col = bluered(100), 
          trace = "none", density.info = "none", Colv = FALSE,
          colsep=c(3:3, 6:6, 9:9, 12:12), rowsep=5:5)

heatmap.2(data104, scale = "row", col = bluered(100), 
          trace = "none", density.info = "none", Colv = FALSE,
          colsep=c(3:3, 6:6, 9:9))
