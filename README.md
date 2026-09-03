<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <title>My School | Official School Website</title>


    <style>

        /* =========================
           GENERAL STYLING
        ========================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background: #f5f8fc;
            color: #222;
        }

        a {
            text-decoration: none;
        }

        section {
            padding: 70px 8%;
            scroll-margin-top: 80px;
        }

        .section-title {
            text-align: center;
            font-size: 32px;
            color: #123c69;
            margin-bottom: 40px;
        }


        /* =========================
           TOP BAR
        ========================== */

        .topbar {

            background: #123c69;

            color: white;

            padding: 10px 8%;

            display: flex;

            justify-content: space-between;

            flex-wrap: wrap;

            font-size: 14px;
        }


        /* =========================
           NAVBAR
        ========================== */

        header {

            background: white;

            position: sticky;

            top: 0;

            z-index: 1000;

            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .navbar {

            min-height: 75px;

            padding: 10px 8%;

            display: flex;

            align-items: center;

            justify-content: space-between;
        }

        .logo {

            font-size: 22px;

            font-weight: bold;

            color: #123c69;
        }

        .logo span {

            color: #f39c12;
        }

        .nav-links {

            display: flex;

            list-style: none;

            gap: 25px;
        }

        .nav-links a {

            color: #222;

            font-weight: bold;

            transition: 0.3s;
        }

        .nav-links a:hover {

            color: #f39c12;
        }

        .menu-btn {

            display: none;

            font-size: 28px;

            cursor: pointer;
        }


        /* =========================
           HOME / HERO
        ========================== */

        .hero {

            min-height: 650px;

            display: flex;

            align-items: center;

            justify-content: center;

            text-align: center;

            color: white;

            padding: 70px 8%;

            background:

                linear-gradient(
                    rgba(18,60,105,0.82),
                    rgba(18,60,105,0.82)
                ),

                url("https://images.unsplash.com/photo-1580582932707-520aed937b7b?auto=format&fit=crop&w=1600&q=80");

            background-size: cover;

            background-position: center;
        }

        .hero-content {

            width: 100%;

            max-width: 1100px;
        }

        .hero-content h1 {

            font-size: 52px;

            margin-bottom: 10px;
        }

        .hero-content h1 span {

            color: #f39c12;
        }

        .hero-content > p {

            font-size: 20px;

            margin-bottom: 25px;
        }


        /* =========================
           HOME MENU
        ========================== */

        .menu-title {

            font-size: 26px;

            margin-top: 25px;

            margin-bottom: 20px;
        }

        .home-menu {

            max-width: 1000px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(4, 1fr);

            gap: 15px;
        }

        .menu-card {

            background: white;

            color: #222;

            padding: 20px 12px;

            border-radius: 10px;

            text-align: center;

            box-shadow:
                0 4px 12px rgba(0,0,0,0.15);

            transition: 0.3s;
        }

        .menu-card:hover {

            transform: translateY(-7px);

            background: #f39c12;

            color: white;
        }

        .menu-icon {

            font-size: 35px;

            margin-bottom: 5px;
        }

        .menu-card h3 {

            color: #123c69;

            font-size: 17px;

            margin-bottom: 3px;
        }

        .menu-card:hover h3 {

            color: white;
        }

        .menu-card p {

            font-size: 12px;
        }


        /* =========================
           NOTICE
        ========================== */

        .notice {

            background: #fff3cd;

            padding: 15px 8%;

            text-align: center;

            font-weight: bold;
        }


        /* =========================
           ABOUT
        ========================== */

        .about-container {

            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 40px;

            align-items: center;
        }

        .about-box {

            background: white;

            padding: 30px;

            border-radius: 10px;

            box-shadow:
                0 4px 15px rgba(0,0,0,0.08);
        }

        .about-box h3 {

            color: #123c69;

            margin-bottom: 15px;
        }


        /* =========================
           STAFF
        ========================== */

        .staff-grid {

            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 25px;
        }

        .staff-card {

            background: white;

            padding: 30px;

            text-align: center;

            border-radius: 10px;

            box-shadow:
                0 4px 15px rgba(0,0,0,0.08);

            transition: 0.3s;
        }

        .staff-card:hover {

            transform: translateY(-5px);
        }

        .staff-icon {

            width: 80px;

            height: 80px;

            margin: auto;

            margin-bottom: 15px;

            border-radius: 50%;

            background: #123c69;

            color: white;

            display: flex;

            align-items: center;

            justify-content: center;

            font-size: 30px;
        }

        .staff-card h3 {

            color: #123c69;
        }


        /* =========================
           FACILITIES
        ========================== */

        .facility-grid {

            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 25px;
        }

        .facility-card {

            background: white;

            padding: 30px;

            border-radius: 10px;

            text-align: center;

            box-shadow:
                0 4px 15px rgba(0,0,0,0.08);

            transition: 0.3s;
        }

        .facility-card:hover {

            transform: translateY(-5px);
        }

        .facility-card .icon {

            font-size: 45px;

            margin-bottom: 15px;
        }

        .facility-card h3 {

            color: #123c69;

            margin-bottom: 10px;
        }


        /* =========================
           MEAL
        ========================== */

        .meal-box {

            max-width: 800px;

            margin: auto;

            background: white;

            padding: 30px;

            border-radius: 10px;

            text-align: center;

            box-shadow:
                0 4px 15px rgba(0,0,0,0.08);
        }

        .meal-items {

            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 15px;

            margin-top: 20px;
        }

        .meal-item {

            background: #f39c12;

            color: white;

            padding: 10px 18px;

            border-radius: 20px;

            font-weight: bold;
        }


        /* =========================
           SPORTS
        ========================== */

        .sports {

            background: #eaf2f8;
        }

        .sports-list {

            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 20px;
        }

        .sport {

            background: white;

            padding: 20px 30px;

            border-radius: 8px;

            font-weight: bold;

            box-shadow:
                0 3px 10px rgba(0,0,0,0.08);

            transition: 0.3s;
        }

        .sport:hover {

            transform: translateY(-5px);
        }


        /* =========================
           ACTIVITIES
        ========================== */

        .activities {

            background: white;
        }

        .activity-box {

            max-width: 800px;

            margin: auto;

            background: #f5f8fc;

            padding: 30px;

            border-left:
                5px solid #123c69;

            border-radius: 5px;
        }


        /* =========================
           CONTACT
        ========================== */

        .contact-container {

            max-width: 700px;

            margin: auto;
        }

        .contact-info {

            background: white;

            padding: 30px;

            border-radius: 10px;

            box-shadow:
                0 4px 15px rgba(0,0,0,0.08);
        }

        .contact-info h3 {

            color: #123c69;

            margin-bottom: 15px;
        }

        .contact-info p {

            margin: 12px 0;
        }


        /* =========================
           FOOTER
        ========================== */

        footer {

            background: #123c69;

            color: white;

            text-align: center;

            padding: 30px 8%;
        }

        .footer-links {

            margin-bottom: 15px;
        }

        .footer-links a {

            color: white;

            margin: 0 10px;
        }


        /* =========================
           RESPONSIVE DESIGN
        ========================== */

        @media (max-width: 900px) {

            .menu-btn {

                display: block;
            }

            .nav-links {

                display: none;

                position: absolute;

                top: 75px;

                left: 0;

                width: 100%;

                background: white;

                flex-direction: column;

                padding: 20px;

                text-align: center;

                box-shadow:
                    0 5px 10px rgba(0,0,0,0.1);
            }

            .nav-links.active {

                display: flex;
            }

            .hero-content h1 {

                font-size: 40px;
            }

            .home-menu {

                grid-template-columns:
                    repeat(2, 1fr);
            }

            .about-container {

                grid-template-columns: 1fr;
            }

            .staff-grid,
            .facility-grid {

                grid-template-columns:
                    1fr 1fr;
            }
        }


        @media (max-width: 600px) {

            .topbar {

                text-align: center;

                justify-content: center;

                gap: 5px;
            }

            section {

                padding: 50px 5%;
            }

            .navbar {

                padding: 10px 5%;
            }

            .hero {

                min-height: 750px;

                padding: 50px 5%;
            }

            .hero-content h1 {

                font-size: 32px;
            }

            .hero-content > p {

                font-size: 17px;
            }

            .menu-title {

                font-size: 22px;
            }

            .home-menu {

                grid-template-columns:
                    repeat(2, 1fr);

                gap: 10px;
            }

            .menu-card {

                padding: 15px 5px;
            }

            .menu-icon {

                font-size: 28px;
            }

            .menu-card h3 {

                font-size: 15px;
            }

            .staff-grid,
            .facility-grid {

                grid-template-columns: 1fr;
            }

            .section-title {

                font-size: 27px;
            }
        }

    </style>

</head>


<body>


    <!-- =========================
         TOP BAR
    ========================== -->

    <div class="topbar">

        <div>
            Welcome to Our School
        </div>

        <div>
            Admissions • Academics • Activities
        </div>

    </div>



    <!-- =========================
         NAVIGATION
    ========================== -->

    <header>

        <nav class="navbar">

            <div class="logo">

                MY <span>SCHOOL</span>

            </div>


            <!-- Mobile Menu Button -->

            <div
                class="menu-btn"
                onclick="toggleMenu()">

                ☰

            </div>


            <ul
                class="nav-links"
                id="navLinks">


                <li>
                    <a
                        href="#home"
                        onclick="closeMenu()">

                        Home

                    </a>
                </li>


                <li>
                    <a
                        href="#about"
                        onclick="closeMenu()">

                        About

                    </a>
                </li>


                <li>
                    <a
                        href="#staff"
                        onclick="closeMenu()">

                        Staff

                    </a>
                </li>


                <li>
                    <a
                        href="#facilities"
                        onclick="closeMenu()">

                        Facilities

                    </a>
                </li>


                <li>
                    <a
                        href="#sports"
                        onclick="closeMenu()">

                        Sports

                    </a>
                </li>


                <li>
                    <a
                        href="#activities"
                        onclick="closeMenu()">

                        Activities

                    </a>
                </li>


                <li>
                    <a
                        href="#contact"
                        onclick="closeMenu()">

                        Contact

                    </a>
                </li>

            </ul>

        </nav>

    </header>



    <!-- =========================
         HOME
    ========================== -->

    <section
        class="hero"
        id="home">


        <div class="hero-content">


            <h1>

                Welcome to
                <span>Our School</span>

            </h1>


            <p>

                Education • Knowledge • Discipline • Success

            </p>



            <!-- HOME MENU -->

            <h2 class="menu-title">

                What do you want to see?

            </h2>



            <div class="home-menu">


                <!-- HOME -->

                <a
                    href="#home"
                    class="menu-card">

                    <div class="menu-icon">
                        🏠
                    </div>

                    <h3>
                        Home
                    </h3>

                    <p>
                        School Home
                    </p>

                </a>



                <!-- ABOUT -->

                <a
                    href="#about"
                    class="menu-card">

                    <div class="menu-icon">
                        🏫
                    </div>

                    <h3>
                        About
                    </h3>

                    <p>
                        About Our School
                    </p>

                </a>



                <!-- STAFF -->

                <a
                    href="#staff"
                    class="menu-card">

                    <div class="menu-icon">
                        👩‍🏫
                    </div>

                    <h3>
                        Staff
                    </h3>

                    <p>
                        Teaching Staff
                    </p>

                </a>



                <!-- FACILITIES -->

                <a
                    href="#facilities"
                    class="menu-card">

                    <div class="menu-icon">
                        🔬
                    </div>

                    <h3>
                        Facilities
                    </h3>

                    <p>
                        School Facilities
                    </p>

                </a>



                <!-- SPORTS -->

                <a
                    href="#sports"
                    class="menu-card">

                    <div class="menu-icon">
                        🏏
                    </div>

                    <h3>
                        Sports
                    </h3>

                    <p>
                        Sports Facilities
                    </p>

                </a>



                <!-- MEAL -->

                <a
                    href="#meal"
                    class="menu-card">

                    <div class="menu-icon">
                        🍛
                    </div>

                    <h3>
                        Meal
                    </h3>

                    <p>
                        School Meal
                    </p>

                </a>



                <!-- ACTIVITIES -->

                <a
                    href="#activities"
                    class="menu-card">

                    <div class="menu-icon">
                        🎵
                    </div>

                    <h3>
                        Activities
                    </h3>

                    <p>
                        Music & Activities
                    </p>

                </a>



                <!-- CONTACT -->

                <a
                    href="#contact"
                    class="menu-card">

                    <div class="menu-icon">
                        📞
                    </div>

                    <h3>
                        Contact
                    </h3>

                    <p>
                        Contact School
                    </p>

                </a>


            </div>

        </div>

    </section>



    <!-- =========================
         NOTICE
    ========================== -->

    <div class="notice">

        📢 Admissions and school information
        will be updated here.

    </div>



    <!-- =========================
         ABOUT
    ========================== -->

    <section id="about">


        <h2 class="section-title">

            About Our School

        </h2>


        <div class="about-container">


            <div class="about-box">

                <h3>
                    Our School
                </h3>

                <p>

                    Our school provides students
                    with a supportive environment
                    for academic learning, sports,
                    creativity and overall development.

                </p>

                <br>

                <p>

                    We focus on Mathematics, Science
                    and other subjects while encouraging
                    students to participate in activities
                    and sports.

                </p>

            </div>



            <div class="about-box">

                <h3>
                    School Leadership
                </h3>

                <p>

                    <strong>
                        Head Master:
                    </strong>

                    Mr. Vanita Vinod Manikar

                </p>

                <br>

                <p>

                    The school works to provide
                    quality education, discipline
                    and opportunities for students.

                </p>

            </div>


        </div>

    </section>



    <!-- =========================
         STAFF
    ========================== -->

    <section id="staff">


        <h2 class="section-title">

            Our Teaching Staff

        </h2>


        <div class="staff-grid">


            <div class="staff-card">

                <div class="staff-icon">
                    👩‍🏫
                </div>

                <h3>
                    Vanita Mam
                </h3>

                <p>
                    Mathematics & Science
                </p>

            </div>



            <div class="staff-card">

                <div class="staff-icon">
                    👩‍🏫
                </div>

                <h3>
                    Subhangi Gatte
                </h3>

                <p>
                    All Subjects
                </p>

            </div>



            <div class="staff-card">

                <div class="staff-icon">
                    👨‍🏫
                </div>

                <h3>
                    Kishor Choudhary
                </h3>

                <p>
                    All Subjects
                </p>

            </div>


        </div>

    </section>



    <!-- =========================
         FACILITIES
    ========================== -->

    <section id="facilities">


        <h2 class="section-title">

            School Facilities

        </h2>


        <div class="facility-grid">


            <div class="facility-card">

                <div class="icon">
                    🔬
                </div>

                <h3>
                    Science Laboratory
                </h3>

                <p>

                    Equipped with skeleton models
                    and chemical equipment.

                </p>

            </div>



            <div class="facility-card">

                <div class="icon">
                    📚
                </div>

                <h3>
                    Library
                </h3>

                <p>

                    A learning space for students
                    to read and study.

                </p>

            </div>



            <div class="facility-card">

                <div class="icon">
                    💻
                </div>

                <h3>
                    Computer Lab
                </h3>

                <p>

                    Computer facilities for
                    digital learning.

                </p>

            </div>



            <div class="facility-card">

                <div class="icon">
                    📐
                </div>

                <h3>
                    Maths Lab
                </h3>

                <p>

                    Practical learning and
                    mathematical activities.

                </p>

            </div>



            <div class="facility-card">

                <div class="icon">
                    🎵
                </div>

                <h3>
                    Activity Room
                </h3>

                <p>

                    Creative activities
                    for students.

                </p>

            </div>



            <div class="facility-card">

                <div class="icon">
                    🚰
                </div>

                <h3>
                    Drinking Water
                </h3>

                <p>

                    Drinking water facility
                    for students.

                </p>

            </div>


        </div>

    </section>



    <!-- =========================
         SCHOOL MEAL
    ========================== -->

    <section id="meal">


        <h2 class="section-title">

            School Meal

        </h2>


        <div class="meal-box">


            <p>

                The school provides meals including
                nutritious food items for students.

            </p>


            <div class="meal-items">


                <span class="meal-item">
                    Dal
                </span>


                <span class="meal-item">
                    Chawal
                </span>


                <span class="meal-item">
                    Vegetable
                </span>


                <span class="meal-item">
                    Pulses
                </span>


                <span class="meal-item">
                    Masala
                </span>


                <span class="meal-item">
                    Bhatt
                </span>


            </div>

        </div>

    </section>



    <!-- =========================
         SPORTS
    ========================== -->

    <section
        class="sports"
        id="sports">


        <h2 class="section-title">

            Sports Facilities

        </h2>


        <div class="sports-list">


            <div class="sport">

                🏏 Cricket

            </div>


            <div class="sport">

                🏸 Badminton

            </div>


            <div class="sport">

                🏃 Running

            </div>


        </div>

    </section>



    <!-- =========================
         ACTIVITIES
    ========================== -->

    <section
        class="activities"
        id="activities">


        <h2 class="section-title">

            Activity & Music Room

        </h2>


        <div class="activity-box">


            <h3>

                Creative Activities

            </h3>


            <p>

                The school has an activity room
                where students can participate in
                creative activities.

            </p>


            <br>


            <p>

                Available instruments include:

            </p>


            <br>


            <strong>

                🎹 Harmonium & 🥁 Tabla

            </strong>


        </div>

    </section>



    <!-- =========================
         CONTACT
    ========================== -->

    <section id="contact">


        <h2 class="section-title">

            Contact Us

        </h2>


        <div class="contact-container">


            <div class="contact-info">


                <h3>

                    School Contact Information

                </h3>


                <p>

                    👨‍💼

                    <strong>
                        Head Master:
                    </strong>

                    Mr. Vanita Vinod Manikar

                </p>


                <p>

                    📞

                    <strong>
                        Phone:
                    </strong>

                    YOUR SCHOOL PHONE NUMBER

                </p>


                <p>

                    📧

                    <strong>
                        Email:
                    </strong>

                    school@example.com

                </p>


                <p>

                    📍

                    <strong>
                        Address:
                    </strong>

                    Fetri, Maharashtra

                </p>


            </div>

        </div>

    </section>



    <!-- =========================
         FOOTER
    ========================== -->

    <footer>


        <div class="footer-links">


            <a href="#home">
                Home
            </a>


            <a href="#about">
                About
            </a>


            <a href="#staff">
                Staff
            </a>


            <a href="#facilities">
                Facilities
            </a>


            <a href="#sports">
                Sports
            </a>


            <a href="#activities">
                Activities
            </a>


            <a href="#contact">
                Contact
            </a>


        </div>


        <p>

            © 2026 My School.
            All Rights Reserved.

        </p>


    </footer>



    <!-- =========================
         JAVASCRIPT
    ========================== -->

    <script>


        /* Mobile Menu */

        function toggleMenu() {

            document
                .getElementById("navLinks")
                .classList.toggle("active");

        }


        /* Close Mobile Menu */

        function closeMenu() {

            document
                .getElementById("navLinks")
                .classList.remove("active");

        }


    </script>


</body>

</html>
