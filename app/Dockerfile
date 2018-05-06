FROM ubuntu:18.04

MAINTAINER asadi.jabar@outlook.com

# Install dist upgrade 
RUN apt-get update && \
    apt-get install -y python && \
    apt-get upgrade -y -o Dpkg::Options::="--force-confold" 
 

# Cleanup
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*



    


