FROM centos:7

RUN yum install epel-release -y && \
    yum update -y && \
    yum install httpd -y

WORKDIR /var/www/html

COPY run.sh .

RUN chmod +x run.sh

CMD [ "./run.sh" ]