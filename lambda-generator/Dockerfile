#
# Lambda Builder Dockerfile
#
FROM digitalsanctum/maven-jdk8-debian

ADD lambda-core/target/lambda-core-1.0-SNAPSHOT.jar /data/
ADD lambda-generator/target/lambda-generator-1.0-SNAPSHOT.jar /data/
ADD lambda-generator/generate.sh /data/
ADD lambda-api-gateway-jersey /data/template

WORKDIR /data

# lambda defaults
ENV LAMBDA_HTTP_METHOD=POST LAMBDA_TIMEOUT=5

RUN chmod a+x /data/generate.sh
