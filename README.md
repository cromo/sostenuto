# Sostenuto

Sustain similar lines while letting everything else through unaltered.

## Overview

Sostenuto follows rules for filtering streaming text files that are more complex
than a simple pattern match, while allowing all unmatched text through.

It is inspired by the
[sostenuto (middle) pedal](https://en.wikipedia.org/wiki/Sostenuto) of a piano.

## Installation

At the moment, just put the `sostenuto` script in your `PATH` and make it
executable.

## Usage

```
sostenuto (<matcher> <matcher_args>*)*
```

Sostenuto provides a number of matchers that take various arguments:

```
counter <pattern> <repetitions>   Prints lines matching <pattern> only once
                                  every <repetitions> occurences.
throttle <pattern> <cooldown>     Prints lines matching <pattern> only once
                                  every <cooldown> seconds.
once <pattern>                    Prints only the first line matching <pattern>.
                                  All further matches are ignored.
expression <pattern> <predicate>  Allows a predicate (Python lambda body) to
                                  determine whether a line is sustained. The
				  parameter names are 'a' and 'b', and are
				  Python match objects.
```

## License

Sostenuto is licensed under the MIT license. The full license is in the
`LICENSE` file.