# CSS Flexbox Uneven Shrinking Bug

This repository demonstrates a common yet subtle bug in CSS Flexbox layouts related to uneven shrinking of flex items when the screen size is reduced. The issue stems from the default behavior of `flex-shrink` and how it interacts with varying content widths.

## Bug Description

The provided `bug.css` file contains a flexbox container with several items. While the layout appears correct on larger screens, when the screen is resized, the items shrink unevenly due to differences in their content widths. This is because the default `flex-shrink` value (1) allows items to shrink proportionally to their initial size, leading to uneven distribution of space.

## Solution

The `bugSolution.css` file provides a fix. By explicitly setting `flex-shrink` to `0` on the `.item` class, we prevent the items from shrinking. The flex container will then distribute available space evenly, ensuring a more consistent and responsive layout. 

## How to Reproduce

1. Clone the repository.
2. Open `bug.html` (which will use `bug.css`) in your browser. Note the uneven shrinking of boxes when resizing the browser window.
3. Open `bugSolution.html` (which uses `bugSolution.css`) in your browser and observe the even distribution of space.

## Additional Notes

Understanding `flex-shrink` is crucial for building robust and predictable responsive layouts using Flexbox. It's important to consider how this property interacts with content widths and use it strategically to achieve the desired behavior.