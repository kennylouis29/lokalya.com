<?php
session_start();

// If the user is already logged in, redirect to main.php
if (isset($_SESSION['user_id'])) {
    header('Location: main.php');
    exit();
}

// Initialize variables
$error_message = '';
$success_message = '';

// Handle form submission
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    // Retrieve and sanitize input
    $email = trim($_POST['email'] ?? '');
    $password = trim($_POST['password'] ?? '');
    $full_name = trim($_POST['full_name'] ?? '');

    // Basic validation
    if (empty($email) || empty($password) || empty($full_name)) {
        $error_message = 'All fields are required.';
    } elseif (!filter_var($email, FILTER_VALIDATE_EMAIL)) {
        $error_message = 'Invalid email format.';
    } elseif (strlen($password) < 6) {
        $error_message = 'Password must be at least 6 characters long.';
    } else {
        // Connect to the database
        $conn = new mysqli('localhost', 'root', '', 'lokalya_db');

        // Check connection
        if ($conn->connect_error) {
            die('Connection failed: ' . $conn->connect_error);
        }

        // Check if email already exists
        $check_sql = "SELECT id FROM users WHERE email = ?";
        $stmt = $conn->prepare($check_sql);
        if ($stmt === false) {
            die('Prepare failed: ' . htmlspecialchars($conn->error));
        }
        $stmt->bind_param('s', $email);
        $stmt->execute();
        $stmt->store_result();

        if ($stmt->num_rows > 0) {
            $error_message = 'Email is already registered. Please use another.';
        } else {
            // Insert new user with plain text password
            $insert_sql = "INSERT INTO users (email, password, full_name) VALUES (?, ?, ?)";
            $insert_stmt = $conn->prepare($insert_sql);
            if ($insert_stmt === false) {
                die('Prepare failed: ' . htmlspecialchars($conn->error));
            }
            $insert_stmt->bind_param('sss', $email, $password, $full_name);

            if ($insert_stmt->execute()) {
                $success_message = 'Registration successful! You can now <a href="index.php">log in</a>.';
            } else {
                $error_message = 'Error registering user: ' . $insert_stmt->error;
            }

            $insert_stmt->close();
        }

        $stmt->close();
        $conn->close();
    }
}
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Sign Up</title>
    <style>
        /* Basic Reset & Styling */
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
            align-items: center;
            justify-content: center;
            padding: 0 20px;
        }
        .banner img {
            height: 100px;
            margin-right: 20px;
        }
        .banner h1 {
            font-size: 36px;
            font-weight: 700;
            color: white;
        }
        /* Container */
        .container {
            display: flex;
            width: 100%;
            flex: 1;
        }
        .image-section {
            width: 50%;
            background: url('img/indonesiaindex.jpeg') no-repeat center center;
            background-size: cover;
            position: relative;
            min-height: 500px;
        }
        .image-overlay {
            background: rgba(106, 125, 90, 0.5);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        .quote {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-size: 20px;
            font-weight: 600;
            text-align: center;
        }
        .credit {
            position: absolute;
            bottom: 10px;
            right: 10px;
            font-size: 12px;
            color: white;
        }
        /* Form Section */
        .form-section {
            width: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 40px;
            background: white;
            flex-direction: column;
        }
        h1, h2 {
            color: #6a7d5a;
            margin-bottom: 10px;
        }
        h2 { font-size: 22px; }
        form {
            display: flex;
            flex-direction: column;
            gap: 15px;
            width: 100%;
        }
        input[type="text"],
        input[type="email"],
        input[type="password"] {
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            width: 100%;
        }
        input[type="submit"] {
            padding: 10px;
            background-color: #6a7d5a;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            font-weight: bold;
            width: 100%;
            box-sizing: border-box;
        }
        input[type="submit"]:hover {
            background-color: #5b6c4d;
        }
        .signup-button {
            display: inline-block;
            text-decoration: none;
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            background-color: #6a7d5a;
            color: white;
            border-radius: 5px;
            font-weight: bold;
            font-size: 14px;
            width: 100%;
            box-sizing: border-box;
        }
        .signup-button:hover { background-color: #5b6c4d; }
        .error-message { color: red; text-align: center; }
        .success-message { color: green; text-align: center; }
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
        .footer-logo img { height: 120px; }
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
        <img src="img/lokalya.png" alt="Lokalya Logo">
        <h1>LOKALYA</h1>
    </div>

    <!-- Container -->
    <div class="container">
        <div class="image-section">
            <div class="image-overlay"></div>
            <div class="quote">"Embark on unforgettable journeys across Indonesia with Lokalya."</div>
            <div class="credit">📸 Mount Egon, Island of Flores</div>
        </div>

        <div class="form-section">
            <h1>Join Lokalya</h1>
            <h2>Sign Up</h2>

            <?php if (!empty($error_message)): ?>
                <p class="error-message"><?= htmlspecialchars($error_message) ?></p>
            <?php endif; ?>

            <?php if (!empty($success_message)): ?>
                <p class="success-message"><?= $success_message ?></p>
            <?php endif; ?>

            <form action="signup.php" method="post">
                <input type="text" name="full_name" placeholder="Full Name" required>
                <input type="email" name="email" placeholder="Email" required>
                <input type="password" name="password" placeholder="Password" required>
                <input type="submit" value="Sign Up">
            </form>
            <a href="index.php" class="signup-button">Back to Log In</a>
        </div>
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
            <p>Public Statistics</p>
            <p>Recommended Destinations</p>
        </div>
        <div class="footer-bottom">
            © 2024 Lokalya. All Rights Reserved.
        </div>
    </div>
</body>
</html>
