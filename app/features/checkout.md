# Feature: Checkout

## Overview
Registered users with items in their cart can complete a purchase.

## Steps

### Step 1 — Review Order
- User sees a summary: items, quantities, subtotal, estimated shipping
- Can return to cart to make changes

### Step 2 — Shipping Details
- User enters: full name, address line 1, address line 2 (optional), city, postcode, country
- All fields except address line 2 are required

### Step 3 — Payment
- Accepted: Visa, Mastercard, PayPal
- User enters card details (number, expiry, CVV) or selects PayPal
- Card number is validated with Luhn algorithm
- CVV is 3 digits (4 for Amex, but Amex is not supported)

### Step 4 — Confirmation
- Order is placed, user sees confirmation page with order number
- Confirmation email is sent to registered email address

### Error States
- Invalid card number: "Please check your card number"
- Expired card: "This card has expired"
- Payment declined: "Payment was declined. Please try another method."

## Out of Scope
- Discount codes (coming in v2)
- Gift wrapping
