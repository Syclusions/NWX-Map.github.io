<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Map with Custom Cursor</title>
    <style>
        /* Change the cursor to a pointer when hovering over clickable areas */
        area {
            cursor: pointer; /* Hand icon for clickable areas */
        }

        /* Optionally, change the cursor for other parts of the image */
        img {
            cursor: crosshair; /* Crosshair cursor for the whole image */
        }
    </style>
</head>
<body>
    <div style="display: grid; place-items: center; height: 100vh;">
        <img src="https://raw.githubusercontent.com/Syclusions/NWX-map/refs/heads/main/Map.png" 
             width="900" height="900" usemap="#image-map" alt="Map">
        
        <map name="image-map">
            <!-- Define clickable areas with a custom cursor -->
            <area shape="rect" coords="760,580,780,600" alt="Area 1" onclick="handleAreaClick('riznee')">
            <area shape="rect" coords="560,580,580,600" alt="Area 2" onclick="handleAreaClick('hymar')">
        </map>
    </div>

    <script>
        // Global variable to store the data
        let data;

        // Function to handle the area click
        function handleAreaClick(areaName) {
            // Store the clicked area name in the global data variable
            data = areaName;

            // Display the area name in the console
            alert(`You clicked on: ${data}`);
        }
    </script>
</body>
</html>



