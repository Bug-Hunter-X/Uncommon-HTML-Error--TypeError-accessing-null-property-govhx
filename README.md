# Uncommon HTML Error: TypeError when accessing null element

This repository demonstrates a common yet easily overlooked error in HTML/JavaScript interaction.  The error arises from attempting to manipulate a DOM element that doesn't exist yet.

## The Bug

The `bug.html` file contains a simple HTML structure with a script that tries to update the `innerHTML` of a div element. However, there is no element with the id "myDiv" created in the HTML.  This leads to a `TypeError` because `document.getElementById("myDiv")` returns `null`, and you cannot access properties of `null`.

## The Solution

The `bugSolution.html` demonstrates the correct approach.  It ensures that the element exists before attempting to manipulate its properties.

This is a crucial detail to watch out for when dealing with asynchronous operations or dynamically generated elements.