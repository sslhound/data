# SSL Hound Data

A home for miscellaneous data published by the [SSL Hound](https://www.sslhound.com/). If you use any of this data for something, please do let us know by opening an issue and telling us about it!

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
* 890 endpoints have certificates that are not valid for the domain ("x509: certificate is valid for A... not B")
* 16 endpoints have certificates that just don't make any sense ("x509: certificate is not valid for any names, but wanted to match ...")

# Copyright information

Open under the MIT License.

Copyright (c) 2019 SSL Hound
