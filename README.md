## ODD23-24-WT-JavaScript
NAME : RENUSRI NARAHARASHETTY

REGISTER NUMBER : 23009126

DEPARTMENT : ARTIFICIAL INTELLIGENCE AND MACHINE LEARNING

# EXP 9(a)
## AIM :
Create a form with java script code to calculate electricity bill.
## PROCEDURE :
# STEP 1:
Create a HTML structure and insert a 'script' tag in the 'head' section for JavaScript.
# STEP 2:
Inside , create a form with fields for previous and current readings. Add a "Generate Bill" button.
# STEP 3:
Connect the "Generate Bill" button to a JavaScript function called calc() using onclick.
# STEP 4:
Write the calc() function to compute the bill based on readings.
# STEP 5:
Run the code to perform calculations and display the output.

## PROGRAM:
```
<html>
<head>
<script type="text/javascript">
function calc()
{
    var prev,curr,units,amt;
    prev=Number(document.getElementById("t1").value);
    curr=Number(document.getElementById("t2").value);
    units=curr-prev;
    if(units<=100)
	    amt=100;
    else if(units>100&&units<=300)
	    amt=100+(units-100)*3;
    else
	    amt=100+600+(units-300)*5;
    document.getElementById("t3").value=amt;
}
</script>
</head>
<body>
    <h2>Electricity Bill</h2>
    <form>
        Enter Previous Reading 
        <input type="text" id="t1">Enter Current Reading
        <input type="text" id="t2">
        <input type="button"  onclick="calc()" value="Generate Bill">
        <input type="text" id="t3">
    </form>
</body>
</html>
```

## OUTPUT :
![a](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/d5aba0fe-a056-430d-8a1a-66c2ea4eef47)




## EXP 9(b)
## AIM :
To develop a JavaScript program to compute the factorial of a given number without recursion.

## PROCEDURE :
# STEP 1:
Create a basic 'html' structure. Inside the 'head', add a 'script' tag to include JavaScript.

## STEP 2 :
In the 'body', create a 'form' for user interaction. Include an input field where users can enter a number they want to find the factorial of.

## STEP 3 :
Define a JavaScript function called show(). Inside this function. Initialize a variable fact to 1 to store the factorial result. Retrieve the number entered by the user using getElementById. Use a loop to calculate the factorial of the entered number. Update the result field with the computed factorial value.

## STEP 4 :
Run the code to calculate the factorial of a given number and display the output.

## PROGRAM :
```
<html>
    <head>
        <script type="text/javascript">
        function show()
        {
            var i, n, fact;
            fact=1;
            n=Number(document.getElementById("num").value);
            for(i=1; i<=n; i++)  
            {
                fact= fact*i;
            }  
            document.getElementById("answer").value= fact;
            }
        </script>
    </head>
    <body>
        <form>
            Enter Number: <input type="text" id="num">
            <button onclick="show()">Factorial</button>
            <input type="text" id="answer">
        </form>
    </body>
</html>
```

## OUTPUT :
![b](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/a6c66b21-436b-43c2-9f3b-a74ea3f9f6de)


## EXP 9(c)
## AIM :
To construct a JavaScript code to generate ‘N’ prime numbers.

## PROCEDURE :
## STEP 1 :
Begin with the basic 'html' structure. In the 'head', embed a 'script' tag to house the JavaScript code.

## STEP 2 :
Inside the 'body', create a 'form' to capture user inputs. Add two input fields (input type="text") for users to enter a range of numbers: a starting number (n1) and an ending number (n2). Insert a button labeled "Generate" that, when clicked, triggers the JavaScript function to find prime numbers within the range.

## STEP 3 :
Define a JavaScript function named show(). Inside this function Retrieve the lower (n1) and upper (n2) limits entered by the user using getElementById. Implement nested loops to iterate through numbers between low and high. Within the loops, for each number: Check if it's divisible by any number between 2 and itself (j).

## STEP 4 :
Run the java code to print the prime numbers N.

## PROGRAM :
```
<html>
    <head>
        <script type="text/javascript">
        function show()
        {
            var low=Number(document.getElementById("n1").value);
            var high=Number(document.getElementById("n2").value);
            var i,j;
            for(i=low;i<=high;i++) 
            {
                var flag=0;
                for(j=2;j<i;j++) 
                {
                    if(i%j==0) 
                    {
                        flag=1;
                        break;
                    }
                }
                if(flag==0&&i>1) 
                    alert(i);
            }
        }
        </script>
    </head>
    <body>
        <form>
            Enter number : 
            <input type="text" id="n1">
            <input type="text" id="n2">
            <input type="button" onclick="show()" value="Generate">
        </form>
    </body>
</html>
```

## OUTPUT :
![c1](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/fbba00d3-72da-4b8b-b0bf-ac4d3ec3dca0)

![c2](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/f6046767-7b73-4d53-a103-c70fb76862ec)



## EXP 9(d)
## AIM :
To construct a JavaScript program to implement a simple calculator.

## PROCEDURE :
## STEP 1 :
Start with the basic 'html' structure. In the 'head', embed a 'script' tag to contain the JavaScript functions.

## STEP 2 :
Within the 'body', create a 'form' element for user interactions. Add multiple buttons, each representing a specific operation (e.g., Add, Subtract, Multiply, etc.). Include two input fields (input type="text") for users to input two numbers (n1 and n2). Provide an input field to display the result (n3).

## STEP 3 :
Define individual JavaScript functions (f1() to f9()) for each operation:

Addition (f1()): Add numbers a and b, then display the result in n3. Subtraction (f2()): Subtract b from a, then display the result. Multiplication (f3()): Multiply a and b, then display the result. Division (f4()): Divide a by b, then display the result. Sine (f5()): Calculate sine of a and display. Cosine (f6()): Calculate cosine of a and display. Tangent (f7()): Calculate tangent of a and display. Square (f8()): Square a and display the result. Clear (f9()): Clear all input and output fields.

## STEP 4 :
Run the code.

## PROGRAM :
```
<html>
    <head>
        <script type="text/javascript">
        function f1()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=a+b;
        }
        function f2()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=a-b;
        }
        function f3()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=a*b;
        }
        function f4()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=a/b;
        }
        function f5()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=Math.sin(a);
        }
        function f6()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=Math.cos(a);
        }
        function f7()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=Math.tan(a);
        }
        function f8()
        {
            var a=Number(document.getElementById("n1").value);
            var b=Number(document.getElementById("n2").value);
            document.getElementById("n3").value=a*a;
        }
        function f9()
        {
            document.getElementById("n1").value=" ";
            document.getElementById("n2").value=" ";
            document.getElementById("n3").value=" ";
        }
        </script>
    </head>
    <body>
        <form>
            <input type="button" onclick="f1()"  value="Add">
            <input type="button" onclick="f2()"  value="Subtract">
            <input type="button" onclick="f3()"  value="Multiply">
            <input type="button" onclick="f4()"  value="Divide">
            <input type="button" onclick="f5()"  value="Sin A">
            <input type="button" onclick="f6()"  value="Cos A">
            <input type="button" onclick="f7()"  value="Tan A">
            <input type="button" onclick="f8()"  value="A Square">
            <input type="button" onclick="f9()"  value="Clear">
            enter num1:
            <input type="text" id="n1">
            enter num2:
            <input type="text" id="n2">
            result:
            <input type="text" id="n3">
        </form>
    </body>
</html>
```

## OUTPUT :
![d1](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/b75d6e1e-e3b0-4ceb-b99c-d68a629ca81b)

![d2](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/2ede6864-8043-4969-806f-349f7a111e1a)

![d3](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/0f9d1b54-781a-4ea4-8b59-b98d4de8f122)

![d4](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/4addf457-61f0-4ff4-8869-66342c83a226)

![d5](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/2dbc597f-4470-4dcb-b888-243294f3967e)

![d6](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/bec04463-c0be-4183-9e59-bdc4e6aa7862)

![d7](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/ab32ca9b-187a-4151-94cd-00fbd591bd4f)

![d8](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/dfa12271-bb80-452d-9a68-3066df7578e4)


## EXP 9(e)
## AIM :
To design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.

## PROCEDURE :
## STEP 1 :
Create an HTML file that will act as the foundation for our text editor. Inside the 'head' section, link to a JavaScript file.

## STEP 2 :
Define the Javascript functions like text bold, text italic, all uppercase, all lowercase etc.

## STEP 3 :
Add buttons in the form of input elements. Each button will have a specific action, like making text bold, aligning text, etc.

## STEP 4 :
Inside each JavaScript function, use the getElementById method to select the text area by its ID ("num"). Apply different styles to the text inside the text area based on the button clicked. For example, the fontWeight property changes the text to bold when the "Bold" button is clicked.

## STEP 5 :
Run the code and display the output.

## PROGRAM :
```
<html>
<head>
<script type="text/javascript">
function f1()
{
document.getElementById("num").style.fontWeight="bold";
}
function f2()
{
document.getElementById("num").style.fontStyle="italic";
}
function f3()
{
document.getElementById("num").style.textTransform="uppercase";
}
function f4()
{
document.getElementById("num").style.textTransform="lowercase";
}
function f5()
{
document.getElementById("num").style.textTransform="capitalize";
}
function f6()
{
document.getElementById("num").style.textAlign="right";
}
function f7()
{
document.getElementById("num").style.textAlign="left";
}
function f8()
{
document.getElementById("num").style.textAlign="center";
}

function f9()
{
document.getElementById("num").style.fontWeight = "normal";
document.getElementById("num").style.textAlign = "left";
document.getElementById("num").style.fontStyle = "normal";
}
</script>
</head>
<body>
<form>
<input type="button" onclick="f1()"  value="Bold">
<input type="button" onclick="f2()"  value="Italics">
<input type="button" onclick="f3()"  value="All Caps">
<input type="button" onclick="f4()"  value="Small Caps">
<input type="button" onclick="f5()"  value="Title Case">
<input type="button" onclick="f6()"  value="Align Right">
<input type="button" onclick="f7()"  value="Align Left">
<input type="button" onclick="f8()"  value="Align Center">
<input type="button" onclick="f9()"  value="Clear Formatting">
<textarea rows="10" cols="35" id="num">
Simple Text Editor using JavaScript
</textarea>
</form>
</body>
</html>
```

## OUTPUT :
![e1](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/4c432221-d5df-494f-8d53-787ece5216fb)

![e2](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/78e39638-2a6b-433b-b47f-5ac3fe36ed3d)

![e3](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/c294ffc7-61c0-42ec-9a60-8e85679ad75a)

![e4](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/d57dcb97-755b-40de-bf59-61aa53c12d13)

![e5](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/e619eb1f-81ab-4f0f-9cb0-0864d49b2b07)

![e6](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/ee480534-6775-461a-9e5f-a79b431d666a)

![e7](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/c9452991-8482-4f3d-8dee-7dbe4f8559d8)

![e8](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/09f1e6e9-e1b7-4f99-a5e5-79fd6ca77adc)

![e9](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/0780ab3c-7abe-4872-bef1-1569a80b4265)


## EXP 9(f)
## AIM :
To design a JavaScript program which displays error messages when a field in form is entered incorrectly.

## PROCEDURE :
## STEP 1 :
Create an HTML file and Create arrays for error divs and input values.

## STEP 2 :
Use validate() to check username, password, and confirmation inputs. Display errors or "OK!" messages accordingly.

## STEP 3 :
Inside validate(), compare password and confirmation to ensure they match.

## STEP 4 :
Implement finalValidate() to ensure both username and password validations are correct before displaying a success message.

## STEP 5 :
Run the code and finally display the output.

## PROGRAM :
```
<!DOCTYPE html>
<html>
<body>

<h2>Form Validation</h2>

<form id="myForm">
  <label for="name">Name:</label><br>
  <input type="text" id="name" name="name"><br>
  <span id="nameError" style="color:red"></span><br>
  <label for="email">Email:</label><br>
  <input type="text" id="email" name="email"><br>
  <span id="emailError" style="color:red"></span><br>
  <input type="button" value="Submit" onclick="validateForm()">
</form>

<script>
function validateForm() {
    var name = document.getElementById("name").value;
    var email = document.getElementById("email").value;
    var nameError = "";
    var emailError = "";

    if (name == "") {
        nameError = "Name must be filled out";
    }

    if (email == "") {
        emailError = "Email must be filled out";
    } else if (!email.includes("@")) {
        emailError = "Email must be a valid email address";
    }

    document.getElementById("nameError").innerHTML = nameError;
    document.getElementById("emailError").innerHTML = emailError;
}
</script>

</body>
</html>
```

## OUTPUT :
![f](https://github.com/Renusri-Naraharasetty/ODD23-24-WT-JavaScript/assets/146916363/9b016ed2-4ccb-4d54-9191-f8528d9c6e02)


## RESULT :
Thus the program has been successfully executed and the output has been verified.
