FROM cpp:ai

ARG id

COPY ./submissions/$id/source /src

RUN mkdir /src/build

RUN cmake -S /src -B /src/build

RUN make -C /src/build

RUN mv /src/build/client/client /

RUN echo "/client 2>&1 | tee /client.log" > run.sh

RUN chmod +x run.sh

CMD ["bash", "run.sh"]
