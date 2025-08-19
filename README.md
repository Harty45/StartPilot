# StartPilot
<!DOCTYPE html>
<html>
<head>
  <title>Login Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f2f2f2;
    }
    .login-box {
      background-color: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      width: 300px;
    }
    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 8px;
      margin: 8px 0;
      border-radius: 4px;
      border: 1px solid #ccc;
    }
    button {
      width: 100%;
      padding: 10px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    .error {
      color: red;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h2>Login</h2>
    <input type="text" id="username" placeholder="Username">
    <input type="password" id="password" placeholder="Password">
    <button onclick="login()">Login</button>
    <div id="error" class="error"></div>
  </div>

  <script>
    // Hardcoded username and password
    const correctUsername = "user123";
    const correctPassword = "pass123";

    function login() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;
      const errorDiv = document.getElementById("error");

      if(username === correctUsername && password === correctPassword) {
        alert("Login successful!");
        errorDiv.textContent = "";
        // You can redirect to another page here
        // window.location.href = "dashboard.html";
      } else {
        errorDiv.textContent = "Invalid username or password";
      }
    }
  </script>
</body>
</html>
