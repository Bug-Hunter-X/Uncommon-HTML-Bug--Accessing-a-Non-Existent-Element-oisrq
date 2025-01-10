# Uncommon HTML Bug: Accessing a Non-Existent Element

This repository demonstrates an uncommon HTML bug that arises from attempting to access and modify the content of a DOM element that doesn't exist yet.  This can lead to unexpected behavior or silent failures.

## The Bug

The `bug.html` file contains a script that tries to set the `textContent` of an element with the ID 'nonExistentElement'. Since this element is not defined in the HTML, the script will fail.  The failure mode depends on the browser's JavaScript engine; in strict mode, it'll likely throw an error; in non-strict mode, it might fail silently.

## The Solution

The `bugSolution.html` file provides a solution by checking if the element exists before attempting to modify its content. This approach makes the code more robust and prevents unexpected errors.