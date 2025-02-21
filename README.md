# Finnxak.github.io
<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tech Enthusiasts</title>
    <style>
        /* General Styling */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: 'Verdana', sans-serif;
            background-color: #e0e4e8;
            color: #333;
        }/* Navigation Bar Styling */
    .nav {
        position: fixed;
        left: 0;
        top: 0;
        width: 250px;
        background-color: #2c3e50;
        color: white;
        height: 100%;
        padding-top: 40px;
        padding-left: 20px;
        font-size: 20px;
        transform: translateX(-100%);
        transition: transform 0.3s ease;
        z-index: 1000;
    }
    .nav.open {
        transform: translateX(0);
    }
    .nav a {
        display: block;
        color: white;
        padding: 12px 18px;
        text-decoration: none;
        margin-bottom: 12px;
        border-radius: 6px;
        transition: background-color 0.3s ease;
    }
    .nav a:hover {
        background-color: #16a085;
    }

    /* Hamburger Menu */
    .hamburger {
        display: block;
        position: fixed;
        top: 20px;
        left: 20px;
        font-size: 30px;
        cursor: pointer;
        z-index: 1001;
    }
    .hamburger span {
        display: block;
        width: 35px;
        height: 5px;
        margin: 6px 0;
        background-color: #333;
        transition: 0.4s;
    }

    /* Main Content */
    .content {
        margin-left: 270px;
        padding: 40px;
    }
    .hidden {
        display: none;
    }

    /* Sections Styling */
    .section {
        background-color: #fff;
        border-radius: 8px;
        padding: 30px;
        box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
    }
</style>

</head>
<body><!-- Hamburger Menu --><div class="hamburger" onclick="toggleMenu()">
    <span></span>
    <span></span>
    <span></span>
</div><!-- Navigation Menu --><div id="navMenu" class="nav">
    <a href="#" onclick="showSection('home')">Home</a>
    <a href="#" onclick="showSection('aboutUs')">About Us</a>
    <a href="#" onclick="showSection('ict')">ICT</a>
</div><!-- Home Section --><div id="home" class="content section">
    <h1>Welcome to Our Tech Haven!</h1>
    <img src="ICT.png" alt="Tech Image" style="width:100%; border-radius:8px;">
    <p>Discover the amazing world of technology and learn more about the tech innovations shaping our future.</p>
</div><!-- About Us Section --><div id="aboutUs" class="content section hidden">
    <h2>Meet the Team</h2>
    <div class="team-container">
        <div class="team-member">
            <img src="Picture(2).jpeg" alt="Althea">
            <p>Althea Falawed</p>
        </div>
        <div class="team-member">
            <img src="Picture(4).jpeg" alt="Neil">
            <p>Neil Eulin</p>
        </div>
        <div class="team-member">
            <img src="Picture(5).jpeg" alt="Nathan">
            <p>Nathan Amante</p>
        </div>
        <div class="team-member">
            <img src="Picture(1).jpeg" alt="Aljur">
            <p>Aljur Salazar</p>
        </div>
        <div class="team-member">
            <img src="Picture(3).jpeg" alt="Shayreen">
            <p>Shayreen Buitizon</p>
        </div>
    </div>
</div><!-- ICT Section --><div id="ict" class="content section hidden">
    <h2>Explore ICT</h2>
    <div class="dropdown">
        <button onclick="toggleDropdown('monitor')">Monitor</button>
        <div id="monitor" class="dropdown-content hidden">
            <p>24-inch LED Monitor: High-resolution display for gaming and work.</p>
        </div>
    </div>
    <div class="dropdown">
        <button onclick="toggleDropdown('mouse')">Mouse</button>
        <div id="mouse" class="dropdown-content hidden">
            <p>Wireless Precision Mouse: Smooth tracking and ergonomic design.</p>
        </div>
    </div>
</div><!-- JavaScript for Menu and Sections --><script>
    function toggleMenu() {
        document.getElementById('navMenu').classList.toggle('open');
    }
    function showSection(sectionId) {
        document.querySelectorAll('.content').forEach(section => {
            section.classList.add('hidden');
        });
        document.getElementById(sectionId).classList.remove('hidden');
    }
    function toggleDropdown(id) {
        document.getElementById(id).classList.toggle('hidden');
    }
</script></body>
</html>
