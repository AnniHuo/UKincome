FROM rocker/binder:4.0.2
LABEL maintainer='Ann'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/AnniHuo/UKincome/raw/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-11-17/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
