<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>24-Hour Watch Face with Zones</title>
  <style>
    body {
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: black;
    }
    canvas {
      border: 2px solid white;
    }
    #digital-time {
      position: absolute;
      color: white;
      font-size: 24px;
      font-family: Arial, sans-serif;
      font-weight: bold;
      bottom: 20px;
    }
  </style>
</head>
<body>

<canvas id="clock" width="400" height="400"></canvas>
<div id="digital-time"></div>

<script>
  const canvas = document.getElementById("clock");
  const ctx = canvas.getContext("2d");

  const centerX = canvas.width / 2;
  const centerY = canvas.height / 2;
  const radius = 150;
  const innerRadius = 50; // Radius for the minute circle

  // Draw the clock face with zones, numbers, hands, and emojis
  function drawFace() {
    // Clear the canvas
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    // Draw zones (rotated by 180 degrees)
    drawZone(8, 17, '#83D8E5'); // Work zone (8 AM to 5 PM)
    drawZone(17, 22, '#A9A6F3'); // Hobby zone (5 PM to 10 PM)
    drawZone(22, 24, '#253363'); // Sleep zone (10 PM to 12 AM)
    drawZone(0, 5, '#253363');  // Sleep zone (12 AM to 5 AM)
    drawZone(5, 8, '#A9A6F3');  // Hobby zone (5 AM to 8 AM)

    // Draw hour numbers (upright, but the clock is rotated)
    for (let i = 0; i < 24; i++) {
      const angle = ((2 * Math.PI) / 24) * i - Math.PI / 2 + Math.PI; // Rotate the clock by 180 degrees
      const numberX = centerX + (radius - 20) * Math.cos(angle);
      const numberY = centerY + (radius - 20) * Math.sin(angle);
      ctx.fillStyle = 'white';
      ctx.font = 'bold 12px Arial';
      ctx.textAlign = 'center';
      ctx.textBaseline = 'middle';
      ctx.fillText(i, numberX, numberY);
    }

    // Draw inner circle
    ctx.beginPath();
    ctx.arc(centerX, centerY, innerRadius, 0, 2 * Math.PI);
    ctx.strokeStyle = 'white';
    ctx.lineWidth = 2;
    ctx.stroke();

    // Mark the minute positions inside the inner circle
    [30, 45, 0, 15].forEach((minute, i) => {
      const angle = ((2 * Math.PI) / 4) * i - Math.PI / 2 + Math.PI; // Rotate the clock by 180 degrees
      const markX = centerX + (innerRadius - 12) * Math.cos(angle);
      const markY = centerY + (innerRadius - 12) * Math.sin(angle);
      ctx.fillText(minute, markX, markY);
    });

    // Draw sun emoji
    ctx.font = '30px Arial';
    ctx.fillText('☀️', centerX, centerY - 90);

    // Draw moon emoji
    ctx.fillText(getMoonPhase(), centerX, centerY + 80);
  }

  // Draw a time zone sector on the clock face
  function drawZone(startHour, endHour, color) {
    // Calculate angles (rotated by 180 degrees)
    const startAngle = ((2 * Math.PI) / 24) * startHour - Math.PI / 2 + Math.PI;
    const endAngle = ((2 * Math.PI) / 24) * endHour - Math.PI / 2 + Math.PI;

    ctx.beginPath();
    ctx.moveTo(centerX, centerY);
    ctx.arc(centerX, centerY, radius, startAngle, endAngle, false);
    ctx.closePath();
    ctx.fillStyle = color;
    ctx.fill();
  }

  // Get the moon phase based on the current date
  function getMoonPhase() {
    const newMoonDate = new Date(2024, 0, 11); // Known new moon date
    const daysSinceNewMoon = (new Date() - newMoonDate) / (1000 * 60 * 60 * 24);
    const phase = daysSinceNewMoon % 29.53;

    // Calculate the moon phase based on the position in the lunar cycle
    if (phase < 1.84566) return "🌑"; // New Moon
    if (phase < 5.53699) return "🌒"; // Waxing Crescent
    if (phase < 9.22831) return "🌓"; // First Quarter
    if (phase < 12.91963) return "🌔"; // Waxing Gibbous
    if (phase < 16.61096) return "🌕"; // Full Moon
    if (phase < 20.30228) return "🌖"; // Waning Gibbous
    if (phase < 24.99361) return "🌗"; // Last Quarter
    return "🌘"; // Waning Crescent
  }

  // Draw clock hands based on the current time
  function drawHands() {
    const now = new Date();
    const hours = now.getHours();
    const minutes = now.getMinutes();
    const seconds = now.getSeconds();
    const fractionalHour = hours + minutes / 60;

    // Hour hand (rotated by 180 degrees)
    const hourAngle = ((2 * Math.PI) / 24) * fractionalHour - Math.PI / 2 + Math.PI;
    drawLine(centerX, centerY, hourAngle, radius - 30, 'white', 4);

    // Minute hand (rotate by ? degrees clockwise)
    const minuteAngle = ((2 * Math.PI) / 60) * minutes - Math.PI / 2 + Math.PI + Math.PI ; // ? degrees
    drawLine(centerX, centerY, minuteAngle, radius - 100, 'white', 2);

    // Update digital time
    document.getElementById('digital-time').innerText =
      `${String(hours).padStart(2, '0')} : ${String(minutes).padStart(2, '0')} : ${String(seconds).padStart(2, '0')}`;
  }

  // Draw a line representing the clock hand
  function drawLine(x, y, angle, length, color, width) {
    ctx.beginPath();
    ctx.moveTo(x, y);
    ctx.lineTo(x + length * Math.cos(angle), y + length * Math.sin(angle));
    ctx.strokeStyle = color;
    ctx.lineWidth = width;
    ctx.stroke();
  }

  // Update the clock every second
  function updateClock() {
    drawFace();
    drawHands();
    setTimeout(updateClock, 1000);
  }

  // Initialize the clock
  updateClock();
</script>

</body>
</html>
