# SSL Hound Data

A home for miscellaneous data published by [SSL Hound](https://www.sslhound.com/). If you use any of this data for something, please do let us know by opening an issue and telling us about it!

# dotgov-domains

There are two sets of data:

* current-full.csv -- A list of domains used as source material for US government certificate discovery and scans.
* current-full-report.csv -- A CSV containing information on the status of certificates using the reference material. This CSV file has heads and the data is sorted by domain (column 1).

The `current-full.csv` file originates from the [GSA/data](https://github.com/GSA/data) dotgov-domains dataset.

Starting with a list of 5,797 domains, we did disocvery which lead to a total 10,764 endpoints. Discovery was based on services on port 443 and no other ports were scanned.

Some highlights:

* 2,323 endpoints failed during the discovery process.
* 192 endpoints have certificates signed by an unknown authority ("x509: certificate signed by unknown authority")
* 153 endpoints have certificates have expired ("x509: certificate has expired or is not yet valid")
* 890 endpoints have certificates that are not valid for the domain ("x509: certificate is valid for [DOMAINS...] not [DOMAIN]")
* 16 endpoints have certificates that just don't make any sense ("x509: certificate is not valid for any names, but wanted to match [DOMAIN]")
* 1018 endpoints are for invalid hosts ("dial tcp: lookup [HOST]: no such host")
* 359 endpoints had connections ("read tcp [ROUTE]: read: connection reset by peer")
* 516 endpoints timed out after 15 seconds ("dial tcp [IP]:443: i/o timeout")
* 228 endpoints refused connections ("dial tcp [IP]:443: connect: connection refused")
* 32 certificiates are being used for 1,075 endpoints. One of them (the arkansas.gov group) is used by 92.
* 7 endpoints have certificates that expired between 27 DEC 2018 and 26 JAN 2019 (2019 US government shutdown).
* 5,626 endpoints have certificates that expire in 2019.
* 2,636 endpoints have certificates that expire after 1 JAN 2020.

# Copyright information

Open under the MIT License.

Copyright (c) 2019 SSL Hound
