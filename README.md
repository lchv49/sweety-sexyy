import zipfile
import os
import shutil

# Créer un répertoire temporaire pour le site
site_dir = "/mnt/data/site_delices_intimes"
os.makedirs(site_dir, exist_ok=True)

# Fichiers HTML
html_files = {
    "index.html": """
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Délices Intimes</title>
  <style>
    body {
      margin: 0;
      font-family: 'Helvetica Neue', sans-serif;
      background-color: #fdf6ee;
      color: #3b2e2a;
    }
    header {
      text-align: center;
      padding: 2rem;
    }
    header h1 {
      font-size: 2.5rem;
    }
    header p {
      font-style: italic;
      margin-top: 0.5rem;
    }
    .intro {
      text-align: center;
      margin-bottom: 2rem;
      font-size: 1.1rem;
    }
    .product {
      text-align: center;
      padding: 2rem;
    }
    .product img {
      max-width: 300px;
      border-radius: 10px;
      cursor: pointer;
    }
    .product h2 {
      font-size: 1.5rem;
      margin: 1rem 0 0.5rem;
    }
    .product p {
      margin-bottom: 1rem;
    }
    .btn {
      background-color: #3b2e2a;
      color: white;
      padding: 0.7rem 1.2rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1rem;
      text-decoration: none;
    }
    .btn:hover {
      background-color: #d62828;
    }
    .grid {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 2rem;
      margin: 2rem;
    }
    .card {
      background: white;
      padding: 1rem;
      border-radius: 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      text-align: center;
      width: 250px;
    }
    .card img {
      width: 100%;
      border-radius: 6px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Délices intimes</h1>
    <p>À croquer… et à dévoiler</p>
  </header>

  <section class="intro">
    <p>Découvrez notre collection gourmande de lingerie : un délice pour les yeux et pour le palais !</p>
  </section>

  <section class="product">
    <a href="sweet-temptation.html">
      <img src="premier-apercu-produit-sweety-sexy.png" alt="Sweet Temptation" />
    </a>
    <a href="sweet-temptation.html" style="text-decoration: none; color: inherit;">
      <h2>Sweet Temptation</h2>
    </a>
    <p>Soutien-gorge triangle avec Tagada dévoileur</p>
    <a href="sweet-temptation.html" class="btn">Découvrir</a>
  </section>

  <section class="grid">
    <div class="card">
      <a href="choco-crush.html">
        <img src="choco-crush.png" alt="Choco-Crush">
        <h3>Choco-Crush</h3>
      </a>
      <p>Culotte
