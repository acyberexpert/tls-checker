# tls-checker
Run automated tests on external infrastructure

# Installation
Dump the files somewhere.

You can install index.html on your webserver and make a symlink to the directory where the scripts are living.

If you want the pages to look fancy, download the Edward Tufte CSS and install in /images/tufte/ within your webroot:
[https://github.com/edwardtufte/tufte-css]

# Configuration
Edit any references to example.com to point to your infrastructure:

. In run-uvt, edit the RECIP variable to be your email address.

. In uvt-tls, edit the two hostnames: one in the wget and one in the openssl line.

# Running
Have a cron job kick off 'run-uvt' at semi-regular intervals, for example, daily is good as that will on Monday catch any changes made during weekend maintenance.

I use:

 10 12 * * * $HOME/tls-checker/run-uvt


# License
BSD 2 clause. Refer to [LICENSE] for details.

I developed this while in the employ of my employer, however it was developed during my own time whilst at home on my own servers, so the copyright remains with me.

Copyright (c) 2015, Stephen D. Cope
All rights reserved.

# Author
Stephen D. Cope
https://sdc.org.nz/
