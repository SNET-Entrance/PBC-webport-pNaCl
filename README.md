This is a patch for building the Pairing-based Cryptography (PBC) library for Google's portable Native Client (pNaCl) environment. 

The PBC Library - Pairing-Based Cryptography - is available at
https://crypto.stanford.edu/pbc/


Prerequirements:
Install nacl webports (former naclports)
Info: https://chromium.googlesource.com/webports/
user@PC1:~/somedirectory$ mkdir webports && cd webports
user@PC1:~/somedirectory/webports$ gclient config --unmanaged –name=src https://chromium.googlesource.com/webports.git
user@PC1:~/somedirectory/webports$ gclient sync --with_branch_heads

Howto compile PBC for pNaCl:
Copy this PBC directory to you Webports src/ports directory.
Build the PBC lib as usual. e.g. 

.../webports/src/ports/pbc$ NACL_ARCH=pnacl make pbc 

PBC Library - Pairing-Based Cryptography - About
https://crypto.stanford.edu/pbc/

Tested with NaCL version: pepper_49 (stable) May 2016.

