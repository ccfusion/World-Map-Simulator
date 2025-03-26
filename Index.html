<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Population Growth Map</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
    <script src="https://d3js.org/d3.v6.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        #map {
            height: 100vh;
        }
        .control-panel {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.7);
            padding: 10px;
            border-radius: 8px;
        }
        button {
            padding: 10px;
            background-color: #008CBA;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #007B9A;
        }
    </style>
</head>
<body>
    <div id="map"></div>
    <div class="control-panel">
        <button id="startButton">Start / Restart</button>
        <div id="info">Click the button to start/restart</div>
    </div>

    <script>
        // Initialize the map
        const map = L.map('map').setView([51.505, -0.09], 2);

        // Set the map layer (OpenStreetMap)
        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(map);

        // Country data (population and location for Germany, France, and Canada)
        const countries = {
            "Germany": { lat: 51.1657, lon: 10.4515, population: 83000000 },
            "France": { lat: 46.6034, lon: 1.8883, population: 67000000 },
            "Canada": { lat: 56.1304, lon: -106.3468, population: 38000000 }
        };

        // Create markers for each country
        const markers = {};
        for (let country in countries) {
            const { lat, lon, population } = countries[country];
            markers[country] = L.marker([lat, lon]).addTo(map)
                .bindPopup(`<b>${country}</b><br>Population: ${population.toLocaleString()}`)
                .openPopup();
        }

        // Function to update population growth
        function simulatePopulationGrowth() {
            const growthRate = Math.random() * (5 - 1) + 1; // Random growth rate between 1 and 5 million
            const years = 10; // Simulate growth over 10 years
            const interval = 500; // Update every 500ms for smooth animation

            for (let country in countries) {
                let { population } = countries[country];
                const targetPopulation = population + growthRate * years;

                // Animate population growth
                let currentPopulation = population;
                let step = (targetPopulation - currentPopulation) / years;

                // Smooth transition over years
                (function update() {
                    if (currentPopulation < targetPopulation) {
                        currentPopulation += step;
                        countries[country].population = Math.round(currentPopulation);
                        markers[country].setPopupContent(`<b>${country}</b><br>Population: ${Math.round(currentPopulation).toLocaleString()}`);
                        setTimeout(update, interval);
                    }
                })();
            }
        }

        // Button click handler to start/restart
        document.getElementById('startButton').addEventListener('click', () => {
            simulatePopulationGrowth();
            document.getElementById('info').textContent = "Simulation in progress...";
        });
    </script>
</body>
</html>
