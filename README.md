# Ex.05 Design a Website for Server Side Processing
## Date:

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Filament </title>
    <link rel="stylesheet" href="STYLE.CSS">
</head>
<body>
    <div class="container">
        <h1>LAMP FILAMENT POWER CALCULATOR</h1>
        <form id="power-form">
            <div class="input-group">
                <label for="intensity">Intensity (I in Amperes):</label>
                <input type="number" id="intensity" name="intensity" step="0.01" required>
            </div>
            <div class="input-group">
                <label for="resistance">Resistance (R in Ohms):</label>
                <input type="number" id="resistance" name="resistance" step="0.01" required>
            </div>
            <button type="submit">Calculate Power</button>
        </form>

        <div class="result" id="result"></div>
    </div>

    <script>
        document.getElementById('power-form').addEventListener('submit', function(event) {
            event.preventDefault();
            const intensity = parseFloat(document.getElementById('intensity').value);
            const resistance = parseFloat(document.getElementById('resistance').value);
            const power = Math.pow(intensity, 2) * resistance;

            document.getElementById('result').innerText = "Power: " + power.toFixed(2) + " Watts";
        });
    </script>
</body>
</html>
```
CSS
```
body {
    font-family: Arial, sans-serif;
    background-color: #23db19;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 400px;
    margin: 50px auto;
    padding: 20px;
    background-color: #d1c2c2cd;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
    color: #333;
}

.input-group {
    margin-bottom: 15px;
}

label {
    display: block;
    margin-bottom: 5px;
    color: #555;
}

input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

button {
    width: 100%;
    padding: 10px;
    background-color: #079ffd;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #218838;
}

.result {
    margin-top: 20px;
    padding: 10px;
    background-color: #e9ecef;
    border: 1px solid #ced4da;
    border-radius: 4px;
    text-align: center;
    font-size: 1.2em;
    color: #333;
}
```


## HOMEPAGE:
![image](https://github.com/user-attachments/assets/ba8d541a-6f00-46a2-8b53-c11a74e8010c)


## RESULT:
The program for performing server side processing is completed successfully.
