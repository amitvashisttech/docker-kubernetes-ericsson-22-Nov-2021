# Base Image
FROM ubuntu:16.04

# Maintainer of Image
MAINTAINER Amit Vashist <amitvashist7@outlook.com>

# Update the Repo.
RUN apt-get update

# Install Apache Packages
RUN apt-get install apache2 -y 

# Run the Apache Service
CMD ["/usr/sbin/apache2ctl", "-D" , "FOREGROUND"]
