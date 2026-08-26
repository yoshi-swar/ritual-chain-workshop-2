# Resolution Checklist

When reading the resolution code, these are the questions I
use now.

## Before resolution

Is the market still open?

Has the scheduled block been reached?

## During external execution

Was an executor selected?

Did the HTTP request produce usable data?

Can jq extract the expected value?

## During settlement

Can the observed value be compared with the target?

Should the market become YES or NO?

## If something fails

Should the attempt be retried?

If all attempts fail, should the market become Invalid?

This checklist is mainly for navigating the code. It is not
another implementation of the resolution mechanism.
