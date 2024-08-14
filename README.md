# Introduction:

Enhance your customer's shopping experience with our Product Image Zoom Extension for Bagisto. This extension allows users to see a magnified view of the product image on hover, providing a detailed and interactive visual of the product.

# Some Key features of the Image Crop Extension

* **Magnified Image View:** 
    * Allows customers to hover over the product image to see a zoomed-in view, offering a closer look at product details.
      
* **Responsive Design:**  
    * Fully responsive and works seamlessly on various devices and screen sizes.

* **Smooth Animation:**
   * Provides a smooth zoom effect with minimal loading time for an enhanced user experience.
 
 * **Compatibility:**  
    * Designed to work with Bagisto versions v2.2.2 and v2.0.0, ensuring broad usability across different installations.

* **Easy Integration:**
   * Simple to install and integrate into existing Bagisto stores with minimal configuration needed.

* **Lightweight:**
   * Optimized for performance to ensure quick loading times and a seamless user experience.
 
 
 
# **Benefits:**
- **Enhanced Image Control**: Admins gain precise control over the display of product images, allowing for better presentation of products with cropped or full images as needed.
- **Improved User Experience**: The image cropper tool provides an easy-to-use interface that enhances the overall user experience for admins managing product images.
- **Flexibility**: The extension caters to different needs by allowing both cropped and full image options, accommodating various preferences and requirements for product presentation.

# Requirements:
* Bagisto: v2.2.2
* PHP: 8.1 or higher
* Composer 2.6.3 or higher

# Installation :
Unzip the respective extension zip and then merge "packages" folder into project root directory

* Goto config/app.php file and add following line under 'providers'

```
Webkul\ImageCrop\Providers\ImageCropServiceProvider::class
```

* Goto composer.json file and add following line under 'psr-4'

```
"Webkul\\ImageCrop\\": "packages/Webkul/ImageCrop/src"
```
* Run these below commands to complete the setup:

```
composer dump-autoload
```
```
php artisan optimize:clear
```
That's it, now just execute the project on your specified domain.
