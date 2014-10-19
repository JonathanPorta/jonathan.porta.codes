---
title: Random Thoughts on Implementing Transactions/Orders in a Shopping Cart
author: Jonathan
layout: post
permalink: /2013/10/21/random-thoughts-on-implementing-a-transactionsorders-in-a-shopping-cart/
categories:
  - Development
  - Web Application Development
---
How should one setup the relationship between an order/transaction, an immutable record of products at prices with payments, and products?

For example, products change over time. They may have a different price. They may be discontinued. How should the relationship between a completed transaction and a product be implemented in order to preserve the record of the sale while allowing the user to see product pages of products purchased in the past?

Obviously, it wouldn&#8217;t be ok for the price of a product to change on a past order, neither would it be acceptable for the product to disappear from the order because it was removed/discontinued from the rest of the site. Plus, if I am a customer, I would want to be able to click and look back at the product page in the future.

I suppose one method would be to store a denormalized dump of the transaction data, including the product id. Then when the user looks at a previous transaction, the product, the price and the payment information are there and I could link the product to the current product page via the id.

If the product was discontinued, the page would say so and direct the user to the replacement product, if any. If the price was different, the product page would just show the updated price.

I am sure there are other ways to tackle this problem, but I think this will work for now without limiting my options in the future if it needs to change.

If you have any ideas, that is, if anyone reads this, let me know in the comments!