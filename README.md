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
    <title>Interactive Photo Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: pink;
        }

        h1 {
            color: black;
            margin-bottom: 20px;
        }

        .gallery {
            display: flex;
            gap: 10px;
        }

        .thumbnail {
            width: 100px;
            height: 100px;
            cursor: pointer;
            transition: transform 0.3s, width 0.3s, height 0.3s;
        }

        .thumbnail:hover {
            transform: scale(1.5);
            width: 150px;
            height: 150px;
        }

        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
        }

        .overlay img {
            max-width: 80%;
            max-height: 80%;
        }

        footer {
            position: absolute;
            bottom: 10px;
            text-align: center;
            width: 100%;
            color: #000;
        }
    </style>
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <div class="gallery">
        <img src="image1.jpg" alt="Image 1" class="thumbnail">
        <img src="images2.jpg" alt="Image 2" class="thumbnail">
        <img src="images3.jpg" alt="Image 3" class="thumbnail">
        <img src="images4.jpg" alt="Image 4" class="thumbnail">
        <img src="images5.jpg" alt="Image 5" class="thumbnail">
        <img src="images6.jpg" alt="Image 6" class="thumbnail">
        <img src="images7.jpg" alt="Image 7" class="thumbnail">

    </div>
    <div class="overlay" id="overlay">
        <img id="enlargedImage" src="" alt="Enlarged Image">
    </div>
    <footer>
        Designed and developed by Rohini @ 2024
    </footer>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const thumbnails = document.querySelectorAll('.thumbnail');
            const overlay = document.getElementById('overlay');
            const enlargedImage = document.getElementById('enlargedImage');

            thumbnails.forEach(thumbnail => {
                thumbnail.addEventListener('click', () => {
                    enlargedImage.src = thumbnail.src;
                    overlay.style.display = 'flex';
                });
            });

            overlay.addEventListener('click', () => {
                overlay.style.display = 'none';
            });
        });
    </script>
</body>
</html>
```
## OUTPUT:
![alt text](<rohini/iapp/static/Screenshot 2024-12-20 125125.png>)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
