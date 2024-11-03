---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
---

# Tests

## Global Range

## Gradient

```{math}
:label: gradient
  y_i = \left| x_i - \frac{x_{i+1} + x_{i-1}}{2} \right|
```

## Spike

The spike check was first proposed in {cite}`GTSPP:1990` and defined as:

```{math}
:label: spike
  y_i = \left| x_i - \frac{x_{i+1} + x_{i-1}}{2} \right| - \left| \frac{x_{i-1} - x_{i+1}}{2} \right|,
```

where $i$ is the time index, i.e. it assumed the data $x$ was sorted by time.
This check is largely used without any modification.

## Digit Rollover

```{math}
:label: digit_rollover
  y_i = x_i - x_{i-1}
```

## Spike - Median

Proposed by {cite}`johnson2021bgc`

```{math}
:label: spike-median
  y_i = \left| x_i - median(x_{i-2}, x_{i-1}, x_i, x_{i+1}, x_{i+2}) \right|
```
