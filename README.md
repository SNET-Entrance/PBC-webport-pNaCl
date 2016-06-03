This is a patch for building the Pairing-based Cryptography (PBC) library for Google's portable Native Client (pNaCl) environment. 

The PBC Library - Pairing-Based Cryptography - is available at
https://crypto.stanford.edu/pbc/


<p>Prerequirements:</p>
Install nacl webports (former naclports)
Info: https://chromium.googlesource.com/webports/
<pre><code>
user@PC1:~/somedirectory$ mkdir webports && cd webports
user@PC1:~/somedirectory/webports$ gclient config --unmanaged –name=src https://chromium.googlesource.com/webports.git
user@PC1:~/somedirectory/webports$ gclient sync --with_branch_heads
</code></pre>

Howto compile PBC for pNaCl:
Copy this PBC directory to you Webports src/ports directory.
Build the PBC lib as usual. e.g. 

<pre><code>
.../webports/src/ports/pbc$ NACL_ARCH=pnacl make pbc 
</code></pre>

Tested with NaCL version: pepper_49 (stable) May 2016.

