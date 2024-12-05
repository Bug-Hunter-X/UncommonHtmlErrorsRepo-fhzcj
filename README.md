# Uncommon HTML Error: Accessing Non-Existent Element Property

This repository demonstrates a subtle error in HTML that can be challenging to debug. The error occurs when trying to access a property of an HTML element that either does not exist or is not yet available in the DOM when the script attempts to access it.

## The Bug

The `bug.html` file contains a script that attempts to access a non-existent property `nonExistentProperty` of the `myDiv` element. This results in a `TypeError`.  A similar error can occur if you try to access an element before the browser has fully parsed and rendered it. 

## The Solution

The `bugSolution.html` file shows how to fix this issue:

1. **Verify Element Existence:** Before attempting to access any property, ensure the element exists and is fully loaded. You can use `document.getElementById()` to get a reference to the element, and check if it's not null.
2. **Check Property Existence:**  After getting a reference to the element, check if the property exists before attempting to use it.  
3. **Event Listeners:** For dynamic elements, attach event listeners (like `DOMContentLoaded`) to ensure your script runs only after the page's content is loaded.

By using these techniques, you can prevent this error and improve the robustness of your HTML code.