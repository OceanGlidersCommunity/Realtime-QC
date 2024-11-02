= Tests

== Global Range

== Gradient

[stem]
++++
X_i = \left| V_i - \frac{V_{i+1} + V_{i-1}}{2} \right|
++++

== Spike

The spike check was first proposed in GTSPP:1990 and defined as:

[stem]
++++
X_i = \left| V_i - \frac{V_{i+1} + V_{i-1}}{2} \right| - \left| \frac{V_{i-1} - V_{i+1}}{2} \right|,
++++

where $i$ is the time index, i.e. it assumed the data $V$ was sorted by time.
This check is largely used without any modification.

== Digit Rollover

[stem]
++++
X_i = V_i - V_{i-1}
++++

== Spike - Median

Proposed at <<BGC_nitrate>>

[stem]
++++
X_i = \left| V_i - median(V_{i-2}, V_{i-1}, V_i, V_{i+1}, V_{i+2}) \right|
++++
