Wallet update, release 2.2.2.1

While work is also done on the switch to BTC codebase v0.17, we haven't forgotten about the current version of the wallet, already available for our community. This update is another set of changes & improvements targeting better stability and user experience - after careful revision, code was added to slightly alter the speed of Enigma transaction handling, as well as some network buffer tracking/shaping. Motivation was to fix the d/c storm issue associated with Enigma transactions. The issue is not (and was not) reproducible on devnet or testnet with relatively small number of nodes - hard to say this is the final solution without testing it "in the wild" as the problem seems to be large network and/or bandwidth related; we would require most of our users to also run testnet nodes. That being said, we are also looking into putting in place a permanent testnet, where issues like this can be tested properly and will provide us with a better place to catch more errors before they hit livenet.

*Note:* To isolate the send/receive mechanics from previous client versions that have the issue, Enigma v1.2 *is not* backwards compatible."

Changelog:
- introduced a small delay in processing enigma onion layers & relaying messages
- added a delay to socket read when receive buffer approaching full to allow time for processing and relaying messages in the main thread
- bumped client version to 2.2.2.1
- bumped Enigma engine version to 1.2

Linux SHA256: 71b9391962183427b546db752593f0377c76df4c05af97d2a85b40412186689b  Linux-cloakcoin-2.2.2.1.zip

Windows SHA256: 07829e4656c99799ce2c2483e4623b13af22375608f6a0b6d4e59bc8ada954de Windows-cloakcoin-2.2.2.1.zip

MacOS SHA256: 509b9c729d4f086df4daa08dd5dd48c6b9a7fb422cdca927abd9adf86b1064af  OSX-cloakcoin-2.2.2.1.zip
