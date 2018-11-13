# 9.10-intro-to-programming
# write this on the 3rd line... class ItemToPurchase:

    def __init__(self):
        self.item_name = "none"
        self.item_price = 0
        self.item_quantity = 0
    def print_item_cost(self):
        cost = self.item_price * self.item_quantity
        print("%s %0.0f @ $%d = $%0.0f" %(self.item_name, self.item_quantity, self.item_price, cost))
        

if __name__ == "__main__":
    print("Item 1")
    first_item = input("Enter the item name:\n")
    price1 = float(input("Enter the item price:\n"))
    quantity1 = int(input("Enter the item quantity:\n\n"))
    print("Item 2")
    second_item = input("Enter the item name:\n")
    price2 = float(input("Enter the item price:\n"))
    quantity2 = int(input("Enter the item quantity:\n\n"))
    
    item1 = ItemToPurchase()
    item1.item_name = first_item
    item1.item_price = price1
    item1.item_quantity = quantity1
    item2 = ItemToPurchase()
    item2.item_name = second_item
    item2.item_price = price2
    item2.item_quantity = quantity2

    print("TOTAL COST")
    item1.print_item_cost()
    item2.print_item_cost()
    total_cost =  ((price1 * quantity1) + (price2 * quantity2))
    print("\nTotal: $%0.0f" %(total_cost))
