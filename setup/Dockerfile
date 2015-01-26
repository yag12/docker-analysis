FROM vistrcm/ipython-notebook

USER root

RUN apt-get -qq update && apt-get -qq upgrade
RUN apt-get -qq install apache2 php5
RUN pip install runipy
RUN pip install PyMySQL

RUN mkdir /logfile

EXPOSE 80
EXPOSE 8888

CMD service apache2 start && ipython notebook --no-browser --ip=0.0.0.0
