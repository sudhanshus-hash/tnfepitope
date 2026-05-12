# TNFepitope: A Webserver for Prediction of TNF-α Inducing Epitopes

TNFepitope is a host-specific computational tool developed for the prediction, design, and scanning of **Tumor Necrosis Factor-alpha (TNF-α) inducing epitopes**.

TNF-α is a major pro-inflammatory cytokine involved in immune regulation, inflammation, cancer, autoimmune disorders, viral infections, and cytokine release syndrome. TNFepitope helps researchers identify peptide regions that may induce TNF-α production, supporting peptide-based vaccine design, subunit vaccine development, and immunotherapy research.



## Web Server

**TNFepitope Web Server:**  
https://webs.iiitd.edu.in/raghava/tnfepitope/

This tool and dataset is also available on Zenodo 



## Citation

If you use TNFepitope in your research, please cite:

Dhall, A., Patiyal, S., Choudhury, S., Jain, S., Narang, K., and Raghava, G.P.S. TNFepitope: A webserver for the prediction of TNF-α inducing epitopes. Computers in Biology and Medicine, 160, 106929, 2023.

DOI: https://doi.org/10.1016/j.compbiomed.2023.106929



## About TNFepitope

Tumor Necrosis Factor-alpha, also known as **TNF-α**, is a pleiotropic pro-inflammatory cytokine that plays an important role in:

- Immune signaling
- Inflammatory response
- Viral infection response
- Cancer biology
- Autoimmune disorders
- Cytokine release syndrome

Higher TNF-α expression has been associated with several diseases, including cancer, autoimmune disorders, rheumatoid arthritis, diabetes, Crohn’s disease, inflammatory bowel disease, HIV infection, and COVID-19-related cytokine storm.

TNFepitope was developed to identify peptide epitopes that can induce TNF-α production. These epitopes can be useful for understanding inflammatory immune responses and designing peptide-based immunotherapeutic strategies.


## Methodology

### Dataset Collection

Experimentally validated TNF-α inducing and non-inducing epitopes were collected mainly from the **Immune Epitope Database**, also known as **IEDB**.

The study focused on two major hosts:

- Human
- Mouse

After preprocessing, peptide sequences were filtered based on length and redundancy.


## Dataset Summary

| Host | TNF-α Inducing Peptides | TNF-α Non-Inducing Peptides |
|---|---:|---:|
| Human | 1215 | 1312 |
| Mouse | 539 | 539 |

An alternate negative dataset was also generated using randomly selected peptides from the Swiss-Prot database.



## Machine Learning Framework

TNFepitope uses both **alignment-free** and **alignment-based** prediction approaches.

### Alignment-Free Approach

Machine learning models were trained using peptide sequence-derived features.

The classifiers used include:

- Random Forest
- Decision Tree
- Gaussian Naive Bayes
- Logistic Regression
- Support Vector Classifier
- K-Nearest Neighbor
- Extra Tree Classifier



## Feature Generation

Peptide features were generated using the **Pfeature** package.

Major feature types include:

- Amino Acid Composition
- Di-Peptide Composition
- Amphiphilic Pseudo Amino Acid Composition
- Atomic Composition
- Composition-Enhanced Transition Distribution
- Distance Distribution of Residues
- Pseudo Amino Acid Composition
- Physico-Chemical Properties Composition
- Quasi-Sequence Order
- Residue Repeat Information
- Conjoint Triad Descriptors
- Shannon Entropy-based features

Among these, **Di-Peptide Composition-based features** showed strong performance for classifying TNF-α inducing and non-inducing peptides.



## Alignment-Based Approach

TNFepitope also uses a **BLAST-based similarity search** approach.

In this method, a query peptide is compared against known TNF-α inducing and non-inducing peptides. The final class is assigned based on similarity with known experimentally validated epitopes.



## Hybrid Prediction Model

A hybrid method was developed by combining:

- BLAST-based similarity score
- Machine learning prediction score

This hybrid approach improved the overall prediction performance.



## Performance Highlights

| Host | Best Hybrid AUROC |
|---|---:|
| Human | 0.83 |
| Mouse | 0.77 |

The hybrid model performed better than individual machine learning or BLAST-based approaches.

---

## Key Features

### 1. TNF-α Epitope Prediction

Users can submit peptide sequences to predict whether they are likely to induce TNF-α production.

### 2. Protein Scanning

Users can submit complete protein sequences to scan for potential TNF-α inducing regions.

### 3. Peptide Design

The design module allows users to generate possible mutants of a peptide and evaluate whether the mutations increase or decrease TNF-α inducing potential.

### 4. BLAST Search

The BLAST search module compares query peptides against a curated database of known TNF-α inducing and non-inducing epitopes.

### 5. Standalone Package

A standalone version is available for users who want to run predictions locally.



## Modules Available

| Module | Description |
|---|---|
| Predict | Predict whether a peptide is TNF-α inducing or non-inducing |
| Design | Generate peptide mutants and predict their TNF-α inducing potential |
| Scan | Scan full-length proteins for TNF-α inducing regions |
| BLAST Search | Search query peptides against known TNF-α inducing and non-inducing epitopes |
| Standalone | Run TNFepitope locally |




## Applications

### Subunit Vaccine Design

TNFepitope can help identify peptide regions that may induce TNF-α-mediated immune responses and may be considered during subunit vaccine development.

### Viral Immunology

The tool can be used to scan viral proteins for TNF-α inducing regions, which may help in understanding inflammatory responses during viral infections.

### Autoimmune and Inflammatory Disease Research

Since TNF-α is involved in autoimmune and inflammatory diseases, TNFepitope may help identify peptides associated with immune activation.

### Peptide-Based Therapeutics

The design module can help researchers modify peptide sequences and study how mutations affect TNF-α inducing potential.

### Immunoinformatics Research

TNFepitope provides a computational framework for studying cytokine-inducing epitopes using sequence-based machine learning and similarity-based methods.



## Corresponding Author

**Prof. Gajendra P. S. Raghava**  
Department of Computational Biology  
Indraprastha Institute of Information Technology Delhi  
Okhla Phase III, New Delhi, India  

**Email:** raghava@iiitd.ac.in  

**Lab Website:** https://webs.iiitd.edu.in/raghava/


## Support and Funding

This work received support from the **Department of Biotechnology, Government of India**.

The authors also acknowledge support from the **Department of Science and Technology INSPIRE program** and infrastructure provided by the **Department of Computational Biology, IIIT Delhi**.



## License

This resource is available for academic and research use.

Users are requested to cite the original publication if they use TNFepitope in their work.


## Acknowledgement

The authors acknowledge the Department of Biotechnology, Government of India, the Department of Science and Technology INSPIRE program, and the Department of Computational Biology, IIIT Delhi, for financial support, fellowships, infrastructure, and facilities used in developing TNFepitope.

