Stegger
=========

**Steganography made simple for Node.JS**


##About#
Stegger is a steganographic utility for Node.JS, to conceal encrypted text
within JPEG images (yes, JPEG!).  It wraps around the UNIX utility, `outguess`.

I couldn't find a working existing module on `npm`, so I made my own. =


##About Steganography#
Stegaography is the art of concealing data within ordinary looking objects,
such that the original file does not appear to be tampered with.
See http://en.wikipedia.org/wiki/Steganography for more
information.


##Example##
**Before:**

![before](https://github.com/toiletfreak/stegger/blob/master/doc/before.jpg)

**After:**

![After](https://github.com/toiletfreak/stegger/blob/master/doc/after.jpg)
        
Encrypted message: 'hello world (안녕하세요! 잘지네세요?)'



##Installation#

1. Install `outguess` with your relevant package manager.  This can be done in Ubuntu via:

    sudo apt-get install outguess

2. Install from `npm`: 

    npm install stegger

3. You're all set!  Load a picture, and get swagging!


##Documentation#

Check out the examples directory.  The example provided, tests the `encrypt()`
and `decrypt()` function sequentially.  This is done via asynchronous sequences.

Easy to use - just call either `encrypt()` or `decrypt()`.  Pass in the
relevant argument object.  Listen for the `promise` callback.


##Issues#

None at the moment.  Post any via the bug tracker.


##Security##
How secure is it?  Well, pretty secure.

1. Text is encrypted with AES-256 cipher and salted.
2. Text is concealed within least-probable detected areas and salted with a second
   salt.
3. Image would have to be earmarked as having embedded information (hard),
   before being cracked.

##Credit#

Joel Haowen TONG (me [at] joeltong [dot] org) 
