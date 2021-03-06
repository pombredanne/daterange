# `daterange`

Like `xrange()`, but for `datetime` objects.

## Example Usage

    >>> import datetime
    >>> start = datetime.date(2009, 6, 21)

    >>> g1 = daterange(start)
    >>> g1.next()
    datetime.date(2009, 6, 21)
    >>> g1.next()
    datetime.date(2009, 6, 22)
    >>> g1.next()
    datetime.date(2009, 6, 23)
    >>> g1.next()
    datetime.date(2009, 6, 24)
    >>> g1.next()
    datetime.date(2009, 6, 25)
    >>> g1.next()
    datetime.date(2009, 6, 26)

    >>> g2 = daterange(start, to=datetime.date(2009, 6, 25))
    >>> g2.next()
    datetime.date(2009, 6, 21)
    >>> g2.next()
    datetime.date(2009, 6, 22)
    >>> g2.next()
    datetime.date(2009, 6, 23)
    >>> g2.next()
    datetime.date(2009, 6, 24)
    >>> g2.next()
    datetime.date(2009, 6, 25)
    >>> g2.next()
    Traceback (most recent call last):
    ...
    StopIteration

    >>> g3 = daterange(start, step='2 days')
    >>> g3.next()
    datetime.date(2009, 6, 21)
    >>> g3.next()
    datetime.date(2009, 6, 23)
    >>> g3.next()
    datetime.date(2009, 6, 25)
    >>> g3.next()
    datetime.date(2009, 6, 27)

    >>> g4 = daterange(start, to=datetime.date(2009, 6, 25), step='2 days')
    >>> g4.next()
    datetime.date(2009, 6, 21)
    >>> g4.next()
    datetime.date(2009, 6, 23)
    >>> g4.next()
    datetime.date(2009, 6, 25)
    >>> g4.next()
    Traceback (most recent call last):
    ...
    StopIteration


## (Un)license

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or distribute this
software, either in source code form or as a compiled binary, for any purpose,
commercial or non-commercial, and by any means.

In jurisdictions that recognize copyright laws, the author or authors of this
software dedicate any and all copyright interest in the software to the public
domain. We make this dedication for the benefit of the public at large and to
the detriment of our heirs and successors. We intend this dedication to be an
overt act of relinquishment in perpetuity of all present and future rights to
this software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF
CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>
