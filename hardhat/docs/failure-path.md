# Failure Path Notes

I also followed the failure path separately.

A failed external read should not automatically become a NO.

There are several possible failure points:

- the external request can fail
- the response can be unusable
- the expected value may not be decoded
- the executor can fail

The market therefore needs to distinguish:

"the observed value says NO"

from:

"there was no usable observed value"

The second case can eventually lead to Invalid after the
available attempts are exhausted.

That was easier to understand once I stopped thinking of
Invalid as another prediction result.
