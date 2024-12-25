<?php
session_start();

// Check if user is logged in; if not, redirect to index
if (!isset($_SESSION['user_id'])) {
    header('Location: index.php');
    exit();
}
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lokalya - Main</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Poppins', sans-serif;
            background: #f4f4f4;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        /* Top Banner */
        .banner {
            width: 100%;
            height: 120px;
            background: #6a7d5a;
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }
        .banner-left {
            display: flex;
            align-items: center;
        }
        .banner-left img {
            height: 100px;
            margin-right: 20px;
        }
        .banner-left h1 {
            font-size: 36px;
            font-weight: 700;
        }
        /* Dropdown Styles */
        .banner-right {
            position: relative;
            display: flex;
            align-items: center;
        }
        .user-dropdown {
            position: relative;
            display: inline-block;
        }
        .user-btn {
            background: none;
            border: none;
            color: white;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            padding: 10px 15px;
        }
        .user-btn:hover {
            background: rgba(0, 0, 0, 0.1);
        }
        .user-dropdown-content {
            display: none;
            position: absolute;
            right: 0;
            top: 100%;
            background-color: #fff;
            min-width: 160px;
            box-shadow: 0px 4px 10px rgba(0,0,0,0.2);
            border-radius: 4px;
            z-index: 9999;
        }
        .user-dropdown-content a {
            display: block;
            color: #333;
            padding: 12px 16px;
            text-decoration: none;
            font-size: 14px;
        }
        .user-dropdown-content a:hover {
            background-color: #f1f1f1;
        }
        .user-dropdown:hover .user-dropdown-content {
            display: block;
        }
        /* Main Content */
        .content-container {
            padding: 40px 20px;
            max-width: 1200px;
            margin: 0 auto;
            flex: 1;
        }
        .greeting {
            text-align: center;
            margin-bottom: 30px;
        }
        .greeting h2 {
            font-size: 28px;
            color: #6a7d5a;
        }
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }
        .feature-card {
            background: white;
            border-radius: 5px;
            padding: 20px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .feature-card h3 {
            font-size: 20px;
            color: #6a7d5a;
            margin-bottom: 10px;
        }
        .feature-card p {
            color: #333;
            font-size: 16px;
            line-height: 1.5;
        }
        /* Footer */
        .footer {
            width: 100%;
            background: #333;
            color: white;
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
        }
        .footer-logo img {
            height: 120px;
        }
        .footer-section h3 {
            font-size: 16px;
            font-weight: bold;
            margin-bottom: 10px;
        }
        .footer-section p {
            font-size: 14px;
            margin-bottom: 5px;
        }
        .footer-bottom {
            width: 100%;
            text-align: center;
            margin-top: 20px;
            font-size: 16px;
            color: #d1d1d1;
        }
    </style>
</head>
<body>
    <!-- Top Banner -->
    <div class="banner">
        <div class="banner-left">
            <img src="img/lokalya.png" alt="Lokalya Logo">
            <h1>LOKALYA</h1>
        </div>
        <!-- Right Section with Dropdown -->
        <div class="banner-right">
            <div class="user-dropdown">
                <div class="communication-logo">
                    <!-- Communication Forum Logo linked to forum page -->
                    <a href="forum.php">
                        <img src="https://t4.ftcdn.net/jpg/05/63/63/55/360_F_563635598_WBC0yMyndr4Ze9aTJDa5AYvV2fj0ZoWA.jpg" alt="Communication Forum Logo">
                    </a>
                </div>
                <button class="user-btn">
                    Hi, <?= htmlspecialchars($_SESSION['full_name']) ?> ▼
                </button>
                <div class="user-dropdown-content">
                    <!-- Link to the new pages -->
                    <a href="profile_settings.php">Profile Settings</a>
                    <a href="booking_history.php">Booking History</a>
                    <a href="my_reviews.php">My Reviews</a>
                    <a href="logout.php">Log Out</a>
                </div>
            </div>
        </div>
    </div>

    <!-- Main Content -->
    <div class="content-container">
        <div class="greeting">
            <h2>Welcome, <?= htmlspecialchars($_SESSION['full_name']) ?>!</h2>
            <p>Explore the best of Indonesia with Lokalya’s unique features.</p>
        </div>

        <div class="features-grid">
            <!-- Personalized Trips -->
            <div class="feature-card">
                <h3>Personalized Trips</h3>
                <p>
                    Get custom itineraries tailored to your interests. From mountains to beaches,
                    we suggest destinations that fit your style.
                </p>
                <h2><a href="book.php" class="btn">Plan Your Trip</a></h2>
            </div>

            <!-- Public Statistics -->
            <div class="feature-card">
                <h3>Public Statistics</h3>
                <p>
                    See real-time data on the hottest tourist spots, visitor counts, and local events.
                </p>
            </div>

            <!-- Recommended Destinations -->
            <div class="feature-card">
                <h3>Recommended Destinations</h3>
                <p>
                    Browse our curated list of must-visit places, from hidden gems to iconic landmarks.
                </p>
            </div>
        </div>
    </div>

<!-- Search Box Section -->
<div style="text-align: center; margin-top: 30px; margin-bottom: 100px; position: relative;">
    <h2 style="color: #6a7d5a;">Where do you want to go?</h2>
    <form action="search_results.php" method="GET" style="margin-top: 20px;">
        <input 
            type="text" 
            name="destination" 
            id="destination-search" 
            placeholder="Search destinations..." 
            style="padding: 10px; font-size: 16px; width: 300px; border: 1px solid #ccc; border-radius: 5px;"
            required
        >
        <button 
            type="submit" 
            style="padding: 10px 20px; background-color: #6a7d5a; color: white; border: none; border-radius: 5px; font-size: 16px; cursor: pointer; margin-left: 10px;"
        >
        <a href="destination.php">Search</a>
        </button>
    </form>
    <!-- Destination Suggestions Dropdown -->
    <ul id="suggestion-list" style="list-style-type: none; padding: 0; margin-top: 10px; display: none; background-color: white; border: 1px solid #ccc; border-radius: 5px; position: absolute; width: 300px; left: 50%; transform: translateX(-50%); z-index: 1000;">
        <li style="padding: 10px; border-bottom: 1px solid #ddd; cursor: pointer;">Bali</li>
        <li style="padding: 10px; border-bottom: 1px solid #ddd; cursor: pointer;">Yogyakarta</li>
        <li style="padding: 10px; border-bottom: 1px solid #ddd; cursor: pointer;">Bandung</li>
        <li style="padding: 10px; border-bottom: 1px solid #ddd; cursor: pointer;">Jakarta</li>
        <li style="padding: 10px; cursor: pointer;">Aceh</li>
    </ul>
</div>

<script>
    // JavaScript for showing the dropdown suggestions
    const searchBox = document.getElementById('destination-search');
    const suggestionList = document.getElementById('suggestion-list');

    searchBox.addEventListener('focus', () => {
        suggestionList.style.display = 'block';
    });

    searchBox.addEventListener('blur', () => {
        setTimeout(() => {
            suggestionList.style.display = 'none';
        }, 200); // Delay to allow clicks on suggestions
    });

    const suggestions = suggestionList.querySelectorAll('li');
    suggestions.forEach(suggestion => {
        suggestion.addEventListener('click', () => {
            searchBox.value = suggestion.textContent;
            suggestionList.style.display = 'none';
        });
    });
</script>

    <!-- Footer -->
<footer class="footer">
    <div class="footer-container">
        <!-- Logo Section -->
        <div class="footer-logo">
            <img src="img/lokalya.png" alt="Lokalya Logo">
        </div>
        
        <!-- Policy Section -->
        <div class="footer-section">
            <h3>Policy</h3>
            <ul>
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Terms of Service</a></li>
            </ul>
        </div>
        
        <!-- Features Section -->
        <div class="footer-section">
            <h3>Explore Features</h3>
            <ul>
                <li><a href="#">Personalized Trips</a></li>
                <li><a href="#">Recommended Destinations</a></li>
            </ul>
        </div>
    </div>
    
    <!-- Bottom Section -->
    <div class="footer-bottom">
        <p>© 2024 Lokalya. All Rights Reserved.</p>
    </div>
</footer>

<!-- Styles -->
<style>
    .footer {
        background: #333;
        color: white;
        padding: 20px 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .footer-container {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        width: 90%;
        max-width: 1200px;
        margin: 0 auto;
    }

    .footer-logo img {
        height: 80px;
    }

    .footer-section {
        margin-left: 20px;
    }

    .footer-section h3 {
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 10px;
    }

    .footer-section ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
    }

    .footer-section ul li {
        margin-bottom: 5px;
    }

    .footer-section ul li a {
        color: #ccc;
        text-decoration: none;
        font-size: 14px;
    }

    .footer-section ul li a:hover {
        color: #fff;
        text-decoration: underline;
    }

    .footer-bottom {
        width: 100%;
        text-align: center;
        margin-top: 20px;
        font-size: 14px;
        color: #d1d1d1;
    }

    .footer-bottom p {
        margin: 0;
    }
</style>

</html>
