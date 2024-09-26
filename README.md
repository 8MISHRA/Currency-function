# Currency Exchange Module

This Python module provides functions for currency conversion using real-time data from an online currency service. The primary functionality is to convert one currency to another based on the amount specified by the user. The module uses string parsing and JSON handling to extract and process data for currency exchange.

## Features

- **Real-time currency exchange** using an online API.
- **String parsing utilities** for handling JSON responses and extracting relevant currency data.
- **Error detection** for invalid currency codes or amounts.

## Functions

### `exchange(old, new, amt)`
- Converts an amount `amt` of currency `old` to currency `new`.
- Returns the converted amount.
- Example:
  ```python
  exchange('USD', 'INR', 100) # Returns amount in INR for 100 USD
  ```

### `is_currency(code)`
- Checks if a given currency code is valid.
- Returns `True` if the code is valid, `False` otherwise.

### `query_website(old, new, amt)`
- Sends a request to the API for converting `amt` of `old` currency to `new`.
- Returns the JSON response.

### Helper Functions
- **`before_space(s)`**: Extracts the substring before the first space.
- **`after_space(s)`**: Extracts the substring after the first space.
- **`first_inside_quotes(s)`**: Retrieves the first substring inside double quotes.
- **`get_lhs(json)`**: Extracts the left-hand side (original currency amount) from the JSON response.
- **`get_rhs(json)`**: Extracts the right-hand side (converted currency amount) from the JSON response.
- **`has_error(json)`**: Checks if the JSON response contains an error message.

## Usage Example

```python
# Convert 100 USD to INR
amount_in_inr = exchange('USD', 'INR', 100)
print(amount_in_inr)
```

## Author
Divyansh Mishra

## Date
30/11/2022

---

This module is designed to be simple and easy to use for anyone interested in performing real-time currency conversions in Python.
