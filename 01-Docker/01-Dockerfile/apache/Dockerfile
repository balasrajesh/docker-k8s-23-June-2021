# Base Image
FROM ubuntu:16.04

MAINTAINER Amit <amitvashist7@outlook.com>

# APT Repo Update
RUN apt-get update


# Install Apache Packages 
RUN apt-get install apache2 -y 

#Deploy Custom WebPage
COPY index.html /var/www/html/


# Expose Port
EXPOSE 80
EXPOSE 3306

# Run the App
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND" ]
