<!DOCTYPE html>
<html lang="en">
<head>
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
        }

        /* Navigation Bar Styling */
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
            transition: transform 0.3s ease;
            transform: translateX(-100%);
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
        #home {
            margin-left: 270px;
            padding: 40px;
            background-color: #fff;
            border-radius: 8px;
            margin-top: 100px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
        }

        #home h1 {
            font-size: 38px;
            color: #2c3e50;
            margin-bottom: 20px;
        }

        #home p {
            font-size: 18px;
            line-height: 1.8;
            color: #7f8c8d;
        }

        /* Large Home Image */
        .home-image {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        /* About Us Section */
        .about-us {
            margin-left: 270px;
            padding: 30px;
            background-color: #fff;
            border-radius: 8px;
            width: 60%;
            margin-top: 30px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        .about-us h2 {
            font-size: 30px;
            color: #34495e;
            text-align: center;
            margin-bottom: 20px;
        }

        .team-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            margin-top: 20px;
        }

        .team-member {
            text-align: center;
            width: 120px;
        }

        .team-member img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }

        .team-member p {
            margin-top: 8px;
            font-size: 16px;
            font-weight: bold;
            color: #34495e;
        }

        /* Email Button */
        .email-button {
            display: block;
            width: fit-content;
            margin: 25px auto;
            padding: 14px 24px;
            background-color: #e74c3c;
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-size: 18px;
            text-align: center;
        }

        .email-button:hover {
            background-color: #c0392b;
        }

        /* ICT Section */
        .ict {
            margin-left: 270px;
            padding: 30px;
            background-color: #fff;
            border-radius: 8px;
            width: 60%;
            margin-top: 30px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        .ict h2 {
            font-size: 30px;
            color: #34495e;
            margin-bottom: 20px;
        }

        /* Dropdown Styling */
        .dropdown {
            background-color: #16a085;
            color: white;
            border: none;
            width: 100%;
            font-size: 20px;
            padding: 14px;
            cursor: pointer;
            text-align: left;
            border-radius: 6px;
            margin-bottom: 18px;
        }

        .dropdown-content {
            display: none;
            background-color: #ecf0f1;
            border-radius: 6px;
            padding: 12px;
            margin-top: 10px;
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }

        .dropdown img {
            width: 60px;
            height: 60px;
            margin-right: 18px;
            border-radius: 6px;
        }

        .dropdown-item {
            display: flex;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid #bdc3c7;
        }

        .dropdown-item:last-child {
            border-bottom: none;
        }

        .dropdown-item p {
            margin-left: 18px;
            font-size: 16px;
            color: #34495e;
        }
    </style>
</head>
<body>

<!-- Hamburger Menu -->
<div class="hamburger" onclick="toggleMenu()">
    <span></span>
    <span></span>
    <span></span>
</div>

<!-- Navigation Menu -->
<div id="navMenu" class="nav">
    <a href="javascript:void(0)" onclick="showSection('home')">Home</a>
    <a href="javascript:void(0)" onclick="showSection('aboutUs')">About Us</a>
    <a href="javascript:void(0)" onclick="showSection('ict')">ICT</a>
</div>

<!-- Main Content -->
<div id="home">
    <h1>Welcome to Our Tech Haven!</h1>
    <img src="ICT.png" alt="Large Banner Image" class="home-image">
    <p>Discover the amazing world of technology and learn more about the tech innovations shaping our future. Dive deeper into our favorite tech tools and the power of ICT!</p>
</div>

<!-- About Us Section -->
<div id="aboutUs" class="about-us" style="display:none;">
    <h2>Meet the Team</h2>
    <div class="team-container">
        <div class="team-member">
            <img src="Picture (2).jpeg" alt="Althea">
            <p>Althea Falawed</p>
        </div>
        <div class="team-member">
            <img src="Picture (4).jpeg" alt="Neil">
            <p>Neil Eulin</p>
        </div>
        <div class="team-member">
            <img src="Picture (5).jpeg" alt="Nathan">
            <p>Nathan Amante</p>
        </div>
        <div class="team-member">
            <img src="Picture (1).jpeg" alt="Aljur">
            <p>Aljur Salazar</p>
        </div>
        <div class="team-member">
            <img src="Picture (3).jpeg" alt="Shayreen">
            <p>Shayreen Buitizon</p>
        </div>
    </div>
    <a href="mailto:brentnathanamante@gmail.com" class="email-button">Send an Email</a>
</div>

<!-- ICT Section -->
<div id="ict" class="ict" style="display:none;">
    <h2>Explore Computer Parts</h2>

    <!-- Monitor Dropdown -->
    <div class="dropdown">
        <button>Monitor</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="monitor.jpg" alt="Monitor">
                <div>
                    <span>24-inch LED Monitor</span>
                    <p>A high-resolution display that delivers crystal-clear visuals for gaming, productivity, and everything in between.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Mouse Dropdown -->
    <div class="dropdown">
        <button>Mouse</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="mouse.jpg" alt="Mouse">
                <div>
                    <span>Wireless Precision Mouse</span>
                    <p>Perfect for everyday tasks, offering high precision with smooth tracking and ergonomic design for comfort.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Keyboard Dropdown -->
    <div class="dropdown">
        <button>Keyboard</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="keyboard.jpg" alt="Keyboard">
                <div>
                    <span>Mechanical RGB Keyboard</span>
                    <p>Fast, durable, and visually striking – this mechanical keyboard features customizable RGB lighting and tactile switches.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- PC Dropdown -->
    <div class="dropdown">
        <button>PC</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="pc.jpg" alt="PC">
                <div>
                    <span>Gaming Desktop PC</span>
                    <p>Packed with top-tier components, this PC is built for heavy-duty gaming and high-performance applications.</p>
                </div>
            </div>
        </div>
    </div>

</div>

<!-- JavaScript -->
<script>
    function toggleMenu() {
        document.getElementById('navMenu').classList.toggle<!DOCTYPE html>
<html lang="en">
<head>
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
        }

        /* Navigation Bar Styling */
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
            transition: transform 0.3s ease;
            transform: translateX(-100%);
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
        #home {
            margin-left: 270px;
            padding: 40px;
            background-color: #fff;
            border-radius: 8px;
            margin-top: 100px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
        }

        #home h1 {
            font-size: 38px;
            color: #2c3e50;
            margin-bottom: 20px;
        }

        #home p {
            font-size: 18px;
            line-height: 1.8;
            color: #7f8c8d;
        }

        /* Large Home Image */
        .home-image {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        /* About Us Section */
        .about-us {
            margin-left: 270px;
            padding: 30px;
            background-color: #fff;
            border-radius: 8px;
            width: 60%;
            margin-top: 30px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        .about-us h2 {
            font-size: 30px;
            color: #34495e;
            text-align: center;
            margin-bottom: 20px;
        }

        .team-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            margin-top: 20px;
        }

        .team-member {
            text-align: center;
            width: 120px;
        }

        .team-member img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }

        .team-member p {
            margin-top: 8px;
            font-size: 16px;
            font-weight: bold;
            color: #34495e;
        }

        /* Email Button */
        .email-button {
            display: block;
            width: fit-content;
            margin: 25px auto;
            padding: 14px 24px;
            background-color: #e74c3c;
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-size: 18px;
            text-align: center;
        }

        .email-button:hover {
            background-color: #c0392b;
        }

        /* ICT Section */
        .ict {
            margin-left: 270px;
            padding: 30px;
            background-color: #fff;
            border-radius: 8px;
            width: 60%;
            margin-top: 30px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        .ict h2 {
            font-size: 30px;
            color: #34495e;
            margin-bottom: 20px;
        }

        /* Dropdown Styling */
        .dropdown {
            background-color: #16a085;
            color: white;
            border: none;
            width: 100%;
            font-size: 20px;
            padding: 14px;
            cursor: pointer;
            text-align: left;
            border-radius: 6px;
            margin-bottom: 18px;
        }

        .dropdown-content {
            display: none;
            background-color: #ecf0f1;
            border-radius: 6px;
            padding: 12px;
            margin-top: 10px;
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }

        .dropdown img {
            width: 60px;
            height: 60px;
            margin-right: 18px;
            border-radius: 6px;
        }

        .dropdown-item {
            display: flex;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid #bdc3c7;
        }

        .dropdown-item:last-child {
            border-bottom: none;
        }

        .dropdown-item p {
            margin-left: 18px;
            font-size: 16px;
            color: #34495e;
        }
    </style>
</head>
<body>

<!-- Hamburger Menu -->
<div class="hamburger" onclick="toggleMenu()">
    <span></span>
    <span></span>
    <span></span>
</div>

<!-- Navigation Menu -->
<div id="navMenu" class="nav">
    <a href="javascript:void(0)" onclick="showSection('home')">Home</a>
    <a href="javascript:void(0)" onclick="showSection('aboutUs')">About Us</a>
    <a href="javascript:void(0)" onclick="showSection('ict')">ICT</a>
</div>

<!-- Main Content -->
<div id="home">
    <h1>Welcome to Our Tech Haven!</h1>
    <img src="ICT.png" alt="Large Banner Image" class="home-image">
    <p>Discover the amazing world of technology and learn more about the tech innovations shaping our future. Dive deeper into our favorite tech tools and the power of ICT!</p>
</div>

<!-- About Us Section -->
<div id="aboutUs" class="about-us" style="display:none;">
    <h2>Meet the Team</h2>
    <div class="team-container">
        <div class="team-member">
            <img src="Picture (2).jpeg" alt="Althea">
            <p>Althea Falawed</p>
        </div>
        <div class="team-member">
            <img src="Picture (4).jpeg" alt="Neil">
            <p>Neil Eulin</p>
        </div>
        <div class="team-member">
            <img src="Picture (5).jpeg" alt="Nathan">
            <p>Nathan Amante</p>
        </div>
        <div class="team-member">
            <img src="Picture (1).jpeg" alt="Aljur">
            <p>Aljur Salazar</p>
        </div>
        <div class="team-member">
            <img src="Picture (3).jpeg" alt="Shayreen">
            <p>Shayreen Buitizon</p>
        </div>
    </div>
    <a href="mailto:brentnathanamante@gmail.com" class="email-button">Send an Email</a>
</div>

<!-- ICT Section -->
<div id="ict" class="ict" style="display:none;">
    <h2>Explore Computer Parts</h2>

    <!-- Monitor Dropdown -->
    <div class="dropdown">
        <button>Monitor</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="monitor.jpg" alt="Monitor">
                <div>
                    <span>24-inch LED Monitor</span>
                    <p>A high-resolution display that delivers crystal-clear visuals for gaming, productivity, and everything in between.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Mouse Dropdown -->
    <div class="dropdown">
        <button>Mouse</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="mouse.jpg" alt="Mouse">
                <div>
                    <span>Wireless Precision Mouse</span>
                    <p>Perfect for everyday tasks, offering high precision with smooth tracking and ergonomic design for comfort.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Keyboard Dropdown -->
    <div class="dropdown">
        <button>Keyboard</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="keyboard.jpg" alt="Keyboard">
                <div>
                    <span>Mechanical RGB Keyboard</span>
                    <p>Fast, durable, and visually striking – this mechanical keyboard features customizable RGB lighting and tactile switches.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- PC Dropdown -->
    <div class="dropdown">
        <button>PC</button>
        <div class="dropdown-content">
            <div class="dropdown-item">
                <img src="pc.jpg" alt="PC">
                <div>
                    <span>Gaming Desktop PC</span>
                    <p>Packed with top-tier components, this PC is built for heavy-duty gaming and high-performance applications.</p>
                </div>
            </div>
        </div>
    </div>

</div>

<!-- JavaScript -->
<script>
    function toggleMenu() {
        document.getElementById('navMenu').classList.toggle
