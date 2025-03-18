# python_discount-

def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount if it's 20% or higher.
    :param price: Original price of the item.
    :param discount_percent: Discount percentage to be applied.
    :return: Final price after applying the discount, or original price if discount is below 20%.
    """
    
    if discount_percent >= 20:
        return price - (price * discount_percent / 100)
    return price

# Prompt user for input
try:
    price = float(input("Enter the original price of the item: "))
    discount_percent = float(input("Enter the discount percentage: "))
    
    # Calculate and display final price
    final_price = calculate_discount(price, discount_percent)
    print(f"Final price: {final_price:.2f}")
except ValueError:
    print("Invalid input. Please enter numeric values.")
