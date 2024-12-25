<?php
session_start();

// Check if user is logged in; if not, redirect to index
if (!isset($_SESSION['user_id'])) {
    header('Location: index.php');
    exit();
}

// Database connection
$conn = new mysqli('localhost', 'root', '', 'lokalya_db');
if ($conn->connect_error) {
    die('Connection failed: ' . $conn->connect_error);
}

// Fetch user's reviews
$userId = $_SESSION['user_id'];
$sql = "SELECT review, rating, created_at FROM gili_reviews WHERE user_id = ? ORDER BY created_at DESC";
$stmt = $conn->prepare($sql);
$stmt->bind_param('i', $userId);
$stmt->execute();
$result = $stmt->get_result();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Lokalya - My Reviews</title>
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
        <h1>My Reviews</h1>
    </div>

    <!-- Content Section -->
    <div class="content">
        <h2>Your Reviews</h2>

        <?php if ($result->num_rows > 0): ?>
            <?php while ($row = $result->fetch_assoc()): ?>
                <div class="review-item">
                    <div class="rating">⭐ <?= $row['rating'] ?>/5.0</div>
                    <div class="review-text"><?= htmlspecialchars($row['review']) ?></div>
                    <div class="review-date"><?= date('F j, Y, g:i a', strtotime($row['created_at'])) ?></div>
                </div>
            <?php endwhile; ?>
        <?php else: ?>
            <p>You haven't submitted any reviews yet.</p>
        <?php endif; ?>

        <a href="main.php" style="display: block; margin-top: 20px; text-align: center; color: #6a7d5a; text-decoration: none;">← Back to Main Page</a>
    </div>
</body>
</html>
