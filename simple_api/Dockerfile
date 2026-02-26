FROM python:3.13-slim
LABEL maintainer="Pierre"
COPY requirements.txt student_age.py /
RUN apt-get update -y && \
    apt-get install -y --no-install-recommends \
        python3-dev \
        libsasl2-dev \
        libldap2-dev \
        libssl-dev \
        gcc \
        build-essential && \
RUN pip3 install -r /requirements.txt
VOLUME [ "/data" ]
EXPOSE 5000
CMD [ "python3", "./student_age.py" ]