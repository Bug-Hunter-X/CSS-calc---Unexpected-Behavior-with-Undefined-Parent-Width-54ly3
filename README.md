# CSS calc() Unexpected Behavior
This repository demonstrates an uncommon bug related to the `calc()` function in CSS. The issue arises when using `calc()` to calculate a dimension based on a percentage of the parent element's width, but the parent element's width is not explicitly defined. In such cases, the calculation may produce unexpected results, causing layout issues.

## Bug Description
The `calc()` function in CSS allows for dynamic calculations of lengths. However, when the parent element's width is not defined (set to `auto`), the calculation might not work as intended. This is because `calc()` depends on the context of the parent's width to perform its calculations. If the parent's width is not specified, it is implicitly determined, which can lead to unexpected results in `calc()` expressions.

## Solution
To fix this, explicitly define the width of the parent element. This ensures that the `calc()` function operates with a concrete value and produces the desired result.
