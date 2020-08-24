# massIngestionDataloader

Companion code to Kx Technical White Paper [“Mass ingestion through data loaders”](https://code.kx.com/q/wp/data-loaders/)


Example usage:

```q
//cd to directory where files are located

//start worker processes
q .mi.slave.q -p 5100
q .mi.slave.q -p 5101
q .mi.slave.q -p 5102

//start orchestrator process
q .mi.runMaster.q -p 5000

//load hdb
cd hdb
q .

//query to confirm data looks good
select count i by date from marketTrades
```