



# Choosing a Decline Type

You can choose the type of decline represented in your data in two ways:
You can choose it manually, or you can have
Value
Navigator automatically select it based on which type is most
appropriate for the well. The decline equations are based on the Arps
Equation.

See [Effective and Nominal Rates](Effective%20and%20Nominal%20Rates.md) for converting the
nominal decline to the effective decline.

## Arps Equation

ai/qin = (dq/dt)qt(n+1)  q = producing day rate

                a = nominal decline (frac/year)

                d = effective decline (frac/year)

                t = time (years)

                Np = cumulative volume

Subscripts           i =initial

                           t = at time t

                           f = at final

There are three types of declines in
Value
Navigator:

## Exponential (n = 0)

qt = qi\*exp(-at)                                        Straight line
plot: ln&#123;rate&#125; vs. time

Npt = 365.25\*((qi-qt)/a)                           Straight line plot:
Rate vs. Cum

d = 1-exp(-a)

a = -ln(1-d)

## Harmonic (n = 1)

qt = qi/(1+ai\*t)                                           No straight
line plot

Npt = 365.25\*((qi/ai)\*ln(qi)/qt)                 Straight line plot:
ln(rate)vs. cum

dt = at/(1+at)

at = dt/(1-dt)    

## Hyperbolic (-4 \
