# Crowd sourced MUD files

[RFC8520](https://datatracker.ietf.org/doc/rfc8520/) describes Manufacturer
Usage Description or MUD files.  These provide ACLs for expected behaviour
for (IoT) devices.

But what if the manufacturer has not provided any files (yet)?

The goal of this repository is to provide a
[crowd sourced](https://en.wikipedia.org/wiki/Crowdsourcing) repository of
files for common and uncommon devices.

At this point we have very few devices, so an ontology of devices is not
really necessary or desireable.    Put things wherever you like for now.
That is, make it up, and don't worry too much. Once we have a few hundred
definitions, then we will want to sort  according to some to be determined
categories.

Please establish a new directory for each device, and name the directory for
the device's common name.  If there are multiple hardware/firmware versions
then further subdirectories would make sense.
Please name the files with the extension ".mud", and the signature ".mud.sig".
Please use relative URLs for the pathname to the signature, and we encourage
you to do generate signatures with an S/MIME key.  You can generate a keypair
using openssl, or get a keypair from a number of CAs that offer email
certificates.

Please include a file "Descrition.md" in each directory that explains what
the device does, and how the MUD file was generated, and which firmware was
observed, if known.  A photo of the device would be appreciated, as would
a photo of any model/firmware stick on the device.  You are encouraged to
redact any serial number information in the picture using a photo editor.


