FROM python:ai

ARG id

COPY ./submissions/$id/source /client

RUN echo "python3 -u /client/Controller.py 2>&1 | tee /client.log" > run.sh

RUN chmod +x run.sh

CMD ["bash", "run.sh"]
