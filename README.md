# Ex.08 Design of Interactive Image Gallery
# Date:
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```gallery.html
<html>
<head>
<title>Bike Image Gallery</title>
<link rel="stylesheet" href="gallery.css">
</head>
<body>

<header>Bike Gallery</header>

<div class="container">
    <div class="gallery-box">
        <img id="galleryImage" src="img1.jpg" alt="Bike Image">
        <p class="caption" id="caption">Mercedes Mayback</p>

        <div class="buttons">
            <button onclick="prev()">Previous</button>
            <button onclick="next()">Next</button>
        </div>
    </div>
</div>

<footer>
Designed by M Aadhavan Nagarajan &copy; 2025
</footer>

<script>
let gallery = [
    "img1.jpg",
    "img2.png",
    "img3.jpg",
    "img4.jpg",
    "img5.png"
];

let captions = [
    "GT 650",
    "Hayabusa",
    "Meteor",
    "Agusta",
    "Ducati"
];

let index = 0;

function next(){
    index++;
    if(index >= gallery.length){
        index = 0;
    }
    document.getElementById("galleryImage").src = gallery[index];
    document.getElementById("caption").innerText = captions[index];
}

function prev(){
    index--;
    if(index < 0){
        index = gallery.length - 1;
    }
    document.getElementById("galleryImage").src = gallery[index];
    document.getElementById("caption").innerText = captions[index];
}
</script>

</body>
</html>

gallery.css
body{
    margin:0;
    font-family: Arial, sans-serif;
    background: linear-gradient(black,rgb(37, 37, 37),rgb(32, 24, 24));
    display:flex;
    flex-direction:column;
    min-height:100vh;
}

header{
    background-color: gray;
    color:black;
    text-align:center;
    padding:15px;
    font-size:22px;
}

.container{
    flex:1;
    display:flex;
    justify-content:center;
    align-items:center;
}

.gallery-box{
    background-image: white;
    width:420px;
    padding:20px;
    border-radius:10px;
    box-shadow:0 5px 15px rgba(0,0,0,0.15);
    text-align:center;
}

.gallery-box img{
    width:100%;
    height:260px;
    object-fit:contain;
    background-color:silver;
    border-radius:8px;
}

.caption{
    margin-top:12px;
    font-size:16px;
    color:#1f2933;
}

.buttons{
    margin-top:15px;
    display:flex;
    justify-content:space-between;
}

.buttons button{
    padding:8px 18px;
    background-color:#6b7280;
    color:white;
    border:none;
    border-radius:6px;
    font-size:14px;
    cursor:pointer;
}

.buttons button:hover{
    background: linear-gradient(black,silver);
}

footer{
    text-align:center;
    padding:10px;
    font-size:13px;
    color:skyblue;
}
```
# OUTPUT:

<img width="375" height="291" alt="image" src="https://github.com/user-attachments/assets/61d78b68-4a29-4633-9de4-f28a3a1dbb06" />

<img width="470" height="350" alt="image" src="https://github.com/user-attachments/assets/f6b64ae3-61af-45cf-bbb5-04c2ce363538" />

<img width="528" height="310" alt="image" src="https://github.com/user-attachments/assets/5bf31328-5b49-4a8e-830e-9a01164a1d1c" />

<img width="454" height="331" alt="image" src="https://github.com/user-attachments/assets/71d7adb1-fbb6-497c-bcab-211cc66a871b" />

<img width="612" height="348" alt="image" src="https://github.com/user-attachments/assets/e4877d68-5c2e-4bbb-99cb-8f797fe0b7b2" />





# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
