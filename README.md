# portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kimberly Amurao - Finance & Admin Professional</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary-color: #FAD59A;
            --accent-color: #bd4ce5;
            --dark-color: #333;
            --light-color: #fff;
            --gray-color: #f4f4f4;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--primary-color);
            color: var(--dark-color);
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        a {
            text-decoration: none;
            color: var(--dark-color);
        }
        
        ul {
            list-style: none;
        }
        
        .btn {
            display: inline-block;
            background: var(--accent-color);
            color: var(--light-color);
            padding: 12px 24px;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #a235c9;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Header Section */
        header {
            background-color: var(--primary-color);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 100;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--dark-color);
        }
        
        .nav-menu {
            display: flex;
        }
        
        .nav-menu li {
            margin-left: 30px;
        }
        
        .nav-menu li a {
            font-weight: 500;
            position: relative;
            padding-bottom: 5px;
        }
        
        .nav-menu li a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background-color: var(--accent-color);
            left: 0;
            bottom: 0;
            transition: width 0.3s ease;
        }
        
        .nav-menu li a:hover:after, .nav-menu li a.active:after {
            width: 100%;
        }
        
        .nav-menu li a.active {
            color: var(--accent-color);
        }
        
        .connect-btn {
            background-color: var(--accent-color);
            color: var(--light-color);
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .connect-btn:hover {
            background-color: #a235c9;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            padding-top: 120px;
            padding-bottom: 60px;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .hero-text {
            flex: 1;
            padding-right: 40px;
        }
        
        .hero-text h1 {
            font-size: 48px;
            line-height: 1;
            margin-bottom: 20px;
            color: var(--dark-color);
        }
        
        .hero-text p {
            font-size: 18px;
            color: #666;
            margin-bottom: 30px;
        }
        
        .hero-img {
            flex: 1;
            position: relative;
        }
        
        .hero-img-container {
            background-color: var(--accent-color);
            border-radius: 20px;
            overflow: hidden;
            width: 100%;
            max-width: 400px;
            margin-left: auto;
        }
        
        .hero-img img {
            display: block;
            width: 100%;
            height: auto;
            object-fit: cover;
        }
        
        .social-icons {
            display: flex;
            margin-top: 30px;
        }
        
        .social-icons a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--light-color);
            margin-right: 15px;
            color: var(--dark-color);
            transition: all 0.3s ease;
            font-size: 18px;
        }
        
        .social-icons a:hover {
            background-color: var(--accent-color);
            color: var(--light-color);
            transform: translateY(-3px);
        }
        
        /* About Section */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            font-size: 36px;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .section-subtitle {
            color: var(--accent-color);
            font-size: 20px;
            margin-bottom: 10px;
            text-align: center;
            font-weight: 600;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .about-text {
            flex: 1;
            padding-right: 40px;
        }
        
        .about-img {
            flex: 1;
        }
        
        .about-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        /* Experience Section */
        .experience {
            background-color: var(--light-color);
            border-radius: 20px;
            padding: 60px 0;
        }
        
        .timeline {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .timeline-item {
            background-color: #fff;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            position: relative;
        }
        
        .timeline-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .timeline-date {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--light-color);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 15px;
        }
        
        .timeline-title {
            color: var(--accent-color);
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .timeline-company {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 15px;
        }
        
        .timeline-desc {
            color: #666;
            margin-bottom: 20px;
        }
        
        .read-more {
            display: inline-flex;
            align-items: center;
            color: var(--accent-color);
            font-weight: 600;
        }
        
        .read-more i {
            margin-left: 5px;
            transition: transform 0.3s ease;
        }
        
        .read-more:hover i {
            transform: translateX(5px);
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }
        
        .skill-item {
            background-color: var(--light-color);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            background-color: var(--accent-color);
            color: var(--light-color);
        }
        
        .skill-item i {
            font-size: 36px;
            margin-bottom: 15px;
            color: var(--accent-color);
        }
        
        .skill-item:hover i {
            color: var(--light-color);
        }
        
        .skill-title {
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .skill-years {
            color: #666;
            font-size: 14px;
        }
        
        .skill-item:hover .skill-years {
            color: rgba(255, 255, 255, 0.8);
        }
        
        /* Contact Section */
        .contact {
            background-color: var(--light-color);
            border-radius: 20px;
            padding: 60px 0;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 30px;
        }
        
        .contact-icon {
            width: 60px;
            height: 60px;
            background-color: var(--accent-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 20px;
            color: var(--light-color);
            font-size: 24px;
        }
        
        .contact-text h3 {
            font-size: 18px;
            margin-bottom: 5px;
        }
        
        .contact-text p {
            color: #666;
        }
        
        .contact-form {
            background-color: #f9f9f9;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-control {
            width: 100%;
            padding: 15px;
            font-size: 16px;
            border: 1px solid #ddd;
            border-radius: 8px;
            background-color: #fff;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: var(--accent-color);
            box-shadow: 0 0 0 2px rgba(189, 76, 229, 0.1);
            outline: none;
        }
        
        textarea.form-control {
            height: 150px;
            resize: none;
        }
        
        /* Footer */
        footer {
            background-color: var(--primary-color);
            padding: 40px 0;
            text-align: center;
        }
        
        .footer-content {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .footer-content p {
            margin-top: 20px;
            color: #666;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            margin-top: 30px;
        }
        
        .footer-links a {
            margin: 0 15px;
            color: #666;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--accent-color);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-text h1 {
                font-size: 48px;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .about-text, .about-img {
                flex: none;
                width: 100%;
                padding: 0;
            }
            
            .about-img {
                margin-top: 40px;
            }
        }
        
        @media (max-width: 768px) {
            .nav-menu {
                position: fixed;
                top: 80px;
                left: -100%;
                background-color: var(--light-color);
                width: 100%;
                height: calc(100vh - 80px);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: left 0.3s ease;
                box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            }
            
            .nav-menu.active {
                left: 0;
            }
            
            .nav-menu li {
                margin: 15px 0;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero-content {
                flex-direction: column-reverse;
            }
            
            .hero-text, .hero-img {
                flex: none;
                width: 100%;
                padding: 0;
            }
            
            .hero-text {
                margin-top: 40px;
                text-align: center;
            }
            
            .hero-img-container {
                margin: 0 auto;
            }
            
            .social-icons {
                justify-content: center;
            }
        }
        
        @media (max-width: 576px) {
            .hero-text h1 {
                font-size: 36px;
            }
            
            .section-title {
                font-size: 28px;
            }
            
            .contact-form {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container nav-container">
            <div class="logo">Portfolio</div>
            <ul class="nav-menu">
                <li><a href="#home" class="active">Home</a></li>
                <li><a href="#about">About Me</a></li>
                <li><a href="#resume">Resume</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="#contact" class="connect-btn">CONNECT</a>
            <div class="hamburger">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <div class="hero-text">
                <h1>Hello 👋, I am<br>Kimberly Amurao</h1>
                <p>Detail-oriented accounting professional with experience in accounts payable, finance support, and administrative management. Skilled in verifying invoices, managing petty cash, and ensuring accurate financial documentation.</p>
                <a href="#" class="btn" id="download-cv">Download CV <i class="fas fa-download"></i></a>
                <div class="social-icons">
    <a href="http://linkedin.com/in/kimberly-amurao-b060581b4" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-linkedin-in"></i>
    </a>
</div>
            </div>
            <div class="hero-img">
                <div class="hero-img-container">
                    <img src="C:\Users\DELL\Pictures\Kim Prof pic.jpeg" alt="Kimberly Amurao">
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <div class="section-subtitle">ABOUT ME</div>
            <h2 class="section-title">Professional Profile</h2>
            <div class="about-content">
               <div class="about-text" style="text-align: justify; font-size: 20px; line-height: 1.5;">
    <p style="margin-bottom: 1.5em;">Detail-oriented accounting professional with a degree from Saint John Colleges and experience at Emapta Global, specializing in accounts payable. Skilled in verifying invoices, managing petty cash, and ensuring accurate financial documentation.</p>
    <p style="margin-bottom: 1.5em;">Proven ability to communicate effectively across departments, streamline processes, and maintain adherence to GAAP principles, with strong proficiency in Microsoft Excel.</p>
    <p>Currently working as a Freelancer providing Administrative and Finance Support services to clients around the world.</p>
</div>
                <div class="about-img">
                    <img src="C:\Users\DELL\Pictures\Kim Prof pic.jpeg" alt="About Kimberly">
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="resume" class="section experience">
        <div class="container">
            <div class="section-subtitle">WORK EXPERIENCE</div>
            <h2 class="section-title">Work History</h2>
            <div class="timeline">
<div class="timeline-item">
    <div class="timeline-date">July 2024 - Present</div>
    <h3 class="timeline-title">Freelancer - Administrative and Finance Support</h3>
    <h4 class="timeline-company">Private Company - Amsterdam, Netherlands</h4>
    <p class="timeline-desc">Managing administrative tasks, processing invoices, preparing sales invoices, and maintaining financial systems.</p>
    <button class="read-more-btn" data-modal="freelancer">Read More <i class="fas fa-arrow-right"></i></button>
</div>

<div id="freelancer-modal" class="modal">
    <div class="modal-content">
        <span class="close-button">&times;</span>
        <h3>Freelancer - Administrative and Finance Support Details</h3>
        <ul>
            <li>Managed daily administrative tasks for smooth operations.</li>
            <li>Processed invoices, credit card expenses, and claims using various financial tools.</li>
            <li>Prepared and filed sales invoices in Productive, ensuring accurate vendor documentation.</li>
            <li>Served as the primary contact for financial inquiries related to invoices and subscriptions.</li>
            <li>Maintained updated project and budget management systems.</li>
            <li>Communicated with clients regarding payment issues and issued timely reminders.</li>
            <li>Conducted weekly reviews of outstanding balances for prompt resolution.</li>
            <li>Collaborated with team members to address billing and invoice discrepancies.</li>
            <li>Assisted in setting up projects and budgets in Productive for accurate monitoring.</li>
            <li>Drafted and reviewed client contracts using DocuSign, ensuring alignment with budgets and terms.</li>
            <li>Tracked payroll changes (promotions, leaves, terminations) for accurate processing.</li>
            <li>Managed access to Microsoft, Google, and password management systems for secure operations.</li>
        </ul>
    </div>
</div>

<style>
/* Basic modal styling - feel free to customize */
.modal {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

.modal-content {
    background-color: #fefefe;
    margin: 15% auto; /* 15% from the top and centered */
    padding: 20px;
    border: 1px solid #888;
    width: 80%; /* Could be more or less, depending on screen size */
    position: relative;
}

.close-button {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.close-button:hover,
.close-button:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}

.read-more-btn {
    background: none;
    border: none;
    color: #9400D3; /* Purple color */
    padding: 0;
    font: inherit;
    cursor: pointer;
    text-decoration: none;
    font-size: 16px; /* Adjust font size as needed */
}

.read-more-btn:hover {
    text-decoration: underline;
}

.modal-content ul {
    list-style-type: disc; /* Use filled circles for bullets */
    padding-left: 20px; /* Add some left padding for the bullets */
}

.modal-content li {
    margin-bottom: 8px; /* Add some spacing between list items */
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const readMoreBtn = document.querySelector('.read-more-btn[data-modal="freelancer"]');
    const modal = document.getElementById('freelancer-modal');
    const closeButton = modal.querySelector('.close-button');

    readMoreBtn.addEventListener('click', function() {
        modal.style.display = "block";
    });

    closeButton.addEventListener('click', function() {
        modal.style.display = "none";
    });

    window.addEventListener('click', function(event) {
        if (event.target == modal) {
            modal.style.display = "none";
        }
    });
});
</script>                
              <div class="timeline-item">
    <div class="timeline-date">Aug 2023 - June 2024</div>
    <h3 class="timeline-title">Administrative Assistant</h3>
    <h4 class="timeline-company">Emapta Philippines Inc.</h4>
    <p class="timeline-desc">Reconciled credit card expenses, generated invoices, monitored project budgets, and acted as primary contact for administrative inquiries.</p>
    <button class="read-more-btn" data-modal="emapta">Read More <i class="fas fa-arrow-right"></i></button>
</div>

<div id="emapta-modal" class="modal">
    <div class="modal-content">
        <span class="close-button">&times;</span>
        <h3>Administrative Assistant Details</h3>
        <ul>
            <li>Reconciled credit card expenses and prepared monthly summary reports for client review.</li>
            <li>Generated and sent timely invoices, ensuring accuracy and compliance using financial tools.</li>
            <li>Followed up on outstanding payments to maintain healthy cash flow and client relationships.</li>
            <li>Acted as the primary contact for administrative, HR, and finance-related inquiries.</li>
            <li>Responded to both internal and external requests with professionalism and efficiency.</li>
            <li>Monitored project budgets and reports, offering insights for decision-making and preparing contracts for clients and suppliers.</li>
        </ul>
    </div>
</div>

<style>
/* Basic modal styling - feel free to customize */
.modal {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

.modal-content {
    background-color: #fefefe;
    margin: 15% auto; /* 15% from the top and centered */
    padding: 20px;
    border: 1px solid #888;
    width: 80%; /* Could be more or less, depending on screen size */
    position: relative;
}

.close-button {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.close-button:hover,
.close-button:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}

.read-more-btn {
    background: none;
    border: none;
    color: #9400D3; /* Purple color */
    padding: 0;
    font: inherit;
    cursor: pointer;
    text-decoration: none;
    font-size: 16px; /* Adjust font size as needed */
}

.read-more-btn:hover {
    text-decoration: underline;
}

.modal-content ul {
    list-style-type: disc; /* Use filled circles for bullets */
    padding-left: 20px; /* Add some left padding for the bullets */
}

.modal-content li {
    margin-bottom: 8px; /* Add some spacing between list items */
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const freelancerReadMoreBtn = document.querySelector('.read-more-btn[data-modal="freelancer"]');
    const freelancerModal = document.getElementById('freelancer-modal');
    const emaptaReadMoreBtn = document.querySelector('.read-more-btn[data-modal="emapta"]');
    const emaptaModal = document.getElementById('emapta-modal');
    const closeButtons = document.querySelectorAll('.close-button');
    const modals = document.querySelectorAll('.modal');

    freelancerReadMoreBtn.addEventListener('click', function() {
        freelancerModal.style.display = "block";
    });

    emaptaReadMoreBtn.addEventListener('click', function() {
        emaptaModal.style.display = "block";
    });

    closeButtons.forEach(button => {
        button.addEventListener('click', function() {
            const modal = this.closest('.modal');
            if (modal) {
                modal.style.display = "none";
            }
        });
    });

    window.addEventListener('click', function(event) {
        modals.forEach(modal => {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        });
    });
});
</script>
                
               <div class="timeline-item">
    <div class="timeline-date">Feb 2021 - Aug 2023</div>
    <h3 class="timeline-title">Admin and Accounts Payable Staff</h3>
    <h4 class="timeline-company">Polyfame Industries Inc.</h4>
    <p class="timeline-desc">Prepared payments, validated supplier documents, managed petty cash, and prepared compliance reports.</p>
    <button class="read-more-btn" data-modal="polyfame">Read More <i class="fas fa-arrow-right"></i></button>
</div>

<div id="polyfame-modal" class="modal">
    <div class="modal-content">
        <span class="close-button">&times;</span>
        <h3>Admin and Accounts Payable Staff Details</h3>
        <ul>
            <li>Prepare payments and control expenses on a day-to-day activities.</li>
            <li>Validation of supplier documents ensuring 3-way PO matching is correctly done.</li>
            <li>Responsible for scheduling supplier payment, communicating discrepancies and documentation, as well as the approval.</li>
            <li>Petty Cash Fund Management.</li>
            <li>Prepares payment and monthly, quarterly and annual BIR compliance report.</li>
            <li>Statement of Account creation for customers.</li>
            <li>Submits quarter and annual compliance report to BIR through EFPS.</li>
            <li>Monitoring of employee attendance (leave, absences and overtime).</li>
            <li>Payroll Processing, cheque manual encashment and manual payment to employees.</li>
            <li>Accounts Payable and Receivable Management (end to end process).</li>
            <li>Responsible for generating and maintaining monthly reports of expenses and collections.</li>
            <li>Conducts weekly audit of supplies, petty cash and vouchers issued.</li>
        </ul>
    </div>
</div>

<style>
/* Basic modal styling - feel free to customize */
.modal {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

.modal-content {
    background-color: #fefefe;
    margin: 15% auto; /* 15% from the top and centered */
    padding: 20px;
    border: 1px solid #888;
    width: 80%; /* Could be more or less, depending on screen size */
    position: relative;
}

.close-button {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.close-button:hover,
.close-button:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}

.read-more-btn {
    background: none;
    border: none;
    color: #9400D3; /* Purple color */
    padding: 0;
    font: inherit;
    cursor: pointer;
    text-decoration: none;
    font-size: 16px; /* Adjust font size as needed */
}

.read-more-btn:hover {
    text-decoration: underline;
}

.modal-content ul {
    list-style-type: disc; /* Use filled circles for bullets */
    padding-left: 20px; /* Add some left padding for the bullets */
}

.modal-content li {
    margin-bottom: 8px; /* Add some spacing between list items */
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const freelancerReadMoreBtn = document.querySelector('.read-more-btn[data-modal="freelancer"]');
    const freelancerModal = document.getElementById('freelancer-modal');
    const emaptaReadMoreBtn = document.querySelector('.read-more-btn[data-modal="emapta"]');
    const emaptaModal = document.getElementById('emapta-modal');
    const polyfameReadMoreBtn = document.querySelector('.read-more-btn[data-modal="polyfame"]');
    const polyfameModal = document.getElementById('polyfame-modal');
    const closeButtons = document.querySelectorAll('.close-button');
    const modals = document.querySelectorAll('.modal');

    freelancerReadMoreBtn.addEventListener('click', function() {
        freelancerModal.style.display = "block";
    });

    emaptaReadMoreBtn.addEventListener('click', function() {
        emaptaModal.style.display = "block";
    });

    polyfameReadMoreBtn.addEventListener('click', function() {
        polyfameModal.style.display = "block";
    });

    closeButtons.forEach(button => {
        button.addEventListener('click', function() {
            const modal = this.closest('.modal');
            if (modal) {
                modal.style.display = "none";
            }
        });
    });

    window.addEventListener('click', function(event) {
        modals.forEach(modal => {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        });
    });
});
</script>
                
               <div class="timeline-item">
    <div class="timeline-date">Oct 2020 - Feb 2021</div>
    <h3 class="timeline-title">Accounting Clerk</h3>
    <h4 class="timeline-company">Groundscape Management Inc.</h4>
    <p class="timeline-desc">Processed check and cash vouchers, reconciled revolving funds, entered data in Quickbooks, and assisted with reports.</p>
    <button class="read-more-btn" data-modal="groundscape">Read More <i class="fas fa-arrow-right"></i></button>
</div>

<div id="groundscape-modal" class="modal">
    <div class="modal-content">
        <span class="close-button">&times;</span>
        <h3>Accounting Clerk Details</h3>
        <ul>
            <li>Handles and processes all check vouchers and cash vouchers transactions.</li>
            <li>Reconciles the replenishment of revolving fund.</li>
            <li>Data Entry in Quickbooks and ensures the accuracy of records.</li>
            <li>Assists in preparation of month-end reports.</li>
            <li>2nd level checker of payroll records and entries.</li>
            <li>Assists in monthly Budget and Variance Report Analysis.</li>
        </ul>
    </div>
</div>

<style>
/* Basic modal styling - feel free to customize */
.modal {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

.modal-content {
    background-color: #fefefe;
    margin: 15% auto; /* 15% from the top and centered */
    padding: 20px;
    border: 1px solid #888;
    width: 80%; /* Could be more or less, depending on screen size */
    position: relative;
}

.close-button {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.close-button:hover,
.close-button:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}

.read-more-btn {
    background: none;
    border: none;
    color: #9400D3; /* Purple color */
    padding: 0;
    font: inherit;
    cursor: pointer;
    text-decoration: none;
    font-size: 16px; /* Adjust font size as needed */
}

.read-more-btn:hover {
    text-decoration: underline;
}

.modal-content ul {
    list-style-type: disc; /* Use filled circles for bullets */
    padding-left: 20px; /* Add some left padding for the bullets */
}

.modal-content li {
    margin-bottom: 8px; /* Add some spacing between list items */
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const freelancerReadMoreBtn = document.querySelector('.read-more-btn[data-modal="freelancer"]');
    const freelancerModal = document.getElementById('freelancer-modal');
    const emaptaReadMoreBtn = document.querySelector('.read-more-btn[data-modal="emapta"]');
    const emaptaModal = document.getElementById('emapta-modal');
    const polyfameReadMoreBtn = document.querySelector('.read-more-btn[data-modal="polyfame"]');
    const polyfameModal = document.getElementById('polyfame-modal');
    const groundscapeReadMoreBtn = document.querySelector('.read-more-btn[data-modal="groundscape"]');
    const groundscapeModal = document.getElementById('groundscape-modal');
    const closeButtons = document.querySelectorAll('.close-button');
    const modals = document.querySelectorAll('.modal');

    freelancerReadMoreBtn.addEventListener('click', function() {
        freelancerModal.style.display = "block";
    });

    emaptaReadMoreBtn.addEventListener('click', function() {
        emaptaModal.style.display = "block";
    });

    polyfameReadMoreBtn.addEventListener('click', function() {
        polyfameModal.style.display = "block";
    });

    groundscapeReadMoreBtn.addEventListener('click', function() {
        groundscapeModal.style.display = "block";
    });

    closeButtons.forEach(button => {
        button.addEventListener('click', function() {
            const modal = this.closest('.modal');
            if (modal) {
                modal.style.display = "none";
            }
        });
    });

    window.addEventListener('click', function(event) {
        modals.forEach(modal => {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        });
    });
});
</script>
                
               <div class="timeline-item">
    <div class="timeline-date">Mar 2019 - Feb 2020</div>
    <h3 class="timeline-title">Administration Support</h3>
    <h4 class="timeline-company">AOBS - Advanced Outsourcing Business and Services Inc.</h4>
    <p class="timeline-desc">Provided daily account balances, processed orders, created floater analysis, and allocated payments.</p>
    <button class="read-more-btn" data-modal="aobs">Read More <i class="fas fa-arrow-right"></i></button>
</div>

<div id="aobs-modal" class="modal">
    <div class="modal-content">
        <span class="close-button">&times;</span>
        <h3>Administration Support Details</h3>
        <ul>
            <li>Provides day to day balances of accounts-in-charge.</li>
            <li>Processing and endorsing of orders.</li>
            <li>Provides floater analysis reconciliation every day.</li>
            <li>Identifies and allocates all payments and ensures that all cash is posted within required time frame.</li>
            <li>Supports to month-end AR reports.</li>
        </ul>
    </div>
</div>

<style>
/* Basic modal styling - feel free to customize */
.modal {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

.modal-content {
    background-color: #fefefe;
    margin: 15% auto; /* 15% from the top and centered */
    padding: 20px;
    border: 1px solid #888;
    width: 80%; /* Could be more or less, depending on screen size */
    position: relative;
}

.close-button {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

.close-button:hover,
.close-button:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
}

.read-more-btn {
    background: none;
    border: none;
    color: #9400D3; /* Purple color */
    padding: 0;
    font: inherit;
    cursor: pointer;
    text-decoration: none;
    font-size: 16px; /* Adjust font size as needed */
}

.read-more-btn:hover {
    text-decoration: underline;
}

.modal-content ul {
    list-style-type: disc; /* Use filled circles for bullets */
    padding-left: 20px; /* Add some left padding for the bullets */
}

.modal-content li {
    margin-bottom: 8px; /* Add some spacing between list items */
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const freelancerReadMoreBtn = document.querySelector('.read-more-btn[data-modal="freelancer"]');
    const freelancerModal = document.getElementById('freelancer-modal');
    const emaptaReadMoreBtn = document.querySelector('.read-more-btn[data-modal="emapta"]');
    const emaptaModal = document.getElementById('emapta-modal');
    const polyfameReadMoreBtn = document.querySelector('.read-more-btn[data-modal="polyfame"]');
    const polyfameModal = document.getElementById('polyfame-modal');
    const groundscapeReadMoreBtn = document.querySelector('.read-more-btn[data-modal="groundscape"]');
    const groundscapeModal = document.getElementById('groundscape-modal');
    const aobsReadMoreBtn = document.querySelector('.read-more-btn[data-modal="aobs"]');
    const aobsModal = document.getElementById('aobs-modal');
    const closeButtons = document.querySelectorAll('.close-button');
    const modals = document.querySelectorAll('.modal');

    freelancerReadMoreBtn.addEventListener('click', function() {
        freelancerModal.style.display = "block";
    });

    emaptaReadMoreBtn.addEventListener('click', function() {
        emaptaModal.style.display = "block";
    });

    polyfameReadMoreBtn.addEventListener('click', function() {
        polyfameModal.style.display = "block";
    });

    groundscapeReadMoreBtn.addEventListener('click', function() {
        groundscapeModal.style.display = "block";
    });

    aobsReadMoreBtn.addEventListener('click', function() {
        aobsModal.style.display = "block";
    });

    closeButtons.forEach(button => {
        button.addEventListener('click', function() {
            const modal = this.closest('.modal');
            if (modal) {
                modal.style.display = "none";
            }
        });
    });

    window.addEventListener('click', function(event) {
        modals.forEach(modal => {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        });
    });
});
</script>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="services" class="section">
        <div class="container">
            <div class="section-subtitle">MY EXPERTISE</div>
            <h2 class="section-title">Professional Skills</h2>
            <div class="skills-container">
                <div class="skill-item">
                    <i class="fas fa-file-invoice-dollar"></i>
                    <h3 class="skill-title">Accounts Payable</h3>
                    <p class="skill-years">4 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-money-check-alt"></i>
                    <h3 class="skill-title">Accounts Receivable</h3>
                    <p class="skill-years">4 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-book"></i>
                    <h3 class="skill-title">Bookkeeping</h3>
                    <p class="skill-years">4 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-credit-card"></i>
                    <h3 class="skill-title">Expense Management</h3>
                    <p class="skill-years">2 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-file-invoice"></i>
                    <h3 class="skill-title">Invoice Processing</h3>
                    <p class="skill-years">4 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-money-bill-wave"></i>
                    <h3 class="skill-title">Cash Flow Management</h3>
                    <p class="skill-years">2 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-users-cog"></i>
                    <h3 class="skill-title">Payroll Processing</h3>
                    <p class="skill-years">2 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-file-contract"></i>
                    <h3 class="skill-title">Contract Creation</h3>
                    <p class="skill-years">2 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fab fa-google"></i>
                    <h3 class="skill-title">Google Suite Admin</h3>
                    <p class="skill-years">2 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fab fa-microsoft"></i>
                    <h3 class="skill-title">Microsoft Office 365</h3>
                    <p class="skill-years">2 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-tasks"></i>
                    <h3 class="skill-title">Project Management</h3>
                    <p class="skill-years">2 years experience</p>
                </div>
                
                <div class="skill-item">
                    <i class="fas fa-user-tie"></i>
                    <h3 class="skill-title">Customer Interaction</h3>
                    <p class="skill-years">5 years experience</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact">
        <div class="container">
            <div class="section-subtitle">GET IN TOUCH</div>
            <h2 class="section-title">Contact Me</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Email</h3>
                            <p>kimberlyamurao60@gmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Phone</h3>
                            <p>+63 927 073 0710</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Location</h3>
                            <p>Calamba City, Laguna, Philippines</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contact-form">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Subject" required>
                        </div>
                        <div class="form-group">
                            <textarea class="form-control" placeholder="Your Message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="logo">Kimberly Amurao</div>
                <p>Finance & Administrative Professional</p>
               <div style="display: flex; justify-content: center;">
  <div class="social-icons">
    <a href="http://linkedin.com/in/kimberly-amurao-b060581b4" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-linkedin-in"></i>
    </a>
</div>
</div>                <p>&copy; 2025 Kimberly Amurao. All rights reserved.</p>
                <div class="footer-links">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                    <a href="#resume">Resume</a>
                    <a href="#contact">Contact</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Mobile Menu Toggle
        const hamburger = document.querySelector('.hamburger');
        const navMenu = document.querySelector('.nav-menu');
        
        hamburger.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });
        
        // Active Menu Item
        const navLinks = document.querySelectorAll('.nav-menu a');
        
        navLinks.forEach(link => {
            link.addEventListener('click', function() {
                navMenu.classList.remove('active');
                
                navLinks.forEach(navLink => {
                    navLink.classList.remove('active');
                });
                
                this.classList.add('active');
            });
        });
        
        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Contact Form Submission
<script>
        // Contact Form Submission
        const contactForm = document.getElementById('contact-form');
        
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Get form inputs
                const formElements = this.elements;
                const name = formElements[0].value;
                const email = formElements[1].value;
                const subject = formElements[2].value;
                const message = formElements[3].value;
                
                // Basic validation
                if (!name || !email || !subject || !message) {
                    alert('Please fill in all fields');
                    return;
                }
                
                // Here you would typically send the form data to your server
                // For demonstration, we'll just show a success message
                alert('Thanks for your message! I will get back to you soon.');
                this.reset();
            });
        }
        
        // Download CV
        const downloadButton = document.getElementById('download-cv');
        
        if (downloadButton) {
            downloadButton.addEventListener('click', function(e) {
                e.preventDefault();
                
                // In a real implementation, this would trigger a file download
                alert('CV download would start here. In a real implementation, link this to your actual CV file.');
            });
        }
        
        // Modal functionality for "Read More" links
        const readMoreLinks = document.querySelectorAll('.read-more');
        
        // Job details content for modals
        const jobDetails = {
            'freelancer': `
                <h3>Freelancer - Administrative and Finance Support</h3>
                <h4>Private Company - Amsterdam, Netherlands (July 2024 - Present)</h4>
                <ul>
                    <li>Managed daily administrative tasks for smooth operations.</li>
                    <li>Processed invoices, credit card expenses, and claims using various financial tools.</li>
                    <li>Prepared and filed sales invoices in Productive, ensuring accurate vendor documentation.</li>
                    <li>Served as the primary contact for financial inquiries related to invoices and subscriptions.</li>
                    <li>Maintained updated project and budget management systems.</li>
                    <li>Communicated with clients regarding payment issues and issued timely reminders.</li>
                    <li>Conducted weekly reviews of outstanding balances for prompt resolution.</li>
                    <li>Collaborated with team members to address billing and invoice discrepancies.</li>
                    <li>Assisted in setting up projects and budgets in Productive for accurate monitoring.</li>
                    <li>Drafted and reviewed client contracts using DocuSign, ensuring alignment with budgets and terms.</li>
                    <li>Tracked payroll changes (promotions, leaves, terminations) for accurate processing.</li>
                    <li>Managed access to Microsoft, Google, and password management systems for secure operations.</li>
                </ul>
            `,
            'emapta': `
                <h3>Administrative Assistant</h3>
                <h4>Emapta Philippines Inc. (Aug 2023 - June 2024)</h4>
                <ul>
                    <li>Reconciled credit card expenses and prepared monthly summary reports for client review.</li>
                    <li>Generated and sent timely invoices, ensuring accuracy and compliance using financial tools.</li>
                    <li>Followed up on outstanding payments to maintain healthy cash flow and client relationships.</li>
                    <li>Acted as the primary contact for administrative, HR, and finance-related inquiries.</li>
                    <li>Responded to both internal and external requests with professionalism and efficiency.</li>
                    <li>Monitored project budgets and reports, offering insights for decision-making.</li>
                    <li>Prepared contracts for clients and suppliers, ensuring all terms were clear and favorable.</li>
                </ul>
            `,
            'polyfame': `
                <h3>Admin and Accounts Payable Staff</h3>
                <h4>Polyfame Industries Inc. (Feb 2021 - Aug 2023)</h4>
                <ul>
                    <li>Prepare payments and control expenses on a day-to-day activities.</li>
                    <li>Validation of supplier documents ensuring 3-way PO matching is correctly done.</li>
                    <li>Responsible for scheduling supplier payment, communicating discrepancies and documentation, as well as the approval.</li>
                    <li>Petty Cash Fund Management.</li>
                    <li>Prepares payment and monthly, quarterly and annual BIR compliance report.</li>
                    <li>Statement of Account creation for customers.</li>
                    <li>Submits quarter and annual compliance report to BIR through EFPS.</li>
                    <li>Monitoring of employee attendance (leave, absences and overtime).</li>
                    <li>Payroll Processing, cheque manual encashment and manual payment to employees.</li>
                    <li>Accounts Payable and Receivable Management (end to end process).</li>
                    <li>Responsible for generating and maintaining monthly reports of expenses and collections.</li>
                    <li>Conducts weekly audit of supplies, petty cash and vouchers issued.</li>
                </ul>
            `,
            'groundscape': `
                <h3>Accounting Clerk</h3>
                <h4>Groundscape Management Inc. (Oct 2020 - Feb 2021)</h4>
                <ul>
                    <li>Handled and processed all check vouchers and cash vouchers transactions.</li>
                    <li>Reconciled the replenishment of revolving fund.</li>
                    <li>Data Entry in Quickbooks and ensures the accuracy of records.</li>
                    <li>Assisted in preparation of month-end reports.</li>
                    <li>2nd level checker of payroll records and entries.</li>
                    <li>Assisted in monthly Budget and Variance Report Analysis.</li>
                </ul>
            `,
            'aobs': `
                <h3>Administration Support</h3>
                <h4>AOBS - Advanced Outsourcing Business and Services Inc. (Mar 2019 - Feb 2020)</h4>
                <ul>
                    <li>Provides day to day balances of accounts-in-charge.</li>
                    <li>Processing and endorsing of orders.</li>
                    <li>Provides floater analysis reconciliation every day.</li>
                    <li>Identifies and allocates all payments and ensures that all cash is posted within required time frame.</li>
                    <li>Supports to month-end AR reports.</li>
                </ul>
            `
        };

        // Create modal
        function createModal(content) {
            // Create modal elements
            const modalOverlay = document.createElement('div');
            modalOverlay.className = 'modal-overlay';
            modalOverlay.style.position = 'fixed';
            modalOverlay.style.top = '0';
            modalOverlay.style.left = '0';
            modalOverlay.style.width = '100%';
            modalOverlay.style.height = '100%';
            modalOverlay.style.backgroundColor = 'rgba(0, 0, 0, 0.7)';
            modalOverlay.style.display = 'flex';
            modalOverlay.style.alignItems = 'center';
            modalOverlay.style.justifyContent = 'center';
            modalOverlay.style.zIndex = '1000';
            
            const modalContent = document.createElement('div');
            modalContent.className = 'modal-content';
            modalContent.style.backgroundColor = '#fff';
            modalContent.style.padding = '30px';
            modalContent.style.borderRadius = '15px';
            modalContent.style.maxWidth = '600px';
            modalContent.style.width = '90%';
            modalContent.style.maxHeight = '80vh';
            modalContent.style.overflow = 'auto';
            modalContent.style.position = 'relative';
            
            const closeBtn = document.createElement('button');
            closeBtn.className = 'modal-close';
            closeBtn.innerHTML = '×';
            closeBtn.style.position = 'absolute';
            closeBtn.style.top = '15px';
            closeBtn.style.right = '15px';
            closeBtn.style.fontSize = '24px';
            closeBtn.style.background = 'none';
            closeBtn.style.border = 'none';
            closeBtn.style.cursor = 'pointer';
            closeBtn.style.color = '#333';
            
            // Add content to modal
            modalContent.innerHTML += content;
            modalContent.appendChild(closeBtn);
            modalOverlay.appendChild(modalContent);
            document.body.appendChild(modalOverlay);
            
            // Close modal on click
            closeBtn.addEventListener('click', function() {
                document.body.removeChild(modalOverlay);
            });
            
            // Close modal when clicking outside
            modalOverlay.addEventListener('click', function(e) {
                if (e.target === modalOverlay) {
                    document.body.removeChild(modalOverlay);
                }
            });
        }
        
        // Add click event to read more links
        if (readMoreLinks) {
            readMoreLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const modalKey = this.getAttribute('data-modal');
                    if (jobDetails[modalKey]) {
                        createModal(jobDetails[modalKey]);
                    }
                });
            });
        }
        
        // Add scroll event for header background
        const header = document.querySelector('header');
        window.addEventListener('scroll', function() {
            if (window.scrollY > 100) {
                header.style.boxShadow = '0 5px 15px rgba(0,0,0,0.1)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0,0,0,0.05)';
            }
        });
        
        // Add active class to nav items on scroll
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-menu a');
            
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (window.scrollY >= (sectionTop - 100)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });
        
        // Add animation on scroll
        function animateOnScroll() {
            const elements = document.querySelectorAll('.timeline-item, .skill-item, .contact-item');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (elementPosition < windowHeight - 100) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        }
        
        // Set initial styles for animation
        document.querySelectorAll('.timeline-item, .skill-item, .contact-item').forEach(element => {
            element.style.opacity = '0';
            element.style.transform = 'translateY(20px)';
            element.style.transition = 'all 0.6s ease';
        });
        
        // Add scroll event for animations
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
        
        // Testimonials slider (if needed in the future)
        
        // Portfolio filter (if needed in the future)
    </script>
</body>
</html>
