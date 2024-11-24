# ArminAlba.github.io
<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Colegul 1</title>
    <link rel="stylesheet" href="style.css"> 
    <script type="text/javascript">
        function switchProfile() {
            // Modifică numele și poziția
            document.getElementById("nameTitle").innerHTML = "Software Engineer la Google";
            document.getElementById("specialization").innerHTML = "Inginer Software";
            
            // Modifică hobby-urile și experiențele
            document.getElementById("hobbies").innerHTML = "Inteligență artificială, robotică, dezvoltare de software.";

            // Schimbă imaginea de profil
            document.getElementById("profileImage").src = "pisici.jpeg";
            document.getElementById("profileImage").style.opacity = "0.7"; // Schimbă opacitatea imaginii
            document.getElementById("profileImage").style.border = "5px solid #4CAF50"; // Schimbă marginea

            // Modifică stilul paginii
            //document.body.style.backgroundColor = "#333"; // Schimbă fundalul paginii
            //document.body.style.color = "#fff"; // Schimbă culoarea textului

            //document.querySelector(".profil").style.backgroundColor = "#444"; // Schimbă fundalul secțiunii
            document.querySelector(".profil").style.boxShadow = "0 8px 16px rgba(0, 0, 0, 0.3)"; // Modifică umbra

            // Schimbă secțiunea de educație (experiențe viitoare)
            document.getElementById("education").innerHTML = "<strong>Realizări viitoare:</strong> Planific să dezvolt aplicații mobile inovative și să particip la proiecte open-source.";
        }

        function calculateAge() {
            // Obține anul nașterii
            var birthYear = 2003; // Anul nașterii (exemplu)
            var currentYear = new Date().getFullYear(); // Anul curent
            var age = currentYear - birthYear; // Calculul vârstei

            // Schimbă conținutul la trecerea cu mouse-ul
            document.getElementById("birthYear").innerHTML = age + " ani";
        }

        function revertAge() {
            // Restabilește anul nașterii atunci când mouse-ul părăsește elementul
            document.getElementById("birthYear").innerHTML = "2003";
        }
    </script>
</head>
<body>
    <section class="profil">
        <h2>Profil Colegul 1</h2>
        <img id="profileImage" src="coleg1.jpg" alt="Colegul 1" class="imagine-profil">
        <p><strong>Nume:</strong><span id="nameTitle">Ion Popescu</span></p>
        <p><strong>Vârstă:</strong> 21 ani</p>
        <p><strong>Specializare:</strong><span id="specialization"> Informatica</span></p>
        <p><strong>Hobby-uri:</strong><span id="hobbies"> Programare, Fotografie, Drumeții</span></p>
        
        <!-- Secțiune de educație / realizări -->
        <p id="education"><strong>Educație:</strong> Student la Facultatea de Informatică.</p>

        <!-- Anul nașterii, cu calcularea vârstei la trecerea cu mouse-ul -->
        <p><strong>Anul nașterii:</strong> <span id="birthYear" onmouseover="calculateAge()" onmouseout="revertAge()">2003</span></p>

        <button id="switchButton" onclick="switchProfile()">Alta Viata</button>
    </section>
</body>
</html>
