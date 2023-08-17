# JSON
## Introduction
JSON is a standardized format for structuring data. It is heavily based on the syntax for JavaScript objects. You will often encounter JSON formatted data when working with external server APIs - it is essentially the universal format for transmitting data on the web.

## Working with JSON 
JSON is a standard text-based format for representing data based on JavaScript object syntax. It is commonly used for transmitting data in web apps. 

## What is JSON? 
JSON is a text-based data format following JavaScript object syntax. Even though it closely resembles JavaScript object literal syntax, it can be used independently from JavaScript, and many programming environment feature the ability to read and generate JSON. 

JSON exists as a string -- useful when you want to transmit data across a network. It needs to be converted to a native JavaScript object when you want to access data. This is not a big issue -- JavaScript provides a global JSON object that has methods available for converting between the two. 

A JSON string can be stored in its own file, which is basically just a text file with an extension of  `.json` 

### JSON structure
JSON is a string whose format very much resembles JavaScript object literal format. You can include the same basic data types inside JSON as you can in a standard JavaScript object -- strings, numbers, arrays, booleans, and other object literals. This allows you to construct a data hierarchy.

### Other notes
- JSON is purely a string with a specified data format -- it contains only properties, not methods
- JSON requires double quotes to be used around strings and property names. Single quotes are not valid other than surrounding the entire JSON string.
- Even a single misplaced comma or colon can cause a JSON file to go wrong, and not work. You should be careful to validate any data you are attempting to use (although computer-generated JSON is less likely to include errors). 
- JSON can actually take the form of any data type that is valid for inclusion inside JSON, not just arrays or objects. So, for example, a single string or number would be valid JSON
- Unlike in JavaScript code in which object properties may be unquoted, in JSON only quoted strings may be used as properties. 