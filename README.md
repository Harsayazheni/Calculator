# Caculator - TechnoHacks

## Aim
To Develop a calculator app that performs basic math operations.

## Program
In calc.html
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="icon" href="icon.jpg">
    <link rel="stylesheet" href="style.css">
    <title>Calculator</title>
</head>

<body>
    <div class="container">

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>0</button></td>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>3</button></td>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>-</button></td>
                </tr>
                <tr>
                    <td><button>6</button></td>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>X</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>9</button></td>
                    <td><button>C</button></td>
                    <td><button>=</button></td>
                    <td><button>/</button></td>
                </tr>
            </table>
        </div>
    </div>

</body>
<script src="index.js"></script>

</html>
```

In style.css
```
.container{
    text-align: center;
    margin: top 10px;
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid black;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: palevioletred;
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid rosybrown;
    background-color:white;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}
body{
    background-color: pink;
}
```

In index.js
```
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}
```

## Output
![OUTPUT](./out.png)