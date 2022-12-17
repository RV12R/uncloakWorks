# Week 4 Notes

## Chapter 6 MAC

* HMAC computes h(K ⊕ a ‖ h(K ⊕ b ‖ m)), where a and b are specified
constants. The message itself is only hashed once, and the output is hashed again with the key.

* The designers of HMAC were of course aware of the problems with hash functions, which we discussed in Chapter 5. For this reason, they did not define HMAC to be something simple like mac(K, m) as h(K ‖ m), h(m ‖ K), or even h(K ‖ m ‖ K), which can create problems if you use one of the standard iterative hash functions

* GMAC was designed for 128-bit block ciphers. GMAC is fundamentally different from CBC-MAC, CMAC, and HMAC. The GMAC authentication function takes three values as input—the key, the message to authenticate, and a nonce.

