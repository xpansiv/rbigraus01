FROM rocker/binder:4.0.2
LABEL maintainer='Angel Blanco'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}

#RUN R -e "install.packages('BiocManager')"\
#&& R -e "BiocManager::install(version = "3.12", update = FALSE)"\
#&& R -e "BiocManager::install(c('edgeR', 'topGO', 'org.Hs.eg.db'), update = FALSE)"

USER ${NB_USER}

