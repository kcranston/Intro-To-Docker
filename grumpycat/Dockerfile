# This is a basic webserver image, for
# Linux@Duke's Introduction To Docker: Do Your Own Docker class

FROM centos:centos6
MAINTAINER Chris Collins <collins.christopher@gmail.com>

RUN yum install -y httpd
RUN yum clean all
RUN rm /etc/httpd/conf.d/welcome.conf

ADD https://upload.wikimedia.org/wikipedia/commons/e/ee/Grumpy_Cat_by_Gage_Skidmore.jpg /var/www/html/grumpycat.jpg
RUN chmod 644 /var/www/html/grumpycat.jpg

RUN echo "Redirect /doge /grumpy/doge.jpg" > /etc/httpd/conf.d/redirect.conf

VOLUME ["/var/www/html"]

EXPOSE 80

CMD ["/usr/sbin/httpd", "-DFOREGROUND"]

