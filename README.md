# TYPO3.Try
A Vagrant box to try out the most recent TYPO3 releases.

Just run `vagrant up` and visit [http://6.2.14.local.typo3.org/typo3/](http://6.2.14.local.typo3.org/typo3/) or [http://7.3.1.local.typo3.org/typo3/](http://7.3.1.local.typo3.org/typo3/).

## Installation
Installation is pretty straight forward. You're just a couple of steps away from 'great success'.

1). Clone TYPO3.Tru and cd into it:
```bash
git clone https://github.com/Tuurlijk/TYPO3.Try.git
cd TYPO3.Try
```

2). Then boot the machine:
```bash
vagrant up
```

3). Now you can visit [http://6.2.14.local.typo3.org/typo3/](http://6.2.14.local.typo3.org/typo3/) or [http://7.3.1.local.typo3.org/typo3/](http://7.3.1.local.typo3.org/typo3/). There you may need to run through the install tool. You can access the databases as user `typo3` with the password `supersecret`. If you are presented with a TYPO3 login screen, you can login as user `admin` with the password `supersecret`.

## How do I get onto the box?
You can login by doing a `vagrant ssh`. That user has full sudo privileges. Or you can `ssh vagrant@local.typo3.org` using password `vagrant`.

## MailCatcher
[MailCatcher](http://mailcatcher.me/) runs a super simple SMTP server which catches any message sent to it to display in a web interface. This makes it easy to test forms without actually sending mail to the 'real' mail address. Set your favourite app to deliver to smtp://127.0.0.1:1025 instead of your default SMTP server, then check out [http://local.typo3.org:1080](http://local.typo3.org:1080) to see the mail that's arrived so far.

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
