

-- Will need to register the Newtonsoft Json via gacutil
	gacutil /i c:\Newtonsoft.Json.dll
	create the tables with the scripts attached in the dw database


-- I have create the etl process from the data side similiar to the ADF process uses. We need to bring the data into stage and work with merge scripts at the target database.
--I have done a daily load of exchange rates into the table, however there is a need to pull through a last run date (max date in exchange rate table)  in to ssis and compare 
 the run date with the max date so that we dont repeatedly keep adding the same dates values as this will break the join in the sproc. (That join is currently commented out in 
 the sproc sql) 
--We need a bulk load of exchange rates from the API. I have ran out of time to create it.




