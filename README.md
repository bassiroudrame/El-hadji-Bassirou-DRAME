# El-hadji-Bassirou-DRAME
PORTFOLIO REFERENT DIGITAL
# Creating HTML and CSS files for the user's CV and zipping them for download.
from pathlib import Path, PurePosixPath
output_dir = Path("/mnt/data/cv_elhadji_site")
output_dir.mkdir(parents=True, exist_ok=True)

html = """<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>CV — Elhadji Bassirou DRAME</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="header">
    <div class="container">
      <div class="intro">
        <h1>Elhadji Bassirou <span>DRAMÉ</span></h1>
        <p class="role">Consultant en communication digitale • Infographiste • Monteur vidéo</p>
      </div>
      <div class="contact">
        <p><strong>Téléphone :</strong> +221 77 263 72 74</p>
        <p><strong>Email :</strong> <a href="mailto:bassiroudrame91@gmail.com">bassiroudrame91@gmail.com</a></p>
        <p><strong>Adresse :</strong> Castors, Rue 13 — Dakar, Sénégal</p>
        <p><strong>Permis :</strong> Catégorie A1</p>
        <p><strong>LinkedIn :</strong> <a href="https://www.linkedin.com/in/elhadji-bassirou-drame-b945039a/" target="_blank">Profil LinkedIn</a></p>
      </div>
    </div>
  </header>

  <main class="container main-grid">
    <section class="about card">
      <h2>À propos</h2>
      <p>Marketing digital, Social Media Manager, vidéographie, infographie, print & web. Maîtrise d'Illustrator, Photoshop, InDesign, Premiere Pro, WordPress et outils d'IA générative.</p>
      <h3>Compétences clés</h3>
      <ul>
        <li>Design graphique & production print</li>
        <li>Création et montage vidéo</li>
        <li>Community management & stratégie social media</li>
        <li>SEO & rédaction web</li>
        <li>Conception de sites WordPress</li>
        <li>Outils : Photoshop, Illustrator, InDesign, Premiere Pro, CapCut, Google Analytics, Meta Business</li>
      </ul>
    </section>

    <section class="experience card">
      <h2>Expériences professionnelles</h2>

      <div class="job">
        <h3>Rédacteur de contenu Web — Futur Digital (France)</h3>
        <span class="date">Déc 2023 – Avr 2024</span>
        <ul>
          <li>Rédaction de contenus web optimisés SEO.</li>
        </ul>
      </div>

      <div class="job">
        <h3>Volontaire Nations Unies — Mauritanie (ID: 5169554)</h3>
        <span class="date">Mars – Août 2023</span>
        <ul>
          <li>Appui en communication pour la conception de supports visuels (projet PBF).</li>
        </ul>
      </div>

      <div class="job">
        <h3>Community Manager — Mouvement AM‑FIT</h3>
        <span class="date">Juil 2022 – Fév 2023</span>
        <ul>
          <li>Animation, visibilité, programmes d’intégration et engagement des membres.</li>
        </ul>
      </div>

      <div class="job">
        <h3>Monteur vidéo & miniatures — Freelance</h3>
        <span class="date">Fév 2022 – Juin 2022</span>
        <ul>
          <li>Montage, couverture des rushes et création de miniatures.</li>
        </ul>
      </div>

      <div class="job">
        <h3>Graphiste — MS Groupe</h3>
        <span class="date">Nov 2021 – Jan 2022</span>
        <ul>
          <li>Affiches, flyers, bâches, montages vidéo et supports digitaux.</li>
        </ul>
      </div>

      <div class="job">
        <h3>Taxateur & Gestionnaire SI — Tex Courrier Logistics</h3>
        <span class="date">Sept 2020 – Oct 2021</span>
        <ul>
          <li>Gestion des stocks, bordereaux, carnets de livraison numérisés, suivi des livreurs et gestion flotte.</li>
        </ul>
      </div>

      <div class="job">
        <h3>Infographiste — Tex Courrier Logistics</h3>
        <span class="date">Mars – Août 2020</span>
        <ul>
          <li>Maquettes, mise en page et supports de communication.</li>
        </ul>
      </div>

      <div class="job">
        <h3>Informaticien — Creatic: TIC & Système Éducatif</h3>
        <span class="date">Fév 2017 – Juil 2019</span>
        <ul>
          <li>Maintenance, formation des enseignants, support utilisateur.</li>
        </ul>
      </div>
    </section>

    <section class="education card">
      <h2>Formations & certifications</h2>
      <ul>
        <li>Licence 3 Journalisme & Communication — IMAN Dakar (2019‑2020)</li>
        <li>Licence 2 Journalisme & Communication — IMAN Dakar (2018‑2019)</li>
        <li>Licence 1 Journalisme & Communication — Up TECH Dakar (2017‑2018)</li>
        <li>Baccalauréat série L — Lycée de Ndoffane Lagheme Kaolack (2013‑2014)</li>
      </ul>

      <h3>Autres qualifications</h3>
      <ul>
        <li>Certificat d’appréciation — Volontaire Nations Unies (Graphique Design)</li>
        <li>Développement web — ESMTIC Dakar</li>
        <li>Marketing digital — ForceN UNCHK</li>
        <li>Attestations SIMPLON, Centre Grand, UP TECH, CKC (diverses formations numériques et PAO)</li>
      </ul>
    </section>

    <aside class="side card">
      <h2>Langues</h2>
      <ul>
        <li>Français (courant)</li>
        <li>Anglais (niveau intermédiaire)</li>
      </ul>

      <h2>Centres d'intérêt</h2>
      <ul>
        <li>Photographie, dessin, cinéma, sport</li>
        <li>Veille technologique, découverte</li>
      </ul>

      <h2>Qualités</h2>
      <ul>
        <li>Patient, créatif, organisé, polyvalent, autonome</li>
      </ul>

      <h2>Liens</h2>
      <ul>
        <li><a href="https://drive.google.com/drive/folders/1RjV3EN1XNAxae2gHYgK_AU9oHix2w545?usp=drive_link" target="_blank">Portfolio / Rushes</a></li>
      </ul>
    </aside>
  </main>

  <footer class="footer">
    <div class="container">
      <p>© <span id="year"></span> Elhadji Bassirou DRAMÉ — CV en ligne</p>
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
"""

css = """
:root{
  --bg:#f8fafc;
  --card:#ffffff;
  --muted:#64748b;
  --accent:#4f46e5;
  --accent-2:#06b6d4;
  --maxw:1100px;
  --radius:12px;
  --gap:20px;
  font-family: Inter, ui-sans-serif, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
}
*{box-sizing:border-box}
body{
  margin:0;
  background:var(--bg);
  color:#0f172a;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  line-height:1.5;
}
.container{
  max-width:var(--maxw);
  margin:0 auto;
  padding:28px;
}
.header{
  background:linear-gradient(90deg, rgba(79,70,229,0.06), rgba(6,182,212,0.03));
  border-bottom:1px solid rgba(15,23,42,0.04);
  padding:18px 0;
  margin-bottom:18px;
}
.header .container{display:flex;gap:20px;align-items:center;justify-content:space-between}
.intro h1{font-size:22px;margin:0}
.intro h1 span{color:var(--accent)}
.role{color:var(--muted);margin-top:6px;font-size:14px}
.contact p{margin:4px 0;color:var(--muted);font-size:14px}
.contact a{color:var(--accent);text-decoration:none}

.main-grid{
  display:grid;
  grid-template-columns: 1fr 320px;
  gap:var(--gap);
  align-items:start;
}
.card{
  background:var(--card);
  border-radius:var(--radius);
  padding:18px;
  box-shadow:0 6px 18px rgba(2,6,23,0.04);
}
.about ul, .experience ul, .education ul, .side ul{padding-left:18px;margin:8px 0;color:var(--muted)}
.experience .job{margin-bottom:14px}
.experience h3{margin:0;font-size:16px;color:#0b1220}
.experience .date{display:block;color:var(--muted);font-size:13px;margin-top:6px;margin-bottom:6px}

.side h2{margin-top:0;margin-bottom:8px}
.side ul{list-style:disc;padding-left:18px}

.footer{padding:14px 0;margin-top:22px;text-align:center;color:var(--muted);font-size:14px}

/* Responsive */
@media (max-width:900px){
  .main-grid{grid-template-columns:1fr; padding-bottom:30px}
  .header .container{flex-direction:column;align-items:flex-start}
  .contact{margin-top:12px}
}
"""

# write files
(index_file := output_dir / "index.html").write_text(html, encoding="utf-8")
(output_dir / "styles.css").write_text(css, encoding="utf-8")

# create a simple README
readme = """Chez Sen Digital Communication — CV en HTML\n\nFichiers:\n- index.html\n- styles.css\n\nPour visualiser localement:\n1. Ouvrez `index.html` dans votre navigateur.\n\nPour publier sur GitHub Pages:\n1. Créez un dépôt et poussez ces fichiers à la racine.\n2. Sur GitHub: Settings → Pages → Source: main branch (/root).\n\nFichier généré automatiquement par ChatGPT.\n"""
(output_dir / "README.md").write_text(readme, encoding="utf-8")

# create zip
import zipfile, shutil
zip_path = Path("/mnt/data/cv_elhadji_site.zip")
with zipfile.ZipFile(zip_path, "w", compression=zipfile.ZIP_DEFLATED) as zf:
    for f in output_dir.rglob("*"):
        zf.write(f, arcname=str(PurePosixPath(f.relative_to(output_dir))))
        
str(zip_path)

