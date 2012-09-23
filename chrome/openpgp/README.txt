All of this openpgp code is by Herbert Hanewinkel, (from http://www.hanewin.net/encrypt/)

The idea is to combine it with gmailr to encrypt messages client-side BEFORE gmail's 
(ajax|websockets|other) sends the message to the Google servers.

The next step is to watch for encrypted messages and decrypt them.

The public keys can be collected using javascript using https://github.com/GPGTools/GPGTools
and stored in Local Storage, (within the web browser.)

The private key can be encrypted using https://github.com/alexxroche/gibberish-aes and then 
stored in the local storage, (actually I would use http://pablotron.org/software/persist-js/ [1].)
(Though remembering that many people back up their email using IMAP: 
http://www.alexx.net/2012/01/email-archive-how-do-you-do-yours.html it might be worth storing keys in an unsubscribed IMAP4 directory.)

Some collaboration with the http://www.enigmail.net Project seems to be in order [2]; 
How about we become enigmail-js?

Eventually a Google Chrome and Firefox add-on would be the goal, (and we might be able to automate the
web-of-trust to some extent if we plagiarise^Wlovingly adapt some of Moxie's work over at http://convergence.io/.)

Alexx Roche 2012


[1] https://github.com/jeremydurham/persist-js is also available, and I think that this should be
forked into persist-js-noCookies, and then take a leaf out of the evercookie book and keep n+1 copies
of the data, (in two or more places), and if one is removed replace it from the other location.

[2] Because they are the big brother that we always wanted to be.
