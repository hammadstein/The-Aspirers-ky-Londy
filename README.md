<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #e4e4e4;
            color: #000;
        }

        header {
            background-color: #075e54;
            color: #fff;
            text-align: center;
            padding: 1em 0;
            position: relative;
        }

        h1 {
            margin: 0;
        }

        #studentList {
            padding: 20px;
            margin-bottom: 20px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #333;
        }

        th {
            background-color: #128C7E;
            color: #fff;
        }

        tr:hover {
            background-color: #ddd;
        }

        #schoolButton {
            background-color: #075e54;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin: 20px auto; /* Center the button */
            display: block;
        }

        /* Popup Styling */
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.5s;
        }

        .overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }

        footer {
            background-color: #075e54;
            color: #fff;
            text-align: center;
            padding: 1em 0;
            margin-top: 20px;
        }

        footer p {
            margin: 5px 0;
        }
    </style>
    <title>Student Details</title>
</head>
<body>
    <header>
        <h1>Matrix School Of IT and Business</h1>
    </header>
    <section id="studentList">
        <table>
            <thead>
                <tr>
                    <th>Roll Number</th>
                    <th>Name</th>
                    <th>Phone Number</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>01</td>
                    <td>Riyasat Ali</td>
                    <td>03443853735</td>
                </tr>
                <tr>
                    <td>02</td>
                    <td>Muhammad Murtaza</td>
                    <td>03150727452</td>
                </tr>
                <tr>
                    <td>03</td>
                    <td>Zeeshan Ali</td>
                    <td>03442472887</td>
                </tr>
                <tr>
                    <td>04</td>
                    <td>Ali Hassan</td>
                    <td>03467248735</td>
                </tr>
                <tr>
                    <td>05</td>
                    <td>Muhammad Ramzan</td>
                    <td>03074207836</td>
                </tr>
                <tr>
                    <td>06</td>
                    <td>Waqas Shair</td>
                    <td>03434797140</td>
                </tr>
                <tr>
                    <td>07</td>
                    <td>Usman Zafar</td>
                    <td>03423857512</td>
                </tr>
                <tr>
                    <td>08</td>
                    <td>Muhammad Shehryar</td>
                    <td>03415231500</td>
                </tr>
            </tbody>
        </table>
    </section>
    <button id="schoolButton" onclick="showPopup()">School</button>

    <!-- Popup Content -->
    <div id="schoolPopup" class="popup">
        <h2>School Information</h2>
        <p><strong>School Name:</strong> Matrix School Of IT and Business</p>
        <p><strong>City:</strong> Mandi Shah Jewana, Jhang</p>
        <button onclick="hidePopup()">Close</button>
    </div>

    <div id="overlay" class="overlay" onclick="hidePopup()"></div>

    <!-- JavaScript -->
    <script>
        function showPopup() {
            var popup = document.getElementById('schoolPopup');
            var overlay = document.getElementById('overlay');

            popup.style.display = 'block';
            overlay.style.display = 'block';

            // Triggering reflow to restart the animation
            void popup.offsetWidth;

            popup.style.opacity = '1';
        }

        function hidePopup() {
            var popup = document.getElementById('schoolPopup');
            var overlay = document.getElementById('overlay');

            popup.style.opacity = '0';

            setTimeout(function() {
                popup.style.display = 'none';
                overlay.style.display = 'none';
            }, 500); // 0.5s, matching the transition duration
        }
    </script>
    <footer>
        <p>&copy; 2023 Matrix School Of IT and Business. All rights reserved.</p>
    </footer>
</body>
</html>
