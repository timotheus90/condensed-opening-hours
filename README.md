# Coding Challenge: Simplify Business Hours

## Problem Description

Your task is to write a function that simplifies the business hours of a store. You will be provided with an array of JSON objects representing the hours of operation for each day of the week. Your function should return a string that represents the simplified version of the business hours.

### Input Format

You will receive an array of objects. Each object contains:
- `dayOfWeek`: The day of the week as a string (e.g., "Montag", "Dienstag", etc.)
- `from`: The opening time of the store in `HH:MM:SS` format
- `to`: The closing time of the store in `HH:MM:SS` format

```json
[
  {"dayOfWeek": "Montag", "from": "07:00:00", "to": "22:00:00"},
  {"dayOfWeek": "Dienstag", "from": "07:00:00", "to": "22:00:00"},
  ...
]
```

### Output Format

Your function should return a string that condenses the business hours into a simplified representation.

```text
"Mo-Fr 07:00 - 22:00, Sa 11:00 - 17:00"
```

## Constraints

- The days will be sorted in the order: Montag, Dienstag, ..., Sonntag.
- The time will be in 24-hour format.
  
## Examples

### Example 1

#### Input

```go
	data := `[{"dayOfWeek": "Montag", "from": "10:00:00", "to": "20:00:00"},
	          {"dayOfWeek": "Dienstag", "from": "10:00:00", "to": "20:00:00"},
	          {"dayOfWeek": "Mittwoch", "from": "09:00:00", "to": "18:00:00"},
	          {"dayOfWeek": "Donnerstag", "from": "09:00:00", "to": "18:00:00"},
	          {"dayOfWeek": "Freitag", "from": "09:00:00", "to": "14:00:00"},
	          {"dayOfWeek": "Samstag", "from": "09:00:00", "to": "14:00:00"},
	          {"dayOfWeek": "Sonntag", "from": "09:00:00", "to": "14:00:00"}]`

```

#### Output

```text
"Mo-Sa 07:00 - 22:00, So 11:00 - 17:00"
```

## Tips 🚀

- Consider using a loop to iterate through the days and group the ones with the same business hours.
- Keep track of sequences (consecutive days with the same hours) to simplify the output.

## Evaluation Criteria 🌟

- Correctness: Does the code perform as required?
- Readability: Is the code easy to follow?
- Simplicity: Is the code straightforward and concise?

Good luck and happy coding! 🎉
