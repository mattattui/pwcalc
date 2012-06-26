# Simple password calculator

This is a browser-based password password calculator. It takes a site name, a username, and a passphrase, then generates a long password. It has been designed to work offline on mobile devices that support HTML5 offline storage. The app doesn't store passwords or send them over the network; everything is calculated in the browser.

## Why?

* The generated passwords are hard for computers to guess, so they're safer than trying to remember a separate password for every site you use.
* Because the passwords are calculated based on information you know, you can recalculate them whenever you like. So you don't have to save them anywhere or write them down.
* Because each site's password is different, if that site gets hacked or your password stolen, then you don't need to worry that your other accounts will be hacked.





## Credit

The idea of calculating passwords was passed on to me by a friend who probably heard about it from someone else and so on into the mysts of time. It's not a new idea, and it's certainly not my idea, but it's a good one.

The password is actually an encrypted hash. Specifically a SHA1 HMAC. The javascript implementation used is from http://code.google.com/p/crypto-js/ 