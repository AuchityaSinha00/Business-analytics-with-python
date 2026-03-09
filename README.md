'''Task1: Sales Data Summary'''

#assign the number of units sold to variables
CategoryA = 150
CategoryB = 200

# Calculate total units sold
Total_units = CategoryA + CategoryB

#calculate the difference between the categories
difference = abs(CategoryA - CategoryB)

#Ratio of Category A to Category B
ratio = CategoryA/CategoryB

#Print results already
print("Sale Data Summary:")
print("Total Units Sold:", Total_units)
print("Difference Between Categories:", difference)
print("Ratio of Category A to Category B", round(ratio,2))

'''Task2: Customer Age Data'''
#Store customer's name and age

customer_name = "John Doe"
customer_age = 30

#Create personalised marketing message using if-else
if customer_age >=30:
    message = f"Dear {customer_name}, at {customer_age}, you're eligible for our premium loyalty program."
else:
    message = f"Dear {customer_name}, at {customer_age}, you're not eligible for our premium loyalty program."

print(message)

'''Task3: Product List Management'''
#Given product prices
product_prices = [10, 20, 50, 120, 80, 450, 320]
premium_product_price = 250

#Find the highest and lowest prices
highest_price = max(product_prices)
lowest_price = min(product_prices)

mid_range_products = product_prices.copy()

# Create a new list with mid range-product prices (exclude highest and lowest)
mid_range_products.remove(highest_price)
mid_range_products.remove(lowest_price)

product_prices.append(premium_product_price)
print("Highest Price:", highest_price)
print("Lowest Price:", lowest_price)
print("Mid Range Products:",mid_range_products)
print("Updated List with Premium Price:", product_prices)

'''Task 4: Inventory Lookup'''
#Create a dictionary with product details
product = {
    "product_name": "Wireless Mouse",
    "SKU": "WM12345",
    "price": 799,
    "Category": "Electronics"
}

# Simulating a query from customer service

print("Product Name:", product["product_name"])
print("SKU:", product["SKU"])

'''Task5: Stock Level Alert System'''

#Take Stock level as input
stock_level = int(input("Enter stock level:"))

#set threshold
Threshold = 20

#check stock against threshold

if stock_level < Threshold:
    print("Reorder Now")
else:
    print("Stock is sufficient")

'''Task6: Sales Report Formatting'''
products_sold = ["laptop", "mouse", "keyboard","monitor","printer"]

print("----Using for Loop----")
for i in products_sold:
    print(i.upper())

print("\n---Using while loop---")
i = 0
while i < len(products_sold):
    print(products_sold[i].upper())
    i += 1

''' Task 7: Area Calculation for Store Layout '''

# Function to calculate area
def calculate_area(length, width):
    return length * width

# Main function
def main():
    length1, width1 = 20, 15
    length2, width2 = 30, 10
    length3, width3 = 25, 12

    print(f"The area of section 1 is {calculate_area(length1, width1)} square meters.")
    print(f"The area of section 2 is {calculate_area(length2, width2)} square meters.")
    print(f"The area of section 3 is {calculate_area(length3, width3)} square meters.")

# Run the program
main()

''' Task 8: Customer Feedback Analysis '''

# Sample customer feedback
feedback = "The service was excellent and very quick!"

# Count the number of vowels
vowels = "aeiouAEIOU"
vowel_count = sum(1 for char in feedback if char in vowels)

# Reverse the feedback
reversed_feedback = feedback[::-1]

# Print the results
print("Customer Feedback Analysis:")
print("Original Feedback:", feedback)
print("Number of Vowels:", vowel_count)
print("Reversed Feedback:", reversed_feedback)

# Task 9: Price Filtering Tool

# Given product prices
product_prices = [150, 85, 300, 120, 45, 200]

# Discount threshold
threshold = 100

# Filter out products below the threshold
eligible_products = [i for i in product_prices if i < threshold]

# Print result
print("Products eligible for the discount campaign:", eligible_products)


# Task 10: Daily Sales Average

# Sales figures for the past 7 days
daily_sales = [1200, 1500, 1100, 1800, 1700, 1600, 1400]

# Calculate average sales
average_sales = sum(daily_sales) / len(daily_sales)

# Print result with 2 decimal places
print(f"Average Daily Sales for the Past Week: $",average_sales)

# Task 11: Customer Segmentation

# Customer spending amounts
customer_spendings = [200, 800, 1500, 3000, 450, 1200]

print("Customer Segmentation Results:")

# Loop through each spending amount
for spending in customer_spendings:
    if spending < 500:
        category = "Low"
    elif 500 <= spending < 1500:
        category = "Medium"
    else:  # spending >= 1500
        category = "High"
    
    print(f"Customer Spending: ${spending} → Category: {category}")

# Task 12: Discount Calculation

# Function to calculate final price after discount
def calculate_discounted_price(original_price, discount_percentage):
    discount_amount = (discount_percentage / 100) * original_price
    final_price = original_price - discount_amount
    return final_price

# List of products
products = [
    {"name": "Product A", "original_price": 100, "discount_percentage": 10},
    {"name": "Product B", "original_price": 250, "discount_percentage": 20},
    {"name": "Product C", "original_price": 75,  "discount_percentage": 15},
    {"name": "Product D", "original_price": 150, "discount_percentage": 5}
]

# Loop through products and print final prices
print("Discounted Prices:")
for product in products:
    final_price = calculate_discounted_price(product["original_price"], product["discount_percentage"])
    print(f"{product['name']} → Original: ${product['original_price']}, Discount: {product['discount_percentage']}%, Final Price: ${final_price:.2f}")

# Task 13: Customer Feedback Sentiment Analysis

# Sample customer feedback
feedback = "I am very happy with the service. It was a good experience!"

# Define positive and negative word lists
positive_words = ["good", "happy", "excellent", "great"]
negative_words = ["bad", "disappointed", "poor", "terrible"]

# Convert feedback to lowercase for easy matching
feedback_lower = feedback.lower()

# Check for sentiment
sentiment = "Neutral"  # default

for i in positive_words:
    if i in feedback_lower:
        sentiment = "Positive"
        break

for i in negative_words:
    if i in feedback_lower:
        sentiment = "Negative"
        break

# Print the results
print("Customer Feedback:", feedback)
print("Sentiment:", sentiment)

# Task 14: Employee Salary Increment Calculator

# Employee data with current salary and rating
employees = {
    "Alice": {"current_salary": 50000, "rating": "Excellent"},
    "Bob": {"current_salary": 40000, "rating": "Good"},
    "Charlie": {"current_salary": 45000, "rating": "Average"},
    "David": {"current_salary": 35000, "rating": "Poor"}
}

# Increment percentages based on performance rating
increments = {
    "Excellent": 20,
    "Good": 15,
    "Average": 10,
    "Poor": 5
}

print("Updated Employee Salaries:")

# Loop through each employee
for name, details in employees.items():
    salary = details["current_salary"]
    rating = details["rating"]
    increment_percentage = increments[rating]  # lookup from increments dictionary
    
    # Calculate increment
    increment_amount = (increment_percentage / 100) * salary
    new_salary = salary + increment_amount
    
    # Print result
    print(f"{name} → Rating: {rating}, Old Salary: ${salary}, Increment: {increment_percentage}%, New Salary: ${new_salary:.2f}")
