# Ex.07 Design of Interactive Image Gallery
## Date:23/12/2023

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
```
image.html

<head>
    <title>Interactive Image Gallery</title>
    <link href="image.css" rel="stylesheet">
</head>
<body>
    <header class="header">
        <h1>Image Gallery</h1>
    </header>

    <div class="gallery-container">
        <div class="gallery-card">
            <img id="galleryImage" src="p1.png" alt="Gallery Image">
            <p class="caption" id="caption">Rolls-Royce La Rose Noire Droptail</p>

            <div class="buttons">
                <button onclick="prevImage()">Previous</button>
                <button onclick="nextImage()">Next</button>
            </div>
        </div>
    </div>

    <footer class="footer">
       VIJAYAPRATHISHA J (25008497)
    </footer>

    <script>
        let gallery = [
            { src: "p1.png", text: "Rolls-Royce La Rose Noire Droptail" },
            { src: "p2.jpg", text: "Bugatti La Voiture Noire" },
            { src: "p3.webp", text: "Pagani Zonda HP Barchetta" },
            { src: "p4.webp", text: "SP Automotive Chaos" },
            { src: "p5.webp", text: "Mercedes Maybach Exelero" },
            { src: "p6.jpg", text: "Koenigsegg Sadair’s Spear" },
            { src: "p7.jpg", text: "Pininfarina B95	" },
        ];
        let index = 0;
        function nextImage() 
        {
            index++;
            if (index >= gallery.length) 
            {
                index = 0;
            }
            updateImage();
        }
        function prevImage() 
        {
            index--;
            if (index < 0) 
            {
                index = gallery.length - 1;
            }
            updateImage();
        }
        function updateImage() 
        {
            document.getElementById("galleryImage").src = gallery[index].src;
            document.getElementById("caption").innerText = gallery[index].text;
        }
    </script>
</body>
</html>

image.css

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body
{
    background-color: darkgray;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.header 
{
    background-color: yellowgreen;
    color: beige;
    text-align: center;
    padding: 15px;
}

.gallery-container 
{
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.gallery-card 
{
    background-color:blanchedalmond;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rebeccapurple;
    text-align: center;
    width: 380px;
}

.gallery-card img 
{
    width: 250px;     
    height: 200px;
    border-radius: 10px;
    margin-bottom: 10px;
}

.caption 
{
    margin: 15px 0;
    font-size: 16px;
    font-weight: bold;
}

.buttons 
{
    display: flex;
    justify-content: center;
    gap: 15px;
}

.buttons button 
{
    background-color: blueviolet;
    color: white;
    border: none;
    padding: 10px 18px;
    border-radius: 8px;
    cursor: pointer;
}

.buttons button:hover 
{
    background-color: violet;
}

.footer 
{
    background-color: bisque;
    color:rebeccapurple;
    text-align: center;
    padding: 12px;
}
```

## OUTPUT:

![alt text](<Screenshot (66).png>)

![alt text](<Screenshot (67)-1.png>)

![alt text](<Screenshot (68)-1.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
