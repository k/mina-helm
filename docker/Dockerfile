FROM ubuntu:18.04

RUN apt-get update && apt-get install -y ca-certificates
RUN echo "deb [trusted=yes] http://packages.o1test.net unstable main" | tee /etc/apt/sources.list.d/coda.list
RUN apt-get update
RUN apt-get install -y -t unstable coda-testnet-postake-medium-curves=0.0.12-beta+406048-feature-bump-genesis-timestamp-3e9b174-PV48525e92

CMD ["coda"]
