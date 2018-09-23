+++
date = "2017-02-07"
title = "Getting started with IPFS"
slug = "getting-started-with-ipfs"
tags = []
categories = []
+++

## Tutorial

Did you ever hear about IPFS? Problably yes right?

Anyway, IPFS is an exciting distributed file system that seeks to connect all computing devices with the same system of files. It’s a new protocol (ipfs://) that probably will replace the traditional web (http://) in a few years (maybe).

I will give a few useful examples of how to get started.

First of all, you need to install the IPFS package using the link bellow:

https://ipfs.io/docs/install

After that, just open your terminal and type:

```
ipfs init
```

This will initialize your IPFS node in your home directory and you will see something like that:

```
initializing ipfs node at /Users/bonesso/.ipfs
generating 2048-bit RSA keypair...done
peer identity: Qmd2JZnAStsH4sJqPmx8iH22h4ydgsiRdq5K6bmbRrtrkf
to get started, enter:

ipfs cat /ipfs/QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz79ojWnPbdG/readme
```

If you want to transfer some files to the IPFS network, just type in your terminal:

```
ipfs add rocket.png
```

And you will get the hash key for your file.

```
added QmaHQK4D726V8cxDEYW4VMvrP5njBotnaCqeUm2K2dQ5NB rocket.png
```

All done, now just open your browser using the hash key that you receive:

https://ipfs.io/ipfs/QmaHQK4D726V8cxDEYW4VMvrP5njBotnaCqeUm2K2dQ5NB

Your file is successful hosted and distributed along the IPFS protocol.

## GUI

IPFS has a nice GUI running at 5001 port, so if you prefer just open in your brower:

http://localhost:5001/webui

That’s it, I hope you guys have enjoyed this amazing tool.
