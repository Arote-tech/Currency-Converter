<div class = "container">
    <h1>Currency Converter</h1>   

<form id = "converter-form">
    <div class = "form-group">
        <label for = "amount">Amount</label>
        <input type = "number" id = "amount" placeholder = "Enter amount" required>
    </div>

<div class = "form-group">
    <label for = "from-currency">From</label>
        <select id = "from-currency">
        <!-- currency options will be inserted from the api -->
        </select>
</div>

<div class = "form-group">
    <label for = "to-currency">To</label>
        <select id = "to-currency">
            <!-- currency options will be inserted from the api -->
        </select>
        </div>

<button type = "submit">Convert</button>

</form>

<div id = "result">
    <p></p>
        <!-- results will be inserted from the api -->
    </div>
</div>


:root {
    --bg-primary: #0f172a;
    --bg-secondary: #1e293b;
    --bg-input: #334155;
    --text-primary: #e2e8f0;
    --text-secondary: #94a3b8;
    --border-color: #475569;
    --accent-primary: #3b82f6;
    --accent-hover: #2563eb;
    --transition: all 0.3s ease;
    --font-sans: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    --font-heading: "Poppins", "Inter", system-ui, "Segoe UI", Roboto, Arial, sans-serif;
}


const converterForm = document.getElementById("converter-form");
const amountInput = document.getElementById("amount");
const fromCurrency = document.getElementById("from-currency");
const resultDiv = document.getElementById("result");
const toCurrency = document.getElementById("to-currency");


window.addEventListener("load", fetchCurrencies);

converterForm.addEventListener("submit", convertCurrency);



