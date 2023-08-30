# phase-3-code-challenge2

Restaurant Review System
Overview
The Restaurant Review System is a Python-based application that allows customers to review restaurants and provides functionality for managing restaurant reviews. This system consists of three main classes: Review, Customer, and Restaurant. These classes facilitate the process of creating and managing restaurant reviews.

Table of Contents
Classes
Review
Customer
Restaurant
Example Usage
Getting Started
Contributing
License
Classes
#Review Class
The Review class represents a customer's review of a restaurant. It includes the customer who wrote the review, the restaurant being reviewed, and a rating.

Methods and Attributes:
__init__(self, customer, restaurant, rating): Initializes a new review instance with the customer, restaurant, and rating.
get_rating(self): Returns the rating of the review.
get_customer(self): Returns the customer who wrote the review.
get_restaurant(self): Returns the restaurant being reviewed.
@classmethod all(cls): Returns a list of all reviews.
#Customer Class
The Customer class represents a customer who can write reviews. It includes the customer's given name and family name.

Methods and Attributes:
__init__(self, given_name, family_name): Initializes a new customer instance with a given name and family name.
get_given_name(self): Returns the given name of the customer.
get_family_name(self): Returns the family name of the customer.
full_name(self): Returns the full name of the customer.
reviewed_restaurants(self): Returns a list of restaurants reviewed by the customer.
add_review(self, restaurant, rating): Adds a new review for a restaurant by the customer.
@classmethod all(cls): Returns a list of all customers.
#Restaurant Class
The Restaurant class represents a restaurant that can be reviewed. It includes the restaurant's name.

Methods and Attributes:
__init__(self, name): Initializes a new restaurant instance with a name.
get_name(self): Returns the name of the restaurant.
__str__(self): Provides a meaningful string representation of the restaurant (name).
reviews(self): Returns a list of reviews for the restaurant.
customers(self): Returns a list of customers who reviewed the restaurant.
average_star_rating(self): Calculates and returns the average star rating for the restaurant based on its reviews.
@classmethod find_by_name(cls, name): Finds a restaurant by its name and returns it.
@classmethod all(cls): Returns a list of all restaurants.
Example Usage
python
Copy code
# Create sample instances for testing
customer1 = Customer("John", "Doe")
restaurant1 = Restaurant("Burger King")
review1 = Review(customer1, restaurant1, 4)

# Test the methods
print(customer1.get_given_name())
print(customer1.get_family_name())
print(customer1.full_name())
print(restaurant1.get_name())
print(review1.get_rating())
print([review.get_restaurant().get_name() for review in Review.all()])
print(review1.get_customer().full_name())
print(review1.get_restaurant().get_name())
print([review.get_rating() for review in restaurant1.reviews()])
print([customer.full_name() for customer in restaurant1.customers()])
print(restaurant1.average_star_rating())
print(Restaurant.find_by_name("Burger King"))
print(restaurant1)  # This displays the restaurant name instead of the memory address
This code snippet demonstrates how to create instances of customers, restaurants, and reviews and how to use the methods provided by the classes.


#Contribution
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

Fork the repository.
Create a new branch for your feature: git checkout -b feature-name.
Make your changes and commit them: git commit -m 'Add new feature'.
Push your changes to your fork: git push origin feature-name.
Create a pull request.

#Author:MISRA ABDI

License
This project is licensed under the MIT License.

This README provides a detailed overview of the Restaurant Review System, including class descriptions, example usage, and instructions for getting started and contributing. It is designed to help you understand and use the code effectively, contributing to a better understanding and potentially a higher grade.
