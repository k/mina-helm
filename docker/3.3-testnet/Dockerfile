FROM ubuntu:18.04

RUN apt-get update && apt-get install -y ca-certificates
RUN echo "deb [trusted=yes] http://packages.o1test.net release main" | tee /etc/apt/sources.list.d/coda.list
RUN apt-get update
RUN apt-get install -y coda-testnet-postake-medium-curves

CMD ["coda"]
