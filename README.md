# Ex.08 Design of Interactive Image Gallery
## Date:08.02.2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: url('pink bg.jpg');
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }

        .header {
            text-align: center;
            padding: 10px;
            background-color: #ffdce5;
            width: 100%;
            height: 100px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            font-family: monospace;
        }

        .header h1 {
            font-size: 2.5rem;
            color: #6a0572;
        }

        .header p {
            font-size: 1.2rem;
            color: #715ac5;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            padding: 20px;
            margin: 20px 0 10px 0;
            width: 90%;
            max-width: 1200px;
        }

        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            border: 10px solid #ffffff;
        }

        .gallery-item img {
            width: 100%;
            height: auto; /* Ensures proper aspect ratio */
            display: block;
            object-fit: cover;
        }

        .gallery-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom right, rgba(255, 255, 255, 0.2), rgba(0, 0, 0, 0.2));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        .footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            width: 100%;
            height: 40px;
            background-color: #ffdce5;
        }

        .footer p {
            font-size: 1.2rem;
            color: #6e5c9f;
        }

        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 80%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        #lightbox:target {
            display: flex;
        }

        #lightbox .close {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #fff;
            border: none;
            font-size: 2rem;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="header">
    <h1>Image Gallery</h1>
</div>

<div class="gallery">
    <div class="gallery-item" onclick="showAlert('Image 1 clicked!')">
        <img src="c:/Users/admin/Downloads/image1.jpg" alt="Image 1">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 2 clicked!')">
        <img src="c:\Users\admin\Downloads\image 2.jpg" alt="Image 2">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 3 clicked!')">
        <img src="c:/Users/admin/Downloads/image 3.jpg" alt="Image 3">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 4 clicked!')">
        <img src="c:/Users/admin/Downloads/image 4.jpg" alt="Image 4">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 5 clicked!')">
        <img src="c:/Users/admin/Downloads/image 5.jpg" alt="Image 5">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 6 clicked!')">
        <img src="c:/Users/admin/Downloads/image 6.jpg" alt="Image 6">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 7 clicked!')">
        <img src="c:/Users/admin/Downloads/image 7.jpg" alt="Image 7">
    </div>
    <div class="gallery-item" onclick="showAlert('Image 8 clicked!')">
        <img src="c:/Users/admin/Downloads/image 8.jpeg" alt="Image 8">
    </div>
</div>

<div id="lightbox">
    <button class="close" onclick="closeLightbox()">&#215;</button>
    <img src="" id="lightbox-img" alt="Full Image">
</div>

<div class="footer">
    <p><b>Designed by Praveena Ashok (24006885)</b></p>
</div>

<script>
    function showAlert(message) {
        alert(message);
    }

    function openLightbox(imageSrc) {
        document.getElementById('lightbox-img').src = imageSrc;
        document.getElementById('lightbox').style.display = 'flex';
    }

    function closeLightbox() {
        document.getElementById('lightbox').style.display = 'none';
    }

    const galleryItems = document.querySelectorAll('.gallery-item');
    galleryItems.forEach(item => {
        item.addEventListener('click', () => {
            const imgSrc = item.querySelector('img').src;
            openLightbox(imgSrc);
        });
    });
</script>

</body>
</html>

```
## OUTPUT:
![alt text](<Screenshot 2024-12-27 223032.png>)
![alt text](<Screenshot 2024-12-27 223045.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
