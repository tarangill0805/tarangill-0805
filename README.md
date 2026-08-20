<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Taranjeet Singh | Cloud & DevOps</title>

    <style>

        /* ==============================
           RESET
        ============================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Inter, Arial, sans-serif;
            background: #0b0f14;
            color: #d1d5db;
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }


        /* ==============================
           NAVBAR
        ============================== */

        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;

            z-index: 1000;

            background: rgba(11, 15, 20, 0.82);

            backdrop-filter: blur(12px);

            border-bottom: 1px solid rgba(255,255,255,0.06);

            padding: 18px 8%;

            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 20px;
            font-weight: 700;
            color: white;
            letter-spacing: -0.5px;
        }

        .logo span {
            color: #60a5fa;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 28px;
        }

        nav ul li a {
            font-size: 14px;
            color: #9ca3af;
            transition: 0.3s;
        }

        nav ul li a:hover {
            color: white;
        }


        /* ==============================
           HERO
        ============================== */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;

            padding: 120px 8% 80px;

            position: relative;

            overflow: hidden;
        }

        /* background glow */

        .hero::before {
            content: "";

            position: absolute;

            width: 500px;
            height: 500px;

            background: #2563eb;

            opacity: 0.08;

            border-radius: 50%;

            filter: blur(120px);

            top: -150px;
            right: -100px;
        }

        .hero-content {
            max-width: 850px;

            position: relative;

            z-index: 1;
        }

        .hello {
            color: #60a5fa;

            font-size: 15px;

            font-weight: 600;

            margin-bottom: 15px;
        }

        .hero h1 {
            font-size: clamp(45px, 7vw, 78px);

            line-height: 1.05;

            color: white;

            letter-spacing: -3px;

            margin-bottom: 20px;
        }

        .hero h1 span {
            color: #60a5fa;
        }

        .hero h2 {
            font-size: clamp(20px, 3vw, 30px);

            font-weight: 500;

            color: #9ca3af;

            margin-bottom: 25px;
        }

        .hero p {
            max-width: 650px;

            color: #6b7280;

            font-size: 16px;
        }


        /* ==============================
           BUTTONS
        ============================== */

        .buttons {
            display: flex;

            gap: 12px;

            margin-top: 32px;
        }

        .btn {
            padding: 11px 20px;

            border-radius: 7px;

            font-size: 14px;

            font-weight: 600;

            transition: 0.3s;
        }

        .primary {
            background: #2563eb;

            color: white;
        }

        .primary:hover {
            background: #3b82f6;

            transform: translateY(-2px);
        }

        .secondary {
            border: 1px solid #30363d;

            color: #d1d5db;

            background: #11161d;
        }

        .secondary:hover {
            border-color: #60a5fa;

            color: white;

            transform: translateY(-2px);
        }


        /* ==============================
           SECTIONS
        ============================== */

        section {
            padding: 100px 8%;

            border-top: 1px solid rgba(255,255,255,0.05);
        }

        .container {
            max-width: 1000px;

            margin: auto;
        }

        .section-label {
            color: #60a5fa;

            font-size: 13px;

            font-weight: 600;

            text-transform: uppercase;

            letter-spacing: 2px;

            margin-bottom: 8px;
        }

        .section-title {
            color: white;

            font-size: 32px;

            letter-spacing: -1px;

            margin-bottom: 12px;
        }

        .section-text {
            color: #6b7280;

            max-width: 650px;

            margin-bottom: 40px;
        }


        /* ==============================
           ABOUT
        ============================== */

        .about-grid {
            display: grid;

            grid-template-columns: 1.5fr 1fr;

            gap: 50px;
        }

        .about-text p {
            color: #9ca3af;

            margin-bottom: 16px;
        }

        .info {
            background: #10151c;

            border: 1px solid #202630;

            border-radius: 12px;

            padding: 25px;
        }

        .info-item {
            display: flex;

            justify-content: space-between;

            gap: 15px;

            padding: 13px 0;

            border-bottom: 1px solid #202630;

            font-size: 14px;
        }

        .info-item:last-child {
            border-bottom: none;
        }

        .info-item span:first-child {
            color: #6b7280;
        }

        .info-item span:last-child {
            color: #e5e7eb;

            text-align: right;
        }


        /* ==============================
           INTERNSHIP
        ============================== */

        .experience {
            background: #10151c;

            border: 1px solid #202630;

            border-radius: 12px;

            padding: 30px;

            position: relative;

            overflow: hidden;
        }

        .experience::before {
            content: "";

            position: absolute;

            left: 0;
            top: 0;

            height: 100%;
            width: 3px;

            background: #2563eb;
        }

        .experience-top {
            display: flex;

            justify-content: space-between;

            align-items: flex-start;

            gap: 20px;

            margin-bottom: 20px;
        }

        .experience h3 {
            color: white;

            font-size: 21px;
        }

        .experience h4 {
            color: #60a5fa;

            font-weight: 500;

            margin-top: 4px;
        }

        .date {
            color: #6b7280;

            font-size: 13px;

            white-space: nowrap;
        }

        .experience ul {
            padding-left: 20px;

            color: #9ca3af;
        }

        .experience li {
            margin-bottom: 8px;
        }


        /* ==============================
           SKILLS
        ============================== */

        .skills {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 15px;
        }

        .skill {
            background: #10151c;

            border: 1px solid #202630;

            padding: 22px;

            border-radius: 10px;

            transition: 0.3s;
        }

        .skill:hover {
            border-color: #374151;

            transform: translateY(-4px);
        }

        .skill-icon {
            font-size: 23px;

            margin-bottom: 12px;
        }

        .skill h3 {
            color: white;

            font-size: 16px;

            margin-bottom: 6px;
        }

        .skill p {
            color: #6b7280;

            font-size: 13px;
        }


        /* ==============================
           TECH STACK
        ============================== */

        .tech {
            display: flex;

            flex-wrap: wrap;

            gap: 10px;
        }

        .tech span {
            padding: 8px 14px;

            background: #10151c;

            border: 1px solid #202630;

            border-radius: 6px;

            color: #9ca3af;

            font-size: 13px;

            transition: 0.3s;
        }

        .tech span:hover {
            color: white;

            border-color: #60a5fa;
        }


        /* ==============================
           PROJECTS
        ============================== */

        .projects {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 15px;
        }

        .project {
            background: #10151c;

            border: 1px solid #202630;

            border-radius: 10px;

            padding: 25px;

            transition: 0.3s;
        }

        .project:hover {
            transform: translateY(-5px);

            border-color: #374151;
        }

        .project-number {
            color: #374151;

            font-size: 13px;

            margin-bottom: 20px;
        }

        .project h3 {
            color: white;

            font-size: 18px;

            margin-bottom: 10px;
        }

        .project p {
            color: #6b7280;

            font-size: 14px;

            margin-bottom: 20px;
        }

        .project-link {
            color: #60a5fa;

            font-size: 13px;

            font-weight: 600;
        }


        /* ==============================
           GOAL
        ============================== */

        .goal {
            text-align: center;

            max-width: 750px;

            margin: auto;
        }

        .goal h2 {
            color: white;

            font-size: 34px;

            margin-bottom: 15px;
        }

        .goal p {
            color: #6b7280;
        }


        /* ==============================
           CONTACT
        ============================== */

        .contact {
            text-align: center;
        }

        .contact h2 {
            color: white;

            font-size: 35px;

            margin-bottom: 12px;
        }

        .contact p {
            color: #6b7280;

            margin-bottom: 28px;
        }

        .contact-links {
            display: flex;

            justify-content: center;

            gap: 12px;
        }

        .contact-links a {
            padding: 10px 18px;

            border: 1px solid #202630;

            border-radius: 7px;

            color: #9ca3af;

            font-size: 14px;

            transition: 0.3s;
        }

        .contact-links a:hover {
            color: white;

            border-color: #60a5fa;
        }


        /* ==============================
           FOOTER
        ============================== */

        footer {
            border-top: 1px solid rgba(255,255,255,0.05);

            padding: 25px 8%;

            text-align: center;

            color: #4b5563;

            font-size: 13px;
        }

        footer span {
            color: #60a5fa;
        }


        /* ==============================
           RESPONSIVE
        ============================== */

        @media(max-width: 850px) {

            nav {
                padding: 15px 5%;
            }

            nav ul {
                display: none;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .skills {
                grid-template-columns: repeat(2, 1fr);
            }

            .projects {
                grid-template-columns: 1fr;
            }

        }


        @media(max-width: 600px) {

            section {
                padding: 75px 6%;
            }

            .hero {
                padding: 120px 6% 70px;
            }

            .hero h1 {
                letter-spacing: -2px;
            }

            .skills {
                grid-template-columns: 1fr;
            }

            .experience-top {
                flex-direction: column;
            }

            .buttons {
                flex-direction: column;

                width: 170px;
            }

            .contact-links {
                flex-direction: column;

                align-items: center;
            }

        }

    </style>

</head>


<body>


    <!-- ==========================
         NAVIGATION
    =========================== -->

    <nav>

        <div class="logo">
            Taranjeet<span>.</span>
        </div>

        <ul>

            <li>
                <a href="#about">About</a>
            </li>

            <li>
                <a href="#experience">Experience</a>
            </li>

            <li>
                <a href="#skills">Skills</a>
            </li>

            <li>
                <a href="#projects">Projects</a>
            </li>

            <li>
                <a href="#contact">Contact</a>
            </li>

        </ul>

    </nav>



    <!-- ==========================
         HERO
    =========================== -->

    <section class="hero">

        <div class="hero-content">

            <div class="hello">
                👋 Hello, I'm
            </div>

            <h1>
                Taranjeet <span>Singh</span>
            </h1>

            <h2>
                BCA Student · Cloud Computing · DevOps
            </h2>

            <p>

                I'm a BCA student at Punjabi University,
                currently building my skills in Cloud Computing
                and DevOps through practical learning and
                internship experience.

            </p>


            <div class="buttons">

                <a
                    href="#projects"
                    class="btn primary">

                    Explore My Work

                </a>

                <a
                    href="#contact"
                    class="btn secondary">

                    Get In Touch

                </a>

            </div>

        </div>

    </section>



    <!-- ==========================
         ABOUT
    =========================== -->

    <section id="about">

        <div class="container">

            <div class="section-label">
                About Me
            </div>

            <h2 class="section-title">
                Building my path in <span>technology.</span>
            </h2>

            <p class="section-text">

                A little about my background and what I'm
                currently working towards.

            </p>


            <div class="about-grid">


                <div class="about-text">

                    <p>

                        I am pursuing my Bachelor of Computer
                        Applications (BCA) from Punjabi University.

                    </p>

                    <p>

                        My current focus is Cloud Computing and
                        DevOps. I enjoy understanding how
                        applications, servers, infrastructure and
                        automation work together.

                    </p>

                    <p>

                        Alongside my studies, I am gaining practical
                        experience through my Cloud Computing +
                        DevOps internship at TechCADD, Mohali.

                    </p>

                    <p>

                        I believe in learning by doing and
                        continuously improving my technical and
                        problem-solving skills.

                    </p>

                </div>


                <div class="info">

                    <div class="info-item">

                        <span>Name</span>

                        <span>Taranjeet Singh</span>

                    </div>

                    <div class="info-item">

                        <span>Education</span>

                        <span>BCA</span>

                    </div>

                    <div class="info-item">

                        <span>University</span>

                        <span>Punjabi University</span>

                    </div>

                    <div class="info-item">

                        <span>Internship</span>

                        <span>Cloud + DevOps</span>

                    </div>

                    <div class="info-item">

                        <span>Organization</span>

                        <span>TechCADD, Mohali</span>

                    </div>

                    <div class="info-item">

                        <span>Focus</span>

                        <span>Cloud & DevOps</span>

                    </div>

                </div>

            </div>

        </div>

    </section>



    <!-- ==========================
         EXPERIENCE
    =========================== -->

    <section id="experience">

        <div class="container">

            <div class="section-label">
                Experience
            </div>

            <h2 class="section-title">
                Where I'm <span>learning.</span>
            </h2>

            <p class="section-text">

                My current professional learning experience.

            </p>


            <div class="experience">

                <div class="experience-top">

                    <div>

                        <h3>
                            Cloud Computing + DevOps Intern
                        </h3>

                        <h4>
                            TechCADD · Mohali
                        </h4>

                    </div>

                    <div class="date">
                        Internship
                    </div>

                </div>


                <ul>

                    <li>
                        Learning Linux and system
                        administration fundamentals.
                    </li>

                    <li>
                        Practicing Git and GitHub for
                        version control.
                    </li>

                    <li>
                        Understanding CI/CD and DevOps
                        workflows.
                    </li>

                    <li>
                        Exploring cloud computing and
                        infrastructure concepts.
                    </li>

                    <li>
                        Working with modern DevOps tools
                        through practical exercises.
                    </li>

                </ul>

            </div>

        </div>

    </section>



    <!-- ==========================
         SKILLS
    =========================== -->

    <section id="skills">

        <div class="container">

            <div class="section-label">
                Skills
            </div>

            <h2 class="section-title">
                What I'm <span>learning.</span>
            </h2>

            <p class="section-text">

                Technologies and concepts that are part of
                my current learning journey.

            </p>


            <div class="skills">


                <div class="skill">

                    <div class="skill-icon">
                        🐧
                    </div>

                    <h3>
                        Linux
                    </h3>

                    <p>
                        Commands, permissions, processes,
                        services and Bash basics.
                    </p>

                </div>


                <div class="skill">

                    <div class="skill-icon">
                        ☁️
                    </div>

                    <h3>
                        Cloud Computing
                    </h3>

                    <p>
                        Cloud concepts, infrastructure and
                        deployment fundamentals.
                    </p>

                </div>


                <div class="skill">

                    <div class="skill-icon">
                        ⚙️
                    </div>

                    <h3>
                        DevOps
                    </h3>

                    <p>
                        DevOps culture, automation,
                        deployment and CI/CD concepts.
                    </p>

                </div>


                <div class="skill">

                    <div class="skill-icon">
                        🔀
                    </div>

                    <h3>
                        Git & GitHub
                    </h3>

                    <p>
                        Repositories, commits, branches
                        and version control.
                    </p>

                </div>


                <div class="skill">

                    <div class="skill-icon">
                        🐳
                    </div>

                    <h3>
                        Docker
                    </h3>

                    <p>
                        Learning containers, images and
                        application deployment.
                    </p>

                </div>


                <div class="skill">

                    <div class="skill-icon">
                        💻
                    </div>

                    <h3>
                        Bash
                    </h3>

                    <p>
                        Shell scripting and Linux
                        task automation.
                    </p>

                </div>

            </div>

        </div>

    </section>



    <!-- ==========================
         TECHNOLOGIES
    =========================== -->

    <section>

        <div class="container">

            <div class="section-label">
                Tech Stack
            </div>

            <h2 class="section-title">
                Tools I <span>work with.</span>
            </h2>

            <p class="section-text">
                My current technology stack.
            </p>


            <div class="tech">

                <span>Linux</span>

                <span>Bash</span>

                <span>Git</span>

                <span>GitHub</span>

                <span>Docker</span>

                <span>Jenkins</span>

                <span>AWS</span>

                <span>Terraform</span>

                <span>CI/CD</span>

                <span>Nginx</span>

                <span>Networking</span>

                <span>Shell Scripting</span>

            </div>

        </div>

    </section>



    <!-- ==========================
         PROJECTS
    =========================== -->

    <section id="projects">

        <div class="container">

            <div class="section-label">
                Projects
            </div>

            <h2 class="section-title">
                Things I've <span>built.</span>
            </h2>

            <p class="section-text">

                Small projects and practical work from
                my learning journey.

            </p>


            <div class="projects">


                <div class="project">

                    <div class="project-number">
                        01
                    </div>

                    <h3>
                        Linux Shell Scripts
                    </h3>

                    <p>

                        Bash scripts for file management,
                        directories, conditions and
                        basic automation.

                    </p>

                    <a
                        href="#"
                        class="project-link">

                        View project →

                    </a>

                </div>


                <div class="project">

                    <div class="project-number">
                        02
                    </div>

                    <h3>
                        DevOps Practice Lab
                    </h3>

                    <p>

                        Hands-on practice with Linux,
                        Git, CI/CD concepts and
                        DevOps workflows.

                    </p>

                    <a
                        href="#"
                        class="project-link">

                        View project →

                    </a>

                </div>


                <div class="project">

                    <div class="project-number">
                        03
                    </div>

                    <h3>
                        University Website
                    </h3>

                    <p>

                        A simple responsive university
                        website created with HTML and CSS.

                    </p>

                    <a
                        href="#"
                        class="project-link">

                        View project →

                    </a>

                </div>

            </div>

        </div>

    </section>



    <!-- ==========================
         CAREER GOAL
    =========================== -->

    <section>

        <div class="container">

            <div class="goal">

                <div class="section-label">
                    My Direction
                </div>

                <h2>
                    Learning today.
                    <span style="color:#60a5fa;">
                        Building tomorrow.
                    </span>
                </h2>

                <p>

                    My goal is to become a skilled Cloud &
                    DevOps professional by gaining strong
                    knowledge of Linux, cloud infrastructure,
                    automation, CI/CD and modern DevOps tools.

                </p>

            </div>

        </div>

    </section>



    <!-- ==========================
         CONTACT
    =========================== -->

    <section id="contact">

        <div class="container">

            <div class="contact">

                <div class="section-label">
                    Contact
                </div>

                <h2>
                    Let's connect.
                </h2>

                <p>

                    I'm always open to learning,
                    collaborating and connecting
                    with people in tech.

                </p>


                <div class="contact-links">

                    <a
                        href="https://github.com/"
                        target="_blank">

                        GitHub

                    </a>

                    <a
                        href="https://linkedin.com/"
                        target="_blank">

                        LinkedIn

                    </a>

                    <a
                        href="mailto:your@email.com">

                        Email

                    </a>

                </div>

            </div>

        </div>

    </section>



    <!-- ==========================
         FOOTER
    =========================== -->

    <footer>

        © 2026
        <span>Taranjeet Singh</span>
        · BCA · Cloud & DevOps

    </footer>


</body>

</html>
