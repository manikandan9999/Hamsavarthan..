<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Finance Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            margin-top: 20px;
        }
        header, footer {
            background-color: #007BFF;
            color: white;
            text-align: center;
            padding: 10px 0;
        }
        h2 {
            text-align: center;
            color: #333;
        }
        .portfolio {
            margin-top: 20px;
        }
        .portfolio-table {
            width: 100%;
            border-collapse: collapse;
        }
        .portfolio-table th, .portfolio-table td {
            padding: 10px;
            border: 1px solid #ccc;
            text-align: left;
        }
        .portfolio-table th {
            background-color: #007BFF;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>Finance Portfolio</h1>
    </header>
    <div class="container">
        <h2>INVESTED AMOUNT/monthly</h2>
        <div class="portfolio">
            <table class="portfolio-table" id="portfolioTable">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Original Amount</th>
                        <th>Interest Rate</th>
                        <th>Total Amount</th>
                        <th>Date</th>
                    </tr>
                </thead>
                <tbody>
                </tbody>
            </table>
        </div>
    </div>
    <footer>
        <p>&copy; 2024 Happy Investing.</p>
    </footer>

    <script>
        function addPortfolioItem(name, amount, interestRate, date) {
            // Calculate total amount with interest
            const totalAmount = amount + (amount * (interestRate / 100));

            // Create table row
            const table = document.getElementById('portfolioTable').getElementsByTagName('tbody')[0];
            const newRow = table.insertRow();

            const cell1 = newRow.insertCell(0);
            const cell2 = newRow.insertCell(1);
            const cell3 = newRow.insertCell(2);
            const cell4 = newRow.insertCell(3);
            const cell5 = newRow.insertCell(4);

            cell1.textContent = name;
            cell2.textContent = `₹${amount.toFixed(2)}`;
            cell3.textContent = `${interestRate}%`;
            cell4.textContent = `₹${totalAmount.toFixed(2)}`;
            cell5.textContent = date;
        }

        window.onload = function() {
            // Replace the following values with the ones you want to enter
            const name = 'C.Hamsavarthan';
            const amount = 8000;
            const interestRate = 1.5;
            const date = '2024-08-06'; // Replace with the desired date

            // Add the portfolio item with the provided values
            addPortfolioItem(name, amount, interestRate, date);
        };
    </script>
</body>
</html>
