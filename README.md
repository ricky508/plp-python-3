# plp-python-3
Here’s a Python program that defines the `calculate_discount` function and uses it to calculate the final price based on user input:

```python
# Define the calculate_discount function
def calculate_discount(price, discount_percent):
    # Check if the discount is 20% or higher
    if discount_percent >= 20:
        # Apply the discount
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        # No discount applied
        return price

# Prompt the user for the original price and discount percentage
original_price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage: "))

# Calculate the final price using the calculate_discount function
final_price = calculate_discount(original_price, discount_percent)

# Print the result
if final_price == original_price:
    print(f"No discount applied. The price is {original_price:.2f}.")
else:
    print(f"After applying a {discount_percent}% discount, the final price is {final_price:.2f}.")
```

### Explanation:
1. **Function Definition**: 
   - `calculate_discount(price, discount_percent)` checks if the discount percentage is 20% or higher. If so, it applies the discount and returns the final price. Otherwise, it returns the original price.
2. **User Input**: The program prompts the user to enter the original price and the discount percentage.
3. **Final Price Calculation**: The program calls `calculate_discount` to calculate the final price and prints the result.

### Example Output:
```
Enter the original price of the item: 100
Enter the discount percentage: 25
After applying a 25.0% discount, the final price is 75.00.
```

If the discount is below 20%, the output will be:
```
Enter the original price of the item: 100
Enter the discount percentage: 10
No discount applied. The price is 100.00.
```
