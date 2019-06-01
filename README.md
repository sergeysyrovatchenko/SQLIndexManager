# SQL Index Manager

This tool lets you quickly and easily find out the status of your indexes and discover which databases need maintenance.   
You can do maintenance through the UI, or generate a T-SQL script to run in SSMS.

## Key Features

* An incredibly fast describe engine
* Multiple databases scanning
* Advice on rebuilding or reorganizing
* Analysis of fragmentation results
* Configurable fragmentation thresholds
* One-click maintenance
* Command-line automation
* Automatic T-SQL script generation
* Columnstore maintenance support
* Index rebuild with compression options
* Export of scan results into Excel, CSV, HTML and text files
* Support for any editions of SQL Server 2008+ and Azure
* And a lot of other improvements :)

## Latest Version

You can download .zip file with the latest build of the master branch from [Google Disk](https://drive.google.com/open?id=15-dhScvyBfn-qJrb0izF6g1gXg3o40wH)

## Future Plans

* Improvements in command-line automation
* Collecting missing indexes
* Statistics maintenance

## Screenshots

![SQL Index Manager](https://habrastorage.org/webt/b6/qa/sd/b6qasd21kq2qpg-nnxxel3anev0.png)
![SQL Index Manager](https://habrastorage.org/webt/_t/ko/8p/_tko8pek1wuwi3mtsj_hlwp3ruc.png)

## Command Line

#### /connection "Data Source=HOMEPC\SQL_2017;Integrated Security=True;User ID=HOME\PC"
This switch is used to specify connection string.
#### /databases "AdventureWorks2017;master"
This switch is used to specify databases to manage indexes in.
#### /connectiontimeout 30
This switch is used to specify connection timeout in seconds. Overrides value specified in the connection string.
#### /commandtimeout 90
This switch is used to specify command execution timeout in seconds.
#### /online
This switch is used to rebuild indexes with online option.
#### /ignoreheap
This switch is used to ignore any heaps during maintenance.
#### /ignorecolumnstore
This switch is used to ignore any columnstore indexes during maintenance.
#### /ignorebtree
This switch is used to ignore any b-tree indexes during maintenance.
#### /maxdop 8
Configure the max degree of parallelism during maintenance.
#### /reorganizethreshold 15
Specifies reorganize the fragmentation threshold in %. Overrides default option (15%).
#### /rebuildthreshold 30
Specifies rebuild the fragmentation threshold in %. Overrides default option (30%).
#### /minindexsize 32
This switch is used to specify the minimum index size in MB. Overrides global option (8 MB).
#### /predescribesize 128
This switch is used to specify the predescribe index size in MB. Overrides global option (256 MB).
#### /maxindexsize 8096
This switch is used to specify the maximun index size in MB. Overrides global option (8 GB).