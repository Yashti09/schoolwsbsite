<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="My School - Official School Website">
    <title>My School | Official School Website</title>

    <style>
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

        button, input, textarea {
            font-family: inherit;
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

        .topbar {
            background: #123c69;
            color: white;
            padding: 10px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 14px;
        }

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
            cursor: pointer;
        }

        .nav-links a:hover,
        .nav-links a.active-link {
            color: #f39c12;
        }

        .menu-btn {
            display: none;
            font-size: 30px;
            cursor: pointer;
            border: none;
            background: none;
        }

        .page {
            display: none;
            min-height: 600px;
        }

        .page.active {
            display: block;
        }

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

        .hero-content {
            max-width: 900px;
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

        .notice {
            background: #fff3cd;
            padding: 15px;
            text-align: center;
            font-weight: bold;
        }

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

        .about-grid,
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 35px;
        }

        .about-box,
        .contact-box {
            background: white;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        .about-box h2,
        .contact-box h3 {
            color: #123c69;
            margin-bottom: 15px;
        }

        .about-box p {
            margin-bottom: 12px;
        }

        .highlight-list {
            list-style: none;
            margin-top: 15px;
        }

        .highlight-list li {
            padding: 9px 0;
            border-bottom: 1px solid #eee;
        }

        .staff-grid,
        .facility-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .staff-card,
        .facility-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            transition: 0.3s;
        }

        .staff-card:hover,
        .facility-card:hover {
            transform: translateY(-6px);
        }

        .staff-icon {
            width: 90px;
            height: 90px;
            margin: auto auto 15px;
            border-radius: 50%;
            background: #123c69;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
        }

        .staff-card h3,
        .facility-card h3 {
            color: #123c69;
            margin-bottom: 10px;
        }

        .facility-card .icon {
            font-size: 45px;
            margin-bottom: 15px;
        }

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

        .meal-box,
        .activity-box {
            max-width: 850px;
            margin: auto;
            background: white;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        .meal-box {
            text-align: center;
        }

        .meal-box h2,
        .activity-box h2,
        .activity-box h3 {
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

        .activity-box {
            border-left: 6px solid #123c69;
        }

        .activity-box h3 {
            margin-top: 22px;
            margin-bottom: 8px;
        }

        .activity-box ul {
            margin-left: 20px;
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

        .form-message {
            margin-top: 15px;
            font-weight: bold;
        }

        .back-home {
            text-align: center;
            margin-top: 40px;
        }

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

    <!-- TOP BAR -->
    <div class="topbar">
        <div>Welcome to Our School</div>
        <div>Admissions • Academics • Activities</div>
    </div>

    <!-- NAVIGATION -->
    <header>
        <nav class="navbar">
            <div class="logo">MY <span>SCHOOL</span></div>

            <button class="menu-btn" onclick="toggleMenu()" aria-label="Open menu">☰</button>

            <ul class="nav-links" id="navLinks">
                <li><a class="nav-link active-link" onclick="showPage('home', this)">Home</a></li>
                <li><a class="nav-link" onclick="showPage('about', this)">About</a></li>
                <li><a class="nav-link" onclick="showPage('staff', this)">Staff</a></li>
                <li><a class="nav-link" onclick="showPage('facilities', this)">Facilities</a></li>
                <li><a class="nav-link" onclick="showPage('sports', this)">Sports</a></li>
                <li><a class="nav-link" onclick="showPage('meal', this)">Meal</a></li>
                <li><a class="nav-link" onclick="showPage('activities', this)">Activities</a></li>
                <li><a class="nav-link" onclick="showPage('contact', this)">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- HOME -->
    <main>
        <div id="home" class="page active">
            <section class="hero">
                <div class="hero-content">
                    <div class="school-icon">🎓</div>
                    <h1>Welcome to <span>Our School</span></h1>
                    <p>Education • Knowledge • Discipline • Success</p>
                    <button class="btn" onclick="showPage('about')">Discover Our School</button>
                </div>
            </section>

            <div class="notice">
                📢 Admissions are open for the new academic session!
            </div>

            <section class="home-menu">
                <div class="container">
                    <h2 class="section-title">Explore Our School</h2>

                    <div class="cards">
                        <div class="card" onclick="showPage('about')">
                            <div class="card-icon">🏫</div>
                            <h3>About Us</h3>
                            <p>Learn about our vision, mission and educational values.</p>
                        </div>

                        <div class="card" onclick="showPage('staff')">
                            <div class="card-icon">👨‍🏫</div>
                            <h3>Our Staff</h3>
                            <p>Meet our dedicated teachers and school staff.</p>
                        </div>

                        <div class="card" onclick="showPage('facilities')">
                            <div class="card-icon">🔬</div>
                            <h3>Facilities</h3>
                            <p>Explore our classrooms, laboratories, library and more.</p>
                        </div>

                        <div class="card" onclick="showPage('sports')">
                            <div class="card-icon">⚽</div>
                            <h3>Sports</h3>
                            <p>Encouraging teamwork, fitness and sporting talent.</p>
                        </div>

                        <div class="card" onclick="showPage('meal')">
                            <div class="card-icon">🍱</div>
                            <h3>School Meal</h3>
                            <p>Information about nutritious meals provided at school.</p>
                        </div>

                        <div class="card" onclick="showPage('activities')">
                            <div class="card-icon">🎨</div>
                            <h3>Activities</h3>
                            <p>Discover cultural, academic and creative activities.</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!-- ABOUT -->
        <div id="about" class="page">
            <div class="page-header">
                <h1>About Our School</h1>
                <p>Building knowledge, character and confidence.</p>
            </div>

            <section>
                <div class="container about-grid">
                    <div class="about-box">
                        <h2>Who We Are</h2>
                        <p>
                            My School is committed to providing students with a supportive
                            environment where they can learn, grow and achieve their goals.
                        </p>
                        <p>
                            We focus on academic excellence, discipline, creativity,
                            teamwork and responsible citizenship.
                        </p>
                    </div>

                    <div class="about-box">
                        <h2>Our Vision</h2>
                        <p>
                            To create confident, knowledgeable and responsible students
                            who are prepared for the future.
                        </p>

                        <ul class="highlight-list">
                            <li>✓ Quality education</li>
                            <li>✓ Strong values and discipline</li>
                            <li>✓ Modern learning environment</li>
                            <li>✓ Sports and extracurricular activities</li>
                            <li>✓ Student-focused development</li>
                        </ul>
                    </div>
                </div>
            </section>

            <div class="back-home">
                <button class="btn" onclick="showPage('home')">← Back to Home</button>
            </div>
        </div>

        <!-- STAFF -->
        <div id="staff" class="page">
            <div class="page-header">
                <h1>Our Staff</h1>
                <p>Dedicated people who support student success.</p>
            </div>

            <section>
                <div class="container">
                    <div class="staff-grid">
                        <div class="staff-card">
                            <div class="staff-icon">👨‍💼</div>
                            <h3>Principal</h3>
                            <p>School Leadership</p>
                            <p>Guiding the school towards academic and overall excellence.</p>
                        </div>

                        <div class="staff-card">
                            <div class="staff-icon">👩‍🏫</div>
                            <h3>Senior Teacher</h3>
                            <p>Academic Department</p>
                            <p>Helping students develop strong academic foundations.</p>
                        </div>

                        <div class="staff-card">
                            <div class="staff-icon">👨‍🏫</div>
                            <h3>Activity Coordinator</h3>
                            <p>Student Activities</p>
                            <p>Organising creative, cultural and extracurricular programmes.</p>
                        </div>
                    </div>
                </div>
            </section>

            <div class="back-home">
                <button class="btn" onclick="showPage('home')">← Back to Home</button>
            </div>
        </div>

        <!-- FACILITIES -->
        <div id="facilities" class="page">
            <div class="page-header">
                <h1>School Facilities</h1>
                <p>Facilities that make learning engaging and comfortable.</p>
            </div>

            <section>
                <div class="container">
                    <div class="facility-grid">
                        <div class="facility-card">
                            <div class="icon">📚</div>
                            <h3>Library</h3>
                            <p>A peaceful place for reading, research and self-learning.</p>
                        </div>

                        <div class="facility-card">
                            <div class="icon">🔬</div>
                            <h3>Science Lab</h3>
                            <p>Practical learning through experiments and activities.</p>
                        </div>

                        <div class="facility-card">
                            <div class="icon">💻</div>
                            <h3>Computer Lab</h3>
                            <p>Technology-based learning and digital skills development.</p>
                        </div>

                        <div class="facility-card">
                            <div class="icon">🏟️</div>
                            <h3>Playground</h3>
                            <p>Space for sports, exercise and outdoor activities.</p>
                        </div>

                        <div class="facility-card">
                            <div class="icon">🚌</div>
                            <h3>Transport</h3>
                            <p>School transport facilities for students and families.</p>
                        </div>

                        <div class="facility-card">
                            <div class="icon">🩺</div>
                            <h3>First Aid</h3>
                            <p>Basic health and first-aid support for students.</p>
                        </div>
                    </div>
                </div>
            </section>

            <div class="back-home">
                <button class="btn" onclick="showPage('home')">← Back to Home</button>
            </div>
        </div>

        <!-- SPORTS -->
        <div id="sports" class="page">
            <div class="page-header">
                <h1>Sports</h1>
                <p>Learn, play, compete and grow together.</p>
            </div>

            <section class="sports-section">
                <div class="container">
                    <h2 class="section-title">Sports at Our School</h2>

                    <div class="sports-list">
                        <div class="sport-box">⚽ Football</div>
                        <div class="sport-box">🏏 Cricket</div>
                        <div class="sport-box">🏸 Badminton</div>
                        <div class="sport-box">🏃 Athletics</div>
                    </div>
                </div>
            </section>

            <div class="back-home">
                <button class="btn" onclick="showPage('home')">← Back to Home</button>
            </div>
        </div>

        <!-- MEAL -->
        <div id="meal" class="page">
            <div class="page-header">
                <h1>School Meal</h1>
                <p>Healthy food for active minds and bodies.</p>
            </div>

            <section>
                <div class="container">
                    <div class="meal-box">
                        <h2>Weekly Meal Highlights</h2>
                        <p>
                            Our school encourages balanced and nutritious meals for students.
                        </p>

                        <div class="meal-items">
                            <span class="meal-item">Rice</span>
                            <span class="meal-item">Dal</span>
                            <span class="meal-item">Vegetables</span>
                            <span class="meal-item">Chapati</span>
                            <span class="meal-item">Fruits</span>
                            <span class="meal-item">Milk</span>
                        </div>
                    </div>
                </div>
            </section>

            <div class="back-home">
                <button class="btn" onclick="showPage('home')">← Back to Home</button>
            </div>
        </div>

        <!-- ACTIVITIES -->
        <div id="activities" class="page">
            <div class="page-header">
                <h1>Activities</h1>
                <p>Learning continues beyond the classroom.</p>
            </div>

            <section>
                <div class="container">
                    <div class="activity-box">
                        <h2>Student Activities</h2>
                        <p>
                            Students get opportunities to participate in activities that
                            develop creativity, communication, leadership and teamwork.
                        </p>

                        <h3>🎨 Cultural Activities</h3>
                        <ul>
                            <li>Dance and music programmes</li>
                            <li>Art and craft competitions</li>
                            <li>Annual cultural events</li>
                        </ul>

                        <h3>🧠 Academic Activities</h3>
                        <ul>
                            <li>Quiz competitions</li>
                            <li>Science exhibitions</li>
                            <li>Debates and presentations</li>
                        </ul>

                        <h3>🌱 Social Activities</h3>
                        <ul>
                            <li>Cleanliness drives</li>
                            <li>Environmental awareness</li>
                            <li>Community service activities</li>
                        </ul>
                    </div>
                </div>
            </section>

            <div class="back-home">
                <button class="btn" onclick="showPage('home')">← Back to Home</button>
            </div>
        </div>

        <!-- CONTACT -->
        <div id="contact" class="page">
            <div class="page-header">
                <h1>Contact Us</h1>
                <p>We would be happy to hear from you.</p>
            </div>

            <section>
                <div class="container contact-grid">
                    <div class="contact-box">
                        <h3>School Information</h3>
                        <p>📍 <strong>Address:</strong> Your School Address, India</p>
                        <p>📞 <strong>Phone:</strong> +91 98765 43210</p>
                        <p>✉️ <strong>Email:</strong> info@myschool.com</p>
                        <p>🕘 <strong>Office Hours:</strong> Monday - Friday, 9:00 AM - 4:00 PM</p>
                    </div>

                    
                </div>
            </section>

            <div class="back-home">
                <button class="btn" onclick="showPage('home')">← Back to Home</button>
            </div>
        </div>
    </main>

    <!-- FOOTER -->
    <footer>
        <div class="footer-links">
            <a onclick="showPage('home')">Home</a>
            <a onclick="showPage('about')">About</a>
            <a onclick="showPage('staff')">Staff</a>
            <a onclick="showPage('contact')">Contact</a>
        </div>

        <p>© 2026 My School. All Rights Reserved.</p>
        <p>Education • Knowledge • Discipline • Success</p>
    </footer>

    <script>
        function showPage(pageId, clickedLink = null) {
            const pages = document.querySelectorAll(".page");
            const links = document.querySelectorAll(".nav-link");
            const nav = document.getElementById("navLinks");

            pages.forEach(page => page.classList.remove("active"));
            links.forEach(link => link.classList.remove("active-link"));

            const selectedPage = document.getElementById(pageId);

            if (selectedPage) {
                selectedPage.classList.add("active");
            }

            if (clickedLink) {
                clickedLink.classList.add("active-link");
            } else {
                links.forEach(link => {
                    if (link.textContent.trim().toLowerCase() === pageId.toLowerCase()) {
                        link.classList.add("active-link");
                    }
                });
            }

            nav.classList.remove("active");
            window.scrollTo({ top: 0, behavior: "smooth" });
        }

        function toggleMenu() {
            document.getElementById("navLinks").classList.toggle("active");
        }

        function submitForm(event) {
            event.preventDefault();

            const name = document.getElementById("name").value.trim();
            const message = document.getElementById("formMessage");

            message.textContent = "Thank you, " + name + "! Your message has been received.";

            event.target.reset();
        }
    </script>

</body>
</html>
