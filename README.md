<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Dropdown Menu</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        nav {
            background-color: #333;
            display: flex;
            flex-wrap: wrap;
        }
        .nav-item {
            color: white;
            padding: 14px 16px;
            cursor: pointer;
            position: relative;
            flex: 1;
        }
        .nav-item:hover {
            background-color: #575757;
        }
        .dropdown {
            display: none;
            position: absolute;
            background-color: #333;
            top: 100%;
            min-width: 160px;
            z-index: 1;
        }
        .nav-item:hover .dropdown {
            display: block;
        }
        .dropdown-item {
            color: white;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
        }
        .dropdown-item:hover {
            background-color: #575757;
        }
        .nested-dropdown {
            display: none;
            position: absolute;
            left: 100%;
            top: 0;
        }
        .dropdown-item:hover .nested-dropdown {
            display: block;
        }
        @media (max-width: 600px) {
            nav {
                flex-direction: column;
            }
            .nav-item {
                text-align: left;
                padding: 10px;
                flex: 1 100%; /* Full width on small screens */
            }
        }
    </style>
</head>
<body>
    <nav>
        <div class="nav-item">Home</div>
        <div class="nav-item">About</div>
        <div class="nav-item">Services</div>
        <div class="nav-item">
            More
            <div class="dropdown">
                <a href="#" class="dropdown-item">Option 1</a>
                <a href="#" class="dropdown-item">Option 2</a>
                <a href="#" class="dropdown-item">
                    Option 3
                    <div class="nested-dropdown">
                        <a href="#" class="dropdown-item">Sub-option 1</a>
                        <a href="#" class="dropdown-item">Sub-option 2</a>
                    </div>
                </a>
                <a href="#" class="dropdown-item">Option 4</a>
            </div>
        </div>
    </nav>
</body>
</html>
