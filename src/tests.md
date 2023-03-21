# Tests

## Global Range

## Gradient

X_i = \left| V_i - \frac{V_{i+1} + V_{i-1}}{2} \right|

## Spike

X_i = \left| V_i - \frac{V_{i+1} + V_{i-1}}{2} \right| - \left| \frac{V_{i+1} - V_{i-1}}{2} \right|

## Digit Rollover

X_i = V_i - V_{i-1}

## Spike - Median

Proposed at <<BGC_nitrate>>

X_i = \left| V_2 - median(V_0, V_1, V_2, V_3, V_4, V_5) \right|
