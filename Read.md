<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to GitHub Clone!</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="logo">
            <img src="octocat.svg" alt="Octocat Logo">
            <h1>GitHub Clone</h1>
        </div>
        <div class="content">
            <div id="register" class="screen <?php if (isset($_GET['register'])) { echo 'active'; } ?>">
                <h2>New User Registration</h2>
                <form id="register-form">
                    <div class="form-group">
                        <label for="username">Username</label>
                        <input type="text" id="username" name="username" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="password">Password</label>
                        <input type="password" id="password" name="password" required>
                    </div>
                    <button type="submit">Register</button>
                </form>
            </div>
            <div id="login" class="screen <?php if (isset($_GET['login'])) { echo 'active'; } ?>">
                <h2>Existing User Login</h2>
                <form id="login-form">
                    <div class="form-group">
                        <label for="login-username">Username</label>
                        <input type="text" id="login-username" name="username" required>
                    </div>
                    <div class="form-group">
                        <label for="login-password">Password</label>
                        <input type="password" id="login-password" name="password" required>
                    </div>
                    <button type="submit">Login</button>
                </form>
            </div>
            <div id="home" class="screen <?php if (!isset($_GET['register']) && !isset($_GET['login'])) { echo 'active'; } ?>">
                <h2>Welcome to GitHub Clone!</h2>
                <p>This is a sample home page for a GitHub-like website.</p>
                <a href="#">Explore Repositories</a>
                <a href="#">Create a New Repository</a>
            </div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
