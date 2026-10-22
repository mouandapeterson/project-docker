FROM python:3.13-slim
LABEL maintainer="Peterson MOUANDA"
COPY requirements.txt student_age.py /
RUN apt update -y && apt install --no-install-recommends -y \
    build-essential \
    python3-dev \
    libsasl2-dev \
    libldap2-dev \
    libssl-dev && \
    rm -rf /var/lib/apt/lists/*
RUN pip3 install -r /requirements.txt
VOLUME ["/data"]
EXPOSE 5000
CMD ["python3", "/student_age.py"]