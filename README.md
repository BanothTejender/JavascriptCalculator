# JavascriptCalculator
<!DOCTYPE html>
<html lang="en">
<head>
<title>JavaScript Calculator</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Ubuntu&display=swap" rel="stylesheet">
<style>
body {
  background-image: url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ77VVcSZzMltTG2WU3CSmfBuk4K_MgnpBRBw&usqp=CAU);
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  font-family: 'Ubuntu', sans-serif;
}

h1 {
  text-align: center;
  padding: 23px;
  color: white;
  border-radius: 16px;
}

#clear {
  width: 280px;
  padding: 10px;
  background-color: rgb(245, 100, 100);
  color: white;
  border: none;
  border-radius: 16px;
  font-size: 16px;
  margin-top: 10px;
  cursor: pointer;
}

#clear:hover {
  background-color: rgb(238, 30, 30);
  transition: background-color 0.3s ease-in-out;
}

.formstyle {
  width: 300px;
  height: 500px;
  margin: auto;
  padding: 50px;
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.6);
  backdrop-filter: blur(8px);
  background-color: rgba(255, 255, 255, 0.2);
}

input[type="text"] {
  width: 100%;
  background-color: rgb(67, 82, 167);
  color: white;
  padding: 15px;
  margin: 10px 0;
  border: 2px solid rgba(255, 255, 255, 0.3);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.6);
  font-size: 16px;
}

input[type="button"] {
  width: 60px;
  height: 60px;
  background-color: rgb(176, 160, 247);
  color: black;
  font-size: 20px;
  margin: 5px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

input[type="button"]:hover {
  background-color: rgb(150, 130, 230);
  transition: background-color 0.3s ease-in-out;
}

#calc-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

</style>
</head>
<body>
<h1>Simple Calculator Program in JavaScript</h1>
<div class="formstyle">
  <form name="form1">
    <input id="calc" type="text" name="answer">
    
    <div id="calc-container">
      <input type="button" value="1" onclick="form1.answer.value += '1'">
      <input type="button" value="2" onclick="form1.answer.value += '2'">
      <input type="button" value="3" onclick="form1.answer.value += '3'">
      <input type="button" value="+" onclick="form1.answer.value += '+'">
      
      <input type="button" value="4" onclick="form1.answer.value += '4'">
      <input type="button" value="5" onclick="form1.answer.value += '5'">
      <input type="button" value="6" onclick="form1.answer.value += '6'">
      <input type="button" value="-" onclick="form1.answer.value += '-'">
      
      <input type="button" value="7" onclick="form1.answer.value += '7'">
      <input type="button" value="8" onclick="form1.answer.value += '8'">
      <input type="button" value="9" onclick="form1.answer.value += '9'">
      <input type="button" value="*" onclick="form1.answer.value += '*'">
      
      <input type="button" value="/" onclick="form1.answer.value += '/'">
      <input type="button" value="0" onclick="form1.answer.value += '0'">
      <input type="button" value="." onclick="form1.answer.value += '.'">
      
      <input type="button" value="log(" onclick="form1.answer.value += 'Math.log('">
      <input type="button" value="exp(" onclick="form1.answer.value += 'Math.exp('">
      <input type="button" value="sin(" onclick="form1.answer.value += 'Math.sin('">
      <input type="button" value="cos(" onclick="form1.answer.value += 'Math.cos('">
      <input type="button" value="tan(" onclick="form1.answer.value += 'Math.tan('">
      
      <input type="button" value="(" onclick="form1.answer.value += '('">
      <input type="button" value=")" onclick="form1.answer.value += ')'">
      <input type="button" value="=" onclick="evaluateExpression()">
    </div>
    
    <br>
    <input type="button" value="Clear All" onclick="form1.answer.value = ''" id="clear">
  </form>
</div>
<script>
function evaluateExpression() {
  const expression = form1.answer.value;
  let result;

  try {
    result = eval(expression);
    form1.answer.value = result;
  } catch (error) {
    form1.answer.value = 'Error';
  }
}
</script>
</body>
</html>
