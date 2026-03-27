# Feature: Add to Cart

## Overview
Registered users can add products to a shopping cart.

## Behaviour

### Adding Items
- Each product page has an "Add to Cart" button
- Clicking it adds 1 unit to the cart
- A confirmation message appears: "Item added to your cart!"
- The cart icon in the header updates to show the number of items

### Quantity
- Users can change quantity on the cart page (min: 1, max: 99)
- Changing quantity updates the subtotal automatically

### Removing Items
- Each item in the cart has a "Remove" button
- Clicking it removes that item and updates the total

### Guest Users
- Guests see an "Add to Cart" button but clicking it shows: "Please log in to add items to your cart"

### Persistence
- Cart contents are saved for 7 days even if the user logs out
