<?php
session_start();
use PHPMailer\PHPMailer\PHPMailer;
use PHPMailer\PHPMailer\Exception;

require 'PHPMailer/src/Exception.php';
require 'PHPMailer/src/PHPMailer.php';
require 'PHPMailer/src/SMTP.php';

include 'db_connect.php'; // Include database connection

// Check if user is logged in
if (!isset($_SESSION['user_id'])) {
    header("Location: index.php");
    exit();
}

$user_id = $_SESSION['user_id'];
$user_email = $_SESSION['email']; // Ensure the email is set in the session during login

// Check if form data exists
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $destination = htmlspecialchars($_POST['destination']);
    $duration = htmlspecialchars($_POST['duration']);
    $num_passengers = htmlspecialchars($_POST['num_passengers']);
    $accommodation = htmlspecialchars($_POST['accommodation']);

    // Insert the data into the database (optional)
    $query = "INSERT INTO book (user_id, destination, duration, num_passengers, accommodation) VALUES (?, ?, ?, ?, ?)";
    $stmt = $conn->prepare($query);
    $stmt->bind_param("isiss", $user_id, $destination, $duration, $num_passengers, $accommodation);

    if ($stmt->execute()) {
        // Use PHPMailer to send the email
        $mail = new PHPMailer(true);

        try {
            // SMTP configuration
            $mail->isSMTP();
            $mail->Host = 'smtp.gmail.com';
            $mail->SMTPAuth = true;
            $mail->Username = 'lokalya1010@gmail.com'; // Your SMTP email
            $mail->Password = 'iuwo emga zymu xfvt'; // Your SMTP password or App Password
            $mail->SMTPSecure = PHPMailer::ENCRYPTION_SMTPS;
            $mail->Port = 465;

            // Recipients
            $mail->setFrom('lokalya1010@gmail.com', 'Lokalya');
            $mail->addAddress($user_email);

            // Email Content
            $mail->isHTML(true);
            $mail->Subject = 'Your Personalized Trip Details';
            $mail->Body = '<h1>Your Trip Details</h1>';
            $mail->Body .= '<table border="1" cellpadding="5" cellspacing="0">';
            $mail->Body .= '<tr><th>Destination</th><th>Duration</th><th>Number of Passengers</th><th>Accommodation</th></tr>';
            $mail->Body .= '<tr>';
            $mail->Body .= '<td>' . $destination . '</td>';
            $mail->Body .= '<td>' . $duration . ' days</td>';
            $mail->Body .= '<td>' . $num_passengers . '</td>';
            $mail->Body .= '<td>' . $accommodation . '</td>';
            $mail->Body .= '</tr>';
            $mail->Body .= '</table>';

            // Send the email
            $mail->send();
            echo "Trip details have been sent to your email!";
            echo '<p>You will be redirected to the main page in 5 seconds...</p>';
            echo '<meta http-equiv="refresh" content="5;url=index.php">';
            
        } catch (Exception $e) {
            echo "Email could not be sent. Mailer Error: {$mail->ErrorInfo}";
        }
    } else {
        echo "Failed to save trip details in the database.";
    }
} else {
    echo "Invalid request. Please submit the form.";
}
?>
