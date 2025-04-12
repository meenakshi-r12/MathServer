# Ex.05 Design a Website for Server Side Processing
## Date:12.4.25

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
```
<html>
<head>
    <title>Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: lightgrey;
            margin: 20px;
            padding: 20px;
            text-align: center;
        }

        h1 {
            color: darkblue;
        }

        form {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px grey;
            display: inline-block;
            margin: auto;
        }

        label {
            font-weight: bold;
            color: black;
        }

        input[type="number"] {
            padding: 5px;
            margin: 10px 0;
            border: 1px solid black;
            border-radius: 4px;
        }

        button {
            background-color: darkblue;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: navy;
        }
    </style>
</head>
<body>
    <h1>Power Calculator</h1>
    <form method="POST">
        {% csrf_token %}
        <label for="I">Enter Current (I in Amps):</label>
        <input type="number" name="intensity" id="I" value="{{ I }}" required>
        <br><br>
        <label for="R">Enter Resistance (R in Ohms):</label>
        <input type="number" name="resistance" id="R" value="{{ R }}" required>
        <br><br>
        <button type="submit">Calculate Power</button>
        <br><br>
        <label for="power">Calculated Power (Watts):</label>
        <input type="number" name="power" id="power" value="{{ power }}" readonly>
    </form>
</body>
</html>

```
## SERVER SIDE PROCESSING:

![Screenshot (12)](https://github.com/user-attachments/assets/feda1947-6476-4019-a4fa-fbec359cef8b)

## HOMEPAGE:

![Screenshot (13)](https://github.com/user-attachments/assets/19239538-aeab-488e-a63f-42d8b36d1624)

## RESULT:
The program for performing server side processing is completed successfully.
