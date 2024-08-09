# Introduction:

The Bagisto Image Crop Extension is designed to enhance the product image management experience within the Bagisto e-commerce platform. This extension offers a seamless solution for cropping images during both the product creation and image editing processes. 

# Some Key features of the Image Crop Extension

* **Image Cropping During Product Creation:** 
    -> When an admin is creating a new product, then at time of uploading the image, the image cropper interface will automatically load.
    -> The image cropper provides an intuitive and user-friendly interface that allows the admin to crop the image according to their preferences. The cropping tool offers adjustable frames to precisely select the desired portion of the image.
    -> After cropping, the admin can save the cropped image, which will then be used as the product image. This ensures that only the most relevant part of the image is displayed to customers.
 
* **Full Image Selection Option:**  
    -> For admins who prefer not to crop the image, the extension offers an option to select the full image without any cropping. This provides flexibility for users who want to use the entire image as is.
    -> The full image will be saved and displayed as the product image, giving admins the freedom to choose between a cropped or full image based on their requirements.

* **Image Editing Functionality:**
-> In addition to cropping images during the product creation process, the extension supports image cropping during the product image editing process.
-> When an admin edits an existing product image, they will be able to access the same cropping tool used during the initial creation. This ensures consistency in image management and allows for adjustments as needed.

# Requirements:
* Bagisto: v2.0.0
* PHP: 8.1 or higher
* Composer 2.6.3 or higher

# Installation :
Unzip the respective extension zip and then merge "packages" folder into project root directory

* Goto config/app.php file and add following line under 'providers'

```
Webkul\Giftcard\Providers\GiftcardServiceProvider::class
```

* Goto composer.json file and add following line under 'psr-4'

```
"Webkul\\Giftcard\\": "packages/Webkul/Giftcard/src"
```
* Run these below commands to complete the setup:

```
composer dump-autoload
```
```
php artisan migrate
```
```
php artisan optimize:clear
```

* Run the below command and select the Giftcard Service provider from the selection :

```
php artisan vendor:publish --force
```
* Include the PayPal credentials in the loadPayPalScript method. Additionally, ensure that the credentials are entered in the PayPal payment gateway section within the Bagisto admin panel.

* Add the below code in the CartResource File after the payment_method_title :

```
$this->mergeWhen($this->giftcard_number, [
    'giftcard_number'           => $this->giftcard_number,
    'giftcard_amount'           => $this->giftcard_amount,
    'remaining_giftcard_amount' => $this->remaining_giftcard_amount,
]),
```
That's it, now just execute the project on your specified domain.
