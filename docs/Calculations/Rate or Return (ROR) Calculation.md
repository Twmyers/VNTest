

# Rate or Return (ROR) Calculation

The Rate Of Return in
Value
Navigator is based on Internal Rate of Return calculations. The
maximum limit for ROR is 500%. In between 500 and 1000, the display is
"\&gt;500". N/A may appear if the ROR is negative, exceeds 1000%, or if
there are multiple calculations for ROR (BTCash flow changes signs too
many times). N/A in this case means that
Value
Navigator cannot calculate the ROR. You may see the N/A if the
case is using acceleration economics, or if the economic limit is not
enabled. You can look at the ROR as equivalent to the XIRR calculation
in Excel.

Value
Navigatoruses an iterative approach (a form of the standard
Newton's method) to solve for the ROR that returns a discounted NPV of
0. There are a few conditions that are used. 1. If the cash flow changes
sign more than once then multiple roots may exist -- depending on the
assumptions and specifics of the algorithm, different results may occur.
2. We calculate the ROR to a certain tolerance -- once our solution
finds that the ROR is changing by less than a certain amount between
iterations (0.005) we assume we have a solution. 3. If we haven't found
a solution after a certain number of iterations (25) we assume no
solution exists.

Value
Navigator discounts monthly, up until the last year that is
specified for monthly output in the Project Settings. So, we use the
mid-month calculation up to the last year for monthly output, then we
use the mid-year calculation.

Net Present Value Discounted mid-year:NPV = FV/(1 + i) ^ n - 0.5

Net Present Value Discount mid-month:NPV = FV/(1+ i) ^ ((n-0.5)/12)"
