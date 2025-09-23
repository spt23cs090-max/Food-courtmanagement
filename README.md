# Food-courtmanagement
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Food Court Management System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding: 20px;
        }
        .section {
            background-color: #fff;
            padding: 20px;
            margin: 10px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            flex: 1;
            min-width: 300px;
        }
        h1, h2 {
            color: #333;
            text-align: center;
        }
        .menu-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }
        .menu-item:last-child {
            border-bottom: none;
        }
        .menu-item button {
            background-color: #28a745;
            color: #fff;
            border: none;
            padding: 5px 10px;
            cursor: pointer;
            border-radius: 4px;
        }
        .order-form input, .order-form select {
            width: calc(100% - 22px);
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .order-form button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
            border-radius: 4px;
        }
        .orders-list {
            list-style-type: none;
            padding: 0;
        }
        .orders-list li {
            padding: 10px;
            border: 1px solid #ccc;
            margin-bottom: 10px;
            border-radius: 4px;
        }
    </style>
</head>
<body>

    <h1>Food Court Management System</h1>

    <div class="container">
        
        <div class="section menu-section">
            <h2>Menu</h2>
            <div id="menu">
                <div class="menu-item">
                    <span>Burger - $5.99</span>
                    <button>Add</button>
                </div>
                <div class="menu-item">
                    <span>Pizza - $12.50</span>
                    <button>Add</button>
                </div>
                <div class="menu-item">
                    <span>Fries - $2.99</span>
                    <button>Add</button>
                </div>
                <div class="menu-item">
                    <span>Soda - $1.50</span>
                    <button>Add</button>
                </div>
            </div>
        </div>

        <div class="section order-form-section">
            <h2>Place an Order</h2>
            <form id="orderForm" class="order-form">
                <label for="customerName">Customer Name:</label>
                <input type="text" id="customerName" name="customerName" required>
                
                <label for="itemSelect">Select Item:</label>
                <select id="itemSelect" name="itemSelect">
                    <option value="Burger">Burger</option>
                    <option value="Pizza">Pizza</option>
                    <option value="Fries">Fries</option>
                    <option value="Soda">Soda</option>
                </select>

                <label for="quantity">Quantity:</label>
                <input type="number" id="quantity" name="quantity" min="1" value="1" required>

                <button type="submit">Submit Order</button>
            </form>
        </div>

        <div class="section orders-display-section">
            <h2>Current Orders</h2>
            <ul id="ordersList" class="orders-list">
                </ul>
        </div>
    </div>

</body>
</html>
