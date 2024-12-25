<?php
session_start();

// 1. Check if user is logged in
if (!isset($_SESSION['user_id'])) {
    header('Location: index.php');
    exit();
}

// 2. Connect to the database
$conn = new mysqli('localhost', 'root', '', 'lokalya_db');
if ($conn->connect_error) {
    die('Connection failed: ' . $conn->connect_error);
}

// Initialize feedback messages
$feedback = '';
$error = '';

// 3. Handle form submission
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $newFullName = trim($_POST['full_name'] ?? '');
    $newBirthday = trim($_POST['birthday'] ?? '');

    // Validate input
    if (empty($newFullName)) {
        $error = 'Full Name cannot be empty.';
    } elseif (!empty($newBirthday) && !preg_match('/^\d{4}-\d{2}-\d{2}$/', $newBirthday)) {
        $error = 'Invalid birthday format. Use YYYY-MM-DD.';
    } else {
        // Prepare the UPDATE query
        $update_sql = "UPDATE users SET full_name = ?, birthday = ? WHERE id = ?";
        $stmt = $conn->prepare($update_sql);
        if ($stmt === false) {
            die('Prepare failed: ' . htmlspecialchars($conn->error));
        }
        $stmt->bind_param('ssi', $newFullName, $newBirthday, $_SESSION['user_id']);

        if ($stmt->execute()) {
            if ($stmt->affected_rows > 0) {
                // Update session variable
                $_SESSION['full_name'] = $newFullName;
                $feedback = 'Profile updated successfully!';
            } else {
                $error = 'No changes were made.';
            }
        } else {
            $error = 'Error updating profile: ' . $stmt->error;
        }

        $stmt->close();
    }
}

// 4. Fetch current profile info to display in the form
$sql = "SELECT full_name, email, birthday FROM users WHERE id = ?";
$stmt = $conn->prepare($sql);
if ($stmt === false) {
    die('Prepare failed: ' . htmlspecialchars($conn->error));
}
$stmt->bind_param('i', $_SESSION['user_id']);
$stmt->execute();
$result = $stmt->get_result();
$userData = $result->fetch_assoc(); // Fetch the user's data
$stmt->close();

$conn->close();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Lokalya - Profile Settings</title>
    <style>
        body { font-family: Arial, sans-serif; background: #f4f4f4; margin: 0; padding: 0; }
        .navbar {
            background: #6a7d5a;
            color: #fff;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .navbar .welcome { font-size: 18px; }
        .navbar .nav-links a {
            color: #fff;
            text-decoration: none;
            margin-left: 15px;
            font-weight: bold;
        }
        .container {
            width: 100%;
            max-width: 500px;
            margin: 40px auto;
            background: #fff;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h2 { text-align: center; color: #6a7d5a; }
        .feedback { padding: 10px; margin-bottom: 15px; border-radius: 4px; }
        .success { background: #e0ffe0; color: #006600; }
        .error { background: #ffe0e0; color: #cc0000; }
        label { display: block; margin: 15px 0 5px; font-weight: 600; }
        input[type="text"], input[type="email"], input[type="date"] {
            width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px;
        }
        button {
            width: 100%; padding: 12px; background: #6a7d5a; color: #fff; border: none; border-radius: 4px; cursor: pointer; font-size: 16px;
        }
        button:hover { background: #5b6c4d; }
        .back-link { text-align: center; margin-top: 20px; }
        .back-link a { color: #0066cc; text-decoration: none; font-weight: bold; }
    </style>
</head>
<body>
    <div class="navbar">
        <div class="welcome">
            Welcome, <?= htmlspecialchars($_SESSION['full_name']) ?>!
        </div>
        <div class="nav-links">
            <a href="main.php">Main Page</a>
            <a href="logout.php">Logout</a>
        </div>
    </div>

    <div class="container">
        <h2>Profile Settings</h2>

        <!-- Display success or error messages -->
        <?php if (!empty($feedback)): ?>
            <div class="feedback success"><?= htmlspecialchars($feedback) ?></div>
        <?php endif; ?>
        <?php if (!empty($error)): ?>
            <div class="feedback error"><?= htmlspecialchars($error) ?></div>
        <?php endif; ?>

        <form action="profile_settings.php" method="post">
            <!-- Email (read-only) -->
            <label for="email">Email (cannot be changed):</label>
            <input type="email" id="email" name="email" value="<?= htmlspecialchars($userData['email'] ?? '') ?>" readonly>

            <!-- Full Name (editable) -->
            <label for="full_name">Full Name:</label>
            <input type="text" id="full_name" name="full_name" value="<?= htmlspecialchars($userData['full_name'] ?? '') ?>" required>

            <!-- Birthday (editable) -->
            <label for="birthday">Birthday:</label>
            <input type="date" id="birthday" name="birthday" value="<?= htmlspecialchars($userData['birthday'] ?? '') ?>">

            <button type="submit">Save Changes</button>
        </form>

        <div class="back-link">
            <a href="main.php">← Back to Main Page</a>
        </div>
    </div>
</body>
</html>
