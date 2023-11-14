# Overview

Adds the input into a list of banned words for the game. When a player attempts to send a message containing banned words, the banned words will be replaced. Each game starts with preset banned words which cannot be edited. It supports a single word as well as a string with multiple comma-separated words.

## Example

List of banned words:

- Bad
- Word

The above list can be achieved through individually adding words, or with a comma-separated string, like "Bad, Word"

Player Input: "Hello there!"
Output: "Hello there!"

Player Input: "This is a bad word!"
Output: "This is a *** ****!"
