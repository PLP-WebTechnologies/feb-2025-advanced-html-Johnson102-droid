(Index.html)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!--External CSS: use ONLY the file name if it's in the same folder -->
    <link rel="stylesheet" href="style.css">

    <!-- Internal CSS -->
    <style>
        p {
            color: rgb(71, 60, 67);
            font-size: 20px;
            text-align: center;
        }
    </style>

    <title>Intro to CSS</title>
</head>
<body>

    <!-- Inline CSS -->
    <h1 style="color: rgb(102, 70, 125); font-size: 50px;">Cascading Stylesheets</h1>

    <p>This is a paragraph styled with internal CSS.</p>

    <a id="google" href="https://www.google.com">Google</a>

    <footer class="home-footer">
        &copy; 2025
    </footer>

</body>
</html>

(Style.css)
#google {
    color: rgb(50, 181, 14);
    text-decoration: none;
    font-weight: bold;
}

.home-footer {
    color: rgb(226, 147, 43);
    font-weight: bold;
}


