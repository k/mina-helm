# Mina daemon helm chart

## Setup

Make sure you set the external ip of the node you are scheduling mina on, ideally it would discover the public IP but in my experience this does not work properly.

**This chart currently only supports 1 replica because of this!**

By default you need to create the secrets for the seed nodes and password for the snark worker.

Make sure you have a big enough node for mina to schedule on!

## Important [Values](./values.yaml)

* `.bashCommand`: update this with the mina command you would like to run
* `.env`: add env vars to populate `$SEED1` `$SEED2` and any secrets like passwords or private keys if you need them