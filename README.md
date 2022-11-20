<!DOCTYPE html>
<html>
<head>
<title>Matchmaker</title>
</head>
<body>
<h1>Matchmaker</h1>
<p>Finding you true love!</p>

<label>
    Nature walks are the best.
</label>
<br>

<select id = "q1">
    <option value="5">Strongly Agree</option>
    <option value="4">Agree</option>
    <option value="3">Indifferent</option>
    <option value="2">Disagree</option>
    <option value="1">Strongly Disagree</option>
</select>

<br>
<br>

<label>
    Dogs are a great house pet.
</label>
<br>

<select id = "q2">
    <option value="5">Strongly Agree</option>
    <option value="4">Agree</option>
    <option value="3">Indifferent</option>
    <option value="2">Disagree</option>
    <option value="1">Strongly Disagree</option>
</select>

<br>
<br>

<label> 
    Chicago is a great city to live in.
</label>
<br>

<select id = "q3">
    <option value="5">Strongly Agree</option>
    <option value="4">Agree</option>
    <option value="3">Indifferent</option>
    <option value="2">Disagree</option>
    <option value="1">Strongly Disagree</option>
</select>

<br>
<br>

<label>
    Roses are a great gift to give.
</label>
<br>

<select id = "q4">
    <option value="5"> Strongly Agree</option>
    <option value="4">Agree</option>
    <option value="3">Indifferent</option>
    <option value="2">Disagree</option>
    <option value="1">Strongly Disagree</option>
</select>
<br><br>

<label>
    Football is a great sport to watch on Sundays.
</label>
<br>

<select id = "q5">
    <option value="5"> Strongly Agree</option>
    <option value="4">Agree</option>
    <option value="3">Indifferent</option>
    <option value="2">Disagree</option>
    <option value="1">Strongly Disagree</option>
</select>

<br><br>

<button onclick="calculateCompatbility()">
    Calculate love
</button>


<br><br>

<p id="score">
    score here
</p>

<br><br>

<script>
    console.log("Starting")

    function calculateLove() {
        const preferedAnswer = [5, 5, 1, 3, 5]
        console.log("calculating love")
        const userAnswers = []
        userAnswer.push(document.getElementById("q1").selectedOptions[0].value)
        userAnswer.push(document.getElementById("q2").selectedOptions[0].value)
        userAnswer.push(document.getElementById("q3").selectedOptions[0].value)
        userAnswer.push(document.getElementById("q4").selectedOptions[0].value)
        userAnswer.push(document.getElementById("q5").selectedOptions[0].value)

        console.log(compatibilityValue3)
        
        let totalCompatibility = 0

        for (let i = 0; i <userAnswers.length; i++){
            const userAnswersInt = parseInt(userAnswers[i])
            let question1Compatibility = 5 - Math.abs(userAnswersInt - preferedAnswer[i])
            totalCompatibility += question1Compatibility
        }
        document.getElementById("score").innerHTML = "Your compatibility is: " + totalCompatibility
    }
</script>



</body>
</html>
