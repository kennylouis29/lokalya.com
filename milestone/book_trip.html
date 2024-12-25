<?php
session_start();

// Check if user is logged in; if not, redirect to index
if (!isset($_SESSION['user_id'])) {
    header('Location: index.php');
    exit();
}

// Connect to the database
$conn = new mysqli('localhost', 'root', '', 'lokalya_db');
if ($conn->connect_error) {
    die('Connection failed: ' . $conn->connect_error);
}

// Handle form submission for booking trips
$successMessage = '';
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $userId = $_SESSION['user_id'];
    $travelDate = $_POST['travel_date'] ?? '';
    $numTravelers = (int)$_POST['num_travelers'] ?? 0;
    $preferences = trim($_POST['preferences'] ?? '');

    if (!empty($travelDate) && $numTravelers > 0) {
        // Save booking to the database
        $stmt = $conn->prepare("INSERT INTO bookings (user_id, destination, travel_date, num_travelers, preferences, created_at) VALUES (?, 'The Gili Islands', ?, ?, ?, NOW())");
        $stmt->bind_param('isis', $userId, $travelDate, $numTravelers, $preferences);

        if ($stmt->execute()) {
            $successMessage = 'Your trip has been successfully booked!';
        } else {
            $successMessage = 'Error booking your trip. Please try again.';
        }
        $stmt->close();
    } else {
        $successMessage = 'Please provide valid travel details.';
    }
}

$conn->close();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Book Your Trip</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        .banner {
            background: #6a7d5a;
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
        }
        .banner-left {
            display: flex;
            align-items: center;
        }
        .banner-left img {
            height: 80px;
            margin-right: 20px;
        }
        .banner-left h1 {
            font-size: 28px;
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
        .content {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        h2 {
            color: #6a7d5a;
            margin-bottom: 15px;
        }
        textarea, select, input, button {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 14px;
        }
        button {
            background: #6a7d5a;
            color: white;
            font-weight: bold;
            cursor: pointer;
            margin-top: 15px;
        }
        button:hover {
            background: #5b6c4d;
        }
        .success-message {
            color: green;
            margin: 15px 0;
            font-weight: bold;
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

    <!-- Content Section -->
    <div class="content">
        <h2>Book Your Trip to The Gili Islands</h2>
        <?php if (!empty($successMessage)): ?>
            <p class="success-message"><?= htmlspecialchars($successMessage) ?></p>
        <?php endif; ?>
        <form action="book_trip.php" method="POST">
            <label for="travel_date">Travel Date:</label>
            <input type="date" id="travel_date" name="travel_date" required>

            <label for="num_travelers">Number of Travelers:</label>
            <input type="number" id="num_travelers" name="num_travelers" min="1" required>

            <label for="preferences">Preferences (optional):</label>
            <textarea id="preferences" name="preferences" rows="4" placeholder="Enter any special requests or preferences..."></textarea>

            <button type="submit">Book Now</button>
        </form>
    </div>
</body>
</html>