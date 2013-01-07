unserved_fixed_broadband
========================

This repository contains the data which fulfills the requirements of the Federal Communication Commission’s November 19 Further Notice of Proposed Rulemaking [see http://www.fcc.gov/document/connect-america-fund-1](http://www.fcc.gov/document/connect-america-fund-1).  It lists census blocks that are reported on the National Broadband Map as unserved by fixed broadband with advertised speeds of 3 Mbps downstream and 768 kbps upstream.  The data relies on the current version of the National Broadband Map, using data as of December 31, 2011.  This map was prepared in conjunction with a Public Notice (see [http://fjallfoss.fcc.gov/edocs_public/Query.do?numberFld=12-1961&numberFld2=&docket=&dateFld=&docTitleDesc](http://fjallfoss.fcc.gov/edocs_public/Query.do?numberFld=12-1961&numberFld2=&docket=&dateFld=&docTitleDesc.  A subsequent Public Notice was released further clarifying the data released and can be found here [http://fjallfoss.fcc.gov/edocs_public/Query.do?numberFld=12-2001&numberFld2=&docket=&dateFld=&docTitleDesc](http://fjallfoss.fcc.gov/edocs_public/Query.do?numberFld=12-2001&numberFld2=&docket=&dateFld=&docTitleDesc.)

This map shows census blocks (those with housing units) where fixed broadband (with a speed of 3 mbps download, 768 kbps upload) is partially unavailable or completely unavailable (in Price Cap areas only).  

- download link - [https://github.com/fccdata/unserved_fixed_broadband/archive/master.zip](https://github.com/fccdata/unserved_fixed_broadband/archive/master.zip)

Files:
------
fixed_unavail_dec2011.csv - the raw csv of blocks with 0 population which are unserved or partially served in Price Cap Areas
- number of records - 1,030,072 (+ header)
- description - includes all 2012 US Census Blocks which are unserved or partially served as described in the National Broadband Map as of December 31, 2011; one row per block
- columns (fields) 
  - block_fips     varchar(15)
	- fixed_3_768_unavail - integer “1” if block is populated and has NO fixed 3_768 availability
	- fixed_3_768_partial_unavail - integer “1” if block is populated and has PARTIAL fixed 3_768 availability
	- usf_type - varchar(13) “ROR”, “PC”, or “UNCLASSIFIED” for all records

fixed_unavail_dec2011.zip - the shapefile of blocks dissolved by state and unserved or partially served
- this shape file is the shapes of blocks in the .csv listed above.


Methods:
--------
The domain of technologies used to prepare this map are:  FIXED BROADBAND TECHNOLOGIES:
Code 	Description
10	Asymmetric DSL
20	Symmetric DSL
30      Other Copper Wireline
40      Cable Modem - DOCSIS 3.0
41	Cable Modem - Other
70	Terrestrial Fixed Wireless - Unlicensed
71	Terrestrial Fixed Wireless - licensed
90	Electric Power Line

The Partially Unavailable Areas (Light Orange) are those Census blocks with some housing units (e.g. > 0) AND have one of the two followingconditions:
  -  Provider(s) offer wireless broadband with speed at least 3mbps/768kbps, but the Wireless footprint covers between 0.41% and 99.4% of the census block OR;
  -  Provider(s) offer fixed broadband with speed at least 3mbps/768kbps, but the total Address Points/Steet Segment data account for less than the total housing units in the census block.

The Completely Unavailable Areas (Dark Oragne) are those Census blocks with some housing units (e.g. > 0) AND in which no provider offers fixed broadband with speed at least 3mbps/768kbps.

The Available Areas (no shading) are all other areas; those that have Availabilty of fixed broadband with speed at least 3mbps/768kbps.


Details: 
--------
fixed_unavail_dec2011.csv 
- Price Cap Count (PC) :  830,093
- ROR Count (ROR):  199,052
- Unclassified Count (UNCLASSIFIED):   927
