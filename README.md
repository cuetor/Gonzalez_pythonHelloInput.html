<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PyScript Example</title>
    <link rel="stylesheet" href="https://pyscript.net/latest/pyscript.css">
    <script defer src="https://pyscript.net/latest/pyscript.js"></script>
</head>
<body>
    <h1>PyScript Input and Output Example</h1>
    <label for="operandOne">Enter a number:</label>
    <input type="text" id="operandOne" />
    <button id="submitBtn">Submit</button>
    
    <div id="total"></div>

    <py-script>
        def process_input(*args):
            input_box = Element("operandOne")
            operandOne = float(input_box.value)
            result = Element("total")
            result.write("Hello! The input says: " + str(operandOne))

        # Attach the function to the button click event
        submit_button = Element("submitBtn")
        submit_button.element.addEventListener("click", process_input)
    </py-script>
</body>
</html>
