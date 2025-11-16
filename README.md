# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM

## image.html
```py
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery – Thalapathy</title>

    <style>
    
        body {
            margin: 0;
            padding: 0;
            font-family: "Poppins", Arial, sans-serif;
            background: url("vj3.jpg") no-repeat center center/cover;
            min-height: 100vh;
        }

        .overlay {
            background: rgba(0, 0, 0, 0.75);
            min-height: 100vh;
            padding: 40px 20px;
        }

        h1 {
            text-align: center;
            color: #fff;
            letter-spacing: 2px;
            font-size: 2.3rem;
            margin-bottom: 30px;
            font-weight: 600;
        }

        .gallery {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 18px;
        }

        .gallery img {
            width: 100%;
            height: 260px;
            object-fit: cover;
            border-radius: 14px;
            cursor: pointer;
            transition: transform 0.35s ease, box-shadow 0.3s ease;
        }

        .gallery img:hover {
            transform: scale(1.06);
            box-shadow: 0px 8px 18px rgba(0, 0, 0, 0.4);
        }

        #popup {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            display: none;
            justify-content: center;
            align-items: center;
            padding: 15px;
            animation: fadeIn 0.3s ease;
        }

        #popup img {
            max-width: 90%;
            max-height: 90vh;
            border-radius: 16px;
            box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.6);
            animation: scaleIn 0.3s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to   { opacity: 1; }
        }

        @keyframes scaleIn {
            from { transform: scale(0.8); }
            to   { transform: scale(1); }
        }
    </style>
</head>

<body>
    <div class="overlay">
        <h1>IMAGE GALLERY (THALAPATHY)</h1>

        <div class="gallery">
            <img src="vijay1.jpg" alt="Image 1">
            <img src="vijay2.jpg" alt="Image 2">
            <img src="vj4.jpg" alt="Image 3">
            <img src="vj5.jpeg" alt="Image 4">
            <img src="vj6.jpg" alt="Image 5">
            <img src="vj7.jpg" alt="Image 6">
            <img src="vj9.webp" alt="Image 7">
            <img src="vj8.jpg" alt="Image 8">
            <img src="vj10.jpg" alt="Image 9">
            <img src="vj11.jpg" alt="Image 0">

        </div>
    </div>

    <div id="popup" onclick="closePopup()">
        <img id="popupImg">
    </div>

    <script>
        const galleryImages = document.querySelectorAll('.gallery img');
        const popup = document.getElementById('popup');
        const popupImg = document.getElementById('popupImg');

        galleryImages.forEach(img => {
            img.addEventListener('click', () => {
                popup.style.display = 'flex';
                popupImg.src = img.src;
            });
        });

        function closePopup() {
            popup.style.display = 'none';
        }
    </script>
</body>
</html>

```



## OUTPUT
<img width="1913" height="1150" alt="image" src="https://github.com/user-attachments/assets/9643c7f2-2ea3-4a6c-a004-8bc25e35ffe9" />
<img width="1913" height="1143" alt="image" src="https://github.com/user-attachments/assets/cd97d114-de72-46fb-ab84-1b6a857b27f9" />
<img width="1867" height="1148" alt="image" src="https://github.com/user-attachments/assets/7a214dbd-48c8-4b3c-bd76-34c81fdc1509" />
<img width="1919" height="1136" alt="image" src="https://github.com/user-attachments/assets/6b6a0fd0-b6fb-4c81-96e5-33747919ffb4" />
<img width="1916" height="1157" alt="image" src="https://github.com/user-attachments/assets/2e394ec3-11f1-43bd-ad0c-31e868dee89b" />



## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
