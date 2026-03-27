# Feature: Product Search

## Overview
Users can search for products using a search bar at the top of every page.

## Behaviour

### Happy Path
- User types a search term and presses Enter or clicks the search icon
- Results page shows all matching products
- Results are sorted by relevance by default
- Each result shows: product image, name, price, and star rating

### Filtering
- Users can filter results by: category, price range, rating
- Filters can be combined
- Applying a filter updates results without a full page reload

### No Results
- If no products match, show: "No results for '[search term]'. Try a different keyword."
- Suggest 3 popular products below the message

### Edge Cases (to be defined)
- Behaviour for very long search strings
- Behaviour for special characters
- Behaviour for search terms in other languages
