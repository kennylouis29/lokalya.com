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

// Handle form submission for ratings and reviews
$successMessage = '';
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $userId = $_SESSION['user_id'];
    $rating = (int)$_POST['rating'] ?? 0;
    $review = trim($_POST['review'] ?? '');

    if ($rating >= 1 && $rating <= 5 && !empty($review)) {
        // Save review to the database
        $stmt = $conn->prepare("INSERT INTO gili_reviews (user_id, rating, review, created_at) VALUES (?, ?, ?, NOW())");
        $stmt->bind_param('iis', $userId, $rating, $review);
        if ($stmt->execute()) {
            $successMessage = 'Thank you for your review!';
        } else {
            $successMessage = 'Error saving your review. Please try again.';
        }
        $stmt->close();
    } else {
        $successMessage = 'Please provide a valid rating and review.';
    }
}

// Fetch all reviews for display
$reviews = [];
$result = $conn->query("SELECT rating, review, created_at FROM gili_reviews ORDER BY created_at DESC");
if ($result) {
    $reviews = $result->fetch_all(MYSQLI_ASSOC);
}

// Fetch rating statistics
$ratingsStats = [];
for ($i = 1; $i <= 5; $i++) {
    $result = $conn->query("SELECT COUNT(*) AS count FROM gili_reviews WHERE rating = $i");
    $row = $result->fetch_assoc();
    $ratingsStats[$i] = $row['count'] ?? 0;
}

// Calculate the average rating
$result = $conn->query("SELECT AVG(rating) AS avg_rating FROM gili_reviews");
$averageRating = $result->fetch_assoc()['avg_rating'] ?? 0;
$averageRating = number_format($averageRating, 1);
$conn->close();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>The Gili Islands</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background: #f4f4f4;
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
        .content img {
            max-width: 100%;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        h2 {
            color: #6a7d5a;
            margin-bottom: 15px;
        }
        .fun-facts ul {
            list-style-type: square;
            padding-left: 20px;
        }
        .rating-stats ul {
            list-style: none;
            padding: 0;
        }
        .rating-stats ul li {
            margin-bottom: 5px;
        }
        .average-rating {
            font-size: 20px;
            color: #6a7d5a;
            font-weight: bold;
        }
        textarea, select, button {
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
        .review-item {
            border-bottom: 1px solid #ddd;
            padding: 15px 0;
        }
        .review-item:last-child {
            border-bottom: none;
        }
        .rating {
            color: #ffc107;
            font-size: 18px;
            font-weight: bold;
        }
        .review-text {
            margin: 10px 0;
            font-size: 16px;
        }
        .review-date {
            font-size: 12px;
            color: #666;
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
        <img src="img/gili.jpg" alt="The Gili Islands">
        <h2>Introduction</h2>
        <p>
            The Gili Islands, located off the coast of Lombok, Indonesia, are a tropical paradise. Known for their crystal-clear waters, white sandy beaches, and vibrant coral reefs, they offer a perfect getaway for travelers seeking serenity and adventure.
        </p>

        <h2>Fun Facts</h2>
        <div class="fun-facts">
            <ul>
                <li>There are three main islands: Gili Trawangan, Gili Meno, and Gili Air.</li>
                <li>No motorized vehicles are allowed on the islands – travel is by bicycle or horse-drawn carts.</li>
                <li>They are a hotspot for scuba diving and snorkeling enthusiasts.</li>
            </ul>
        </div>

        <h2>Rating Statistics</h2>
        <div class="rating-stats">
            <p class="average-rating">Average Rating: <?= $averageRating ?>/5.0</p>
            <ul>
                <?php for ($i = 5; $i >= 1; $i--): ?>
                    <li>⭐<?= $i ?>: <?= $ratingsStats[$i] ?? 0 ?> reviews</li>
                <?php endfor; ?>
            </ul>
        </div>

        <!-- Book the Trip Button -->
<h2>Book the Trip</h2>
<p>Ready to experience the beauty of the Gili Islands? Click the button below to book your trip now!</p>
<form action="book_trip.php" method="GET" style="text-align: center; margin-top: 20px;">
    <button type="submit" style="
        background-color: #6a7d5a;
        color: white;
        border: none;
        border-radius: 5px;
        padding: 15px 30px;
        font-size: 16px;
        font-weight: bold;
        cursor: pointer;
    ">
        Book the Trip
    </button>
</form>

        <h2>Leave Your Rating and Review</h2>
        <?php if (!empty($successMessage)): ?>
            <p class="success-message"><?= htmlspecialchars($successMessage) ?></p>
        <?php endif; ?>
        <form action="gili.php" method="POST" class="review-form">
            <label for="rating">Rating (1 to 5):</label>
            <select id="rating" name="rating" required>
                <option value="" disabled selected>Select your rating</option>
                <option value="1">1 - Poor</option>
                <option value="2">2 - Fair</option>
                <option value="3">3 - Good</option>
                <option value="4">4 - Very Good</option>
                <option value="5">5 - Excellent</option>
            </select>

            <label for="review">Your Review:</label>
            <textarea id="review" name="review" rows="5" placeholder="Share your experience..." required></textarea>

            <button type="submit">Submit Review</button>
        </form>

        <h2>All Reviews</h2>
        <?php if (!empty($reviews)): ?>
            <?php foreach ($reviews as $review): ?>
                <div class="review-item">
                    <div class="rating">⭐ <?= htmlspecialchars($review['rating']) ?>/5.0</div>
                    <div class="review-text"><?= htmlspecialchars($review['review']) ?></div>
                    <div class="review-date"><?= date('F j, Y, g:i a', strtotime($review['created_at'])) ?></div>
                </div>
            <?php endforeach; ?>
        <?php else: ?>
            <p>No reviews yet. Be the first to leave one!</p>
        <?php endif; ?>
    </div>
</body>
</html>
