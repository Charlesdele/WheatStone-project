# 📸 WheatStone project

![forthebadge](https://forthebadge.com/images/badges/made-with-c-sharp.svg) ![forthebadge](https://forthebadge.com/images/badges/uses-brains.svg)

<img src=https://user-images.githubusercontent.com/63778269/137594887-d327dc1f-a49d-41a2-a77f-a43955160e3e.PNG width=400/>

This project aims to recreate the pixel and bitmap librairies of C# from scratch and implement them in multiple ways including basic LSB steganography, generating qr-code, histograms or fractals, and manipulating images with filters and tools.
The name of the project was inspired from Charles Wheatstone with his invention of the stereogram, which we implemented in the form of autostereogram generation in the project.

<br/>
<br/>

## Set up

When running the code for the first time, choose the image you want to work on.
A few ones are already in an image folder like the parot (coco), the eagle (lac) and the girl (lea).

<p align="left"> 
  <img src=https://user-images.githubusercontent.com/63778269/137762800-f053eb76-5e1a-433a-90cb-7af69e7f52c9.PNG height=225/>
  <img src=https://user-images.githubusercontent.com/63778269/137762934-f0d40a5b-f4b1-48e3-baa4-9238d5b7ae43.PNG height=225/>
  <img src=https://user-images.githubusercontent.com/63778269/137763073-d000fbf0-25e0-48c5-af11-f136f33aab46.PNG height=225/>
</p>

If you want to use your images put them in the folder **images_de_base** at the following path : _ProjectWheatstone/bin/Debug/images_de_base_

Be careful you have to use bitmap images. You'll find the images you will modify in the folder **images** (in the Debug)

<br/>
<br/>

## The functions

* Image transformation
  * Resize Image
  * Black and White conversion
  * Greyscale
  * Rotation
  * Flip
  * Invert Colours
  * Cropping
  * Channels
* Matrix Convolution
  * Edge Detect
  * Edge Enhance
  * Emboss
  * BoxBlur
  * Sharpen
* New Image
  * Histogram
  * Steganography
  * Mandelbrot Fractal
  * Julia's sets Fractals
* QR code generator
* Create your autostereogram

<br/>
<br/>

## Examples


### Manipulating images and using filters

<p align="left"> 
  <img src=https://user-images.githubusercontent.com/63778269/137770357-50a645b8-a57f-4421-966b-82d2921dc472.png height=150/>
  <img src=https://user-images.githubusercontent.com/63778269/137770361-81e79a3c-5530-47d9-9fb6-09aa7d6974fe.png height=150/>
  <img src=https://user-images.githubusercontent.com/63778269/137770368-bd361430-b1fd-45c9-bad7-2f74291c77c8.png height=150/> 
</p>
Black and white conversion | Greyscale | Inverted Colors

<br/>
<br/>

<p align="left"> 
  <img src=https://user-images.githubusercontent.com/63778269/137770697-ee276ed4-bfbb-46de-84c9-f3a447ab5d8c.png height=150/>
  <img src=https://user-images.githubusercontent.com/63778269/137770709-8b60c97d-3704-4226-a4e1-e064648ecd97.png height=150/>
  <img src=https://user-images.githubusercontent.com/63778269/137770752-83de0261-7c59-40a9-9585-740a76c7eea5.png height=150/> 
</p>
Edge detect | Emboss | Blur

<br/>
<br/>

<p align="left"> 
  <img src=https://user-images.githubusercontent.com/63778269/137770911-c5844c42-71ac-45d7-9472-9b899fb8d238.png height=150/>
  <img src=https://user-images.githubusercontent.com/63778269/137770919-39d85dd5-21c9-44f0-ac35-c1723950ec74.png height=150/>
  <img src=https://user-images.githubusercontent.com/63778269/137770935-921605d8-ee9a-49fc-8b2b-b717464d5f4c.png height=150/> 
</p>
60° rotation | 152° rotation | Vertical flip

You can even play with the filters and add some as much as you want to combine them. For example :

<img src=https://user-images.githubusercontent.com/63778269/137804366-f5803097-bd4d-41e9-b257-fbdb6c544d47.PNG height = 230/>


<br/>

### Histogram

<p align="left"> 
<img src=https://user-images.githubusercontent.com/63778269/137773197-b085cf51-85cb-4b13-b467-62c042073ed2.png height=200/>
</p>

Histogram of the image coco.bmp.

### Steganography

You can choose wether you want to encode or decode an image. If you wanna encode an image, you can choose the filter we put in the **images_de_base** folder called _autostereogramfilter_, select it as your work image. You can try to encode the image and hide a message for example with the _stereotest_ image where it is written "HELLO". Then choose how many significant byte you want to hide. Here we'll hide 4 bytes.

<p align="left"> 
<img src=https://user-images.githubusercontent.com/63778269/137775174-9a63b87c-8d5d-4a79-beff-af3bfdf2d312.png height=200/>
</p>

If you focus hard enough you can approximately see the word "HELLO" written through the image.

Here is the method how to see stereograms.

<img src=https://user-images.githubusercontent.com/63778269/137803277-8aee47a2-5371-49bc-8288-d94ff1db6c74.PNG height=300/>

Now if you wanna decode this image, choose it as the work image and your image will be decoded through different significant bytes.

<p align="left"> 
<img src=https://user-images.githubusercontent.com/63778269/137775876-b6422ca7-83c4-4f78-871c-363a5d2f64f4.PNG width=500/>
</p>

<br/>

### Fractals

The Julia Set and Mandelbrot Set are sets on the complex plane that create those pretty infinitely detailed images (fractals) that can even be considered as art.
The Mandelbrot set can be considered a map of all Julia sets because it uses a different c at each location. A specific Julia set can be defined by a point in the Mandelbrot set matching its constant c value, and the look of an entire Julia set is usually similar in style to the Mandelbrot set at that corresponding location. 

Mandelbrot set

<p align="left"> 
  <img src=https://user-images.githubusercontent.com/63778269/137801623-cadb6340-e454-4b73-82d2-f449faba9525.png height=300/>
  <img src=https://user-images.githubusercontent.com/63778269/137801984-fd90af53-8942-48be-b48f-5b13222fcbdd.gif height=300/>
</p>

Points near the edges of the Mandelbrot set typically give the most interesting Julia sets. Here are some popular Julia sets you can make and their corresponding locations in the Mandelbrot set.

<p align="left"> 
  <img src=https://user-images.githubusercontent.com/63778269/137777912-ac20188e-4906-461a-aa9d-70ccab9afd50.png width=200/>
  <img src=https://user-images.githubusercontent.com/63778269/137777919-88c8ab95-fc88-4267-a8c8-145492e2f3c4.png width=200/>
  <img src=https://user-images.githubusercontent.com/63778269/137777926-70418b4f-9a3f-4049-831e-ec3c9986edcf.png width=200/> 
  <img src=https://user-images.githubusercontent.com/63778269/137777933-d115dece-cca8-49bf-87a0-788f6fe15143.png width=200/> 
</p>
c = -0.4 + 0.6i | c = -0.54 + 0.54i | c = 0.285 + 0.01i | c = -0.8i

<br/>

So now it's your turn to be an artist and create the fractal you want !

<br/>


### QR Code

Our QR code class can create QR codes to the largest size which is 177x177 pixels (version 40). The level of correction is L, which allows the code to be read even if 7% of it is is unreadable. You can only encode alphanumeric data mode. 

You can create a QR Code for your github profile for example, like this 😉

<img src=https://user-images.githubusercontent.com/63778269/137807740-cc6cad91-1089-4195-9f9d-4bc2cdc60a79.png width=300/>

<br/>
<br/>

## Note

The python code is in english so do not hesitate to contact me if you want more details in French.

### Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

<br/>
<br/>

# 🧍‍♂️ Authors

* **Clovis Carlier** _alias_ [@Joytide](https://github.com/Joytide)
* **Charles Delemazure** _alias_ [@Charlesdele](https://github.com/Charlesdele)
