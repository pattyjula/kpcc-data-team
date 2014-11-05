# KPCC/SCPR Data

A repository containing datasets, information and other goodies from KPCC/SCPR

* **[2014-la-county-certified-primary-results](https://github.com/SCPR/data/tree/master/2014-la-county-certified-primary-results)**
    * **WHAT**: Certified results from LA County for the June 3, 2014 primary.
    * **HOW ACQUIRED**: Purchased from the LA County Registrar/Recorder for $54.00
    * **NOTES**: Converted from original .xls files to .csv using csvkit and the following commands.
        * Change the file permissions

                chmod -R 777 .

        * Convert .xls to .csv using csvkit

                for file in *.xls ; do in2csv $file > _$file | mv _$file `echo _$file | sed 's/\(.*\.\)xls/\1csv/'` ; done

* **[la-county-voter-turnout-historic](https://github.com/SCPR/data/tree/master/la-county-voter-turnout-historic)**
    * **WHAT**: Dates, registration, ballots cast, turnout and source data for midterm primary and general elections in Los Angeles County between 1942 and 2014.
    * **HOW ACQUIRED**: Acquired via [available data](http://apps1.lavote.net/General/ARCHIVES/OFFICIAL_ELECTION_RETURNS/Default.cfm) on the LA County Registrar/Recorder website
    * **NOTES**:
        * Registered voters not available for elections between 1942 and 1958.
        * Turnout figures not available for elections between 1942 and 1950; the 1954 midterm primary ; the 1958 midterm primary.

* **[2014-ca-election-tweets](https://github.com/SCPR/data/tree/master/2014-ca-election-tweets)**
    * **WHAT**: Tweets that used the hashtag #CAElection and #CAElections between 8 a.m. on Nov. 4, 2014 and 12:10 a.m. on Nov. 5, 2014.
    * **HOW ACQUIRED**: Pulled using the Twitter API.