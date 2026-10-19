Fabric Spark on One Page - companion notebooks

1. In a TEST Fabric workspace, create (or pick) a test lakehouse.
2. Import all 7 notebooks: Workspace > Import > Notebook > From this computer.
   Keep the names exactly as they are (the notebooks call each other by name).
3. Open each NB0x notebook and attach the test lakehouse as its default lakehouse
   (nb_silver, nb_dim_customer and nb_dim_product need it too).
4. Run NB01_Part1_Essentials, then NB02_Part2_Spark_Performance (Run all).
   Each one runs NB00_Setup_Sample_Data first to (re)create the sample data.
5. Run NB03_Session_Cells one cell at a time, following its notes.

Cells headed "Page N" are copied exactly from the book.
Cells starting "# TEST SETUP" are not in the book; they create inputs for the next card.
If a cell fails, note the page number and the error, then use "Run cells below".

WARNING: NB00 overwrites the sample tables and Files/ folders listed at its top.
Use a test lakehouse, never production.
