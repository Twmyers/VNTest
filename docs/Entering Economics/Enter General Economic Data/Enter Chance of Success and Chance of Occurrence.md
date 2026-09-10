



# Enter Chance of Success and Chance of Occurrence

Chance of Success and Chance of Occurrence are entered on **Economics \|
General**.

Chance of Success (COS) is the confidence level that the well will
produce. It is a risk factor used to take the probability that the
entity will be successful into account in determining the expected
value. You can define which of your capital costs apply to the success
or failure case, or both (Common) in the Capital Cost header - Cost
Stream.

Chance of Occurrence is the chance that a project will proceed, and has
nothing to do with risk factors. It is used as a simple factor on the
expected value.

## Using Chance of Success

When you enter COS for a case, the costs are allocated for Canadian
Development Expenses (CDE) and Canadian Exploration Expenses (CEE) as
follows (using M\$100 and a COS @ 75%):

When COS is used for CDE costs, the common and success portions are
allocated to CDE, while the failure portion is allocated to CEE as
illustrated in Table 1.

| Cost (M\$100) | CDE | CEE |
|---------------|-----|-----|
| Common        | 75  | 25  |
| Success       | 75  | --  |
| Failure       | --  | 25  |

Table 1: Allocation of CDE Capital Costs

When you enter COS for CEE costs, the common, success, and failure
portions are allocated to CEE as illustrated in Table 2.

| Cost (M\$100) | CDE | CEE |
|---------------|-----|-----|
| Common        | --  | 100 |
| Success       | --  | 75  |
| Failure       | --  | 25  |

Table 2: Allocation of CEE Capital Costs

## Using Chance of Occurrence

When you use COO for CEE and CDE capital costs, only the success portion
of common or success costs is allocated to either category. Failure
portions or failure costs are not allocated to either category.

## Combining COO and COS

When you use COO and COS, the COS portion is calculated first and the
COO portion is calculated based on the COS value. The final amount is
then allocated to the CDE or CEE category as described in Tables 1 and 2
above.

Table 3 illustrates how a CDE capital cost of M\$100 would be allocated
with a COO of 75% and a COS of 75%.

| Cost (M\$100) |  CDE   |  CEE   |
|---------------|--------|--------|
| Common        |  56.25 |  18.75 |
| Success       |  56.25 |  --    |
| Failure       |  --    |  18.75 |

Table 3
