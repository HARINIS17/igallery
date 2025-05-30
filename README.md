# Ex.08 Design of Interactive Image Gallery
## Date:20-5-2025git

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
<html>
<head>
    <title>Interactive Gallery</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 20px;
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            color: #fff;
        }

        h1 {
            color: #f9d423;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            font-size: 2.5rem;
            text-align: center;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 25px;
            width: 100%;
            max-width: 1000px;
            padding: 25px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .photo {
            background: rgba(255, 255, 255, 0.15);
            padding: 15px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            cursor: pointer;
            overflow: hidden;
        }

        .photo:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.3);
            background: rgba(255, 255, 255, 0.25);
        }

        .photo img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.3s;
        }

        .photo:hover img {
            transform: scale(1.05);
        }

        .photo p {
            margin-top: 15px;
            font-weight: 600;
            color: #fff;
            font-size: 1.1rem;
        }

        footer {
            margin-top: 40px;
            font-size: 14px;
            color: rgba(255, 255, 255, 0.7);
            background: rgba(0, 0, 0, 0.2);
            padding: 12px 25px;
            border-radius: 50px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        @media (max-width: 768px) {
            .gallery {
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
                gap: 15px;
                padding: 15px;
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <h1>Indian Cricket Stars Gallery</h1>

    <div class="gallery">
        <div class="photo" onclick="openImage('webimg1.webp')">
            <img src="webimg1.webp" alt="M.S.Dhoni">
            <p>M.S.Dhoni</p>
        </div>
        <div class="photo" onclick="openImage('webimg2.jpeg')">
            <img src="webimg2.jpeg" alt="Virat Kohli">
            <p>Virat Kohli</p>
        </div>
        <div class="photo" onclick="openImage('webimg3.jpeg')">
            <img src="webimg3.jpeg" alt="Ravindra Jadeja">
            <p>Ravindra Jadeja</p>
        </div>
        <div class="photo" onclick="openImage('webimg5.jpeg')">
            <img src="webimg5.jpeg" alt="Shreyas Iyer">
            <p>Shreyas Iyer</p>
        </div>
        <div class="photo" onclick="openImage('webexp6.jpeg')">
            <img src="webexp6.jpeg" alt="Hardik Pandya">
            <p>Hardik Pandya</p>
        </div>
        <div class="photo" onclick="openImage('webexp7.jpeg')">
            <img src="webexp7.jpeg" alt="Rohit Sharma">
            <p>Rohit Sharma</p>
        </div>
        <div class="photo" onclick="openImage('webexp8.jpeg')">
            <img src="webexp8.jpeg" alt="Rishabh Pant">
            <p>Rishabh Pant</p>
        </div>
        <div class="photo" onclick="openImage('webimg9.webp')">
            <img src="webimg9.webp" alt="Shubman Gill">
            <p>Shubman Gill</p>
        </div>
    </div>

    <footer>&copy; 2023 Cricket Gallery | Created by Harini S</footer>

    <script>
        function openImage(src) {
            const newWindow = window.open("", "_blank");
            newWindow.document.write(`
                <html>
                    <head><title>Image View</title></head>
                    <body style="margin:0;display:flex;justify-content:center;align-items:center;height:100vh;background:#0f2027;">
                        <img src="${src}" style="max-width:90%;max-height:90%;border-radius:10px;box-shadow:0 10px 30px rgba(0,0,0,0.5);">
                    </body>
                </html>
            `);
        }
    </script>

</body>
</html>
```
## OUTPUT:
![alt text](<Screenshot 2025-05-20 182422.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
