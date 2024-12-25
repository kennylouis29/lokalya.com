<?php
session_start();

// Check if user is logged in; if not, redirect to index
if (!isset($_SESSION['user_id'])) {
    header('Location: index.php');
    exit();
}

// Reset the chat history every time we visit
if (!isset($_SESSION['messages'])) {
    $_SESSION['messages'] = [
        ['username' => 'Chatbot', 'message' => 'Hello! How can I assist you today?']
    ];
}

// Handle new message (send a message to the "chat")
if ($_SERVER['REQUEST_METHOD'] == 'POST' && isset($_POST['new_message'])) {
    $message = $_POST['message'];
    $username = $_SESSION['full_name']; // Get the logged-in user's name

    // Add the new message from the user to the session array
    $_SESSION['messages'][] = ['username' => $username, 'message' => $message];

    // Generate a response from the chatbot based on the message
    $bot_reply = generateBotResponse($message);
    $_SESSION['messages'][] = ['username' => 'Chatbot', 'message' => $bot_reply];
}

// Function to generate a bot response based on user input
function generateBotResponse($userMessage) {
    $userMessage = strtolower($userMessage);

    // 1. Handle basic mathematical operations (addition, subtraction, etc.)
    if (preg_match('/(\d+)\s*\+\s*(\d+)/', $userMessage, $matches)) {
        $result = $matches[1] + $matches[2];
        return "The result of {$matches[1]} + {$matches[2]} is {$result}.";
    } elseif (preg_match('/(\d+)\s*\-\s*(\d+)/', $userMessage, $matches)) {
        $result = $matches[1] - $matches[2];
        return "The result of {$matches[1]} - {$matches[2]} is {$result}.";
    } elseif (preg_match('/(\d+)\s*\*\s*(\d+)/', $userMessage, $matches)) {
        $result = $matches[1] * $matches[2];
        return "The result of {$matches[1]} * {$matches[2]} is {$result}.";
    } elseif (preg_match('/(\d+)\s*\/\s*(\d+)/', $userMessage, $matches)) {
        if ($matches[2] == 0) {
            return "Division by zero is not allowed.";
        }
        $result = $matches[1] / $matches[2];
        return "The result of {$matches[1]} / {$matches[2]} is {$result}.";
    }

    // 2. Respond to greetings or polite conversation
    if (strpos($userMessage, 'hello') !== false || strpos($userMessage, 'hi') !== false) {
        return "Hello! How can I assist you today?";
    } elseif (strpos($userMessage, 'how are you') !== false) {
        return "I'm doing great! How about you?";
    } elseif (strpos($userMessage, 'thank you') !== false) {
        return "You're welcome! I'm happy to help!";
    }

    // 3. Handle general knowledge queries
    if (strpos($userMessage, 'capital of france') !== false) {
        return "The capital of France is Paris.";
    } elseif (strpos($userMessage, 'earth') !== false) {
        return "The Earth is the third planet from the Sun and is the only known planet to support life.";
    } elseif (strpos($userMessage, 'indonesia') !== false) {
        return "Indonesia is an archipelago in Southeast Asia, made up of over 17,000 islands.";
    }

    // 4. Weather inquiries
    if (strpos($userMessage, 'weather') !== false) {
        return "The weather in Indonesia is tropical, with distinct wet and dry seasons depending on the region.";
    }

    // 5. Travel-related queries
    if (strpos($userMessage, 'bali') !== false) {
        return "Bali is known for its stunning beaches, temples, and rich cultural heritage.";
    } elseif (strpos($userMessage, 'mount bromo') !== false) {
        return "Mount Bromo is an active volcano in East Java, Indonesia. It is famous for its sunrise views.";
    }

    // Default fallback response
    return "I'm not sure how to respond to that. Could you clarify or ask something else?";
}
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chatbot - Communication Forum</title>
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
            position: relative;
        }

        /* Background Banner */
        .banner {
            width: 100%;
            height: 120px;
            background: #6a7d5a;
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: absolute;
            top: 0;
            left: 0;
            padding: 0 20px;
            z-index: -1;
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

        /* Footer */
        .footer {
            width: 100%;
            background: #333;
            color: white;
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            position: absolute;
            bottom: 0;
            left: 0;
            z-index: -1;
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

        /* Main Content */
        .content-wrapper {
            position: relative;
            z-index: 2;
            padding: 20px;
            width: 100%;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .chat-container {
            max-width: 800px;
            width: 100%;
            margin: 30px auto;
            background: rgba(255, 255, 255, 0.9); /* Slight transparency */
            padding: 20px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }

        .chat-box {
            height: 400px;
            overflow-y: auto;
            border: 1px solid #ddd;
            padding: 15px;
            background: #f9f9f9;
            margin-bottom: 20px;
            border-radius: 5px;
        }

        .chat-message {
            margin: 10px 0;
        }

        .chat-message .message-user {
            font-weight: bold;
        }

        .chat-message .message-text {
            margin-left: 10px;
            background: #e9e9e9;
            padding: 8px;
            border-radius: 5px;
        }

        .chat-input {
            display: flex;
            gap: 10px;
        }

        .chat-input input {
            width: 80%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .chat-input button {
            width: 18%;
            background-color: #6a7d5a;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 5px;
        }

        .chat-input button:hover {
            background-color: #556b46;
        }

    </style>
</head>
<body>

<!-- Top Banner -->
<div class="banner">
    <div class="banner-left">
        <img src="lokalya.png" alt="Logo">
        <h1>LOKALYA</h1>
    </div>
</div>

<!-- Content Wrapper -->
<div class="content-wrapper">
    <div class="chat-container">
        <h2>Welcome to the Communication Forum</h2>

        <!-- Chat Box -->
        <div class="chat-box" id="chat-box">
            <?php foreach ($_SESSION['messages'] as $message): ?>
                <div class="chat-message">
                    <span class="message-user"><?= htmlspecialchars($message['username']) ?>:</span>
                    <span class="message-text"><?= nl2br(htmlspecialchars($message['message'])) ?></span>
                </div>
            <?php endforeach; ?>
        </div>

        <!-- Chat Input -->
        <form method="POST" class="chat-input">
            <input type="text" name="message" id="message" placeholder="Type your message here..." required>
            <button type="submit" name="new_message">Send</button>
        </form>
    </div>
</div>

<!-- Footer -->
<div class="footer">
    <div class="footer-logo">
        <img src="lokalya.png" alt="Logo">
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

<script>
    // Scroll to the bottom of the chat box
    const chatBox = document.getElementById('chat-box');
    chatBox.scrollTop = chatBox.scrollHeight;
</script>

</body>
</html>
