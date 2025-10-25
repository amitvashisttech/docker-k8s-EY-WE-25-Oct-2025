## Base Image 
FROM ubuntu:noble 

## Owner Details 
MAINTAINER Amit Vashist <amitvashist7@outlook.com>

## Update the APT Repo
RUN apt-get update 

## Install Apache2 Packages 
RUN apt-get install apache2 -y 

## Execute the Service 
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND" ]
