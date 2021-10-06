FROM rocker/binder:3.6.3
LABEL maintainer='Angel Blanco'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}

RUN R -e "install.packages('BiocManager')"\
&& 
&& R -e "BiocManager::install('ComplexHeatmap')"

USER ${NB_USER}



RUN wget https://github.com/xpansiv/rbigraus01/raw/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-07-16/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
