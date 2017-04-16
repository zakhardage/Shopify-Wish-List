Shopify-Wish-List
=================

non-app wish list using customer.tags

[NOTE] 
*February 6, 2017 Shopify updated customer forms: "Customers submitting a contact form or signing up for a mailing list more than once in a 24 hour period need to complete a captcha to verify that they’re human."*

*This update breaks the wishlist functionality. You can contact support and request they update your store ("it's actually a tag that has to be added on the back end") to remove the captcha functionality. Of course, this makes your shop vulnerable to spam.*

---

To make this wish list work, you'll need to add an include tag for wishlist-product.liquid in your product template -- make sure that it is not within the add-to-cart form. And you'll need to add a collection template for collection.wishlist.liquid.

There's no in-line styling so this should pick up your product and page template styling.

The wish list works by adding the product id to the customers account tags. To remove the item, another tag is added 
with an "x" preceding the product id. Re-adding the item to the wish list adds another "x". At this point there are 
three tags for the one product. If a customer went crazy with the wish list, adding and removing and re-adding 
products, it could fill up their customer tags quickly. If there's any issue with their account or interference 
with an app (like a wholesale app), I'd look first to their tags.

For a version that works with variants, check out Jim's version here: https://github.com/jimlakey/Shopify-Wish-List

*Note on limitations from one user:*<br />
"So I've been testing my wishlist function for months now and I've run into a wall because of the # of tags used for one user. Any account page that I tried to access for that user was not accessible and I got the following error message 'liquid error: memory limits exceeded'."
