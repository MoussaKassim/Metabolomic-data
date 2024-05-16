<!DOCTYPE html>
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
        .navbar-nav .nav-link {
            font-family: "Source Sans Pro", Arial, sans-serif;
            font-size: 16px;
        }

        /* Navbar Styles */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 500;
            background-color: #333333;
            padding-top: 0;
            padding-bottom: 0;
            height: 50px;
            width: 100%;
        }

        .navbar-brand {
            margin-top: -5px;
        }

        .navbar-nav .nav-item {
            margin-bottom: 0px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 0 0 rgba(0, 0, 0, 0);
        }

        .navbar-nav .nav-item:nth-child(4) {
            margin-right: 10cm;
            margin-left: auto;
        }

        .navbar-nav .source-code-link {
            margin-top: 40px;
        }

        .container {
            padding-left: 8.5cm;
        }

        /* Body padding to compensate for fixed navbar */
        body {
            padding-top: 50px;
            background-color: #ffffff;
            color: #333;
            margin: 0;
        }

        /* Sidebar Styles */
        #sidebar {
            position: fixed;
            top: 2.5cm;
            bottom: 2cm;
            left: 7.5cm;
            width: 180%;
            max-width: 260px;
            max-height: 17%;
            overflow-y: auto;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.0);
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
            background-color: #f4f4f4;
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
            margin-left: 0.2cm;
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
            background-color: #f4f4f4;
            border: 1px solid #ccc;
            border-radius: 5px;
            padding: 10px;
            margin-bottom: 20px;
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

        .card {
            transition: transform 0.3s;
            border: none;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            background-color: #fff;
            color: #333;
            margin-bottom: 20px;
        }

        .card:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
        }

        .card-deck {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin-top: 20px;
        }

        .card-deck .card {
            flex: 0 0 calc(33.333% - 20px);
            max-width: calc(33.333% - 20px);
            margin-bottom: 20px;
        }

        @media (max-width: 992px) {
            .card-deck .card {
                flex: 0 0 calc(50% - 20px);
                max-width: calc(50% - 20px);
            }
        }

        @media (max-width: 768px) {
            .card-deck .card {
                flex: 0 0 100%;
                max-width: 100%;
            }
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
                        <a class="nav-link" href="#introduction">Introduction</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#software-tutorial">Tutorial</a>
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
                            <a class="dropdown-item" href="#mds">MDS</a>
                            <a class="dropdown-item" href="#tsne">tSNE</a>
                            <a class="dropdown-item" href="#umap">UMAP</a>
                            <a class="dropdown-item" href="#kodama">KODAMA</a>
                        </div>
                    </li>
                </ul>
                <div class="navbar-nav ml-auto">
                    <a class="nav-link source-code-link" href="#">Source Code</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Sidebar -->
    <div id="sidebar">
        <ul>
            <li><a href="#introduction">Introduction</a></li>
            <li><a href="#software-tutorial">Tutorial</a></li>
            <li><a href="#simulation">Simulation</a></li>
            <li>
                <a href="#">Data Analyses</a>
                <ul>
                    <li><a href="#mds">MDS</a></li>
                    <li><a href="#tsne">tSNE</a></li>
                    <li><a href="#umap">UMAP</a></li>
                    <li><a href="#kodama">KODAMA</a></li>
                </ul>
            </li>
        </ul>
    </div>

    <!-- Main Content -->
    <div class="container">
        <section id="introduction" class="data-section">
            <div class="container">
                <h2>Metabolomic data</h2>
                <p>
                    The data belong to a cohort of 22 healthy donors (11 male and 11 female) where each provided
                    about 40 urine samples over the time course of approximately 2 months, for a total of 873 samples.
                    Each sample was analysed by Nuclear Magnetic Resonance Spectroscopy. Each spectrum was divided in
                    450 spectral bins.
                </p>
            </div>
        </section>

        <section id="software-tutorial" class="data-section">
            <div class="container">
                <h2>Tutorial</h2>
                <p>
                    Here, we load the MetRef dataset. Columns with only zero values are removed.
                </p>
                <div class="code-container">
                    <pre><code>
data(MetRef)
u=MetRef$data
u=u[,-which(colSums(u)==0)]
                    </code></pre>
                </div>
                <p>
                    We apply the Probabilistic Quotient Normalization
                </p>
                <div class="code-container">
                    <pre><code>
u=normalization(u)$newXtrain
                    </code></pre>
                </div>
                <p>
                    We mean-center and univariate scaling the data set.
                </p>
                <div class="code-container">
                    <pre><code>
u=scaling(u)$newXtrain
                    </code></pre>
                </div>
                <p>
                    Two classification vectors are created
                </p>
                <div class="code-container">
                    <pre><code>
class=as.numeric(as.factor(MetRef$gender))
class2=as.numeric(as.factor(MetRef$donor))
                    </code></pre>
                </div>
                <p>
                    Different algorithms for dimensionality reduction are applied
                </p>
                <div class="code-container">
                    <pre><code>
res_MDS=cmdscale(dist(u))
res_tSNE=Rtsne(u)$Y
res_UMAP = umap(u)$layout
                    </code></pre>
                </div>
                <p>
                    We apply KODAMA with Partial Least Square Discriminant Analysis (PLS-DA) as classifier with 50
                    components to drive the accuracy maximization. The KODAMA dissimilarity matrix's is converted in a
                    low dimensionality space using three different methods (i.e., MDS, t-SNE, and UMAP).
                </p>
                <div class="code-container">
                    <pre><code>
kk=KODAMA.matrix(u,f.par = 50)
res_KODAMA_MDS=KODAMA.visualization(kk,method = "MDS")
res_KODAMA_tSNE=KODAMA.visualization(kk,method = "t-SNE")
res_KODAMA_UMAP=KODAMA.visualization(kk,method = "UMAP")
                    </code></pre>
                </div>
                <p>
                    Visualize the different clustering algorithms:
                </p>
                <p>
                    a) labelled by the gender
                </p>
                <div class="code-container">
                    <pre><code>
par(mfrow = c(2,3))
plot(res_MDS,pch=21,bg=rainbow(2)[class],main="MDS")
plot(res_tSNE,pch=21,bg=rainbow(2)[class],main="tSNE")
plot(res_UMAP,pch=21,bg=rainbow(2)[class],main="UMAP")
plot(res_KODAMA_MDS,pch=21,bg=rainbow(2)[class],main="KODAMA_MDS",)
plot(res_KODAMA_tSNE,pch=21,bg=rainbow(2)[class],main="KODAMA_tSNE")
plot(res_KODAMA_UMAP,pch=21,bg=rainbow(2)[class],main="KODAMA_UMAP")
                    </code></pre>
                </div>
                <p align="center">
                    <img src="https://github.com/tkcaccia/KODAMA/blob/main/figures/metabolites.gender.png"
                        alt="Clustering by gender" />
                </p>
                <p>
                    b) labelled by the donor
                </p>
                <div class="code-container">
                    <pre><code>
plot(res_MDS,pch=21,bg=rainbow(22)[class2],main="MDS")
plot(res_tSNE,pch=21,bg=rainbow(22)[class2],main="tSNE")
plot(res_UMAP,pch=21,bg=rainbow(22)[class2],main="UMAP")
plot(res_KODAMA_MDS,pch=21,bg=rainbow(22)[class2],main="KODAMA_MDS",)
plot(res_KODAMA_tSNE,pch=21,bg=rainbow(22)[class2],main="KODAMA_tSNE")
plot(res_KODAMA_UMAP,pch=21,bg=rainbow(22)[class2],main="KODAMA_UMAP")
                    </code></pre>
                </div>
                <p align="center">
                    <img src="https://github.com/tkcaccia/KODAMA/blob/main/figures/metabolites.donor.png"
                        alt="Clustering by donor" />
                </p>
            </div>
        </section>
    </div>

    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.5.4/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>

</html>
