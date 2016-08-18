# SHOPIFY COLLECTIONS

## How to add collection and maintain the modified look and feel
Basically you follow the same process for any Shopify template to add collections.

The real trick is that we have modified the original template to display an image collection for certain collections and made some changes to the look and feel to persist the same look and feel

### Before starting

#### Installing ShopifyFD chrome extension
Make sure you have installed the [ShopifyFD chrome extension](http://shopifyfd.com/), otherwise it will never work.

#### Understanding Metafields in Shopify
If you want to know how [Metafields](https://help.shopify.com/themes/liquid/objects/metafield) work the basic documentation is there. Nothing really groundbreaking, it's just a way to create a Map data structure an easily access it from the products pages in liquid.

### Let's talk about displaying *All Products* collection
This is an special collection that we have created to display all the products available in our site. Since we don't want to display an image for this collection because in reality doesn't have its own identity, we have added some metadata code to indicate that we should not be doing displaying an image for this collection. The way this collection is the following.

* Click Add Collection
* Populate the normal information for that product
* Click the ShopifyFD chrome extension icon
* Another Metafield's screen will appear, add the following metadata
```
collection_slideshow
collection_display_image
0
```
* Save as Integer
* Add another one for the title
```
collection_slideshow
collection_display_title
Products
```
* Save (Not Save as Integer)
* Click the blue Shopify button Save to persist your changes.

### Let's talk about displaying a *normal* collection
We have modify the template to display an image to represent the collection and we have to indicate that we want to display it. In order to do this we will do the following:

* Click Add Collection
* Populate the normal information for that product
* Click the ShopifyFD chrome extension icon
* Another Metafield's screen will appear, add the following metadata
```
collection_slideshow
collection_display_image
1
```
* Save as Integer
* Add another one for the title
```
collection_slideshow
collection_display_title
Tech Fitness
```
* Save (Not Save as Integer)
* Add another to indicate the image that you will display for that collection
```
collection_slideshow
collection_display_image_name
collection_slideshow_tech-fitness.jpg
```
* Save (Not Save as Integer)
* Click the blue Shopify button Save to persist your changes.

#### Let's upload the image for the collection
Nothing complicated, you just need to provide an image with specific size and follow the process:

* Create an image to represent your collection with size 1280 X 450px in Canva
* Download as jpeg and rename it to something similar to collection_slideshow_tech-fitness.jpg
* Edit HTML/CSS in Shopify
* Click the Assets folder
* Upload the image that you just created
