<!--This is an age calculator, In order to use it, you have to run it first and then insert your age-->

# age_calculator

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="This is description.">
    <meta name="keywords" content="html , html tutorials , web development">
    <meta name="robots" content="INDEX ,FOLLOW ">
    <title>Age Calculator</title>
</head>
<body>
    
    <span style="border: 2px solid blue;"><b>Calculate your age by your birthdate</b></span>
    <br>
    <br>

    <form action="find" method = "post">

        {% csrf_token %}

        <div>
            <label for="date">Enter your birthday here : </label>
            <input type="date" name="date" id="date" placeholder="date">
        </div>

        <div>
            <input type="Submit">
        </div>

        <div>

            {% for message in messages %}
                <h3 style="border: 2px solid red;"> {{message}} </h3>
            {% endfor %}
    
        </div>

    </form>

</body>
</html>
