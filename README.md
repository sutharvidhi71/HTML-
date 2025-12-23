<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Current Date & Time</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #4facfe, #00f2fe);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .clock-container {
            text-align: center;
            background: rgba(0, 0, 0, 0.25);
            padding: 30px 50px;
            border-radius: 12px;
        }

        .date {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        .time {
            font-size: 3rem;
            font-weight: bold;
        }
    </style>
</head>
<body>

<div class="clock-container">
    <div class="date" id="date"></div>
    <div class="time" id="time"></div>
</div>

<script>
    function updateDateTime() {
        const now = new Date();

        const options = {
            weekday: 'long',
            year: 'numeric',
            month: 'long',
            day: 'numeric'
        };

        const date = now.toLocaleDateString('en-US', options);
        const time = now.toLocaleTimeString('en-US');

        document.getElementById('date').textContent = date;
        document.getElementById('time').textContent = time;
    }

    // Update immediately and every second
    updateDateTime();
    setInterval(updateDateTime, 1000);
</script>

</body>
</html>

