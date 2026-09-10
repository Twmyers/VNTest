



# Calculate a 1+WOR Forecast

1+WOR forecasts are used to forecast oil production based on total fluid
production.

Once you have calculated the parameters, enter them in the
[Edit Decline Parameters on an Entity](Edit%20Decline%20Parameters%20on%20an%20Entity.md) on
**Predictions \| Declines**.

## Calculate 1+WOR Forecast Parameters

In the following example, you want to calculate the decline parameters
for a new well with the following values:

- Qi= 62.5 bbl/d
- Qf= 5 bbl/d
- Maximum pump capacity=250 bbl/d
- Oil Ultimate=67 000 bbl

To create the decline you must calculate the **Qi**, the **Qf**, and the
**Di**.

To calculate the Qi and Qf for a 1+WOR forecast

1+WOR= 1+inv (Qo/Qw)

If the Maximum pump capacity=250 bbl/d and the Qi=62.5 bbl/d, then:

1+WOR Qi           = 1+inv &#123;Initial oil rate / (Total fluid production
rate – Initial oil rate)&#125;

=1+inv &#123;62.5 / (250-62.5)&#125;

=1+inv (62.5 / 187.5)

= 1+inv (.333333)

= 1+3

= 4

**If the Qf= 5 bbl/d, then:**

1+WOR Qf           = 1+inv &#123;Final oil rate / (Total fluid production
rate – Final oil rate)&#125;

=1+inv &#123;5 / (250-5)&#125;

=1+inv (5 / 245)

= 1+inv (.020408)

= 1+49

= 50

To calculate the Di for a 1+WOR forecast:

Di            = ((ln (Initial 1+WOR) – ln (Final 1+WOR)) / -Oil
Ultimate) \*1000

= ((3.91-1.38) / -67000) \* 1000

= -0.0377612
