/* Βασικά Στυλ */
body {
    background: linear-gradient(to right, #266052dc, #b2a26c); /* Αλλαγή από το πορτοκαλί στο ροδακινί */
  }
  h1 {
    font-family: 'Corinthia', cursive; /* Μια καλλιγραφική γραμματοσειρά */
    font-size: 80px; /* Μέγεθος γραμματοσειράς */
    color: #ffffff; /* Χρώμα κειμένου */
    text-shadow: 8px 8px 6px #000000; /* Σκιά κειμένου για πρόσθετη αισθητική */
    text-align: center; /* Ευθυγράμμιση του τίτλου στο κέντρο */
  }
body {
    font-family: 'Times New Roman', sans-serif;
    margin: 10;
    padding: 0;
    line-height: 1.6;
    color: #000000;
}

/* Τμήμα Υποδοχής */
.hero-section {
    background: url('ChronoResort 02.jpg') no-repeat center center/cover;
    color:rgba(0, 0, 0, 0.901);
    text-align: center;
    padding: 100px 20px;
}

.hero-section .btn {
    display: inline-block;
    margin-top: 20px;
    padding: 10px 30px;
    background: #2b2a2a;
    color:#f0d85dc5;
    text-decoration: none;
    border-radius: 6px;
}

/* Ενότητα Δωματίων */
.rooms {
    display: flex;
    justify-content: space-around;
    margin: 20px;
}

.room {
    border: 3px solid #000000cf;
    padding: 20px;
    text-align: center;
    border-radius: 20px;
}

/* Φόρμα Κράτησης */
.booking-form {
    padding: 20px;
    background: #ffe89ccc;
}

.booking-form form {
    display: flex;
    flex-direction: column;
}

.booking-form label {
    margin: 10px 0 5px;
}

.booking-form input, .booking-form button {
    padding: 10px;
    margin-bottom: 10px;
}

footer {
    text-align: center;
    padding: 10px;
    background: #000000;
    color: #c7b661;
}
