[index.html](https://github.com/user-attachments/files/23566324/index.html)
<!DOCTYPE html>
<html lang="en">
<head>![Uploading logo.png.jpeg…]()

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aurevian MUN - Home</title>

<style>
    body {
        margin: 0;
        font-family: Arial, sans-serif;
        color: white;
        text-align: center;

        background: linear-gradient(145deg, #00172e, #00376f, #00172e);
        background-size: 300% 300%;
        animation: moveGlow 10s infinite alternate ease-in-out;
    }

    @keyframes moveGlow {
        0% { background-position: 20% 0%; }
        50% { background-position: 80% 100%; }
        100% { background-position: 40% 20%; }
    }

    .container {
        margin-top: 60px;
    }

.card {
    background: rgba(0, 0, 0, 0.35);
    width: 70%;
    margin: auto;
    padding: 40px;
    border-radius: 25px;

    /* Faded mixed glow instead of strong neon */
    box-shadow: 0 0 25px rgba(120,150,255,0.35), 
                0 0 60px rgba(255,255,255,0.15);

    backdrop-filter: blur(6px);
}

.logo-circle {
    width: 120px;     /* ORIGINAL size */
    height: 120px;    /* ORIGINAL size */
    border-radius: 50%;
    padding: 4px;
    background: transparent;
    border: 2px solid rgba(255,255,255,0.85);
    margin: auto;
    display: flex;
    justify-content: center;
    align-items: center;
}

.logo-circle img {
    width: 88%;       /* original image size scale */
    border-radius: 50%;
}
}

    h1 {
        font-size: 32px;
        margin-top: 12px;
    }

    .subtitle {
        font-size: 22px;
        font-weight: 300;
        margin-bottom: 25px;
    }

    /* BUTTONS */
    .big-button,
    .small-button {
        background: #4da6ff;
        color: white;
        border-radius: 14px;
        text-decoration: none;
        padding: 14px;
        transition: 0.3s;
        font-weight: bold;
    }

    .big-button {
        font-size: 22px;
        display: block;
        width: 60%;
        margin: 20px auto;
    }

    .row-buttons {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin-top: 25px;
    }

    .small-button {
        font-size: 18px;
        width: 30%;
        padding: 12px;
    }

    .big-button:hover,
    .small-button:hover {
        background: #1f8fff;
        box-shadow: 0 0 15px #9ed3ff;
    }

    footer {
        margin-top: 40px;
        padding: 20px;
        color: #aad4ff;
        font-size: 16px;
        opacity: 0.7;
    }
</style>
</head>

<body>

<div class="container">
    <div class="card">

        <!-- GLOWING LOGO CIRCLE -->
        <div class="logo-circle">
            <img src="logo.png.jpeg" alt="Aurevian MUN Logo">
        </div>

        <h1>Aurevian MUN</h1>
        <p class="subtitle">Welcome To The Official Homepage</p>

        <!-- BUTTONS -->
        <a href="registration.html" class="big-button">1 Registration Form</a>

        <div class="row-buttons">
            <a href="teams.html" class="small-button">2 Teams</a>
            <a href="terms.html" class="small-button">3 Terms & Conditions</a>
            <a href="https://instagram.com/" target="_blank" class="small-button">4 Instagram Handle</a>
        </div>

    </div>
</div>

<footer>
    Created by Mridul Kapoor
</footer>

</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Aurevian MUN – Registration Form</title>
<style>
    body {
        margin: 0;
        font-family: Poppins, sans-serif;
        background: radial-gradient(circle at top, #0a0f24, #000);
        color: white;
    }

    .form-container {
        width: 90%;
        max-width: 500px;
        margin: 40px auto;
        background: rgba(255,255,255,0.05);
        padding: 25px;
        border-radius: 18px;
        backdrop-filter: blur(6px);
        border: 1px solid rgba(255,255,255,0.15);
    }

    h1 {
        text-align: center;
        margin-bottom: 20px;
        font-weight: 600;
    }

    label {
        display: block;
        margin: 12px 0 5px;
        font-size: 15px;
    }

    input, select {
        width: 100%;
        padding: 10px;
        border-radius: 10px;
        border: none;
        outline: none;
        margin-bottom: 10px;
        background: rgba(255,255,255,0.08);
        color: white;
    }

    input[type="file"] {
        padding: 4px;
    }



    button {
        width: 100%;
        padding: 14px;
        border: none;
        border-radius: 12px;
        margin-top: 10px;
        background: #1a73e8;
        color: white;
        cursor: pointer;
        font-size: 16px;
        transition: 0.2s;
    }

    button:hover {
        background: #3b8bff;
    }

    option:disabled {
        color: #777;
        background: #222;
    }
</style>
</head>
<body>

<div class="form-container">
    <h1>Aurevian MUN Registration</h1>

    <form id="regForm" enctype="multipart/form-data">

        <label>Name</label>
        <input type="text" name="name" required>

        <label>Phone Number</label>
        <input type="tel" name="phone" required>

        <label>Alternate Phone Number (Optional)</label>
        <input type="tel" name="alt_phone">

        <label>School / Institution</label>
        <input type="text" name="school">

        <label>Email ID</label>
        <input type="email" name="email" required>

        <label>Select Team</label>
        <select name="team" id="teamSelect" required></select>

        <label>UPI Payment ID</label>
        <input type="text" name="upi" value="8595635419@pthdfc" readonly>

        <label>Upload Payment Proof</label>
        <input type="file" name="payment" accept="image/*" required>

        <label>Reference (If Any)</label>
        <input type="text" name="reference">

        <label><input type="checkbox" required> I agree to all Terms & Conditions</label>

        <button type="submit">Submit</button>
    </form>
</div>

<script>

const WEB_APP_URL = "https://script.google.com/macros/s/AKfycbzn7OoTJ0izr4iIFnHk1OAx2nBkCABLsw3k9tWv7mup_ZsHWbVViBEi-2CypfEpgjkRcA/exec";

// Load teams from Google Apps Script
async function loadTeams() {
    const res = await fetch(WEB_APP_URL + "?action=getTeams");
    const teams = await res.json();

    const dropdown = document.getElementById("teamSelect");
    dropdown.innerHTML = "";

    teams.forEach(t => {
        const opt = document.createElement("option");
        opt.value = t.name;
        opt.textContent = t.name;

        if (t.locked) opt.disabled = true;

        dropdown.appendChild(opt);
    });
}

// Submit registration form
document.getElementById("regForm").addEventListener("submit", async (e) => {
    e.preventDefault();

    const formData = new FormData(e.target);

    const res = await fetch(WEB_APP_URL, {
        method: "POST",
        body: formData
    });

    const data = await res.json();

    alert(data.message);

    if (data.success) loadTeams();
});

loadTeams();

</script>


// Submit form data
document.getElementById("regForm").addEventListener("submit", async (e) => {
    e.preventDefault();

    const formData = new FormData(e.target);
    const res = await fetch("/register", {
        method: "POST",
        body: formData
    });

    const data = await res.json();
    alert(data.message);
    if (data.success) loadTeams();
});

loadTeams();
</script>

</body>
</html>

