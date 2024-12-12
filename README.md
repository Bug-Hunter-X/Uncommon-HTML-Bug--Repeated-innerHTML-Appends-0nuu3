# Uncommon HTML Bug: Repeated innerHTML Appends

This repository demonstrates a subtle but uncommon bug related to repeatedly using `innerHTML` to append content to the DOM in HTML.  While seemingly simple, this approach can lead to unexpected behavior and performance issues, especially with large amounts of data.

## The Bug
The `bug.html` file shows an example of this bug.  Notice how appending multiple elements using `innerHTML +=` can lead to loss of elements or unexpected behavior. This happens because `innerHTML` completely replaces the existing content within an element.

## The Solution
The solution provided in `bugSolution.html` demonstrates a better approach using `insertAdjacentHTML` which offers greater control and avoid unwanted behavior.   This method is generally preferred for appending elements dynamically.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in your web browser. Observe the outcome.
3. Open `bugSolution.html`. Observe that elements are appended correctly.

## Learning Points
* Avoid repeatedly using `innerHTML` for appending to the DOM. This can lead to performance issues and unexpected behavior.
* Use `insertAdjacentHTML`, `appendChild`, or other DOM manipulation methods for greater control and efficiency.
* Always prioritize better ways to update the DOM for better performance and avoiding unexpected results.