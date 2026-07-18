<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StudyHub Pro</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<nav class="navbar">
    <div class="logo">📚 StudyHub Pro</div>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Lectures</a></li>
        <li><a href="#">Notes</a></li>
        <li><a href="#">Progress</a></li>
    </ul>
</nav>

<header class="hero">
    <h1>Welcome to StudyHub Pro</h1>
    <p>Your Personal Study Dashboard</p>
    <a href="#" class="btn">Start Learning</a>
</header>

<section class="subjects">

    <div class="card">
        <h2>⚛ Physics</h2>
        <p>Lectures • Notes • DPP</p>
    </div>

    <div class="card">
        <h2>🧪 Chemistry</h2>
        <p>Lectures • Notes • DPP</p>
    </div>

    <div class="card">
        <h2>📐 Mathematics</h2>
        <p>Lectures • Notes • DPP</p>
    </div>

    <div class="card">
        <h2>🧬 Biology</h2>
        <p>Lectures • Notes • DPP</p>
    </div>

</section>

<section class="progress">
    <h2>Your Progress</h2>

    <div class="bar">
        <div class="fill"></div>
    </div>

    <p>70% Completed</p>
</section>

<footer>
    © 2026 StudyHub Pro
</footer>

</body>
</html>/* Google Font */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:linear-gradient(135deg,#0f172a,#1e293b,#312e81);
min-height:100vh;
color:white;
}

/* Navbar */

.navbar{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 8%;
backdrop-filter:blur(15px);
background:rgba(255,255,255,.08);
position:sticky;
top:0;
}

.logo{
font-size:28px;
font-weight:700;
}

.navbar ul{
display:flex;
list-style:none;
gap:30px;
}

.navbar a{
text-decoration:none;
color:white;
transition:.3s;
}

.navbar a:hover{
color:#38bdf8;
}

/* Hero */

.hero{
text-align:center;
padding:80px 20px;
}

.hero h1{
font-size:55px;
margin-bottom:15px;
}

.hero p{
font-size:20px;
opacity:.85;
margin-bottom:30px;
}

.btn{
display:inline-block;
padding:15px 35px;
background:#3b82f6;
color:white;
text-decoration:none;
border-radius:40px;
transition:.3s;
}

.btn:hover{
transform:translateY(-4px);
background:#2563eb;
}

/* Subject Cards */

.subjects{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:30px;
padding:50px 8%;
}

.card{
background:rgba(255,255,255,.08);
border-radius:20px;
padding:30px;
backdrop-filter:blur(12px);
transition:.3s;
cursor:pointer;
}

.card:hover{
transform:translateY(-10px);
box-shadow:0 20px 40px rgba(0,0,0,.35);
}

.card h2{
margin-bottom:12px;
}

/* Progress */

.progress{
padding:50px 8%;
}

.bar{
height:20px;
background:#1e293b;
border-radius:30px;
overflow:hidden;
margin:20px 0;
}

.fill{
height:100%;
width:70%;
background:linear-gradient(90deg,#06b6d4,#3b82f6);
border-radius:30px;
}

/* Footer */

footer{
text-align:center;
padding:30px;
opacity:.8;
}

/* Responsive */

@media(max-width:768px){

.navbar{
flex-direction:column;
gap:15px;
}

.navbar ul{
flex-wrap:wrap;
justify-content:center;
}

.hero h1{
font-size:38px;
}

.hero p{
font-size:17px;
}

}<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StudyHub Pro - Dashboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<nav class="navbar">
    <div class="logo">📚 StudyHub Pro</div>

    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="#">Lectures</a></li>
        <li><a href="#">Notes</a></li>
        <li><a href="#">Progress</a></li>
    </ul>
</nav>

<header class="hero">
    <h1>Dashboard</h1>
    <p>Continue your study journey</p>
</header>

<section class="subjects">

    <div class="card">
        <h2>⚛ Physics</h2>
        <p>12 Chapters</p>
        <p>Progress: 65%</p>
        <button class="btn">Open</button>
    </div>

    <div class="card">
        <h2>🧪 Chemistry</h2>
        <p>18 Chapters</p>
        <p>Progress: 42%</p>
        <button class="btn">Open</button>
    </div>

    <div class="card">
        <h2>📐 Mathematics</h2>
        <p>15 Chapters</p>
        <p>Progress: 70%</p>
        <button class="btn">Open</button>
    </div>

    <div class="card">
        <h2>🧬 Biology</h2>
        <p>16 Chapters</p>
        <p>Progress: 80%</p>
        <button class="btn">Open</button>
    </div>

</section>

<section class="progress">

<h2>Today's Goal</h2>

<div class="bar">
<div class="fill"></div>
</div>

<p>Complete 2 Lectures + 1 DPP</p>

</section>

<footer>
© 2026 StudyHub Pro
</footer>

</body>
</html>// StudyHub Pro

// Welcome Message
window.addEventListener("load", () => {
    console.log("Welcome to StudyHub Pro");
});

// Search Function
function searchSubject() {
    const input = document.getElementById("search").value.toLowerCase();
    const cards = document.querySelectorAll(".card");

    cards.forEach(card => {
        const title = card.querySelector("h2").innerText.toLowerCase();

        if (title.includes(input)) {
            card.style.display = "block";
        } else {
            card.style.display = "none";
        }
    });
}

// Dark Mode
const body = document.body;

function toggleTheme() {
    body.classList.toggle("light-mode");

    if (body.classList.contains("light-mode")) {
        localStorage.setItem("theme", "light");
    } else {
        localStorage.setItem("theme", "dark");
    }
}

// Load Theme
window.onload = function () {
    const theme = localStorage.getItem("theme");

    if (theme === "light") {
        body.classList.add("light-mode");
    }
};

// Progress Example
let progress = 70;

function updateProgress(value) {
    progress = value;

    document.querySelector(".fill").style.width = progress + "%";
}
