# Fabric_Spark_Anand
Fabric and Spark Notebooks
## Fabric Spark on One Page: book and companion notebooks

This project tracks the last checks before publishing **Fabric Spark on One Page**: a 48-page visual cheat sheet on Microsoft Fabric lakehouse essentials, Spark performance tuning and capacity (CU) usage.

**Author:** Muruganandam Nalluswamy
**Repository:** [Anand15oct/Fabric-notes](https://github.com/Anand15oct/Fabric-notes)

### What's being tested

| Item | Contents |
|---|---|
| `Fabric-Spark-on-One-Page.pdf` | The book: 48 pages, US Letter |
| `NB00_Setup_Sample_Data` | Builds a sample lakehouse (2,000 orders, 200 customers) |
| `NB01_Part1_Essentials` | Code cards from pages 5–18 |
| `NB02_Part2_Spark_Performance` | Code cards from pages 19–34 |
| `NB03_Session_Cells` | Cards that stop or restart the session; run one at a time |
| `nb_silver`, `nb_dim_customer`, `nb_dim_product` | Small helpers the other notebooks call |

### How to test

1. Use a **test** workspace and lakehouse, never production. NB00 overwrites its sample tables.
2. Import all 7 notebooks without renaming them, and attach the test lakehouse to each one.
3. Use **Run all** on NB01, then on NB02. Each one runs NB00 first.
4. Run NB03 one cell at a time, following its notes.

Cells headed **Page N** are copied exactly from the book. Cells starting with `# TEST SETUP` only create sample inputs.

### Logging problems

Open one issue per failing card:

- **Title:** `p27 – Z-order only recent partitions fails`
- **Body:** the notebook name, the error message and the Fabric runtime version
- **Label:** `code-fix`, `content-fix` or `layout`

### Board columns

**To test** → **Failing** → **Fixed in book** → **Verified**

### Done when

- [ ] NB01 and NB02 run end to end with no errors
- [ ] Every NB03 cell behaves as its note describes
- [ ] All fixes are copied into the book PDF
- [ ] Cover is finished
- [ ] Listing text is ready
- [ ] Uploaded to KDP and Gumroad
