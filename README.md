<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

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

        .container {
            width: 84%;
            max-width: 1200px;
            margin: auto;
        }

        section {
            padding: 70px 0;
        }

        .section-title {
            text-align: center;
            font-size: 34px;
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
            align-items: center;

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

            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.12);
        }

        .navbar {
            width: 84%;
            max-width: 1200px;
            min-height: 75px;

            margin: auto;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #123c69;
        }

        .logo span {
            color: #f39c12;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 20px;
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
            font-size: 30px;
            cursor: pointer;
        }


        /* =========================
           ALL PAGES / SECTIONS
        ========================== */

        .page {
            display: none;
            min-height: 600px;
        }

        .page.active {
            display: block;
        }


        /* =========================
           HOME
        ========================== */

        .hero {
            min-height: 600px;

            display: flex;
            align-items: center;
            justify-content: center;

            text-align: center;

            color: white;

            padding: 80px 20px;

            background:
                linear-gradient(
                    rgba(18, 60, 105, 0.82),
                    rgba(18, 60, 105, 0.82)
                ),
                url("https://images.unsplash.com/photo-1580582932707-520aed937b7b?auto=format&fit=crop&w=1600&q=80");

            background-size: cover;
            background-position: center;
        }

        .school-icon {
            width: 100px;
            height: 100px;

            margin: 0 auto 25px;

            background: white;

            border-radius: 50%;

            display: flex;
            align-items: center;
            justify-content: center;

            font-size: 50px;
        }

        .hero h1 {
            font-size: 55px;
            margin-bottom: 15px;
        }

        .hero h1 span {
            color: #f39c12;
        }

        .hero p {
            font-size: 21px;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;

            background: #f39c12;
            color: white;

            padding: 13px 28px;

            border-radius: 6px;

            font-weight: bold;

            border: none;

            cursor: pointer;

            transition: 0.3s;
        }

        .btn:hover {
            background: #d68910;
            transform: translateY(-3px);
        }


        /* =========================
           NOTICE
        ========================== */

        .notice {
            background: #fff3cd;

            padding: 15px;

            text-align: center;

            font-weight: bold;
        }


        /* =========================
           HOME MENU CARDS
        ========================== */

        .home-menu {
            padding: 70px 0;
        }

        .cards {
            display: grid;

            grid-template-columns: repeat(3, 1fr);

            gap: 25px;
        }

        .card {
            background: white;

            padding: 30px;

            border-radius: 12px;

            text-align: center;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);

            transition: 0.3s;

            color: #222;

            cursor: pointer;
        }

        .card:hover {
            transform: translateY(-7px);
        }

        .card-icon {
            font-size: 45px;
            margin-bottom: 15px;
        }

        .card h3 {
            color: #123c69;
            margin-bottom: 10px;
        }


        /* =========================
           PAGE HEADER
        ========================== */

        .page-header {
            background: #123c69;

            color: white;

            text-align: center;

            padding: 70px 20px;
        }

        .page-header h1 {
            font-size: 45px;
        }

        .page-header p {
            font-size: 18px;
            margin-top: 10px;
        }


        /* =========================
           ABOUT
        ========================== */

        .about-grid {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 35px;
        }

        .about-box {
            background: white;

            padding: 35px;

            border-radius: 12px;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        .about-box h2 {
            color: #123c69;

            margin-bottom: 15px;
        }


        /* =========================
           STAFF
        ========================== */

        .staff-grid {
            display: grid;

            grid-template-columns: repeat(3, 1fr);

            gap: 25px;
        }

        .staff-card {
            background: white;

            padding: 30px;

            border-radius: 12px;

            text-align: center;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);

            transition: 0.3s;
        }

        .staff-card:hover {
            transform: translateY(-6px);
        }

        .staff-icon {
            width: 90px;
            height: 90px;

            margin: auto;
            margin-bottom: 15px;

            border-radius: 50%;

            background: #123c69;

            color: white;

            display: flex;
            align-items: center;
            justify-content: center;

            font-size: 40px;
        }

        .staff-card h3 {
            color: #123c69;
        }


        /* =========================
           FACILITIES
        ========================== */

        .facility-grid {
            display: grid;

            grid-template-columns: repeat(3, 1fr);

            gap: 25px;
        }

        .facility-card {
            background: white;

            padding: 30px;

            border-radius: 12px;

            text-align: center;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);

            transition: 0.3s;
        }

        .facility-card:hover {
            transform: translateY(-6px);
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
           SPORTS
        ========================== */

        .sports-section {
            background: #eaf2f8;
        }

        .sports-list {
            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 25px;
        }

        .sport-box {
            background: white;

            padding: 30px 45px;

            border-radius: 12px;

            font-size: 20px;

            font-weight: bold;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);

            transition: 0.3s;
        }

        .sport-box:hover {
            transform: translateY(-5px);
        }


        /* =========================
           MEAL
        ========================== */

        .meal-box {
            max-width: 800px;

            margin: auto;

            background: white;

            padding: 35px;

            text-align: center;

            border-radius: 12px;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        .meal-box h2 {
            color: #123c69;
        }

        .meal-items {
            margin-top: 25px;

            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 12px;
        }

        .meal-item {
            background: #f39c12;

            color: white;

            padding: 10px 20px;

            border-radius: 25px;

            font-weight: bold;
        }


        /* =========================
           ACTIVITIES
        ========================== */

        .activity-box {
            max-width: 850px;

            margin: auto;

            background: white;

            padding: 35px;

            border-left: 6px solid #123c69;

            border-radius: 8px;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        .activity-box h2,
        .activity-box h3 {
            color: #123c69;
        }


        /* =========================
           CONTACT
        ========================== */

        .contact-grid {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 30px;
        }

        .contact-box {
            background: white;

            padding: 35px;

            border-radius: 12px;

            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        .contact-box h3 {
            color: #123c69;

            margin-bottom: 20px;
        }

        .contact-box p {
            margin: 15px 0;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;

            padding: 13px;

            margin-bottom: 15px;

            border: 1px solid #ccc;

            border-radius: 6px;

            font-size: 15px;
        }

        .contact-form textarea {
            height: 130px;

            resize: vertical;
        }


        /* =========================
           BACK HOME BUTTON
        ========================== */

        .back-home {
            text-align: center;

            margin-top: 40px;
        }


        /* =========================
           FOOTER
        ========================== */

        footer {
            background: #123c69;

            color: white;

            text-align: center;

            padding: 30px 20px;
        }

        .footer-links {
            margin-bottom: 15px;
        }

        .footer-links a {
            color: white;

            margin: 0 8px;

            cursor: pointer;
        }

        .footer-links a:hover {
            color: #f39c12;
        }


        /* =========================
           MOBILE
        ========================== */

        @media (max-width: 1000px) {

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

                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            }

            .nav-links.active {
                display: flex;
            }

            .cards,
            .staff-grid,
            .facility-grid {
                grid-template-columns: 1fr 1fr;
            }

            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .hero h1 {
                font-size: 45px;
            }
        }


        @media (max-width: 600px) {

            .topbar {
                flex-direction: column;

                text-align: center;

                gap: 5px;
            }

            .navbar,
            .container {
                width: 90%;
            }

            .hero {
                min-height: 550px;
            }

            .hero h1 {
                font-size: 35px;
            }

            .hero p {
                font-size: 17px;
            }

            .cards,
            .staff-grid,
            .facility-grid {
                grid-template-columns: 1fr;
            }

            .page-header h1 {
                font-size: 35px;
            }

            .section-title {
                font-size: 28px;
            }

            .sport-box {
                width: 100%;
                text-align: center;
            }

        }

    </style>

</head>


<body>


<!-- =====================================================
     TOP BAR
===================================================== -->

<div class="topbar">

    <div>
        Welcome to Our School
    </div>

    <div>
        Admissions • Academics • Activities
    </div>

</div>


<!-- =====================================================
     NAVIGATION
===================================================== -->

<header>

    <nav class="navbar">

        <div class="logo">
            MY <span>SCHOOL</span>
        </div>


        <div class="menu-btn"
             onclick="toggleMenu()">
            ☰
        </div>


        <ul class="nav-links"
            id="navLinks">

            <li>
                <a href="#home"
                   onclick="showPage('home')">
                    Home
                </a>
            </li>

            <li>
                <a href="#about"
                   onclick="showPage('about')">
                    About
                </a>
            </li>

            <li>
                <a href="#staff"
                   onclick="showPage('staff')">
                    Staff
                </a>
            </li>

            <li>
                <a href="#facilities"
                   onclick="showPage('facilities')">
                    Facilities
                </a>
            </li>

            <li>
                <a href="#sports"
                   onclick="showPage('sports')">
                    Sports
                </a>
            </li>

            <li>
                <a href="#meal"
                   onclick="showPage('meal')">
                    Meal
                </a>
            </li>

            <li>
                <a href="#activities"
                   onclick="showPage('activities')">
                    Activities
                </a>
            </li>

            <li>
                <a href="#contact"
                   onclick="showPage('contact')">
                    Contact
                </a>
            </li>

        </ul>

    </nav>

</header>


<!-- =====================================================
     HOME PAGE
===================================================== -->

<div id="home"
     class="page active">


    <section class="hero">

        <div>

            <div class="school-icon">
                🎓
            </div>

            <h1>
                Welcome to
                <span>Our School</span>
            </h1>

            <p>
                Education • Knowledge • Discipline • Success
            </p>

        </div>

    </section>


    <div class="notice">

        📢 Admissions and school information
        will be updated here.

    </div>


    <section class="home-menu">

        <div class="container">

            <h2 class="section-title">
                What Would You Like To See?
            </h2>


            <div class="cards">


                <div class="card"
                     onclick="showPage('about')">

                    <div class="card-icon">
                        🏫
                    </div>

                    <h3>
                        About School
                    </h3>

                    <p>
                        Learn about our school,
                        vision and leadership.
                    </p>

                </div>


                <div class="card"
                     onclick="showPage('staff')">

                    <div class="card-icon">
                        👩‍🏫
                    </div>

                    <h3>
                        Teaching Staff
                    </h3>

                    <p>
                        Meet our dedicated
                        teaching staff.
                    </p>

                </div>


                <div class="card"
                     onclick="showPage('facilities')">

                    <div class="card-icon">
                        🔬
                    </div>

                    <h3>
                        Facilities
                    </h3>

                    <p>
                        Explore our school
                        facilities.
                    </p>

                </div>


                <div class="card"
                     onclick="showPage('sports')">

                    <div class="card-icon">
                        🏏
                    </div>

                    <h3>
                        Sports
                    </h3>

                    <p>
                        Explore sports and
                        physical activities.
                    </p>

                </div>


                <div class="card"
                     onclick="showPage('meal')">

                    <div class="card-icon">
                        🍛
                    </div>

                    <h3>
                        School Meal
                    </h3>

                    <p>
                        Information about
                        school meals.
                    </p>

                </div>


                <div class="card"
                     onclick="showPage('activities')">

                    <div class="card-icon">
                        🎵
                    </div>

                    <h3>
                        Activities
                    </h3>

                    <p>
                        Creative and musical
                        activities.
                    </p>

                </div>


                <div class="card"
                     onclick="showPage('contact')">

                    <div class="card-icon">
                        📞
                    </div>

                    <h3>
                        Contact Us
                    </h3>

                    <p>
                        Contact information
                        of our school.
                    </p>

                </div>


            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     ABOUT PAGE
===================================================== -->

<div id="about"
     class="page">


    <div class="page-header">

        <h1>
            About Our School
        </h1>

        <p>
            Learn more about our school
        </p>

    </div>


    <section>

        <div class="container">

            <div class="about-grid">


                <div class="about-box">

                    <h2>
                        Our School
                    </h2>

                    <br>

                    <p>
                        Our school provides students
                        with a supportive environment
                        for academic learning, sports,
                        creativity and overall development.
                    </p>

                    <br>

                    <p>
                        We focus on Mathematics,
                        Science and other subjects
                        while encouraging students
                        to participate in activities
                        and sports.
                    </p>

                </div>


                <div class="about-box">

                    <h2>
                        School Leadership
                    </h2>

                    <br>

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


            <div class="back-home">

                <button class="btn"
                        onclick="showPage('home')">
                    ← Back to Home
                </button>

            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     STAFF PAGE
===================================================== -->

<div id="staff"
     class="page">


    <div class="page-header">

        <h1>
            Our Teaching Staff
        </h1>

        <p>
            Meet our dedicated teachers
        </p>

    </div>


    <section>

        <div class="container">

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


            <div class="back-home">

                <button class="btn"
                        onclick="showPage('home')">
                    ← Back to Home
                </button>

            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     FACILITIES PAGE
===================================================== -->

<div id="facilities"
     class="page">


    <div class="page-header">

        <h1>
            School Facilities
        </h1>

        <p>
            Facilities available for students
        </p>

    </div>


    <section>

        <div class="container">

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


            <div class="back-home">

                <button class="btn"
                        onclick="showPage('home')">
                    ← Back to Home
                </button>

            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     SPORTS PAGE
===================================================== -->

<div id="sports"
     class="page">


    <div class="page-header">

        <h1>
            Sports Facilities
        </h1>

        <p>
            Sports and physical activities
        </p>

    </div>


    <section class="sports-section">

        <div class="container">

            <div class="sports-list">


                <div class="sport-box">
                    🏏 Cricket
                </div>


                <div class="sport-box">
                    🏸 Badminton
                </div>


                <div class="sport-box">
                    🏃 Running
                </div>


            </div>


            <div class="back-home">

                <button class="btn"
                        onclick="showPage('home')">
                    ← Back to Home
                </button>

            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     MEAL PAGE
===================================================== -->

<div id="meal"
     class="page">


    <div class="page-header">

        <h1>
            School Meal
        </h1>

        <p>
            Nutritious food for students
        </p>

    </div>


    <section>

        <div class="container">

            <div class="meal-box">

                <h2>
                    School Meal Program
                </h2>

                <br>

                <p>
                    The school provides meals
                    including nutritious food
                    items for students.
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


            <div class="back-home">

                <button class="btn"
                        onclick="showPage('home')">
                    ← Back to Home
                </button>

            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     ACTIVITIES PAGE
===================================================== -->

<div id="activities"
     class="page">


    <div class="page-header">

        <h1>
            Activity & Music Room
        </h1>

        <p>
            Creative and musical activities
        </p>

    </div>


    <section>

        <div class="container">

            <div class="activity-box">

                <h2>
                    Creative Activities
                </h2>

                <br>

                <p>
                    The school has an activity room
                    where students can participate
                    in creative activities.
                </p>

                <br>

                <p>
                    Students can participate in
                    various educational and
                    creative activities.
                </p>

                <br>

                <h3>
                    Musical Instruments
                </h3>

                <br>

                <p>
                    🎹 Harmonium
                </p>

                <p>
                    🥁 Tabla
                </p>

            </div>


            <div class="back-home">

                <button class="btn"
                        onclick="showPage('home')">
                    ← Back to Home
                </button>

            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     CONTACT PAGE
===================================================== -->

<div id="contact"
     class="page">


    <div class="page-header">

        <h1>
            Contact Us
        </h1>

        <p>
            Get in touch with our school
        </p>

    </div>


    <section>

        <div class="container">

            <div class="contact-grid">


                <!-- CONTACT INFORMATION -->

                <div class="contact-box">

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


                <!-- CONTACT FORM -->

                <div class="contact-box contact-form">

                    <h3>
                        Send Us a Message
                    </h3>


                    <form id="contactForm">

                        <input
                            type="text"
                            id="name"
                            placeholder="Your Name"
                            required
                        >


                        <input
                            type="email"
                            placeholder="Your Email"
                            required
                        >


                        <input
                            type="text"
                            placeholder="Subject"
                            required
                        >


                        <textarea
                            placeholder="Your Message"
                            required>
                        </textarea>


                        <button
                            type="submit"
                            class="btn">

                            Send Message

                        </button>

                    </form>

                </div>


            </div>


            <div class="back-home">

                <button class="btn"
                        onclick="showPage('home')">
                    ← Back to Home
                </button>

            </div>

        </div>

    </section>

</div>


<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

    <div class="footer-links">

        <a onclick="showPage('home')">
            Home
        </a>

        <a onclick="showPage('about')">
            About
        </a>

        <a onclick="showPage('staff')">
            Staff
        </a>

        <a onclick="showPage('facilities')">
            Facilities
        </a>

        <a onclick="showPage('sports')">
            Sports
        </a>

        <a onclick="showPage('meal')">
            Meal
        </a>

        <a onclick="showPage('activities')">
            Activities
        </a>

        <a onclick="showPage('contact')">
            Contact
        </a>

    </div>

    <p>
        © 2026 My School. All Rights Reserved.
    </p>

</footer>


<!-- =====================================================
     JAVASCRIPT
===================================================== -->

<script>

    /* =========================
       SHOW SELECTED PAGE
    ========================== */

    function showPage(pageId) {

        // Hide all pages

        const pages =
            document.querySelectorAll(".page");

        pages.forEach(function(page) {

            page.classList.remove("active");

        });


        // Show selected page

        const selectedPage =
            document.getElementById(pageId);

        if (selectedPage) {

            selectedPage.classList.add("active");

        }


        // Close mobile menu

        document
            .getElementById("navLinks")
            .classList.remove("active");


        // Go to top

        window.scrollTo({
            top: 0,
            behavior: "smooth"
        });

    }


    /* =========================
       MOBILE MENU
    ========================== */

    function toggleMenu() {

        document
            .getElementById("navLinks")
            .classList.toggle("active");

    }


    /* =========================
       CONTACT FORM
    ========================== */

    const contactForm =
        document.getElementById("contactForm");


    if (contactForm) {

        contactForm.addEventListener(
            "submit",
            function(event) {

                event.preventDefault();

                const name =
                    document.getElementById("name").value;


                alert(
                    "Thank you, " +
                    name +
                    "! Your message has been received."
                );


                contactForm.reset();

            }
        );

    }

</script>


</body>

</html>
