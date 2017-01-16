FROM jangorecki/r-base-dev

ADD requirements.R requirements.R
RUN apt-get update && apt-get -y install libgdal-dev libproj-dev
RUN wget https://github.com/jgm/pandoc/releases/download/1.19.1/pandoc-1.19.1-1-amd64.deb
RUN dpkg -i pandoc-1.19.1-1-amd64.deb
RUN Rscript -e 'source("requirements.R"); install.packages(pkg_list,repos="https://cran.rstudio.com/")'
RUN Rscript -e 'install.packages("devtools"); devtools::install_github("Rdatatable/data.table")'
RUN apt-get -y remove libgdal-dev libproj-dev && apt-get -y autoremove

CMD ["R"]
