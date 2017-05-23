```R
# Creat R package 
library(devtools)
setwd("/home/malab4/Documents/G2P_paper/G2P_package/G2P/")
load_all()
document()
check()
build(manual = T)

# Generate PDF manaul
setwd("/home/malab4/Documents/G2P_paper/G2P_package/")
pack <- "G2P"
path <- find.package(pack)
system(paste(shQuote(file.path(R.home("bin"), "R")),
             "CMD", "Rd2pdf", shQuote(path)))
```
