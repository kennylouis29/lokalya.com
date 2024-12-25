<?php
session_start();

// Check if user is logged in; if not, redirect to index
if (!isset($_SESSION['user_id'])) {
    header('Location: index.php');
    exit();
}

// Optionally capture the GET parameter (?destination=...) if you want to display or filter results
$searchQuery = isset($_GET['destination']) ? htmlspecialchars($_GET['destination']) : null;
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Lokalya - Destinations</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        html, body {
            height: 100%;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background: #f4f4f4;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        .banner {
            width: 100%;
            height: 120px;
            background: #6a7d5a;
            color: white;
            display: flex;
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
        .content-container {
            padding: 40px 20px;
            max-width: 1200px;
            margin: 0 auto;
            flex: 1;
        }
        .content-container h2 {
            text-align: center;
            font-size: 28px;
            color: #6a7d5a;
            margin-bottom: 30px;
        }
        .destinations {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-between;
        }
        .dest-card {
            flex: 1 1 calc(33.333% - 20px);
            max-width: calc(33.333% - 20px);
            background: white;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        .dest-card:hover {
            transform: scale(1.02);
        }
        .dest-card img {
            width: 100%;
            height: 200px; 
            object-fit: cover;
        }
        .dest-info {
            padding: 20px;
            text-align: center;
        }
        .dest-info h3 {
            font-size: 20px;
            color: #6a7d5a;
            margin-bottom: 10px;
        }
        .dest-info p {
            font-size: 14px;
            color: #333;
        }
        .rating {
            margin-top: 10px;
            color: #ffc107; /* gold star color */
            font-weight: bold;
        }
        /* Footer */
        .footer {
            background: #333;
            color: white;
            padding: 20px 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-top: auto;
        }
        .footer p {
            font-size: 14px;
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
        <div class="banner-right">
            <div class="user-dropdown">
                <button class="user-btn">
                    Hi, <?= htmlspecialchars($_SESSION['full_name']) ?> ▼
                </button>
                <div class="user-dropdown-content">
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
        <h2>
            <?php if ($searchQuery): ?>
                Destinations for "<?= $searchQuery ?>"
            <?php else: ?>
                Explore Indonesian Destinations
            <?php endif; ?>
        </h2>

        <!-- Destination Boxes -->
        <div class="destinations">
            <!-- Destination 1: Komodo National Park -->
            <div class="dest-card">
                <img src="img/komodo.jpg" alt="Komodo National Park">
                <div class="dest-info">
                    <h3>Komodo National Park</h3>
                    <p>Home to the Komodo dragons</p>
                    <div class="rating">⭐4.0/5.0</div>
                </div>
            </div>

            <!-- Destination 2: Tana Toraja -->
            <div class="dest-card">
                <img src="img/toraja.jpg" alt="Tana Toraja">
                <div class="dest-info">
                    <h3>Tana Toraja</h3>
                    <p>Cultural highlands in South Sulawesi</p>
                    <div class="rating">⭐4.0/5.0</div>
                </div>
            </div>

            <!-- Destination 3: Kerinci Valley -->
            <div class="dest-card">
                <img src="img/kerinci.jpg" alt="Kerinci Valley">
                <div class="dest-info">
                    <h3>Kerinci Valley</h3>
                    <p>Volcanic landscapes and lush tea fields</p>
                    <div class="rating">⭐4.0/5.0</div>
                </div>
            </div>

            <!-- Destination 4: The Gili Islands -->
            <div class="dest-card">
                <a href="gili.php" style="text-decoration: none; color: inherit;">
                    <img src="img/gili.jpg" alt="The Gili Islands">
                    <div class="dest-info">
                        <h3>The Gili Islands</h3>
                        <p>Crystal-clear waters & vibrant marine life</p>
                        <div class="rating">⭐4.0/5.0</div>
                    </div>
                </a>
            </div>

            <!-- Destination 5: Candi Prambanan -->
            <div class="dest-card">
                <img src="img/prambanan.jpg" alt="Candi Prambanan">
                <div class="dest-info">
                    <h3>Candi Prambanan</h3>
                    <p>Majestic Hindu temple compound</p>
                    <div class="rating">⭐4.0/5.0</div>
                </div>
            </div>

            <!-- Destination 6: Kawah Ijen -->
            <div class="dest-card">
                <img src="img/kawah_ijen.jpg" alt="Kawah Ijen">
                <div class="dest-info">
                    <h3>Kawah Ijen</h3>
                    <p>Famed for its blue fire and sulfur lake</p>
                    <div class="rating">⭐4.0/5.0</div>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="footer">
        <p>© 2024 Lokalya. All Rights Reserved.</p>
    </footer>
</body>
</html>
