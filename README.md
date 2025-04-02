# PRODIGY_WD_01
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            height: 2000px; /* Just for scrolling effect */
        }
        
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: transparent;
            padding: 15px 20px;
            transition: background 0.3s ease;
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        
        .navbar a {
            text-decoration: none;
            color: black;
            font-size: 18px;
            padding: 10px 15px;
            transition: color 0.3s ease, background 0.3s ease;
        }
        
        .navbar a:hover {
            background: black;
            color: white;
            border-radius: 5px;
        }
        
        .scrolled {
            background: rgba(0, 0, 0, 0.8);
        }
        
        .scrolled a {
            color: white;
        }
    </style>
</head>
<body>
    
    <nav class="navbar" id="navbar">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
    </nav>
    
    <script>
        window.addEventListener('scroll', function() {
            let navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
    </script>
</body>
</html>
