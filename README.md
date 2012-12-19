unserved_fixed_broadband
========================

This repository contains the data which fulfills the requirements of the Federal Communication Commission’s November 19 Further Notice of Proposed Rulemaking [see http://www.fcc.gov/document/connect-america-fund-1](http://www.fcc.gov/document/connect-america-fund-1).  It lists census blocks that are reported on the National Broadband Map as unserved by fixed broadband with advertised speeds of 3 Mbps downstream and 768 kbps upstream.  The data relies on the current version of the National Broadband Map, using data as of December 31, 2011.

Files:
------
fixed_unavail_dec2011.csv 
- download link - [https://github.com/fccdata/unserved_fixed_broadband/archive/master.zip](https://github.com/fccdata/unserved_fixed_broadband/archive/master.zip)
- number of records - 1,030,072 (+ header)
- description - includes all 2012 US Census Blocks which are unserved or partially served as described in the National Broadband Map as of December 31, 2011; one row per block
- columns (fields) 
  - block_fips     varchar(15)
	- fixed_3_768_unavail - integer “1” if block is populated and has NO fixed 3_768 availability
	- fixed_3_768_partial_unavail - integer “1” if block is populated and has PARTIAL fixed 3_768 availability
	- usf_type - varchar(13) “ROR”, “PC”, or “UNCLASSIFIED” for all records

Details: 
--------
- Price Cap Count (PC) :  830,093
- ROR Count (ROR):  199,052
- Unclassified Count (UNCLASSIFIED):   927