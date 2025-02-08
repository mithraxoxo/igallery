# Ex.08 Design of Interactive Image Gallery
## Date:17/12/2024

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
gallery.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    
    <header>
        <h1>My Interactive Image Gallery</h1>
    </header>


    <div class="gallery-container">
        <div class="gallery-item" onclick="openModal(0)">
            <img src="image1.jpg" alt="Image 1" class="gallery-image">
        </div>
        <div class="gallery-item" onclick="openModal(1)">
            <img src="image2.jpg" alt="Image 2" class="gallery-image">
        </div>
        <div class="gallery-item" onclick="openModal(2)">
            <img src="image3.jpg" alt="Image 3" class="gallery-image">
        </div>
        <div class="gallery-item" onclick="openModal(3)">
            <img src="image4.jpg" alt="Image 4" class="gallery-image">
        </div>
        <div class="gallery-item" onclick="openModal(4)">
            <img src="image5.jpg" alt="Image 5" class="gallery-image">
        </div>
        <div class="gallery-item" onclick="openModal(5)">
            <img src="image6.jpg" alt="Image 6" class="gallery-image">
        </div>
    </div>

    
    <div id="modal" class="modal" onclick="closeModal()">
        <span class="close-btn" onclick="closeModal()">×</span>
        <img id="modal-image" src="" alt="Full Screen Image" class="modal-content">
    </div>

    
    <footer>
        <p>Designed and Developed by Harini S</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

styles.css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family:'Times New Roman', Times, serif;
    background-image: url('background.jpg');
    background-size: cover;
    background-position: center;
    color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 100vh;
    padding: 0 10px;
}

header {
    text-align: center;
    margin-top: 20px;
}

header h1 {
    font-size: 36px;
    color: #fff;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
}

.gallery-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 15px;
    padding: 20px;
}

.gallery-item {
    position: relative;
    overflow: hidden;
    cursor: pointer;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
}

.gallery-image {
    width: 100%;
    height: auto;
    transition: transform 0.3s ease;
    border-radius: 8px;
}

.gallery-item:hover .gallery-image {
    transform: scale(1.1);
}

.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
    z-index: 1000;
}


.modal-content {
    max-width: 90%;
    max-height: 90%;
    border-radius: 8px;
}

.close-btn {
    position: absolute;
    top: 10px;
    right: 20px;
    font-size: 36px;
    color: white;
    background-color: transparent;
    border: none;
    cursor: pointer;
}

footer {
    text-align: center;
    margin: 20px 0;
    font-size: 16px;
    color: #fff;
    background-color: rgba(0, 0, 0, 0.6);
    padding: 10px;
    border-radius: 5px;
}

footer p {
    margin: 0;
}

scripts.js
const modal = document.getElementById('modal');
const modalImage = document.getElementById('modal-image');

const images = [
    'image1.jpg',
    'image2.jpg',
    'image3.jpg',
    'image4.jpg',
    'image5.jpg',
    'image6.jpg'
];

function openModal(index) {
    modal.style.display = 'flex';
    modalImage.src = images[index];
}

function closeModal() {
    modal.style.display = 'none';
}

```

## OUTPUT:

![Screenshot (44)](https://github.com/user-attachments/assets/d24c41fa-8962-4f41-a6dd-6d4d44014e45)
![Screenshot (45)](https://github.com/user-attachments/assets/e3445b45-625c-48ca-89f1-72ad5cbbcff0)
![Screenshot (46)](https://github.com/user-attachments/assets/496ef2fc-cbb1-46fa-b3ff-e963e627f61b)
![Screenshot (47)](https://github.com/user-attachments/assets/08011719-59fb-49cb-8ee7-4f0f7988b8b0)
![Screenshot (48)](https://github.com/user-attachments/assets/e80e9ac1-aa27-4865-a7c4-06781deedc5a)
![Screenshot (49)](https://github.com/user-attachments/assets/430d236e-c00e-4f52-ac12-a466daa303bc)
![Screenshot (50)](https://github.com/user-attachments/assets/087eabf3-22d6-4796-b829-e49049058af0)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
