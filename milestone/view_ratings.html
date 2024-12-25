<?php
session_start();

// Check if user is logged in; if not, redirect to index
if (!isset($_SESSION['user_id'])) {
    header('Location: index.php');
    exit();
}

// Database connection (update with your credentials)
$conn = new mysqli('localhost', 'root', '', 'lokalya_db');
if ($conn->connect_error) {
    die('Connection failed: ' . $conn->connect_error);
}

// Fetch all reviews and ratings for the Gili Islands
$sql = "SELECT rating, review, created_at FROM gili_reviews ORDER BY created_at DESC";
$result = $conn->query($sql);
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Gili Islands - Reviews</title>
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
            padding: 20px;
            text-align: center;
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
        .review-item {
            border-bottom: 1px solid #ddd;
            padding: 15px 0;
        }
        .review-item:last-child {
            border-bottom: none;
        }
        .rating {
            color: #ffc107; /* Gold for stars */
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
        .back-btn {
            display: block;
            margin-top: 20px;
            padding: 10px 20px;
            background: #6a7d5a;
            color: white;
            text-align: center;
            text-decoration: none;
            border-radius: 5px;
        }
        .back-btn:hover {
            background: #5b6c4d;
        }
    </style>
</head>
<body>
    <!-- Top Banner -->
    <div class="banner">
        <h1>Reviews for The Gili Islands</h1>
    </div>

    <!-- Content Section -->
    <div class="content">
        <h2>Customer Reviews</h2>

        <?php if ($result->num_rows > 0): ?>
            <?php while ($row = $result->fetch_assoc()): ?>
                <div class="review-item">
                    <div class="rating">⭐ <?= $row['rating'] ?>/5.0</div>
                    <div class="review-text"><?= htmlspecialchars($row['review']) ?></div>
                    <div class="review-date"><?= date('F j, Y, g:i a', strtotime($row['created_at'])) ?></div>
                </div>
            <?php endwhile; ?>
        <?php else: ?>
            <p>No reviews yet. Be the first to leave a review!</p>
        <?php endif; ?>

        <a href="gili.php" class="back-btn">Back to The Gili Islands</a>
    </div>
</body>
</html>
