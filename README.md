# -SANDEEP-CAR-ZONE-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Online Car Booking</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: url('https://wallpapercave.com/wp/wp2026578.jpg') no-repeat center center fixed;
      background-size: cover;
      color: #00ffff;
      position: relative;
      overflow-x: hidden;
    }

    .floating-cars {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('https://i.imgur.com/v0J4IUZ.png') repeat;
      opacity: 0.05;
      animation: float 60s linear infinite;
      z-index: 0;
    }

    @keyframes float {
      from { background-position: 0 0; }
      to { background-position: 1000px 0; }
    }

    header, .booking-form, .contact-info, footer {
      position: relative;
      z-index: 1;
    }

    header {
      background-color: rgba(0, 0, 0, 0.8);
      text-align: center;
      padding: 1em;
      font-size: 1.5em;
      font-weight: bold;
      color: #ff00ff;
      border-bottom: 2px solid #00ffff;
    }

    .booking-form {
      background-color: rgba(0, 0, 0, 0.7);
      max-width: 500px;
      margin: 50px auto;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 15px #00ffff;
    }

    .booking-form input, .booking-form select, .booking-form button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: none;
      border-radius: 5px;
      font-size: 1em;
    }

    .booking-form input, .booking-form select {
      background: #222;
      color: #0ff;
    }

    .booking-form button {
      background: #ff00ff;
      color: white;
      cursor: pointer;
    }

    .contact-info {
      text-align: center;
      margin: 20px 0;
      color: #0ff;
    }

    .contact-info a {
      color: #ff00ff;
      text-decoration: none;
    }

    footer {
      text-align: center;
      padding: 1em;
      background-color: rgba(0, 0, 0, 0.8);
      color: #ff00ff;
      font-size: 1.2em;
      font-weight: bold;
      position: fixed;
      bottom: 0;
      width: 100%;
      border-top: 2px solid #00ffff;
    }
  </style>
</head>
<body>
  <div class="floating-cars"></div>

  <header>
    Warning: Price of CNG is Rs.13/km
  </header>

  <div class="booking-form">
    <h2>Book Your Ride</h2>
    <form id="bookingForm">
      <input type="text" id="name" placeholder="Your Name" required>
      <input type="tel" id="phone" placeholder="Phone Number" required>
      <input type="date" id="date" required>
      
      <select id="car_type" required>
        <option value="">Select Car Type</option>
        <option value="Swift">Swift</option>
        <option value="Scorpio">Scorpio</option>
        <option value="Ertiga">Ertiga</option>
      </select>

      <select id="fuel_type" required>
        <option value="">Select Fuel Type</option>
        <option value="CNG">CNG</option>
        <option value="Petrol">Petrol</option>
      </select>

      <button type="submit">Book Now</button>
    </form>
  </div>

  <div class="contact-info">
    WhatsApp: 9050017441<br>
    Instagram: <a href="https://www.instagram.com/sandeep4764kumar" target="_blank">@sandeep4764kumar</a>
  </div>

  <footer>
    Price of Petrol is Rs.15/km
  </footer>

  <script>
    document.getElementById('bookingForm').addEventListener('submit', function(e) {
      e.preventDefault();

      const name = document.getElementById('name').value;
      const phone = document.getElementById('phone').value;
      const date = document.getElementById('date').value;
      const carType = document.getElementById('car_type').value;
      const fuelType = document.getElementById('fuel_type').value;

      const message = `*New Booking Request*%0AName: ${name}%0APhone: ${phone}%0ADate: ${date}%0ACar Type: ${carType}%0AFuel Type: ${fuelType}`;
      const whatsappUrl = `https://wa.me/919050017441?text=${message}`;
      
      window.open(whatsappUrl, '_blank');
    });
  </script>
</body>
</html>
