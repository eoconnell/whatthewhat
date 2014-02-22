What the What?
==============

Launch a Google search for exceptions from ~~Python apps~~ programs.

This is a fork of [Doug Hellmann's What the What?](https://github.com/dhellmann/whatthewhat). Working to make it effective for more than just Python. The API is slightly different.

Usage:
```bash
$ wtw 'python tester.py'
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

`TypeError: unhashable type: 'list'` will be sent to Google.


Inspired by
===========

![](https://raw2.github.com/dhellmann/whatthewhat/master/tweets.png)


Installation
============

You can drop `wtw` into `~/bin` or `/usr/local/bin`. Just be sure the directory you pick is included in your `PATH`. The file should be executable but if for some reason it is not: `chmod +x wtw`.

TODO
====

* Improve browser delegation
