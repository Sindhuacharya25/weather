<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NYC Weather</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        .weather-icon {
            font-size: 48px;
            margin-bottom: 16px;
        }
    </style>
</head>
<body class="h-screen bg-blue-100 flex justify-center items-center p-4">
    <div class="bg-white p-8 rounded-md shadow-md w-full max-w-sm md:p-12 lg:p-16 xl:p-20">
        <h1 class="text-2xl font-bold mb-4 text-center text-blue-500">NYC Weather</h1>
        <div id="weather" class="mb-4 p-4 text-center">
            <div id="temperature" class="text-4xl font-bold mb-4"></div>
            <div id="condition" class="text-xl font-medium mb-4"></div>
            <div id="humidity" class="text-lg font-light mb-2">Humidity: <span id="humidity-value"></span>%</div>
            <div id="wind" class="text-lg font-light mb-2">Wind: <span id="wind-value"></span> mph</div>
            <i id="weather-icon" class="weather-icon text-blue-500"></i>
        </div>
    </div>
    <p class="fixed bottom-0 left-0 right-0 text-center p-4 text-gray-600 md:p-6 lg:p-8 xl:p-10">
        Built on <a class="text-blue-600" href="https://cerebrascoder.com">Cerebras Coder</a>
    </p>

    <script>
        // Sample weather data
        const weatherData = {
            temperature: 75,
            condition: 'Sunny',
            humidity: 60,
            wind: 10,
            icon: 'sun'
        };

        document.getElementById('temperature').innerText = `${weatherData.temperature}°F`;
        document.getElementById('condition').innerText = weatherData.condition;
        document.getElementById('humidity-value').innerText = weatherData.humidity;
        document.getElementById('wind-value').innerText = weatherData.wind;

        // Map weather icon
        const weatherIcons = {
            'sun': '&#9728;',
            'cloud': '&#9728;',
            'rain': '&#9731;',
            'snow': '&#9732;'
        };

        document.getElementById('weather-icon').innerHTML = weatherIcons[weatherData.icon] || '';
    </script>
</body>
</html>
