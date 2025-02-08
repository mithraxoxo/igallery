# Ex.08 Design of Interactive Image Gallery
## Date: 26.12.2024

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
    <title>Interactive Harry Potter Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: black; /* Set background to black */
            color: white; /* Set text color to white for visibility */
        }

        h1 {
            font-family: 'Harrington', sans-serif;
            font-size: 4rem;
            text-align: center;
            margin-top: 50px;
            color: #f5a623; /* Harry Potter-themed golden color */
        }

        .gallery {
            padding: 50px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .thumbnail-container {
            display: flex;
            justify-content: center;
            gap: 50px;
            flex-wrap: wrap;
        }

        .thumbnail {
            width: 300px;
            height: 200px;
            object-fit: cover;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .thumbnail:hover {
            transform: scale(1.1);
        }

        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .lightbox-img {
            max-width: 80%;
            max-height: 80%;
            margin: 20px 0;
            border: 2px solid rgb(0, 0, 0);
            box-shadow: 0 0 10px rgb(8, 44, 144);
        }

        .caption {
            color: white;
            text-align: center;
            font-size: 18px;
        }

        .close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 30px;
            color: white;
            cursor: pointer;
        }

        footer {
          text-align: center;
          padding: 5px;
          background-color: #faf4c7;
          color: rgb(0, 0, 0);
          position: absolute;
          bottom: 0;
          width: 100%;
        }
    </style>
</head>
<body>

    <h1>Harry Potter Movies</h1>
    <hr>
    
    <div class="gallery">
        <div class="thumbnail-container">
            <img src="hp1.jpg" class="thumbnail" alt="Harry Potter and the Philosopher's Stone">
            <img src="hp2.jpg" class="thumbnail" alt="Harry Potter and the Chamber of Secrets">
            <img src="hp3.jpg" class="thumbnail" alt="Harry Potter and the Prisoner of Azkaban">
            <img src="hp4.jpg" class="thumbnail" alt="Harry Potter and the Goblet of Fire">
            <img src="hp5.jpg" class="thumbnail" alt="Harry Potter and the Order of the Phoenix">
            <img src="hp6.jpg" class="thumbnail" alt="Harry Potter and the Half Blood-Prince">
            <img src="hp7.jpg" class="thumbnail" alt="Harry Potter and the Deathly Hallows Part 1">
            <img src="hp8.jpg" class="thumbnail" alt="Harry Potter and the Deathly Hallows Part 2">
        </div>

        <div class="lightbox">
            <span class="close">&times;</span>
            <img class="lightbox-img" src="" alt="">
            <div class="caption"></div>
        </div>
    </div>

    <script>
        const thumbnails = document.querySelectorAll('.thumbnail');
        const lightbox = document.querySelector('.lightbox');
        const lightboxImg = document.querySelector('.lightbox-img');
        const caption = document.querySelector('.caption');
        const closeBtn = document.querySelector('.close');

        // Event listeners for thumbnails
        thumbnails.forEach(thumbnail => {
            thumbnail.addEventListener('click', () => {
                lightbox.style.display = 'flex';
                lightboxImg.src = thumbnail.src;
                caption.textContent = thumbnail.alt;
            });
        });

        // Close button functionality
        closeBtn.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });

        // Close lightbox on click outside image
        lightbox.addEventListener('click', (e) => {
            if (e.target !== lightboxImg) {
                lightbox.style.display = 'none';
            }
        });
    </script>

    <footer>
        <p>Designed by MERIL GOLDLINA A (24007299)</p>
    </footer>
    
</body>
</html>

```
## OUTPUT:
![alt text](<Screenshot 2024-12-26 224401.png>)
![alt text](<Screenshot 2024-12-26 224436.png>)
![alt text](<Screenshot 2024-12-26 224453.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
