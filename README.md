# Calculator
Calculator With Js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="calculator.css">
    <style>
    *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: consolas;
}
body{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #333;
}
.container{
    position: relative;
    min-width: 300px;
    min-height: 400px;
    background: #333;
padding: 40px 30px 30px;
border-radius: 20px ;
box-shadow: 25px 25px 30px rgba(0,0,0,0.25), 
10px 10px 70px rgba(0,0,0,0.25),
inset -5px -5px 15px rgba(0,0,0,0.5),
inset -5px -5px 15px rgba(0,0,0,0.5);
}
.calculator{
    display: grid;
    position: relative;
}
.calculator .value{
    position: relative;
    grid-column: span 4;
    height: 100px;
    width: calc(100% -23px);
    left:10px;
border: none;
outline: none;
background: #a7af7c;
margin-bottom: 10px;
border-radius: 10px;
box-shadow:0 0 0 2px rgba(0,0,0,0.75);
text-align: right;
padding: 10px;
font-size: 2em;
 }

.calculator span{
    color:#fff;
    display: grid;
    width:80px;
    place-items: center;
    margin: 8px;
    height:80px;
    background: linear-gradient(180deg,#2f2f2f,#3f3f3f);
    box-shadow: inset -8px 0px 8px rgba(0,0,0,0.15),
    inset 0px -8px 8px rgba(0,0,0,0.25),
    0 0 0 2px rgba(0,0,0,0.75),
    10px 20px 25px rgba(0,0,0,0.4);
    position: relative;
user-select: none;
cursor: pointer;
font-weight: 400;
border-radius: 10px;
}
.calculator span i
{
    position: relative;
    font-style: normal;
    font-size: 1.5em;
    text-transform: uppercase;
}
.calculator span::before{
    content:''; 
    top:3px;
    left: 4px;
    border-radius: 10px;
box-shadow: -5px -5px 15px rgba(0,0,0,0.1),
10px 5px 10px rgba(0,0,0,0.15);
border-left: 1px solid #0004;
border-bottom: 1px solid #0004;
border-top: 1px solid #0009;
    bottom:14px;
    right: 12px;
    position: absolute;
    background: linear-gradient(90deg,#2d2d2d,#4d4d4d);

}
.calculator span:active{
   filter: brightness(1.5); 
}
.calculator .clear{
grid-column: span 2;
width: 170px;
background: #f00;
}
.calculator .clear::before{
  background: linear-gradient(90deg,#d20000,#ffffff5c);  
border-left: 1px solid #fff4;
border-bottom: 1px solid #fff4;
border-top: 1px solid #fff4;
}
.calculator .plus{
    grid-row:span 2;
    height: 180px;
}
.calculator .equal{
background: #2196f3;
}
.calculator .equal::before{
    background: linear-gradient(90deg,#1479c9,#ffffff5c);  
    border-left: 1px solid #fff4;
    border-bottom: 1px solid #fff4;
    border-top: 1px solid #fff4;
}
    </style>
</head>
<body>
 <div class="container">
     <form class="calculator" name="calc"> 
         <input type="text" class="value" readonly name="txt">
   <span class="num clear" onclick="calc.txt.value=''"><i>C</i></span>
   <span class="num" onclick="calc.txt.value+='/'"><i>/</i></span>
   <span class="num" onclick="calc.txt.value+='*'"><i>*</i></span>
   <span class="num" onclick="calc.txt.value+='7'"><i>7</i></span>
   <span class="num" onclick="calc.txt.value+='8'"><i>8</i></span>
   <span class="num" onclick="calc.txt.value+='9'"><i>9</i></span>
   <span class="num" onclick="calc.txt.value+='-'"><i>-</i></span>
   <span class="num" onclick="calc.txt.value+='4'"><i>4</i></span>
   <span class="num" onclick="calc.txt.value+='5'"><i>5</i></span>
   <span class="num" onclick="calc.txt.value+='6'"><i>6</i></span>
   <span class="num plus" onclick="calc.txt.value+='+'"><i>+ </i></span>
   <span class="num" onclick="calc.txt.value+='1'"><i>1</i></span>
   <span class="num" onclick="calc.txt.value+='2'"><i>2</i></span>   
   <span class="num" onclick="calc.txt.value+='3'"><i>3</i></span>
   <span class="num" onclick="calc.txt.value+='0'"><i>0</i></span>
   <span class="num" onclick="calc.txt.value+='00'"><i>00</i></span>
   <span class="num" onclick="calc.txt.value+='.'"><i>.</i></span>
   <span class="num equal" onclick="document.calc.txt.value=eval(calc.txt.value)"><i>=</i></span>

</form>
 </div>
    <script src="calculator.js"></script>
</body>
</html>
