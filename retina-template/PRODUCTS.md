# SHOPIFY PRODUCTS

## How to add products and maintain the modified look and feel
Basically you follow the same process for any Shopify template to add products.

The real trick is that we have modified the original template to display currencies, show a different button for external websites and add the original reviewer of the website.

### Before starting

#### Installing ShopifyFD chrome extension
Make sure you have installed the [ShopifyFD chrome extension](http://shopifyfd.com/), otherwise it will never work.

#### Understanding Metafields in Shopify
If you want to know how [Metafields](https://help.shopify.com/themes/liquid/objects/metafield) work the basic documentation is there. Nothing really groundbreaking, it's just a way to create a Map data structure an easily access it from the products pages in liquid.

### Modifying the Buy button
Everything has been implemented when you are creating/modifying your products. What you have to do is:

* Click Add product
* Populate the normal information for that product
* Click the ShopifyFD chrome extension icon
* Another Metafield's screen will appear, add the following metadata
```
productBuyButton
metadataBuyButtonFieldName
Buy Now Via Official Website
```
* Save (Not Save as Integer)
* Add another one
```
productBuyButton
metadataBuyButtonFieldValue
http://i-aurai.com/
```
* Save (Not Save as Integer)
* Click the blue Shopify button Save to persist your changes.

### Modifying the currency
Follow the above steps for the following metadata:

```
product_currency
product_currency_display
USD
```

### Modifying the product review
Follow the above steps for the following metadata:

```
product_review
product_review_by
GadgetFlow
```
```
product_review
product_review_by_url
http://thegadgetflow.com/
```

#### Let's upload the image for the product review
Nothing complicated, but you need to be aware of uploading an image that will go to the thumbnail of the reviewer. Follow the steps:

* Create an image to represent your reviewer with size 96 X 96px in Canva. If it's a company google the image and get the one with the best quality and size.
* Download as jpeg and rename it to something similar to Gadget-flow-logo-avatar.jpg
* Edit HTML/CSS in Shopify
* Click the Assets folder
* Upload the image that you just created
