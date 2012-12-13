# Unmaintained

Magic Password Generator ''is unmaintained''.
Please do not report bugs, they will not be fixed.
If you'd like to adopt it, and maintenance of it, please contact the author.

# Download

 * http://static.arantius.com/misc/mpwgen-1.5.4.xpi

# Documentation

## What is it?

The idea is that it is more secure to give every website a different password.
If one site has naughty administrators, or gets hacked, the same compromised password won't work for your account on another site.
But how can one remember a different password for every site?
Don't, let the computer make one for you!

You remember one master password.
'''(It is not stored anywhere, don't forget it!)'''
Then, with a (somewhat simple) [cryptographic hash function](http://en.wikipedia.org/wiki/Cryptographic_hash_function), the extension combines your master password and the domain name of the site to make another unique password for that site.
The password is not saved in Firefox, or anywhere else.
It's secure!

For example, if your master password is "`juice`" and you are on "`ebay.com`" this tool will scramble those two pieces together and come out with "`203a29e`" for the password.
However, if you are on "`google.com`" with the same master password, the generated password will be "`d382e9ce`".
Neither site has any idea what your real password is, or what your real password for the other site would be, even if they steal the password you used for their site.

There's two other nice features that make logging in even easier.
You can configure a username and/or an email address to fill in, at the same time that the password is filled in.

For advanced users, with a catchall address at a domain, just put "@example.com" (whatever your domain is) for the address, and MPWGen will make a different email for every site too!
Alternately, use "foo+@example.com" and the value will be inserted after the + sign, for email accounts that support this feature, like gmail.

## How to use it?

First, after installing, right click on your toolbar and choose "Customize".
In the window that comes up, you'll find a new lock icon, labeled Magic Password.
Drag that icon onto your toolbar.
Optionally now, configure a username and/or email address to use.

Now, whenever you go to a website asking for a password to log in, simply click the icon and type your master password in the prompt that comes up.
Alternately, right-click in any password field, and select the 
That's it!

Another note: There is an option labeled "disable password remembering."
This option will disable Firefoxes default password remembering feature, for passwords filled out with this extension.
When it is on, you can just tap ENTER twice after filling in your master password; the second tap will almost always submit the form.

## At another computer?

If you are at a public/shared computer that doesn't have the extension or perhaps Firefox at all, you can use [this bookmarklet](http://bookmarklets.arantius.com/password+maker+bookmarklet) to do the same password magic.

You can also use [this form](http://arantius.com/misc/mypass.html) to find out what your password for any site is.

## Help! I forgot my master password, how do I recover it?

The master password is ''purposely'' not stored anywhere.
There is no recover.
There is no reset.
It is in your brain only, and perhaps anywhere else you wrote it down.

## How do I change the master password for the Password Manager, I forgot it!

There is a feature in Firefox called the "Password Manager".
This feature will store your usernames and passwords, so you don't have to remember them.
Optionally, you may give that tool a "master password" which it uses to encrypt the data it saves, so that your passwords are not visible to just anyone who happens to sit down at your computer.
But, I did not write Firefox, and I am not related to that feature!
Don't forget this password, because you can't get it back.

You can [reset it](http://kb.mozillazine.org/Master_password#Reset_your_master_password), but doing this will erase all the stored data at the same time.
But please, don't send me mail about the Firefox Password Manager.
It is in no way related to this extension.

# Similar Projects

MPG is far from the only tool to provide a feature like this.
In no particular order:

 * http://bookmarklets.arantius.com/password+maker+bookmarklet 
   (The compatible bookmarklet version, works in Firefox and IE.)
 * http://www.angel.net/~nic/passwdlet.html
   (The original inspiration for this extension.)
 * http://crypto.stanford.edu/PwdHash/
 * http://www.xs4all.nl/~jlpoutre/BoT/Javascript/PasswordComposer/
 * http://wijjo.com/passhash/
 * http://passwordmaker.org/

# Changelog

 * Version 1.5.4 (Jun 28, 2011)
   * Updated translations from babelzilla.org.
   * Firefox 5.0 compatibility flag.
 * Version 1.5.3 (Jan 14, 2011)
   * Compatibility with Firefox 4.0.
   * Add translations: ar, da, de, fr, mk-MK, nl, pl, sr.
   * Update translations: ca-AD, es-AR, fi-FI, it-IT, pt-BR, uk-UA, zh-CN, zh-TW.
 * Version 1.5.2 (Nov 10, 2009)
   * Compatibility with Firefox 3.6.
   * Do not fill values into invisible fields.
 * Version 1.5.1 (Apr 30, 2009)
   * Improve site compatibility; never alter hidden fields.
   * More accurately detect field type by examining the "id" as well as the "name".
   * Gracefully handle third-level (i.e. .co.uk) domain names.
 * Version 1.5 (May 23, 2008)
   * Offer the ability to remember the master password, to reduce typing.
   * Firefox 3.0 compatibility.
 * Version 1.4 (Jun 21, 2007)
   * Allow plus-address expansion.
 * Version 1.3.5 (Mar 28, 2007)
   * Add translations: zh-CH, nb-NO, fi-FI.
 * Version 1.3.3
   * Add translations: ca-AD, ja-JP, ko-KR, ms-MY, tr-TR, zh-TW.
   * Add keyboard shortcut: {{{CTRL-ALT-M}}} (Ticket #2).
   * Bug fix: Do not reset usernames and/or emails that are already filled in, when not configured with a value to put in that field (Ticket #1).
 * Version 1.3.2
   * Internal fix for locale translations.
 * Version 1.3.1
   * Translation updates.
 * Version 1.3:
   * Compatiblity with Firefox 2.0.
   * Improved detection for which fields should hold usernames, and which emails.
   * Ability to activate by right-clicking on a password field in addition to the standard toolbar button.
 * Version 1.2.2
   * 8 more translations.
 * Version 1.2.1
   * Translations for 4 languages, thanks to BabelZilla.
 * Version 1.2
   * Disable Password Remembering feature.
 * Version 1.1
   * Compatibility with Firefox 1.5.
   * Better detection of which field should get an email.

# Credits

 * The icon comes from the eXperience Crystal gtk theme, by [everaldo](http://www.everaldo.com/).

# License

Magic Password Generator is released under the MIT license.
