+++
date = "2017-12-05"
title = "IP address lookup using Python"
slug = "ip-address-lookup-using-python"
tags = []
categories = []
+++

## Tutorial

Hi all, today we are going to create an IP address lookup tool using Python, very useful when you need to discover where some list of domains are hosted at the moment or something like that 🙂

First of all we need to set our environment and import some python packages:

```
#!/usr/bin/env python

import sys
import os
import socket
```

We need to read our domains list from somewhere, I’ll use an simple input file that will be separated by line as example:

```
domains_input = raw_input("Enter input domains file:")
```

And a output file to save our results:

```
domains_output = raw_input("Enter input domains file:")
```

Now we will open our output file:

```
open(domains_output, 'w').close()
```

Here is where the magic happens:

```
try:
    with open(domains_input, "r") as domains:
        for domain in domains:
            try:
                line = domain.replace("\n", "") + " - " + socket.getaddrinfo(domain.replace("\n", ""), 80)[0][4][0]
            except Exception, error:
                line = domain.replace("\n", "") + " - " + str(error)

            print line

            with open(domains_output, "a") as file:
                file.write(line + "\n")
except Exception, error:
    print "Error: " + error
```

Terminal:

```
python your-ip-lookup.py
```

Output:

```
bonesso.io - 127.0.0.1
google.com - 209.85.201.113
```

This is a very simple example, but Python is a very powerful language for day-to-day tasks like that.
