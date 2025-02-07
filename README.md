# Unresponsive Button Bug in HTML
This repository demonstrates a subtle bug in HTML where a button becomes unresponsive after its first click. The bug arises from the improper handling of an element's visibility state.

## Bug Description
The provided HTML code includes a button that hides a div element when clicked. However, the code lacks a check to handle the case when the div is already hidden. This results in the button failing to trigger any further action after the first click because the `display` style is already set to `none`, and thus trying to set it to `none` again has no visual effect and the function silently fails, leading to the user thinking the button is broken.

## Solution
The solution ensures that the button remains responsive even if the element is already hidden. This involves adding a conditional statement that checks the current display style of the div element before changing it.