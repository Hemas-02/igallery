# Ex.08 Design of Interactive Image Gallery
## Date:27/05/25

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
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Actor Image Gallery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #1e1e2f;
      margin: 0;
      padding: 20px;
      text-align: center;
    }

    h1 {
      color: #f5b400;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
      margin-top: 30px;
    }

    .gallery img {
      width: 100%;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    .popup {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      background-color: rgba(0,0,0,0.85);
      justify-content: center;
      align-items: center;
      z-index: 10;
    }

    .popup img {
      max-width: 90%;
      max-height: 90%;
      border: 5px solid #fff;
      border-radius: 10px;
    }

    footer {
      margin-top: 40px;
      font-size: 14px;
      color: #ccc;
    }
  </style>
</head>
<body>

  <h1>Famous Actors Gallery 🎥</h1>

  <div class="gallery">
    <img src="actor1.jpg" alt="Actor 1">
    <img src="actor2.jpg" alt="Actor 2">
    <img src="actor3.jpg" alt="Actor 3">
    <img src="actor4.jpg" alt="Actor 4">
    <img src="actor5.jpg" alt="Actor 5">
    <img src="actor6.jpg" alt="Actor 6">
    <img src="actor7.jpg" alt="Actor 7">
  </div>

  <div class="popup" id="popup">
    <img id="popup-img" src="" alt="Popup Image">
  </div>

  <script>
    const images = document.querySelectorAll('.gallery img');
    const popup = document.getElementById('popup');
    const popupImg = document.getElementById('popup-img');

    images.forEach(image => {
      image.addEventListener('click', () => {
        popup.style.display = 'flex';
        popupImg.src = image.src;
      });
    });

    popup.addEventListener('click', () => {
      popup.style.display = 'none';
    });
  </script>

  <footer>
    <p>Designed by Hemalatha R</p>
  </footer>
</body>
</html>
## OUTPUT:
![Screenshot (73)](https://github.com/user-attachments/assets/9e914e3d-6c02-493a-b5c7-092f55ffd372)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
