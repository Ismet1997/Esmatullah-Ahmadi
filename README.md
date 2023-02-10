class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price

    def display_product(self):
        print("Name:", self.name)
        print("Price:", self.price)


class ShoppingCart:
    def __init__(self):
        self.products = []

    def add_product(self, product):
        self.products.append(product)

    def display_cart(self):
        print("Shopping Cart:")
        for product in self.products:
            product.display_product()
        print("Total:", self.get_total())

    def get_total(self):
        total = 0
        for product in self.products:
            total += product.price
        return total


# Create some products
product1 = Product("Apple", 0.99)
product2 = Product("Banana", 0.69)
product3 = Product("Cherries", 4.99)

# Create a shopping cart and add products to it
shopping_cart = ShoppingCart()
shopping_cart.add_product(product1)
shopping_cart.add_product(product2)
shopping_cart.add_product(product3)

# Display the shopping cart
shopping_cart.display_cart()
