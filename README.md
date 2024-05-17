<KODAMA>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KODAMA</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <style>
        /* Font Family and Size */
        body,
        .navbar-nav .nav-link {color: #ffffff;
        .navbar-nav .nav-link {
            font-family: "Source Sans Pro", Arial, sans-serif;
            font-size: 16px;
            color: #ffffff;
            background-color: ;
        }}
         
        /* Navbar Styles */
        .navbar {
            position: fixed;
            top: 0;
            left: 0cm;
            right: 0;
            z-index: 500;
            background-color: #333333;
            padding-top: 0;
            padding-bottom: 0;
            height: 50px;
            width: calc(100%);
        }

        .navbar-brand {
            margin-top: -5px;
        }

        .navbar-nav .nav-item {
            margin-bottom: 04px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 109px 109px rgba(0, 0, 0, 0);
        }

        .navbar-nav .nav-link {
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .navbar-nav .nav-item:nth-child(1) {
            margin-top: 20px;
        }

        .navbar-nav .nav-item:nth-child(2) {
            margin-top: 20px;
        }

        .navbar-nav .nav-item:nth-child(3) {
            margin-top: 20px;
        }

        .navbar-nav .nav-item:nth-child(4) {
            margin-top: 20px;
            margin-right: 10cm;
            margin-left: auto;
        }

        .navbar-nav .source-code-link {
            margin-top: 40px;
        }

        .container {
            padding-left: 7.3cm;
        }

        .navbar-brand,
        .navbar-nav .nav-link {
            padding: 0.1px 1rem;
            text-decoration: none;
            display: inline-block;
        }

        .navbar-brand {
            font-size: 20px;
            margin-right: 5px;
            position: relative;
            display: block;
        }

        .navbar-brand:hover,
        .navbar-nav .nav-link:hover {
            text-decoration: none;
        }

        .navbar-nav {
            display: flex;
            align-items: center;
            margin-left: 05px;
        }

        /* Body padding to compensate for fixed navbar */
        body {
            padding-top: 0cm;
            background-color: #ffffff;
            color: #333;
            margin: 0;
        }

        /* Sidebar Styles */
        #sidebar {
            position: fixed;
            top: 2.5cm;
            bottom: 2cm;
            left: 9.5cm;
            width: 180%;
            max-width: 260px;
            max-height: 19%;
            overflow-y: auto;
            box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.0);
            padding: 5px;
            line-height: 20px;
            border-radius: 6px;
            border: 1px solid #ccc;
        }

        #sidebar ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        #sidebar ul li {
            padding: 5px;
            transition: background-color 0.3s;
            cursor: pointer;
        }

        #sidebar ul li:hover {
            background-color: #none;
        }

        #sidebar ul li a {
            color: #000000;
            text-decoration: none;
            font-size: 16px;
            font-family: "Source Sans Pro", Arial, sans-serif;
        }

        #sidebar ul li a i {
            font-size: 10px;
        }

        /* Main Content Styles */
        .container {
            margin-left: 1.5cm;
        }

        /* Sections Styles */
        .data-section {
            margin-bottom: 20px;
        }

        /* Adjusting margin for Introduction */
        .navbar-nav .nav-item:first-child {
            margin-top: 20px;
        }

        /* Active link styles */
        .active-link {
            background-color: #2780e3 !important;
        }

        .active-link a {
            color: white !important;
        }

        /* Code container styles */
        .code-container {
            position: relative;
            background-color: #f8f9fa;
            border: 1px solid #ccc;
            padding: 10px;
            margin-top: 10px;
            border-radius: 6px;
            overflow: hidden;
        }

        pre {
            margin: 0;
            padding: 0;
            overflow-x: auto;
        }

        button {
            position: absolute;
            top: 5px;
            right: 5px;
            background-color: transparent;
            border: none;
            color: #007bff;
            cursor: pointer;
        }

        button:hover {
            color: #0056b3;
        }

        button.copied {
            color: #28a745;
        }

        button.copied:hover {
            color: #218838;
        }
    

    </style>
</head>

<body>
        <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">KODAMA</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav mr-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="https://moussakassim.github.io/KODAMA1/">Introduction</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#software-tutorial">Software Tutorial</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#simulation">Simulation</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                            data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            Data Analyses
                        </a>
                        <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                            <a class="dropdown-item"
                                href="https://github.com/tkcaccia/KODAMA/blob/main/docs/Metabolomics_data.md">Metabolomic
                                data</a>
                            <a class="dropdown-item"
                                href="https://github.com/tkcaccia/KODAMA/blob/main/docs/Single_cell_RNA_seq.md">Single
                                cell RNA seq data</a>
                            <a class="dropdown-item"
                                href="https://github.com/tkcaccia/KODAMA/blob/main/docs/Spatial%20_transcriptomic.md">Spatial
                                Transcriptomic data</a>
                        </div>
                    </li>
                </ul>
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="https://github.com/tkcaccia/KODAMA">
                            <span class="fab fa-github"></span>
                            Source code
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
   
    <!-- Sidebar -->
    <div id="sidebar">
        <ul>
            <li id="TutorialLink" data-toggle="tooltip" data-placement="right" title="Tutorial">
                <a href="#Tutorial">
                    <i class="fas fa-book-open"></i>
                    <span>Tutorial</span>
                </a>
            </li>
            <li id="MDS, tSNE and UMAPLink" data-toggle="tooltip" data-placement="right" title="MDS, tSNE and UMAP">
                <a href="#MDS, tSNE and UMAP">
                    <i class="fas fa-newspaper"></i>
                    <span>MDS, tSNE and UMAP</span>
                </a>
            </li>
            <li id="KODAMALink" data-toggle="tooltip" data-placement="right" title="KODAMA">
                <a href="#KODAMA">
                    <i class="fas fa-tools"></i>
                    <span>KODAMA</span>
                </a>
            </li>
            <li id="Visualize the different clustering algorithmsLink" data-toggle="tooltip" data-placement="right" title="Visualize the different clustering algorithms">
                <a href="#Visualize the different clustering algorithms">
                    <i class="fas fa-tasks"></i>
                    <span>Visualize the different clustering algorithms</span>
                </a>
            </li>
        </ul>
    </div>
     <script>
        // Fonction pour changer le style de l'élément actif
        function setActiveLink(linkId) {
            // Supprimer la classe active-link de tous les éléments
            var links = document.querySelectorAll('#sidebar ul li');
            links.forEach(function (item) {
                item.classList.remove('active-link');
            });

            // Ajouter la classe active-link à l'élément sélectionné
            var selectedLink = document.getElementById(linkId);
            selectedLink.classList.add('active-link');
        }

        // Ajouter un écouteur d'événement pour chaque élément de la barre latérale
        var sidebarLinks = document.querySelectorAll('#sidebar ul li');
        sidebarLinks.forEach(function (link) {
            link.addEventListener('click', function (event) {
                // Empêcher le comportement par défaut du lien
                event.preventDefault();
                
                // Récupérer l'ID de l'élément cliqué
                var linkId = event.currentTarget.id;
                
                // Appeler la fonction pour définir l'élément actif
                setActiveLink(linkId);
            });
        });
    </script>
   <!-- Main Content -->
<div>
 <!-- Metabolomic Data -->
        <section id="Metabolomic Data" class="data-section">
            <div class="container">
    <h2>Metabolomic Data</h2>
    <p>The data belong to a cohort of 22 healthy donors (11 male and 11 female) where each provided about 40 urine samples over the time course of approximately 2 months, for a total of 873 samples. Each sample was analysed by Nuclear Magnetic Resonance Spectroscopy. Each spectrum was divided in 450 spectral bins.</p>
 </div>
        </section>
    <!-- Tutorial Section -->
<section id="Tutorial" class="data-section">
    <div class="container">
        <h2>Tutorial</h2>
        <p>Here, we load the MetRef dataset. Columns with only zero values are removed.</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>data(MetRef)
u = MetRef$data
u = u[,-which(colSums(u) == 0)]
</code></pre>
        </div>
        <p>We apply the Probabilistic Quotient Normalization</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>u = normalization(u)$newXtrain
</code></pre>
        </div>
        <p>We mean-center and univariate scaling the data set.</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>u = scaling(u)$newXtrain
</code></pre>
        </div>
        <p>Two classification vectors are created</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>class = as.numeric(as.factor(MetRef$gender))
class2 = as.numeric(as.factor(MetRef$donor))
</code></pre>
        </div>
    </div>
</section>

    <!-- MDS, tSNE and UMAP Section -->
<section id="MDS_tSNE_UMAP" class="data-section">
    <div class="container">
        <h2>MDS, tSNE and UMAP</h2>
        <p>Different algorithms for dimensionality reduction are applied</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>res_MDS = cmdscale(dist(u))
res_tSNE = Rtsne(u)$Y
res_UMAP = umap(u)$layout
</code></pre>
        </div>
    </div>
</section>

    <!-- KODAMA Section -->
<section id="KODAMA" class="data-section">
    <div class="container">
        <h2>KODAMA</h2>
        <p>We apply KODAMA with Partial Least Square Discriminant Analysis (PLS-DA) as classifier with 50 components to drive the accuracy maximization. The KODAMA dissimilarity matrix is converted in a low dimensionality space using three different methods (i.e., MDS, t-SNE, and UMAP).</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>kk = KODAMA.matrix(u, f.par = 50)
res_KODAMA_MDS = KODAMA.visualization(kk, method = "MDS")
res_KODAMA_tSNE = KODAMA.visualization(kk, method = "t-SNE")
res_KODAMA_UMAP = KODAMA.visualization(kk, method = "UMAP")
</code></pre>
        </div>
    </div>
</section>

    <!-- Visualize the different clustering algorithms Section -->
<section id="Visualize_the_different_clustering_algorithms" class="data-section">
    <div class="container">
        <h2>Visualize the different clustering algorithms:</h2>
        <p>a) Labelled by the gender</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>par(mfrow = c(2, 3))
plot(res_MDS, pch = 21, bg = rainbow(2)[class], main = "MDS")
plot(res_tSNE, pch = 21, bg = rainbow(2)[class], main = "tSNE")
plot(res_UMAP, pch = 21, bg = rainbow(2)[class], main = "UMAP")
plot(res_KODAMA_MDS, pch = 21, bg = rainbow(2)[class], main = "KODAMA_MDS")
plot(res_KODAMA_tSNE, pch = 21, bg = rainbow(2)[class], main = "KODAMA_tSNE")
plot(res_KODAMA_UMAP, pch = 21, bg = rainbow(2)[class], main = "KODAMA_UMAP")
</code></pre>
        </div>
        <p align="center">
            <img src="https://github.com/tkcaccia/KODAMA/blob/main/figures/metabolites.gender.png" alt="Gender clustering">
        </p>

        <p>b) Labelled by the donor</p>
        <div class="code-container">
            <button class="copyButton"><i class="far fa-copy"></i></button>
            <pre><code>plot(res_MDS, pch = 21, bg = rainbow(22)[class2], main = "MDS")
plot(res_tSNE, pch = 21, bg = rainbow(22)[class2], main = "tSNE")
plot(res_UMAP, pch = 21, bg = rainbow(22)[class2], main = "UMAP")
plot(res_KODAMA_MDS, pch = 21, bg = rainbow(22)[class2], main = "KODAMA_MDS")
plot(res_KODAMA_tSNE, pch = 21, bg = rainbow(22)[class2], main = "KODAMA_tSNE")
plot(res_KODAMA_UMAP, pch = 21, bg = rainbow(22)[class2], main = "KODAMA_UMAP")
</code></pre>
        </div>
        <p align="center">
            <img src="https://github.com/MoussaKassim/Metabolomic-data/blob/main/metabolites.donor.png" alt="Donor clustering">
        </p>
    </div>
</section>

        
    <!-- Bootstrap Scripts -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.3/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

    <!-- Font Awesome Script -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/js/all.min.js"></script>

    <!-- JavaScript for interactive functionality -->
    <script>
    // Fonction pour déplacer la page vers l'élément correspondant
function scrollToSection(sectionId) {
    var section = document.getElementById(sectionId);
    section.scrollIntoView({ behavior: 'smooth', block: 'start' });
}

// Ajouter un écouteur d'événement pour chaque élément de la barre latérale
var sidebarLinks = document.querySelectorAll('#sidebar ul li');
sidebarLinks.forEach(function (link) {
    link.addEventListener('click', function (event) {
        // Empêcher le comportement par défaut du lien
        event.preventDefault();

        // Récupérer l'ID de la section correspondante
        var sectionId = link.querySelector('a').getAttribute('href').replace('#', '');

        // Défiler jusqu'à la section correspondante
        scrollToSection(sectionId);
    });
});

        // Fonction pour ajouter la classe de couleur de fond au survol
        function addBackgroundOnHover(element) {
            element.addEventListener('mouseenter', function () {
                element.classList.add('bg-color');
            });
            element.addEventListener('mouseleave', function () {
                element.classList.remove('bg-color');
            });
        }

        // Fonction pour gérer le clic sur un élément de la liste
        function handleItemClick(element) {
            element.addEventListener('click', function () {
                // Supprimer la classe de couleur de fond de tous les éléments
                var listItems = document.querySelectorAll('.nav-item');
                listItems.forEach(function (item) {
                    item.classList.remove('bg-color');
                });

                // Ajouter la classe de couleur de fond à l'élément cliqué
                element.classList.add('bg-color');
            });
        }

        // Sélectionnez tous les éléments de la liste du menu
        var menuItems = document.querySelectorAll('.nav-item');

        // Ajouter la logique d'interaction pour chaque élément de la liste du menu
        menuItems.forEach(function (item) {
            handleItemClick(item);
            addBackgroundOnHover(item);
        });
       
    var copyButton = document.getElementById('copyButton');
    var codeBlock = document.querySelector('.code-container pre code');

    document.getElementById('copyButton1').addEventListener('click', function() {
    var codeBlock = document.getElementById('codeBlock1');
    var textToCopy = codeBlock.querySelector('code').innerText;
    navigator.clipboard.writeText(textToCopy)
        .then(function() {
            // Changement de couleur du bouton pour indiquer que la copie a réussi
            document.getElementById('copyButton1').classList.add('copied');
            setTimeout(function() {
                document.getElementById('copyButton1').classList.remove('copied');
            }, 1000);
        })
        .catch(function(err) {
            console.error('Failed to copy: ', err);
        });
});

         </script>
</body>

</html>
