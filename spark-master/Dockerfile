FROM java:7

ENV SPARK_VERSION spark-2.0.0-preview-bin-hadoop2.7

RUN wget http://www.apache.org/dist/spark/spark-2.0.0-preview/$SPARK_VERSION.tgz -O /root/spark.tgz
RUN tar xf /root/spark.tgz -C /usr/local/
RUN cd /usr/local && ln -s $SPARK_VERSION spark

EXPOSE 7077
EXPOSE 8080
CMD ["/usr/local/spark/bin/spark-class","org.apache.spark.deploy.master.Master"]
