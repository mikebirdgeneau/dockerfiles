FROM jangorecki/r-base-dev

ADD requirements.R requirements.R
RUN apt-get update && apt-get -y install libgdal-dev libproj-dev
RUN Rscript -e 'source("requirements.R"); install.packages(pkg_list,repos="https://cran.rstudio.com/")'
RUN apt-get -y remove ibgdal-dev libproj-dev

CMD ["R"]
