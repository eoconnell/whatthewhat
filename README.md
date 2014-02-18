What the What?
==============

Launch a Google search for exceptions from ~~Python apps~~ programs.

This is a fork of [Doug Hellmann's What the What?](https://github.com/dhellmann/whatthewhat). Working to make it effective for more than just Python. The API is slightly different and arguably worse. Since the aim is to help beginners get comfortable with googling for errors, this command may be too difficult to remember.

Basic usage:
```bash
$ ./tester.py 2>&1 | wtw
```

`2>&1` redirects standard error to standard in. (grep doesn't work with stderr)

However, if your shell supports `|&`, you can try this simplified command:
```bash
$ ./tester.py |& wtw
```

Standard Error:
```
Traceback (most recent call last):
  File "tester.py", line 7, in <module>
      f()
        File "tester.py", line 5, in f
            return {['a', 'b']: ['c', 'd']}
            TypeError: unhashable type: 'list'
```

"TypeError: unhashable type: 'list'" will be sent to Google.


Inspired by
===========

![](https://raw2.github.com/dhellmann/whatthewhat/master/tweets.png)


Requirements
============

* Mac OSX - the script uses `open(1)` to launch your browser. AFAIK, this is only shipped with OSX. I'm hoping this is temporary.


Installation
============

You can drop `wtw` into `~/bin` or `/usr/local/bin`. Just be sure the directory you pick is included in your `PATH`. The file should be executable but if for some reason it is not: `chmod +x wtw`.

TODO
====

* Remove the hard dependency on `open(1)`
* Make the API more beginner friendly

