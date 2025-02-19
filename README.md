# Tailwind CSS Responsive Class Conflicts

This repository demonstrates a common but subtle bug in Tailwind CSS related to responsive class conflicts.  The bug occurs when applying multiple responsive classes to a single element, resulting in unexpected styles depending on the screen size.

## Bug Description
The core issue is the unintended precedence of responsive classes.  When multiple classes are applied, the order and specificity of Tailwind's responsive modifiers (e.g., `md:`, `lg:`, `sm:`) can cause the wrong styles to be applied.  This is particularly difficult to debug because it's not always obvious which class is overriding another.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Resize the browser window. Observe how the element's styling changes unexpectedly.

## Solution
The solution involves carefully considering the order and specificity of responsive classes.  Using Tailwind's `@apply` directive or carefully restructuring the CSS can resolve these conflicts.