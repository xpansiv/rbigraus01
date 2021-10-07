## Use a tag instead of "latest" for reproducibility
FROM rocker/binder:4.0.2

## Declares build arguments
ARG NB_USER
ARG NB_UID

## Copies your repo files into the Docker Container
USER root
COPY . ${HOME}
## Enable this to copy files from the binder subdirectory
## to the home, overriding any existing files.
## Useful to create a setup on binder that is different from a
## clone of your repository
## COPY binder ${HOME}
RUN chown -R ${NB_USER} ${HOME}

ENV RSESSION_PROXY_RSTUDIO_1_4=yes

#RUN R -e "install.packages('BiocManager')"\
#&& R -e "BiocManager::install(version = "3.12", update = FALSE)"\
#&& R -e "BiocManager::install(c('edgeR', 'topGO', 'org.Hs.eg.db'), update = FALSE)"


## Become normal user again
USER ${NB_USER}

