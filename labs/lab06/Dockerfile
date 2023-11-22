## Dockerfile to create an Apache Container Image
## Set to expose port 80 for web traffic
## Set to run Apache on launch
## Uses Universal base image for RHEL7 as RHEL8 not in REPO
FROM ubi7/ubi:7.7
MAINTAINER Attila Balogh-Biro <abaloghb@redhat.com>
LABEL description="Custom webserver demo for DO180"
RUN yum install -y httpd vim && yum clean all
RUN echo "This is a demo of Apache for DO180 from a Dockerfile" > /var/www/html/index.html
EXPOSE 80
ENTRYPOINT ["httpd", "-D", "FOREGROUND"]