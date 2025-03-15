   
<head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Corinthia:wght@400;700&family=Ephesis&display=swap" rel="stylesheet">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chrono Resort</title>
    <link rel="stylesheet" href="CSS/ChronoResort Style VS.css">
</head>
<body>
</body>
    <header class="hero-section">
        <h1>Welcome to Chrono Resort, a trip through time</h1>
        <img src="images/ChronoResort 02.webp" alt="Ένα ταξίδι στο χρόνο" width="600">
        <p>Απολαύστε πολυτέλεια και χαλάρωση στις διακοπές σας</p>
        <a href="#booking" class="btn">Κάντε Κράτηση / Make a Reservation</a>
    </header>
    <section class="about">
        <h2>Σχετικά με Εμάς</h2>
        <p>Καλώς ήρθατε στο Chrono Resort, ένα ξενοδοχείο που συνδυάζει την ιστορία με τη φύση και τη τεχνολογία, δημιουργώντας μοναδικές εμπειρίες για τους επισκέπτες του. Το ξενοδοχείο μας είναι Family friendly. Είναι ένα μέρος μοναδικό στο οποίο θα απασχοληθείτε με δραστηριότητες βασισμένες πάνω στο θέμα της διαμονής σας. 
            Τα θέματα του ξενοδοχείου μας είναι: η Μεσαιωνική εποχή, το Πράσινο περιβάλλον, η Μοντέρνα εποχή και η Εξελιγμένη εποχή (όσον αφορά τη τεχνολογία). Ο πελάτης έχει τη δυνατότητα κατά τη κράτηση του, να επιλέξει ένα από αυτά τα θέματα. Παράλληλα, με την επιλογή ενός θέματος, ο πελάτης θα περάσει τη διαμονή του σε ένα δωμάτιο αντίστοιχο του θέματος. Με την επιλογή ενός θέματος, έρχονται και κάποιες δραστηριότητες που είναι αποκλειστικές μόνο για εκείνα τα θέματα.
            Στο Chrono Resort, κάθε στιγμή είναι ένα ταξίδι μέσα στον χρόνο και στη φύση, όπου οι επισκέπτες μπορούν να απολαύσουν τις διαφορετικές εποχές και περιβάλλοντα που προσφέρουμε. Καλώς ήρθατε στον κόσμο του Chrono Resort.
            </p>
    <p className="text-md font-semibold mb-4">Επικοινωνήστε μαζί μας:</p>
    <p className="text-md">Τηλέφωνο: +30 210 8202567</p>
    <p className="text-md mb-6">Email: info@chronoresort.com</p>
    </section>
    <section class="gallery">
        <h2>Gallery</h2>
        <img src="images/AD ERA ROOM 1.png" alt="Advanced Room 2" width="300">
        <img src="images/AD ERA ROOM 2.png" alt="Advanced Room 1" width="300">
        <img src="images/MOD ERA ROOM 1.png" alt="Modern Room 2" width="300">
        <img src="images/MOD ERA ROOM 2.png" alt="Modern Room 1" width="300">
        <img src="images/GE ROOM 1.png" alt="Green Enviroment Room 2" width="300">
        <img src="images/GE ROOM 2.png" alt="Green Enviroment Room 1" width="300">
        <img src="images/MED ERA ROOM 1.png" alt="Medieval Room 2" width="300">
        <img src="images/MED ERA ROOM 2.png" alt="Medieval Room 1" width="300">
        <img src="images/ChronoResort PL.webp" alt="Our Pool" width="300">
        <img src="images/ChronoResort RE.webp" alt="Our Restaurant" width="300">
        <img src="images/ChronoResort VW.webp" alt="The View" width="300">    
    <section class="rooms">
        <h2>Τα Δωμάτιά Μας</h2>
        <div class="room">
            <h3>Standard Family Room</h3>
            <p>€120 τη βραδιά/the night</p>
        </div>
        <div class="room">
            <h3>Superior Suite</h3>
            <p>€180 τη βραδιά/the night</p>
        </div>
	<div class="room">
            <h3>Deluxe Family Suite</h3>
            <p>€250 τη βραδιά/the night</p>
	</div>
	<div class="room">
            <h3>Premium Chrono Travel Suite</h3>
            <p>€400 τη βραδιά/the night</p>
    	</div>
    </section>
    <section id="booking" class="booking-form">
        <h2>Κράτηση/Reservation</h2>
        <form>
            <label for="name">Όνομα/Name:</label>
            <input type="text" id="name" name="name" required>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            <label for="date">Ημερομηνία Άφιξης/Arrival Date:</label>
            <input type="date" id="date" name="date" required>        
            <label for="date">Ημερομηνία Αναχώρισης/Departure Date:</label>
            <input type="date" id="date" name="date" required>
            <button type="submit">Υποβολή/Submit</button>
        </form>
    </section>
    <footer>
        <p>&copy; 2025 Chrono Resort. Thank you for choosing us! We wish you safe travels.</p>
    </footer>
