# Cell Painting Visualization for Drug Discovery

<img src="https://github.com/mekz-data/drug_discovery/blob/main/images/cell_painting.png" height="400">

This project explores the use of Cell Painting, a high-content image-based assay, to facilitate drug discovery. Our goal was to allow for easier drug discovery by building interactive visualizations. It was part of my Master's in Analytics at Georgia Tech. Due to academic integrity policies, detailed reports and code are not publicly shared.    

## Project Overview:
- Developed an interactive visualization tool using Dash to analyze the massive JUMP Cell Painting dataset.
- Compared dimension reduction techniques: PCA, t-SNE, and UMAP.
- Evaluated clustering methods: K-Means, Birch, and DBSCAN.
- Integrated chemical structure visualization using the ChemPub Restful API.  
- [Project Proposal](https://youtu.be/wn6c_DhxlOo)    
- [Presentation](https://youtu.be/J4o2ygYiUPQ)
- [Poster](https://github.com/mekz-data/drug_discovery/blob/main/team093poster.pdf)    
    
<img src = "https://github.com/mekz-data/drug_discovery/blob/main/images/structure.png" height="350">

## Code and Resources Used
**Python Version:** 3.7  
**Packages used:** boto3, dask, rdkit, dash, plotly, scikit-learn        
**Dataset:** JUMP Cell Painting dataset from AWS S3 and metadata from GitHub.

## Data 
- Downloaded 2378 parquet files from AWS S3, totaling nearly 50GB.
- Cleaned data by removing unhelpful columns and calculating the median of features per perturbation.
- Reduced features using PCA, UMAP, and t-SNE for clustering.

## Explanation of Key Features
- **Dimension Reduction:** Techniques like PCA, t-SNE, and UMAP were used to reduce the high-dimensional data for visualization.
- **Clustering:** Methods such as K-Means, Birch, and DBSCAN were applied to group similar perturbations.
- **ECFP:** Extended-Connectivity Fingerprints were used to characterize molecular structures.

<img src = "https://github.com/mekz-data/drug_discovery/blob/main/images/viz2.png">


## Visualization
- Built using Dash for interactivity, allowing users to select different combinations of dimension reduction techniques and clustering methods.
- Visualized perturbations as dots on a scatter plot, with options to adjust methods via dropdowns.
- Displayed metadata and compound structures using the ChemPub Restful API.
- [Here's a brief demonstration.](https://youtu.be/TxNSQ6sGdgM?si=WDRbx3LQNWHFBXTL&t=43)

<img src="https://github.com/mekz-data/drug_discovery/blob/main/images/viz.png" height="300">





## Experiments and Evaluation
- **Feature Reduction:** PCA captured global structures, while t-SNE and UMAP preserved local and global structures, respectively.
- **Clustering:** Birch clustering produced the highest degree of similarity between compounds within clusters.
- **Evaluation:** Used Tanimoto coefficient for compound similarity analysis, with Birch showing the highest similarity.

## Takeaways
- Birch clustering with UMAP or PCA feature reduction is recommended for processing and analyzing the dataset.
- The project demonstrated the potential of unsupervised learning algorithms in visualizing complex biological data.
- The interactive tool democratizes access to data analysis for research scientists, offering flexibility and control over visualization.

