# Resolution Flow Notes

I followed the resolution path separately from the betting
logic.

The sequence I wrote down was:

1. The market is created.
2. A resolve block is selected.
3. The Scheduler triggers the callback.
4. The contract chooses an HTTP-capable executor.
5. The HTTP precompile reads the oracle endpoint.
6. The jq precompile extracts the value.
7. The value is compared with the target.
8. The market is resolved or marked invalid.

The important thing I noticed is that these are different
responsibilities.

The Scheduler does not decide YES or NO.

The HTTP request does not decide YES or NO.

The jq step only extracts the value.

The comparison is what turns the observed value into the
market result.

That separation made the contract easier for me to follow.
