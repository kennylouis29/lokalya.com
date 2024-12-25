<?php
session_start();
include 'db_connect.php'; // Include your database connection file

// Check if user is logged in
if (!isset($_SESSION['user_id'])) {
    header("Location: index.php");
    exit();
}

$user_id = $_SESSION['user_id'];

// Handle form submission for custom trips
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $destination = $_POST['destination'];
    $duration = $_POST['duration'];
    $num_passengers = $_POST['num_passengers'];
    $accommodation = $_POST['accommodation'];

    // Insert into database
    $query = "INSERT INTO book (user_id, destination, duration, num_passengers, accommodation) VALUES (?, ?, ?, ?, ?)";
    $stmt = $conn->prepare($query);
    $stmt->bind_param("isiss", $user_id, $destination, $duration, $num_passengers, $accommodation);

    if ($stmt->execute()) {
        $success_message = "Trip successfully saved!";
    } else {
        $error_message = "Failed to save trip. Please try again.";
    }
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

    <div class="container">
        <h1>Personalize Your Trip</h1>

        <?php if (isset($success_message)) echo "<p class='success'>$success_message</p>"; ?>
        <?php if (isset($error_message)) echo "<p class='error'>$error_message</p>"; ?>

        <form action="sendmail.php" method="POST">
            <label for="destination">Destination:</label>
            <input type="text" id="destination" name="destination" required>

            <label for="duration">Duration (days):</label>
            <input type="number" id="duration" name="duration" min="1" required>

            <label for="num_passengers">Number of Passengers:</label>
            <input type="number" id="num_passengers" name="num_passengers" min="1" required>

            <label for="accommodation">Preferred Accommodation:</label>
            <input type="text" id="accommodation" name="accommodation" required>

            <button type="submit">Save Trip and Send Email</button>
        </form>
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