## Celsius to Farenheit

This simple example will help you understand how to convert from degrees celsiu to farenheit using Java Script functions. 

Inside this example you will find the use of ```HTML```, ```CSS```, and ```JavaScript``` elements that will help you to continue building a better progress in the adoption of programming tools. 

### Capturing the values of a Radio button in JavaScript

The challenge in this project was how to capture the radio buttons implemented in the ```HTML``` code to be called by the function in order to identify which option the user wants to convert.

### JavaScript code  

```javascript

function convertCelsiustoFah(celcius) {
    let result = celcius * 9 / 5.0 + 32;
    return result;
}

function convertFahToCelsius(fahrenheit) {
    let result = (fahrenheit - 32)  * 5 / 9.0;
    return result;       
}

const form = select('form');
const numberOne = select('.number-one');
const btnConvert = select('.get-result');
const output = select('.output p');
const btnLightMode = select('.show-modal');

onEvent('click', btnConvert, function() {
    output.innerText = '';
    let initialNumber = numberOne.value.trim();
    if(!initialNumber) {
        output.innerText = 'Please input the number.';
        return;
    }

    let selectedRadioButton = select("input[name='convert']:checked");
    if(!selectedRadioButton)  {
        output.innerText = 'Please select the desired unit of temperature.';
        return;
    }

    let result;
    if(selectedRadioButton.value == "fahrenheit")  {
        result = convertCelsiustoFah(initialNumber);
        output.innerText = `${initialNumber}°C = ${result}°F`;
    } else if(selectedRadioButton.value == "celcius") {
        result = convertFahToCelsius(initialNumber);
        output.innerText = `${initialNumber}°F = ${result}°C`;
    }    
});
```

### Example in Web Page  

[Celsius To Farenheit](/celsiustofahrenheit/index.html)

### References

- [w3schools](https://www.w3schools.com/jsref/prop_radio_value.asp)
- [MDN Plus](https://developer.mozilla.org/en-US/docs/Web/API/RadioNodeList/value)
- [MDN Plus Functions](https://www.w3schools.com/js/js_function_definition.asp)
