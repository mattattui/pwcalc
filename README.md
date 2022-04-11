# Simple password calculator

This is a browser-based password password calculator. It takes a site name, a username, and a passphrase, then generates a long password. It has been designed to work offline on mobile devices that support HTML5 offline storage. The app doesn't store passwords or send them over the network; everything is calculated in the browser.

It was a fun exercise, but I don't seriously recommend you use this (or anything like it). Instead you should use a password manager. There are plenty out there; your browser or OS probably has one built in, or there are apps and services like 1Password, Keepass, and Dashlane among many, many others. Find one you aren't too strongly locked into and use it religiously.

## Why?

* The generated passwords are hard for computers to guess, so they're safer than trying to remember a separate password for every site you use.
* Because the passwords are calculated based on information you know, you can recalculate them whenever you like. So you don't have to save them anywhere or write them down.
* Because each site's password is different, if that site gets hacked or your password stolen, then you don't need to worry that your other accounts will be hacked.

## Why not?

* Needless to say, if someone ever gets out your passphrase, they can guess the rest and generate all your passwords.
* If one account is compromised, you can't generate a different password for it without changing something else. Keeping track of that "something else" becomes harder the more often it happens. At the point you start having to write this stuff down somewhere, you'll probably start wondering why you aren't just using a password manager instead.


## Credit

The idea of calculating passwords is a great idea, but it's not my idea.

The password is actually an encrypted hash. Specifically a SHA1 HMAC. The javascript implementation used is from http://code.google.com/p/crypto-js/ which is new BSD licensed.

Password hashes are generated with the Password Hasher JS from http://wijjo.com/passhash/ -- it's MPL/GPLv2/LGPL. This means you can install that extension and get the same passwords out of it, and some other nice features too (like remembering the settings for each site).

Anything that isn't mentioned above can be assumed to be mine and new BSD licensed.
