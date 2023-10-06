<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f6f8fa;
            margin: 0;
            padding: 0;
        }
        .header {
            background-color: #24292e;
            color: white;
            padding: 10px 20px;
            text-align: center;
        }
        .profile {
            display: flex;
            justify-content: center;
            margin-top: 50px;
        }
        .avatar {
            margin-right: 50px;
        }
        .avatar img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
        }
        .info {
            line-height: 30px;
            width: 300px;
        }
        .info h2, .info p {
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>GitHub Profile</h1>
    </div>
    <div class="profile">
        <div class="avatar">
            <img src="avatar.jpg" alt="Avatar">
        </div>
        <div class="info">
            <h2>Username</h2>
            <p><strong>Bio:</strong> This is a short bio.</p>
            <p><strong>Location:</strong> City, Country</p>
            <p><strong>Repositories:</strong> 10</p>
            <p><strong>Followers:</strong> 200</p>
            <p><strong>Following:</strong> 150</p>
        </div>
    </div>
</body>
</html>
