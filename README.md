# Ebolavirus Genomic Sequence & Metadata Comparator

This repository hosts a lightweight, browser-based educational tool to analyze and compare Ebolavirus variants (Bundibugyo, Sudan, Zaire) associated with the 2025/2026 outbreaks. 

The application is built using vanilla HTML, JavaScript, and Tailwind CSS. It is designed to be hosted via **GitHub Pages** and performs all FASTA sequence parsing and TSV metadata extraction directly in the user's browser, requiring no backend server.

## Repository Structure

To ensure the application functions correctly, the repository must maintain the following structure:

* `index.html` - The main dashboard interface containing the sequence comparison and metadata logic.
* `README.md` - Project documentation and setup instructions.
* `ATTRIBUTION.md` - **CRITICAL**: Contains the Pathoplexus Data Use Terms acknowledgments, Submitting Group credits, and SeqSet DOIs.
* `/data/` - The directory containing the raw data files downloaded from Pathoplexus.
  * `ebola-bdbv_aligned-nuc_2026-05-18T1850.fasta`
  * `ebola-sudan_aligned-nuc_2026-05-18T1850.fasta`
  * `ebola-zaire_aligned-nuc_2026-05-18T1851.fasta`
  * `ebola-bdbv_metadata_2026-05-18T1849.tsv`
  * `ebola-sudan_metadata_2026-05-18T1849.tsv`
  * `ebola-zaire_metadata.tsv` *(Ensure this file is added)*

## Updating the Data

As the outbreak evolves, you can update the dashboard simply by replacing the files in the `/data/` directory:
1. Download the latest aligned `.fasta` and metadata `.tsv` files.
2. Ensure the filenames match the JavaScript fetch requests in `index.html`.
3. If new Submitting Groups have contributed *Restricted-Use Data* that falls within your **Focal Set**, you MUST update `ATTRIBUTION.md` and generate a new SeqSet DOI prior to pushing to GitHub.

## Data Attribution & Ethical Compliance

Genomic epidemiology relies on the rapid, hard work of researchers, clinicians, and submitting laboratories. This repository strictly adheres to the [Pathoplexus Data Use Terms](https://pathoplexus.org).

Per these terms, sequence data utilized here is divided into two categories:
1. **Focal Set:** Sequences critical to the comparative analysis. 
2. **Background Set:** Sequences providing historical or epidemiological context.

Users of Pathoplexus data must create a SeqSet containing the accession numbers and generate a DOI to properly credit the submitting groups. Please see the `ATTRIBUTION.md` file for full credits, laboratory acknowledgments, and associated SeqSet DOIs.

## Deployment on GitHub Pages

1. Navigate to your repository settings on GitHub.
2. Click **Pages** in the left sidebar.
3. Under "Build and deployment", select **Deploy from a branch**.
4. Select the `main` branch and the `/` (root) folder, then click **Save**.
5. Your analysis tool will be live and accessible via your unique GitHub Pages URL within a few minutes.
