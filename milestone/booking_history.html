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

// Fetch booking history for the logged-in user
$user_id = $_SESSION['user_id'];

$sql = "SELECT id, destination, travel_date, num_travelers, preferences, created_at 
        FROM bookings WHERE user_id = ?";
$stmt = $conn->prepare($sql);
if ($stmt === false) {
    die('Prepare failed: ' . htmlspecialchars($conn->error));
}
$stmt->bind_param('i', $user_id);
$stmt->execute();
$result = $stmt->get_result();
$bookings = $result->fetch_all(MYSQLI_ASSOC);

$stmt->close();
$conn->close();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lokalya - Booking History</title>
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
            flex: 1;
            padding: 40px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .content-container h2 {
            color: #6a7d5a;
            font-size: 28px;
            margin-bottom: 20px;
            text-align: center;
        }

        table {
            margin: 20px auto;
            border-collapse: collapse;
            width: 90%;
            background: white;
            border-radius: 5px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        th, td {
            padding: 12px 15px;
            text-align: left;
        }
        th {
            background: #6a7d5a;
            color: #fff;
        }
        tr:nth-child(even) {
            background: #f9f9f9;
        }
        td {
            font-size: 14px;
            color: #333;
        }
        .no-history {
            text-align: center;
            margin: 40px 0;
            color: #666;
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
        <h2>Booking History</h2>
        <?php if (!empty($bookings)): ?>
            <table>
                <tr>
                    <th>Booking ID</th>
                    <th>Destination</th>
                    <th>Travel Date</th>
                    <th>Travelers</th>
                    <th>Preferences</th>
                    <th>Created At</th>
                </tr>
                <?php foreach ($bookings as $booking): ?>
                    <tr>
                        <td><?= htmlspecialchars($booking['id']) ?></td>
                        <td><?= htmlspecialchars($booking['destination']) ?></td>
                        <td><?= htmlspecialchars($booking['travel_date']) ?></td>
                        <td><?= htmlspecialchars($booking['num_travelers']) ?></td>
                        <td><?= htmlspecialchars($booking['preferences']) ?></td>
                        <td><?= htmlspecialchars($booking['created_at']) ?></td>
                    </tr>
                <?php endforeach; ?>
            </table>
        <?php else: ?>
            <p class="no-history">You have no booking history yet.</p>
        <?php endif; ?>
    </div>

    <!-- Footer -->
    <div class="footer">
        <div class="footer-logo">
            <img src="img/lokalya.png" alt="Lokalya Logo">
        </div>
        <div class="footer-section">
            <h3>Policy</h3>
            <p>Privacy Policy</p>
            <p>Terms of Service</p>
        </div>
        <div class="footer-section">
            <h3>Explore Features</h3>
            <p>Personalized Trips</p>
            <p>Recommended Destinations</p>
        </div>
        <div class="footer-bottom">
            © 2024 Lokalya. All Rights Reserved.
        </div>
    </div>

</body>
</html>
