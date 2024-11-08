# PLP-Python-Control-flows-and-functions-week-three-assignment
Create a function named calculate_discount(price, discount_percent) that calculates the final price after applying a discount. The function should take the original price (price) and the discount percentage (discount_percent) as parameters. If the discount is 20% or higher, apply the discount; otherwise, return the original price.
Using the calculate_discount function, prompt the user to enter the original price of an item and the discount percentage. Print the final price after applying the discount, or if no discount was applied, print the original price.

#Create a function named calculate_discount(price, discount_percent) that 
#The function should take the original price (price) and the discount percentage (discount_percent) as parameters. 
def calculate_discount(price,discount_percent):
#calculates the final price after applying a discount. 
    if discount_percent >= 20 :
     # Calculate the discounted price
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
# If the discount is less than 20%, return the original price
        return price

#Using the calculate_discount function, 
# prompt the user to enter the original price of an item and the discount percentage. 
# Print the final price after applying the discount, or if no discount was applied, print the original price.
price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage: "))

# Calculate the final price using the function
final_price = calculate_discount(price, discount_percent)

if final_price != price:
    print(f"The final price after applying the discount is: ${final_price:.2f}")
else:
    print(f"No discount applied. The original price is: ${final_price:.2f}")
