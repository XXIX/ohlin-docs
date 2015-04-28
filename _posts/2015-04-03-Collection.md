Due to restrictions with Shopify Collections, in order to customise the look and feel for each Collection we match a Product to the Collection (what we refer to as a Collection Product) and use the Collection Product attributes to customise the look and feel of the Collection.

## IMPORTANT

The Collection Product must be the first Product in the Collection.

### Creating a new Collection and Collection Product
1. Create a Collection
2. Take note of the handle e.g. `f-w-2014`
3. Save the Collection
4. Create a Product
5. Ensure the Product has the same handle as the Collection e.g. `f-w-2014`
6. Set the template of the Product to `product.collection`
7. Add the Product to the Collection

## Make Collection 'Not for Sale'
 
You can prevent all items within a collection from being for sale by creating a
metafield for the collection with the following attributes:
+ namesapce: `shop`
+ key: `not_for_sale`
+ value: `true`
 
To make the items within the Collection for sale, just delete the metafield.

The look and feel of a Collection on the [Collection Listing](https://ohlin.myshopify.com/collections) page is done via the Collection Product.

## Collection Listing

The look and feel of a Collection on the [Collection Listing](https://ohlin.myshopify.com/collections) page is done via the Collection Product.

### Collection background color

The background color can be set by creating a tag with the prefix `listing-bg-` followed by the color value.  
e.g. `#listing-bg-#000000`

### Collection background image

The background image can be set by uploading an image and setting the `alt` as `listing-bg`.

### Collection image

The feature image can be set by uploading an image and setting the `alt` as `listing-image`.

### Collection title

The title can be set by updating the Collection Product title.

### Collection title Color

The title color can be set by creating a tag with the prefix `listing-color-` followed by the color value.  
e.g. `#listing-color-#ffffff`

### Order of Collections

Shopify does not provide a way to easily order Collections shown, so we have to use a Link List to define the order we want the collections displayed in.

To update, remove or add a new Collection to the Listings page, once the Collection has been created go to `Navigation` and then edit the `Collections` link list.

## Collection Page

The look and feel of a Collection on the [Collection Page](https://ohlin.myshopify.com/collections/f-w-2014) page is done via the Collection Product.

### Layout

The layout is determined by the template and can be set to one of the following:
+ `collection`: Only Products
+ `collection.split`: Split view: Campaign and Products
+ `collection.all`: Special layout used for the [Shop Page](https://ohlin.myshopify.com/collections/all) showing only Products

#### Invert Navigation/Cart

If you choose a dark background color for the Campaign/Products you might want to invert the navigation and cart so they are white instead of black.

The navigation/cart can be inverted by creating the tag `layout-invert`.

#### Products background color

The background color can be set by creating a tag with the prefix `products-bg-` followed by the color value.  
e.g. `#products-bg-#000000`

#### Products text color

The text color of the product description can be set by creating a tag with the prefix `products-text-` followed by the color value.  
e.g. `#products-text-#000000`

### Only products

#### Sidebar background color

The background color can be set by creating a tag with the prefix `campaign-bg-` followed by the color value.  
e.g. `#campaign-bg-#000000`

### Split Campaign

#### Campaign background color

The background color can be set by creating a tag with the prefix `campaign-bg-` followed by the color value.  
e.g. `#campaign-bg-#000000`

The split campaign shows the Campaign Collection and the Collection Products side by side.

To control the about of the campaign images, they are grouped together. Below, I will show an example of images in the same group.

#### Campaign title color

The title color can be set by creating a tag with the prefix `campaign-title-` followed by the color value.  
e.g. `#campaign-title-#000000`

#### Campaign images

Images are grouped in rows which are configured by setting the `alt` as `campaign—n` where `n` is the row number the image should appear in.
e.g. `campaign-1`

Each row is an independent 12 column grid which is used to place and size the images.




##### Image position

Images can be positioned by appending any of the following class names after the row number, separating each class name with an asterisk `*`.  https://cdn.shopify.com/s/files/1/0743/8111/products/ss15-lookbook_01.jpg?v=1427381196
e.g. `campaign-1-bottom*left` or `campaign-1-bg*bgCover`

+ `back`: Sets the `z-index` to 0.
+ `front`: Set the `z-index` to 10.
+ `bottom`: Align to the very bottom of the column, minus the vertical  padding.
+ `top`: Align to the very top of the column, minus the vertical padding.
+ + `left`: Align to the very left of the column, minus the gutter width.
+ `right`: Align to the very right of the column, minus the gutter width.https://cdn.shopify.com/s/files/1/0743/8111/products/ss15-lookbook_01.jpg?v=1427381992
+ `up`: Pull the image up 25%.
+ `down`: Push the image down 25%.
+ `bg`: Set for all images to be used as background images (set `position: absolute`).
+ `bgCover`: Full-size background image to cover entire row
+ `bgContain`: Full-size background image keeping proportions
+ `bgBottom`: Background image aligned to bottom of column, minus vertical padding.
+ `bgTop`: Background image aligned to very top of column, minus vertical padding.
+ `bgLeft`: Align to the left of the row, minus the gutter width.
+ `bgRight`: Align to the right of the row, minus the gutter width.

##### Image size and placement

Images can be sized and placed by setting the final string in the `alt` tag (after `campaign-n`) to `x+y` where `x` is the number of columns wide the image should be, and `y` is the number of columns to offset from the left.
e.g. `campaign-1 8+2`

Images are set to fill the entire width of the columns they are placed in.

#### Campaign Feature Image 

The feature image for a set of images can be set by uploading an image and setting the `alt` as `campaign—n-feature` where `nhttps://cdn.shopify.com/s/files/1/0743/8111/products/ss15-lookbook_02_2x.jpg?v=1427461627` is the block number.  
e.g. `campaign-1-feature`

The size and position of the image is based on a 12x12 grid and can be configured by appending the desired grid widths and offset after the campaign alt tag.  
e.g. `campaign-1-feature 11+1` will span 11 grid withs and be offset by 1 grid width.

#### Campaign Inset Image 

The inset image for a set of images can be set by uploading an image and setting the `alt` as `campaign—n-inset` where `n` is the block number.  
e.g. `campaign-1-feature`

The size and position of the image is based on a 12x12 grid and can be configured by appending the desired grid widths and offset after the campaign alt tag.  
e.g. `campaign-1-inset 3` will span 3 grid withs and be offset by 0 grid widths.

#### Campaign trigger color switcher

You can trigger colors to switch by attaching `trigger` to the alt tag of a campaign image. This image should be the first in a row.
e.g. `campaign-5 8+2 trigger`

#### Campaign trigger background color

The trigger background color can be set by creating a tag with the prefix `campaign-trigger-bg-` followed by the color value.  
e.g. `#campaign-bg-#000000`

#### Products trigger background color

The trigger background color can be set by creating a tag with the prefix `products-trigger-bg-` followed by the color value.  
e.g. `#products-trigger-bg-#000000`

#### Products trigger text color

The trigger text color of the product description can be set by creating a tag with the prefix `products-trigger-text-` followed by the color value.  
e.g. `#products-trigger-text-#000000`
