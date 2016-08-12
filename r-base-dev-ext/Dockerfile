FROM jangorecki/r-base-dev

RUN apt-get update && apt-get -y install libgdal-dev libproj-dev &&
Rscript -e 'install.packages(c("data.table","ggplot2", "foreach", "sp", "gstat", "rgdal", "GA", "R6", "lintr", "testthat","caret"),repos="https://cran.rstudio.com/")'

CMD ["R"]
