<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mythic Calculator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'MS Sans Serif', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: #008080; /* Classic Windows 98 teal background */
            padding: 20px;
        }
        
        .calculator {
            width: 100%;
            max-width: 300px;
            background-color: #c0c0c0; /* Classic Windows gray */
            border: 2px outset #c0c0c0; /* 3D outset border */
            box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
            padding: 4px;
        }
        
        .title-bar {
            background: linear-gradient(90deg, #000080, #1084d0); /* Windows 98 title bar gradient */
            color: white;
            padding: 3px 5px;
            font-size: 11px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 8px;
        }
        
        .title-text {
            font-weight: bold;
        }
        
        .title-buttons {
            display: flex;
        }
        
        .title-button {
            width: 16px;
            height: 14px;
            margin-left: 2px;
            font-size: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #c0c0c0;
            border: 1px outset #c0c0c0;
            cursor: default;
        }
        
        .display {
            background-color: white;
            border: 2px inset #c0c0c0; /* 3D inset border */
            padding: 8px 5px;
            text-align: right;
            margin-bottom: 8px;
            min-height: 50px;
        }
        
        .previous-operand {
            color: #424242;
            font-size: 12px;
            min-height: 14px;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .current-operand {
            color: black;
            font-size: 18px;
            font-weight: bold;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 3px;
        }
        
        button {
            border: 2px outset #c0c0c0; /* 3D outset for buttons */
            background-color: #c0c0c0;
            color: black;
            font-size: 14px;
            font-weight: bold;
            padding: 8px 0;
            cursor: pointer;
            min-height: 30px;
        }
        
        button:active {
            border: 2px inset #c0c0c0; /* 3D inset when pressed */
        }
        
        button:hover {
            background-color: #d4d0c8; /* Slightly lighter on hover */
        }
        
        .operator {
            background-color: #d4d0c8;
        }
        
        .equals {
            background-color: #d4d0c8;
            grid-column: span 2;
        }
        
        .clear, .delete {
            background-color: #d4d0c8;
        }
        
        .footer {
            text-align: center;
            padding: 5px;
            color: #424242;
            font-size: 10px;
            margin-top: 8px;
            border-top: 1px solid #808080;
        }
        
        /* Windows 98 specific styling */
        .window-container {
            border: 2px outset #c0c0c0;
            background-color: #c0c0c0;
        }
        
        @media (max-width: 400px) {
            button {
                padding: 6px 0;
                font-size: 12px;
            }
        }
    </style>
</head>
<body>
    <div class="calculator">
        <div class="title-bar">
            <div class="title-text">Mythic Calculator</div>
            <div class="title-buttons">
                <div class="title-button">_</div>
                <div class="title-button">□</div>
                <div class="title-button">×</div>
            </div>
        </div>
        
        <div class="display">
            <div class="previous-operand" id="previous-operand"></div>
            <div class="current-operand" id="current-operand">0</div>
        </div>
        
        <div class="buttons">
            <button class="clear" data-action="clear">C</button>
            <button class="delete" data-action="delete">CE</button>
            <button class="operator" data-operation="÷">/</button>
            <button class="operator" data-operation="*">*</button>
            
            <button data-number="7">7</button>
            <button data-number="8">8</button>
            <button data-number="9">9</button>
            <button class="operator" data-operation="-">-</button>
            
            <button data-number="4">4</button>
            <button data-number="5">5</button>
            <button data-number="6">6</button>
            <button class="operator" data-operation="+">+</button>
            
            <button data-number="1">1</button>
            <button data-number="2">2</button>
            <button data-number="3">3</button>
            <button class="equals" data-action="calculate">=</button>
            
            <button data-number="0">0</button>
            <button data-number=".">.</button>
        </div>
        
        <div class="footer">
            Mythic | Calculator for Windows 98
        </div>
    </div>

    <script>
        // Calculator state
        let currentOperand = '0';
        let previousOperand = '';
        let operation = undefined;
        let resetScreen = false;

        // DOM elements
        const currentOperandElement = document.getElementById('current-operand');
        const previousOperandElement = document.getElementById('previous-operand');

        // Button event listeners
        document.querySelectorAll('[data-number]').forEach(button => {
            button.addEventListener('click', () => {
                appendNumber(button.innerText);
                updateDisplay();
            });
        });

        document.querySelectorAll('[data-operation]').forEach(button => {
            button.addEventListener('click', () => {
                chooseOperation(button.innerText);
                updateDisplay();
            });
        });

        document.querySelector('[data-action="calculate"]').addEventListener('click', () => {
            calculate();
            updateDisplay();
        });

        document.querySelector('[data-action="clear"]').addEventListener('click', () => {
            clear();
            updateDisplay();
        });

        document.querySelector('[data-action="delete"]').addEventListener('click', () => {
            deleteNumber();
            updateDisplay();
        });

        // Keyboard support
        document.addEventListener('keydown', event => {
            if (event.key >= 0 && event.key <= 9) {
                appendNumber(event.key);
                updateDisplay();
            }
            if (event.key === '.') {
                appendNumber('.');
                updateDisplay();
            }
            if (event.key === '+' || event.key === '-' || event.key === '*' || event.key === '/') {
                chooseOperation(event.key);
                updateDisplay();
            }
            if (event.key === 'Enter' || event.key === '=') {
                calculate();
                updateDisplay();
            }
            if (event.key === 'Escape') {
                clear();
                updateDisplay();
            }
            if (event.key === 'Backspace') {
                deleteNumber();
                updateDisplay();
            }
        });

        // Calculator functions
        function appendNumber(number) {
            if (resetScreen) {
                currentOperand = '';
                resetScreen = false;
            }
            
            // Prevent multiple decimal points
            if (number === '.' && currentOperand.includes('.')) return;
            
            // Replace initial zero if needed
            if (currentOperand === '0' && number !== '.') {
                currentOperand = number;
            } else {
                currentOperand += number;
            }
        }

        function chooseOperation(op) {
            if (currentOperand === '') return;
            if (previousOperand !== '') {
                calculate();
            }
            
            operation = op;
            previousOperand = currentOperand;
            resetScreen = true;
        }

        function calculate() {
            let computation;
            const prev = parseFloat(previousOperand);
            const current = parseFloat(currentOperand);
            
            if (isNaN(prev) || isNaN(current)) return;
            
            switch (operation) {
                case '+':
                    computation = prev + current;
                    break;
                case '-':
                    computation = prev - current;
                    break;
                case '*':
                    computation = prev * current;
                    break;
                case '÷':
                case '/':
                    if (current === 0) {
                        computation = 'Error';
                    } else {
                        computation = prev / current;
                    }
                    break;
                default:
                    return;
            }
            
            currentOperand = computation.toString();
            operation = undefined;
            previousOperand = '';
            resetScreen = true;
        }

        function clear() {
            currentOperand = '0';
            previousOperand = '';
            operation = undefined;
        }

        function deleteNumber() {
            if (currentOperand.length === 1 || (currentOperand.length === 2 && currentOperand.startsWith('-'))) {
                currentOperand = '0';
            } else {
                currentOperand = currentOperand.slice(0, -1);
            }
        }

        function updateDisplay() {
            currentOperandElement.innerText = currentOperand;
            
            if (operation) {
                previousOperandElement.innerText = `${previousOperand} ${operation}`;
            } else {
                previousOperandElement.innerText = previousOperand;
            }
        }

        // Initialize display
        updateDisplay();
    </script>
</body>
</html>
