# pattern_match

pattern_match is an abuse of _some_ change to python syntax added in 3.8 with the walrus operator `:=`. It is code that has been carved out of [Panoramix](https://github.com/eveem-org/panoramix) and not at all my original work.

[kolinko](https://github.com/kolinko) built Tilde (here as `pattern_match`) which adds the `~` operator for pattern matching. A `~` denotes a pattern to be matched and then replaced with a series of `:=` operators underneath.  Because of this, Python 3.8 is required.

## Installation:

```
git clone https://github.com/caccavale/pattern_match
```

## Usage:

Currently, encodings are only available in imported modules so trying to run a file using `pattern_match` will fail:

```
$ python imports_pattern_match.py
File "imports_pattern_match.py", line 1
SyntaxError: encoding problem: pattern_match
```

To fix this, have an another file that imports the `pattern_match` using file:

```shell
$ cat wrapper.py
import imports_pattern_match
$ python wrapper.py
```



