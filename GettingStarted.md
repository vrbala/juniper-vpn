# Getting Started #

Assuming you have downloaded the Juniper VPN software, have the necessary JRE, have converted the ncui.so into an executable, and obtained the SSL certificate for your company's login page, you're ready to begin using this script.  If you have not yet done these things, look first at the [Mad Scientist's page](http://mad-scientist.us/juniper.html) and next at [sdeming's page](http://makefile.com/.plan/2009/10/27/juniper-vpn-64-bit-linux-an-unsolved-mystery).


# Downloading #

Download the script following the instructions on the download page.  Feel free to make it executable (chmod +x junipervpn.py) and place it in your PATH.

# First Execution #

The first time you run it, use the `-c` or `--create` switch to create a configuration file.  It will prompt for user information such as your user name, your SecurID token, the URL of the page you would normally login into in order to retrieve your DSID cookie, etc.  You may optionally store your password in the configuration file.

# Normal Execution #

After you have a valid configuration file, simply execute the script:
```
./junipervpn.py
```

If you have not elected to store your password in the configuration file, you will be first prompted for that information.  Next, you will be prompted for your SecurID token.  At this point, your VPN connection will be initiated.

# Assumptions #

This script was written with logging into my company's webpage in mind and as such, makes many assumptions.  It's likely that your form input field names on your login page will be different.  If this is the case, take a look at the `login` method and modify as you see fit.  Additionally, the various realms are not tested, so again, modifications will most likely be necessary.  Hopefully this will be sufficient to get you started.