# XSS Vulnerability in HTML using innerHTML

This repository demonstrates a common yet easily overlooked security vulnerability in HTML that arises from the improper use of `innerHTML`.  When `innerHTML` is used with untrusted user input, it creates a Cross-Site Scripting (XSS) vulnerability, allowing malicious code injection.

## The Problem

The `bug.html` file showcases a vulnerable code snippet.  A user is prompted to enter text, which is then directly inserted into the HTML using `innerHTML`.  A malicious user could enter JavaScript code, potentially stealing cookies, redirecting the user, or performing other harmful actions.

## The Solution

The `solution.html` file illustrates how to mitigate this vulnerability. Instead of directly using `innerHTML`, it demonstrates using `textContent`, which only sets the plain text content and avoids the XSS risk.