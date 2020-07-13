FROM java:ai

ARG id

COPY ./submissions/$id/source /src

RUN mkdir /out

RUN javac -d /out -classpath $(find /src -iname '*.jar' | paste -sd ":" -): $(find /src -iname '*.java')

RUN find -iname '*.jar' -exec unzip {} -x META-INF/MANIFEST.MF -d /out \;

RUN cd /out && jar -cvfe /client.jar client.Main ./

RUN rm -rf /src

RUN rm -rf /out

RUN echo "java -jar /client.jar 2>&1 | tee /client.log" > run.sh

RUN chmod +x run.sh

CMD ["bash", "run.sh"]
