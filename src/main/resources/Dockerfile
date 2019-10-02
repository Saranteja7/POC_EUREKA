#############################################################################
# Dockerfile that provides the image for OR - Writes Intergration Layer Image
#############################################################################

################Use Latest Base Image with CentOS and OpenJDK 1.8#############
FROM oneartifactory.verizon.com:8091/vzw/b6vv/orbpm/orbpm-centosopenjdk-baseimg:v1.0

# Define ARG variables
ARG jar_name=dummy
ARG packaging_type=dummy

####### MAINTAINER ############
MAINTAINER "Kaithapuram, Varshini" "varshini.kaithapuram@one.verizon.com" 

########################CREATE FOLDER STRUCTURE############################
RUN mkdir -p /app/application/logs/;

# Add application jar
ADD poc_eureka.jar  /app/application/poc_eureka.jar
RUN chmod 775  /app/application/poc_eureka.jar

RUN sh -c 'touch /app/application/poc_eureka.jar'

EXPOSE 8761



ENTRYPOINT ["java","-jar","/app/application/poc_eureka.jar"]