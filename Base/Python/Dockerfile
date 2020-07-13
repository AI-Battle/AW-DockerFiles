FROM python:3.7.1

RUN pip install --upgrade pip

COPY ./pip /pip

RUN pip3 install --no-index --find-links=file:/pip -r /pip/requirements.txt

RUN rm -rf /pip

#RUN pip3 install numpy==1.19.0

#RUN pip3 install pandas==1.0.5

#RUN pip3 install tensorflow==2.1

#RUN pip3 install torch==1.5.1
