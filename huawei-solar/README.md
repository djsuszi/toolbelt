# FusionSolar -> PVOutput synchronization

The purpose of this script is to synchronize energy and power
genration data produced by Huawei SUN2000 inverter (available
in FusionSolar system) with [PVOutput](https://pvoutput.org/).

Lack of public api on FusionSolar requires simulating user login.
The script sychronizes entire history and live data

## Usage

First, build the image:

    docker build -t huawei-pvoutput .

Then, run it, providing your user credentials for FusionSolar
and API keys for PVOutput:

    docker run -d huawei-pvoutput:latest \
        --fusionsolar-user xxxx@xxxx.com \
        --fusionsolar-password xxxxx \
        --pvoutput-api-key xxxxxxx \
        --pvoutput-system-id 00000

If this is the first time you run the script, add

    --start-date YYYY-MM-DD

indicating the date when your inverter was connected to 
the network. Next scripts runs use status based on PVOutput
data, so this parameter is not required.
