# ADS IOC example

An example ADS-based IOC with a paired TwinCAT3 solution.

All IOC adoption work was completed by mcbrowne and the [ESS](https://europeanspallationsource.se/). 

## Configuring the IOC

You can edit the IOC's basic configuration options here: `iocBoot/templates/st.cmd`.
The following terms in `[BRACKETS]` with the information about the PLC your IOC is communicating with. 
`adsAsynPortDriverConfigure("ADS_1","[IP_ADDRESS]","[AMS_NET_ID]",851,1000, 0, 0, 500, 1000, 1000, 0)`

## Editing the records

Edit `adsApp/Db/adsTest.db` to create/edit/delete epics records.

## Building the IOC

Use `make` in the main direcotry.

## Running the IOC

After building the IOC, it can be run from `children/build/iocBoot/ioc-tst-ads/st.cmd`

## Before pushing to github

Clean the project with `make distclean`. `make clean` is not sufficient.
