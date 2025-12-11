# Program-Structure-COOKBOOK-

/* ===============================
RESET
=============================== */

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  }

/* ===============================
BODY – GLASS THEME BASE
=============================== */
body {
font-family: Arial, sans-serif;
background: linear-gradient(135deg, #b46143 0%, #f5bb9a 50%, #ffd8c0 100%);
background-attachment: fixed;
color: #333;
line-height: 1.6;
}

/* ===============================
GLASS UTILITY CLASS
=============================== */
.glass {
background: rgba(255, 255, 255, 0.25);
backdrop-filter: blur(18px) saturate(180%);
-webkit-backdrop-filter: blur(18px) saturate(180%);
border: 1px solid rgba(255, 255, 255, 0.35);
border-radius: 16px;
box-shadow: 0 8px 25px rgba(0,0,0,0.12);

display: block;
width: auto;
height: auto;
padding: 20px;
overflow: visible;
}

/* ===============================
NAVBAR – iOS Glassy
=============================== */
.navbar {
display: flex;
justify-content: space-between;
align-items: center;
padding: 15px 30px;
color: #fff;
position: sticky;
top: 0;
z-index: 1000;

background: rgba(255, 255, 255, 0.17);
backdrop-filter: blur(15px);
-webkit-backdrop-filter: blur(15px);
border-bottom: 1px solid rgba(255,255,255,0.25);
}

.navbar .nav-logo {
font-size: 26px;
font-weight: bold;
color: white;
text-shadow: 0 0 8px rgba(255,255,255,0.6);
}

.navbar .nav-links {
list-style: none;
display: flex;
gap: 25px;
}

.navbar .nav-links li a {
color: white;
text-decoration: none;
font-weight: bold;
transition: 0.2s;
padding: 6px 10px;
border-radius: 10px;
}

.navbar .nav-links li a:hover {
background: rgba(255,255,255,0.25);
}

/* ===============================
HOMEPAGE – Glass Hero Area
=============================== */
.home-container {
display: flex;
flex-direction: column;
align-items: center;
padding: 80px 20px 40px;
}

.brand-title {
font-size: 60px;
margin-bottom: 40px;
color: white;
text-shadow: 0 0 12px rgba(255,255,255,0.8);
}

.search-area {
position: relative;
width: 100%;
max-width: 500px;
}

#searchInput {
width: 100%;
padding: 12px 15px;
font-size: 18px;
border-radius: 12px;
background: rgba(255, 255, 255, 0.25);
border: 1px solid rgba(255,255,255,0.45);
color: #333;
backdrop-filter: blur(15px);
}

.suggestions {
position: absolute;
top: 100%;
left: 0;
right: 0;
background: rgba(255, 255, 255, 0.35);
backdrop-filter: blur(12px);
border-radius: 0 0 12px 12px;
max-height: 300px;
overflow-y: auto;
z-index: 10;
}

.suggestion-item {
padding: 12px;
cursor: pointer;
transition: 0.2s;
color: #333;
}

.suggestion-item:hover {
background: rgba(255,255,255,0.45);
}

.suggestion-item .sdesc {
font-size: 13px;
color: #444;
}

/* ===============================
INTRO PARAGRAPH
=============================== */
.intro-text {
margin-top: 40px;
max-width: 800px;
padding: 25px;
font-size: 17px;
color: #333;
background: rgba(255, 255, 255, 0.30);
border-radius: 16px;
backdrop-filter: blur(12px);
line-height: 1.7;
text-align: center;
}

/* ===============================
RECIPES PAGE – Cards Grid
=============================== */
/* ===============================
RECIPES PAGE – Layout & Sidebar
=============================== */
.recipes-page-wrapper {
  display: flex;
  gap: 20px;
  padding: 20px;
  justify-content: center; /* center content if screen is wide */
}

/* Sidebar */
.recipes-sidebar {
  flex: 0 0 250px; /* fixed width for sidebar */
  padding: 20px;
  border-radius: 16px;
  background: rgba(255,255,255,0.25);
  backdrop-filter: blur(14px);
  border: 1px solid rgba(255,255,255,0.3);
  height: fit-content; /* only as tall as content */
}

/* Cards container */
.recipes-cards-container {
  flex: 1; /* take remaining space */
  display: flex;
  flex-wrap: wrap; /* allow wrapping to new rows */
  gap: 20px;
}

/* Each recipe card */
.recipe-card {
  flex: 0 0 calc(33.33% - 20px); /* 3 cards per row, minus gap */
  box-sizing: border-box;
  padding: 20px;
  border-radius: 16px;
  background: rgba(255,255,255,0.30);
  backdrop-filter: blur(14px);
  border: 1px solid rgba(255,255,255,0.4);
}

/* Adjust for smaller screens */
@media (max-width: 1000px) {
  .recipe-card {
    flex: 0 0 calc(50% - 20px); /* 2 cards per row */
  }
}

@media (max-width: 700px) {
  .recipes-page-wrapper {
    flex-direction: column;
  }

  .recipes-cards-container {
    width: 100%;
  }

  .recipe-card {
    flex: 0 0 100%; /* 1 card per row */
  }
}

/* ===============================
ADD RECIPE PAGE – Glass Form
=============================== */
.add-recipe-container {
max-width: 900px;  /* wider container */
margin: 40px auto;
padding: 40px;
background: rgba(255,255,255,0.30);
backdrop-filter: blur(18px);
border-radius: 18px;
border: 1px solid rgba(255,255,255,0.4);
}

.add-recipe-container input,
.add-recipe-container textarea {
width: 100%;
margin-bottom: 15px;
background: rgba(255,255,255,0.35);
border-radius: 12px;
padding: 12px;
border: 1px solid rgba(255,255,255,0.45);
}

/* Steps input row */
.steps-input-row {
display: flex;
gap: 10px;
margin-bottom: 20px;
}

.steps-input-row input#stepInput {
flex: 1;
padding: 12px;
border-radius: 12px;
border: 1px solid rgba(255,255,255,0.45);
background: rgba(255,255,255,0.35);
backdrop-filter: blur(12px);
}

.steps-input-row button#addStepBtn {
padding: 12px 20px;
border-radius: 12px;
border: none;
background: rgba(255,255,255,0.45);
backdrop-filter: blur(12px);
cursor: pointer;
transition: 0.2s;
}

.steps-input-row button#addStepBtn:hover {
background: rgba(255,255,255,0.65);
}

/* ===============================
LOGIN PAGE – Centered Glass
=============================== */
.login-container {
max-width: 400px;
margin: 80px auto;
padding: 40px;
background: rgba(255,255,255,0.30);
backdrop-filter: blur(16px);
border-radius: 16px;
border: 1px solid rgba(255,255,255,0.35);
display: flex;
flex-direction: column;
align-items: center;
}

.login-container input {
width: 100%;
margin-bottom: 20px;
padding: 12px;
border-radius: 12px;
border: 1px solid rgba(255,255,255,0.45);
background: rgba(255,255,255,0.35);
backdrop-filter: blur(12px);
}

/* ===============================
RECIPE PAGE – Centered Glass Card
=============================== */
.recipe-detail-wrapper {
display: flex;
justify-content: center;
padding: 60px 20px;
}

.recipe-detail-container {
max-width: 800px;
width: 100%;
padding: 40px;
border-radius: 20px;
background: rgba(255, 255, 255, 0.30);
backdrop-filter: blur(18px);
border: 1px solid rgba(255, 255, 255, 0.4);
color: #333;
text-align: left;
}

.recipe-detail-container h1,
.recipe-detail-container h2 {
margin-bottom: 15px;
}

.recipe-detail-container p,
.recipe-detail-container ul,
.recipe-detail-container .steps-checklist {
margin-bottom: 20px;
}

.steps-checklist .step-row {
display: flex;
align-items: center;
gap: 12px;
margin-bottom: 12px;
}

/* Uniform Glassy Checkboxes */
.steps-checklist .step-row input[type="checkbox"] {
width: 22px;
height: 22px;
min-width: 22px;
min-height: 22px;
accent-color: rgba(255,255,255,0.6);
background: rgba(255,255,255,0.35);
border: 1px solid rgba(255,255,255,0.45);
border-radius: 6px;
backdrop-filter: blur(12px);
cursor: pointer;
transition: 0.2s;
}

.steps-checklist .step-row input[type="checkbox"]:checked {
background: rgba(255,255,255,0.55);
}

.recipe-detail-container ul li {
margin-left: 20px;
margin-bottom: 8px;
}

/* ===============================
GLASSY BUTTONS – Unified Style
=============================== */
button {
background: rgba(255, 255, 255, 0.40);
backdrop-filter: blur(12px);
border: 1px solid rgba(255, 255, 255, 0.35);
color: #333;
padding: 10px 16px;
border-radius: 12px;
cursor: pointer;
font-weight: bold;
transition: 0.2s;
text-align: center;
}

button:hover {
background: rgba(255, 255, 255, 0.60);
}

/* ===============================
SORTING BUTTONS (Sidebar)
=============================== */
.sort-buttons button {
width: 100%;
margin-bottom: 10px;
}

/* ===============================
RECIPE CARDS – View Full Recipe Button
=============================== */
.recipe-card button {
display: block;
margin-top: 15px;
width: auto;
}

/* ===============================
ADD RECIPE PAGE – Add Step / Save Buttons
=============================== */
#addStepBtn, #saveRecipeBtn {
display: inline-block;
}

/* ===============================
LOGIN PAGE – Glassy Login Button
=============================== */
#loginBtn {
display: block;
width: 100%;
margin-top: 20px;
}

/* ===============================
BREADCRUMBS NAVIGATION
=============================== */
.breadcrumbs-nav {
  display: flex;
  align-items: center;
  gap: 5px;
  padding: 10px 20px;
  background: rgba(255, 255, 255, 0.25);
  backdrop-filter: blur(12px);
  border-radius: 12px;
  font-size: 14px;
  color: #333; /* text color */
}

.breadcrumbs-nav ul {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0;
  margin: 0;
}

.breadcrumbs-nav li {
  display: flex;
  align-items: center;
}

.breadcrumbs-nav li a {
  text-decoration: none;
  color: #333; /* link text color */
  font-weight: bold;
}

.breadcrumbs-nav li a:hover {
  text-decoration: underline;
}

.breadcrumbs-nav li span.separator {
  margin: 0 5px;
  color: #555;
}

.breadcrumbs-nav {
position: sticky; 
top: 60px;
background: rgba(255, 255, 255, 0.2);
backdrop-filter: blur(10px);
-webkit-backdrop-filter: blur(10px);
padding: 10px 20px;
z-index: 999;
border-bottom: 1px solid rgba(255, 255, 255, 0.3);
}

#breadcrumbsList {
list-style: none;
display: flex;
gap: 5px;
margin: 0;
padding: 0;
font-size: 0.95rem;
font-weight: 500;
}

#breadcrumbsList li {
display: flex;
align-items: center;
}

#breadcrumbsList li a {
text-decoration: none;
color: #333; /* link color */
transition: color 0.2s;
}

#breadcrumbsList li a {
color: #000; /* hover color */
}

#breadcrumbsList li .separator {
margin: 0 5px;
color: #666; /* arrow color */
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Add Recipe</title>
    <link rel="stylesheet" href="cookbook_plus_styles.css">
    <script defer src="script.js"></script>
</head>
<body>

<!-- NAVBAR -->
<nav class="navbar glass">
  <div class="nav-logo">Cookbook+</div>
  <ul class="nav-links">
    <li><a href="homepage.html">Home</a></li>
    <li><a href="recipes.html">Recipes</a></li>
    <li><a href="add_recipe.html">Add Recipe</a></li>
    <li><a href="dashboard.html">Dashboard</a></li>
  </ul>
</nav>
<!-- BREADCRUMBS -->
<nav aria-label="breadcrumb" class="breadcrumbs-nav">
  <ul id="breadcrumbsList"></ul>
</nav>

<!-- PAGE WRAPPER -->
<div class="add-recipe-wrapper">
  <section class="add-recipe-container glass">
    <h1>Add a New Recipe</h1>

    <form id="addRecipeForm">

      <label>Recipe Name</label>
      <input type="text" id="recipeNameInput" placeholder="Enter recipe name">

      <label>Description (optional)</label>
      <textarea id="recipeDescInput" placeholder="Short description"></textarea>

      <label>Ingredients</label>
      <textarea id="ingredientsInput" placeholder="Enter ingredients separated by commas"></textarea>

      <label>Steps / Procedures</label>

      <div class="steps-input-row">
        <input type="text" id="stepInput" placeholder="Enter step...">
        <button type="button" id="addStepBtn">Add Step</button>
      </div>

      <!-- ONLY ONE stepsContainer (was duplicated before) -->
      <div id="stepsContainer"></div>

      <button type="submit" id="saveRecipeBtn">Save Recipe</button>
<script src="/cooksmart/js/add_recipe.js"></script>

    </form>
  </section>
</div>

</body>
</html>

<?php
require __DIR__ . '/config.php';
if ($_SERVER['REQUEST_METHOD'] !== 'POST') {
  http_response_code(405); echo json_encode(['error'=>'Method not allowed']); exit;
}
if (!isset($_FILES['image'])) { http_response_code(400); echo json_encode(['error'=>'No file uploaded']); exit; }
$uploadDir = __DIR__ . '/../assets/uploads/';
if (!is_dir($uploadDir)) mkdir($uploadDir, 0755, true);
$file = $_FILES['image'];
if ($file['error'] !== UPLOAD_ERR_OK) { http_response_code(400); echo json_encode(['error'=>'Upload error','code'=>$file['error']]); exit; }
$ext = pathinfo($file['name'], PATHINFO_EXTENSION);
$basename = bin2hex(random_bytes(8));
$target = $uploadDir . $basename . '.' . $ext;
if (!move_uploaded_file($file['tmp_name'], $target)) { http_response_code(500); echo json_encode(['error'=>'Failed to move uploaded file']); exit; }
$webPath = 'assets/uploads/' . $basename . '.' . $ext;
echo json_encode(['ok'=>true, 'path'=>$webPath]);
exit;

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Recipe Details</title>
    <link rel="stylesheet" href="cookbook_plus_styles.css">
    <script defer src="script.js"></script>
</head>
<body>

<!-- NAVBAR (unchanged structure) -->
<nav class="navbar">
  <div class="nav-logo">Cookbook+</div>
  <ul class="nav-links">
    <li><a href="homepage.html">Home</a></li>
    <li><a href="recipes.html">Recipes</a></li>
    <li><a href="add_recipe.html">Add Recipe</a></li>
    <li><a href="dashboard.html">Dashboard</a></li>
  </ul>
</nav>
<!-- BREADCRUMBS -->
<nav aria-label="breadcrumb" class="breadcrumbs-nav">
  <ul id="breadcrumbsList"></ul>
</nav>




<!-- RECIPE DETAILS – GLASSED CENTERED BOX -->
<div class="recipe-detail-wrapper">
  <div class="recipe-detail-container glass">
    <h1 id="recipeName"></h1>
    <p id="recipeDescription"></p>

    <h2>Ingredients</h2>
    <ul id="recipeIngredients"></ul>

    <h2>Steps</h2>
    <div id="stepsChecklist" class="steps-checklist"></div>
  </div>
</div>



</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cookbook+ | Recipes</title>
  <link rel="stylesheet" href="cookbook_plus_styles.css">
</head>
<body>

<!-- NAVBAR -->
<nav class="navbar glass">
  <div class="nav-logo">Cookbook+</div>
  <ul class="nav-links">
    <li><a href="homepage.html">Home</a></li>
    <li><a href="recipes.html">Recipes</a></li>
    <li><a href="add_recipe.html">Add Recipe</a></li>
    <li><a href="dashboard.html">Dashboard</a></li>
  </ul>
</nav>
<!-- BREADCRUMBS -->
<nav aria-label="breadcrumb" class="breadcrumbs-nav">
  <ul id="breadcrumbsList"></ul>
</nav>


<!-- PAGE CONTENT -->
<div class="recipes-page-wrapper">

  <!-- Sidebar -->
  <aside class="recipes-sidebar">
    <h3>Recipes</h3>
    <input type="text" id="recipesSearch" placeholder="Search recipes..." style="width:100%;padding:8px;margin-bottom:-3px;border-radius:10px;border:1px solid rgba(255,255,255,0.4);background:rgba(255,255,255,0.25);backdrop-filter:blur(12px);">

    <div class="sort-buttons" style="margin-top:20px;">
      <button id="sortAsc">Sort A-Z</button>
      <button id="sortDesc">Sort Z-A</button>
    </div>
    <ul id="recipeList"></ul>
  </aside>

  <!-- Cards Container -->
  <div id="recipesContainer" class="recipes-cards-container"></div>

</div>

<script src="script.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cookbook+ | Login</title>
  <link rel="stylesheet" href="cookbook_plus_styles.css">
</head>
<body>

<!-- NAVBAR -->
<nav class="navbar glass">
  <div class="nav-logo">Cookbook+</div>
  <ul class="nav-links">
    <li><a href="homepage.html">Home</a></li>
    <li><a href="recipes.html">Recipes</a></li>
    <li><a href="add_recipe.html">Add Recipe</a></li>
    <li><a href="login.html">Login</a></li>
  </ul>
</nav>

<!-- LOGIN FORM -->
<section class="login-container glass">
    <h1>Login</h1>

    <form class="login-form">
      <label>Username</label>
      <input type="text" id="username" class="glass">

      <label>Password</label>
      <input type="password" id="password" class="glass">

      <button type="button" id="loginBtn">Login</button>
    </form>
</section>

<script src="script.js"></script>
</body>
</html>

<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <title>Dashboard Login</title>
  <link rel="stylesheet" href="cookbook_plus_styles.css">
  <style>
    body { background:#f6f7fb; font-family: Inter, system-ui, Arial, sans-serif; }
    .login-box { max-width:420px;margin:90px auto;padding:24px;background:rgba(255,255,255,0.95);border-radius:12px; box-shadow:0 8px 24px rgba(0,0,0,0.08); }
    .login-box h2 { margin:0 0 8px 0; }
    .hint { color:#555;font-size:0.95rem;margin-top:8px; }
    .small { font-size:0.9rem;color:#666;margin-top:10px; }
    .navbar { padding:12px 20px; background:linear-gradient(90deg, rgba(255,255,255,0.65), rgba(255,255,255,0.45)); box-shadow:0 2px 8px rgba(0,0,0,0.05); }
    .nav-logo { font-weight:600; }
    input, button { font-size:1rem; }
    button { cursor:pointer; padding:10px 14px; border-radius:8px; border:0; background:#2b6cb0; color:white; }
  </style>
</head>
<body>
  <nav class="navbar"><div class="nav-logo">Cookbook+</div></nav>

  <div class="login-box">
    <h2>Dashboard Access</h2>
    <p>Enter dashboard password.</p>

    <input id="pwd" type="password" placeholder="Password" style="width:100%;padding:10px;margin-bottom:10px;border-radius:8px;border:1px solid #e2e8f0;">
    <div style="display:flex;gap:8px;">
      <button id="loginBtn">Enter</button>
      <button id="visitSite" style="background:#e2e8f0;color:#111;">Visit Site</button>
    </div>

    <div style="margin-top:10px;">
      <a href="#" id="showHint">Forgot? Show hint</a>
      <div id="hintText" class="hint" aria-hidden="true"></div>
    </div>

    <p class="small">If the dashboard hasn't been initialized yet, run the init command (see README or ask me) to set a password.</p>
  </div>

<script>
const API = 'api/dashboard_auth.php';

document.getElementById('loginBtn').addEventListener('click', async () => {
  const pw = document.getElementById('pwd').value;
  if (!pw) return alert('Enter password');
  const res = await fetch(API + '?action=login', {
    method:'POST',
    headers:{'Content-Type':'application/json'},
    body: JSON.stringify({password: pw})
  });
  const j = await res.json();
  if (res.ok && j.ok) {
    window.location.href = 'dashboard.html';
  } else {
    alert(j.error || 'Login failed');
  }
});

document.getElementById('showHint').addEventListener('click', async (e) => {
  e.preventDefault();
  const r = await fetch(API + '?action=hint');
  const j = await r.json();
  if (r.ok && j.hint) {
    document.getElementById('hintText').textContent = j.hint;
    document.getElementById('hintText').ariaHidden = false;
  } else {
    document.getElementById('hintText').textContent = 'No hint set.';
  }
});

document.getElementById('visitSite').addEventListener('click', () => {
  window.location.href = 'homepage.html';
});
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Cookbook+ | Home</title>
    <link rel="stylesheet" href="cookbook_plus_styles.css">
    <script defer src="script.js"></script>
</head>
<body>

<!-- NAVBAR -->
<nav class="navbar">
  <div class="nav-logo">Cookbook+</div>
  <ul class="nav-links">
    <li><a href="homepage.html">Home</a></li>
    <li><a href="recipes.html">Recipes</a></li>
    <li><a href="add_recipe.html">Add Recipe</a></li>
    <li><a href="dashboard.html">Dashboard</a></li>
  </ul>
</nav>
<nav aria-label="breadcrumb" class="breadcrumbs-nav">
    <ul id="breadcrumbsList"></ul>
</nav>



<!-- HOMEPAGE CONTENT -->
<div class="home-container">

    <h1 class="brand-title">Cookbook+</h1>

    <!-- Search Bar -->
    <div class="search-area">
        <input type="text" id="searchInput" placeholder="Search recipes...">
        <div id="suggestions" class="suggestions"></div>
    </div>

    <!-- INTRO PARAGRAPH (NEW) -->
    <p class="intro-text glass">
        Welcome to Cookbook+, your new best friend on a budget! We get it. You’re fueled by coffee,
        running on three hours of sleep, and your brain is currently crammed with more information
        than a faulty USB drive. The last thing you need is a complicated recipe that costs half
        your textbook fund and takes longer to make than a procrastination session. This book is a 
        survival guide to delicious, simple, and seriously budget-friendly meals.
        <br><br>
        Think of it as your culinary cheat sheet—because your biggest worry right now should be 
        passing that final, not mastering a béchamel sauce. Let's ditch the instant ramen and 
        start cooking!
    </p>

</div>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>CookSmart+ Dashboard</title>
  <link rel="stylesheet" href="cookbook_plus_styles.css">
</head>
<body>
<nav class="navbar glass">
  <div class="nav-logo">Cookbook+ Admin</div>
  <ul class="nav-links">
    <li><a href="homepage.html">Home</a></li>
    <li><a href="recipes.html">Recipes</a></li>
    <li><a href="add_recipe.html">Add Recipe</a></li>
    <li><a href="dashboard.html">Dashboard</a></li>
  </ul>
</nav>

<div style="max-width:1100px;margin:40px auto;padding:20px;">
  <h1>Recipe Management</h1>
  <div style="margin-bottom:16px;">
    <button id="createNewBtn">Add New Recipe</button>
    <input id="dashboardSearch" placeholder="Search recipes..." style="margin-left:12px;padding:8px;border-radius:8px;">
  </div>

  <table id="recipesTable" style="width:100%;border-collapse:collapse;">
    <thead>
      <tr>
        <th style="text-align:left;padding:8px">ID</th>
        <th style="text-align:left;padding:8px">Title</th>
        <th style="text-align:left;padding:8px">Short Desc</th>
        <th style="text-align:left;padding:8px">Created</th>
        <th style="text-align:left;padding:8px">Actions</th>
      </tr>
    </thead>
    <tbody></tbody>
  </table>

  <div id="editModal" style="display:none;position:fixed;left:50%;top:50%;transform:translate(-50%,-50%);background:white;padding:20px;border-radius:12px;box-shadow:0 10px 30px rgba(0,0,0,0.2);z-index:999;max-width:800px;width:95%;">
    <h3 id="modalTitle">Edit Recipe</h3>
    <div>
      <label>Title</label><br>
      <input id="modalTitleInput" style="width:100%;padding:8px;margin-bottom:10px;">
      <label>Short Description</label><br>
      <input id="modalShortInput" style="width:100%;padding:8px;margin-bottom:10px;">
      <label>Description</label><br>
      <textarea id="modalDescInput" style="width:100%;padding:8px;height:120px;margin-bottom:10px;"></textarea>
      <label>Ingredients (one per line)</label><br>
      <textarea id="modalIngredientsInput" style="width:100%;padding:8px;height:100px;margin-bottom:10px;"></textarea>
      <label>Steps (one per line)</label><br>
      <textarea id="modalStepsInput" style="width:100%;padding:8px;height:120px;margin-bottom:10px;"></textarea>
      <div style="display:flex;gap:8px;">
        <button id="saveModalBtn">Save</button>
        <button id="cancelModalBtn">Cancel</button>
      </div>
    </div>
  </div>

  <div id="overlay" style="display:none;position:fixed;left:0;top:0;right:0;bottom:0;background:rgba(0,0,0,0.4);z-index:998;"></div>
</div>

<script src="dashboard.js"></script>
</body>
</html>

-- create_db.sql (minimal)
CREATE DATABASE IF NOT EXISTS cooksmart CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE cooksmart;

CREATE TABLE IF NOT EXISTS recipes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  short_desc VARCHAR(512) DEFAULT '',
  description TEXT,
  image_path VARCHAR(255) DEFAULT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS ingredients (
  id INT AUTO_INCREMENT PRIMARY KEY,
  recipe_id INT NOT NULL,
  ingredient TEXT NOT NULL,
  `order_index` INT DEFAULT 0,
  FOREIGN KEY (recipe_id) REFERENCES recipes(id) ON DELETE CASCADE
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS steps (
  id INT AUTO_INCREMENT PRIMARY KEY,
  recipe_id INT NOT NULL,
  step_number INT NOT NULL,
  instruction TEXT NOT NULL,
  FOREIGN KEY (recipe_id) REFERENCES recipes(id) ON DELETE CASCADE
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

<?php
// api/recipes.php
header('Content-Type: application/json; charset=utf-8');

require __DIR__ . '/config.php'; // expects $pdo or create it here

// Ensure config.php defines $pdo (PDO instance). If not, create it:
if (!isset($pdo)) {
    try {
        $pdo = new PDO($dsn, $db_user, $db_pass, [
            PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION,
            PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC,
        ]);
    } catch (PDOException $e) {
        http_response_code(500);
        echo json_encode(['ok' => false, 'error' => 'DB connection error: '.$e->getMessage()]);
        exit;
    }
}

$method = $_SERVER['REQUEST_METHOD'];

try {
    if ($method === 'GET') {
        // GET /api/recipes.php           -> list all
        // GET /api/recipes.php?id=1      -> single recipe
        // GET /api/recipes.php?search=qq  -> optional search
        if (isset($_GET['id'])) {
            $stmt = $pdo->prepare("SELECT * FROM recipes WHERE id = :id");
            $stmt->execute([':id' => (int)$_GET['id']]);
            $row = $stmt->fetch();
            if (!$row) {
                http_response_code(404);
                echo json_encode(['ok' => false, 'error' => 'Not found']);
                exit;
            }
            // decode JSON fields for convenience
            $row['ingredients'] = json_decode($row['ingredients'], true) ?: [];
            $row['steps'] = json_decode($row['steps'], true) ?: [];
            echo json_encode(['ok' => true, 'data' => $row]);
            exit;
        } else {
            if (!empty($_GET['search'])) {
                $q = '%' . $_GET['search'] . '%';
                $stmt = $pdo->prepare("SELECT id,title,short_desc,image_path,created_at FROM recipes WHERE title LIKE :q OR short_desc LIKE :q ORDER BY created_at DESC");
                $stmt->execute([':q'=>$q]);
            } else {
                $stmt = $pdo->query("SELECT id,title,short_desc,image_path,created_at FROM recipes ORDER BY created_at DESC");
            }
            $list = $stmt->fetchAll();
            echo json_encode(['ok' => true, 'data' => $list]);
            exit;
        }
    }

    if ($method === 'POST') {
        // Accept JSON body
        $raw = file_get_contents('php://input');
        $data = json_decode($raw, true);
        if (!$data || !is_array($data)) {
            http_response_code(400);
            echo json_encode(['ok'=>false,'error'=>'Invalid JSON body']);
            exit;
        }

        // validate fields: title required
        $title = trim($data['title'] ?? '');
        if ($title === '') {
            http_response_code(400);
            echo json_encode(['ok'=>false,'error'=>'Title required']);
            exit;
        }

        $short_desc = trim($data['short_desc'] ?? '');
        // ingredients & steps should be JSON-encoded strings or arrays
        $ingredients = $data['ingredients'] ?? '[]';
        if (is_string($ingredients)) {
            // If input already JSON string, keep, else convert
            $tmp = json_decode($ingredients, true);
            if ($tmp === null && $tmp !== []) {
                // treat as newline separated list
                $ingredients = array_filter(array_map('trim', preg_split("/\r\n|\n|\r|,|;/", $ingredients)));
            } else {
                $ingredients = $tmp ?: [];
            }
        }
        if (!is_array($ingredients)) $ingredients = [];

        $steps = $data['steps'] ?? '[]';
        if (is_string($steps)) {
            $tmp = json_decode($steps, true);
            if ($tmp === null && $tmp !== []) {
                $steps = array_filter(array_map('trim', preg_split("/\r\n|\n|\r/", $steps)));
            } else {
                $steps = $tmp ?: [];
            }
        }
        if (!is_array($steps)) $steps = [];

        $image_path = trim($data['image_path'] ?? '');

        // insert
        $stmt = $pdo->prepare("INSERT INTO recipes (title, short_desc, description, ingredients, steps, image_path) VALUES (:title, :short_desc, :description, :ingredients, :steps, :image_path)");
        // description column may be same as short_desc if you don't have full description field; guard it
        $description = $data['description'] ?? $short_desc;

        $stmt->execute([
            ':title' => $title,
            ':short_desc' => $short_desc,
            ':description' => $description,
            ':ingredients' => json_encode(array_values($ingredients), JSON_UNESCAPED_UNICODE),
            ':steps' => json_encode(array_values($steps), JSON_UNESCAPED_UNICODE),
            ':image_path' => $image_path
        ]);
        $newId = (int)$pdo->lastInsertId();
        echo json_encode(['ok'=>true,'id'=>$newId]);
        exit;
    }

    if ($method === 'PUT') {
        parse_str(file_get_contents("php://input"), $put_vars);
        // try JSON first
        $raw = file_get_contents('php://input');
        $data = json_decode($raw, true);
        if (!$data || !is_array($data)) $data = $put_vars;

        if (empty($data['id'])) {
            http_response_code(400);
            echo json_encode(['ok'=>false,'error'=>'Missing id']);
            exit;
        }
        $id = (int)$data['id'];

        $fields = [];
        $params = [':id'=>$id];
        if (isset($data['title'])) { $fields[] = 'title = :title'; $params[':title'] = $data['title']; }
        if (isset($data['short_desc'])) { $fields[] = 'short_desc = :sd'; $params[':sd'] = $data['short_desc']; }
        if (isset($data['description'])) { $fields[] = 'description = :desc'; $params[':desc'] = $data['description']; }
        if (isset($data['image_path'])) { $fields[] = 'image_path = :ip'; $params[':ip'] = $data['image_path']; }
        if (isset($data['ingredients'])) { $fields[] = 'ingredients = :ing'; $params[':ing'] = json_encode($data['ingredients']); }
        if (isset($data['steps'])) { $fields[] = 'steps = :stp'; $params[':stp'] = json_encode($data['steps']); }

        if (!$fields) {
            http_response_code(400);
            echo json_encode(['ok'=>false,'error'=>'No updatable fields']);
            exit;
        }

        $sql = "UPDATE recipes SET " . implode(', ', $fields) . " WHERE id = :id";
        $stmt = $pdo->prepare($sql);
        $stmt->execute($params);
        echo json_encode(['ok'=>true,'changed'=>$stmt->rowCount()]);
        exit;
    }

    if ($method === 'DELETE') {
        // Delete by id: /api/recipes.php?id=1
        $id = $_GET['id'] ?? null;
        if (!$id) {
            http_response_code(400);
            echo json_encode(['ok'=>false,'error'=>'Missing id']);
            exit;
        }
        $stmt = $pdo->prepare("DELETE FROM recipes WHERE id = :id");
        $stmt->execute([':id'=>(int)$id]);
        echo json_encode(['ok'=>true,'deleted'=>$stmt->rowCount()]);
        exit;
    }

    // method not allowed
    http_response_code(405);
    echo json_encode(['ok'=>false,'error'=>'Method not allowed']);

} catch (Exception $e) {
    http_response_code(500);
    echo json_encode(['ok'=>false,'error'=>'Server error: '.$e->getMessage()]);
    exit;
}

<?php
// api/dashboard_auth.php
require __DIR__.'/config.php';

// file to store dashboard password/hint (not accessible via web by default)
$pwd_file = __DIR__ . '/.dashboard_pwd';

function read_pwd() {
  global $pwd_file;
  if (!file_exists($pwd_file)) return null;
  $json = file_get_contents($pwd_file);
  return json_decode($json, true);
}

function write_pwd($hash, $hint='') {
  global $pwd_file;
  $data = ['hash'=>$hash, 'hint'=>$hint];
  file_put_contents($pwd_file, json_encode($data, JSON_UNESCAPED_UNICODE), LOCK_EX);
}

$action = $_GET['action'] ?? $_POST['action'] ?? 'check';

if ($action === 'check') {
  $ok = !empty($_SESSION['dashboard_auth']) && $_SESSION['dashboard_auth'] === true;
  json_send(['authorized' => $ok]);
}

if ($action === 'login') {
  $body = json_decode(file_get_contents('php://input'), true) ?: $_POST;
  $pass = $body['password'] ?? '';
  if ($pass === '') json_send(['error'=>'password required'],400);
  $info = read_pwd();
  if (!$info) json_send(['error'=>'no password set','need_init'=>true],403);
  if (password_verify($pass, $info['hash'])) {
    $_SESSION['dashboard_auth'] = true;
    json_send(['ok'=>true]);
  } else {
    json_send(['error'=>'invalid password'],401);
  }
}

if ($action === 'hint') {
  $info = read_pwd();
  if (!$info) json_send(['error'=>'no password set','need_init'=>true],403);
  json_send(['hint'=> ($info['hint'] ?? '')]);
}

if ($action === 'logout') {
  $_SESSION['dashboard_auth'] = false;
  session_destroy();
  json_send(['ok'=>true]);
}

if ($action === 'change') {
  $body = json_decode(file_get_contents('php://input'), true) ?: $_POST;
  $old = $body['old_password'] ?? '';
  $new = $body['new_password'] ?? '';
  $hint = $body['hint'] ?? '';
  if (!$old || !$new) json_send(['error'=>'old and new required'],400);
  $info = read_pwd();
  if (!$info) json_send(['error'=>'no password set','need_init'=>true],403);
  if (!password_verify($old, $info['hash'])) json_send(['error'=>'old password invalid'],401);
  $newhash = password_hash($new, PASSWORD_DEFAULT);
  write_pwd($newhash, $hint);
  json_send(['ok'=>true]);
}

if ($action === 'init') {
  if (file_exists($pwd_file)) json_send(['error'=>'already initialized'],403);
  $body = json_decode(file_get_contents('php://input'), true) ?: $_POST;
  $pass = $body['password'] ?? '';
  $hint = $body['hint'] ?? '';
  if (!$pass) json_send(['error'=>'password required'],400);
  $hash = password_hash($pass, PASSWORD_DEFAULT);
  write_pwd($hash, $hint);
  json_send(['ok'=>true]);
}

json_send(['error'=>'unknown action'],400);

<?php

// api/config.php
header('Content-Type: application/json; charset=utf-8');
// error reporting for dev
ini_set('display_errors', 1);
error_reporting(E_ALL);

session_start();

$db_host = '127.0.0.1';
$db_name = 'cooksmart';
$db_user = 'root';
$db_pass = 'root';  
$dsn = "mysql:host=$db_host;dbname=$db_name;charset=utf8mb4";

try {
  $pdo = new PDO($dsn, $db_user, $db_pass, [
    PDO::ATTR_ERRMODE => PDO::ERRMODE_EXCEPTION,
    PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC
  ]);
} catch (Exception $e) {
  http_response_code(500);
  echo json_encode(['error'=>'DB connection failed','msg'=>$e->getMessage()]);
  exit;
}

function json_send($data, $code = 200) {
  http_response_code($code);
  echo json_encode($data, JSON_UNESCAPED_UNICODE);
  exit;
}
