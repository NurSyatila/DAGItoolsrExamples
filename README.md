# DAGItoolsrExamples

This section describes results from DAGItoolsr package.<br>

## 1) GeneSearch Workflow<br>

> results <- genesearch_workflow(queryTerms,disgenet=TRUE,"youremail@gmail.com","yourpassword")<br>

Terminal capture:<br>
[1] "DisGeNET data will be included."<br>
[1] "Processing (ClinVar)..."<br>
[1] "Processing (MedGen)..."<br>
[1] "No results from MedGen."<br>
[1] "Processing (OMIM)..."<br>
[1] "No results from OMIM."<br>
[1] "Processing (GTR)..."<br>
[1] "No results from GTR."<br>
[1] "Processing (PheGenI)... "<br>
[1] "Processing (GWAS Catalog)... "<br>
[1] "Processing DISEASES (Text Mining category)..."<br>
[1] "Processing DISEASES (Knowledge category)..."<br>
[1] "Processing DISEASES (Experiments category)..."<br>
[1] "Processing (MESH)..."<br>
[1] "D004715"<br>
[1] "Processing (DisGeNET).."<br>
[1] "Perform PPI and functional enrichment analysis.."<br>
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current<br>
                                 Dload  Upload   Total   Spent    Left  Speed<br>
100 20.7M  100 20.7M    0     0  2280k      0  0:00:09  0:00:09 --:--:-- 3261k<br>
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current<br>
                                 Dload  Upload   Total   Spent    Left  Speed<br>
100 1857k  100 1857k    0     0  96080      0  0:00:19  0:00:19 --:--:--  420k<br>
[1] "Get PPI network.."<br>
Warning:  we couldn't map to STRING 1% of your identifiers  % Total    % Received % Xferd  Average Speed   Time <br>   Time     Time  Current<br>
                                 Dload  Upload   Total   Spent    Left  Speed<br>
100 69.3M  100 69.3M    0     0  4987k      0  0:00:14  0:00:14 --:--:-- 7706k<br>
[1] "Functional enrichment analysis.."<br>
[1] "** BP **"<br>
[1] "** MF **"<br>
[1] "** CC **"<br>
[1] "** KEGG **"<br>
[1] "pathview"<br>
[1] "** DO **"<br>
[1] "Get top 10/20 genes.."<br>
[1] "pathview"<br>
[1] "Get gene modules/clusters.."<br>
[1] "Get modules from clustering.."<br>
[1] "Get pathways for individual clusters.."<br>

## 2) Single Differential Expression Workflow<br>

queryTerms <- c("endometriosis","endometrioma")<br>
> GSEaccession <- "GSE23339"<br>
> GSEplatform <- "GPL6102"<br>
> results <- differentialexpression_single_workflow(queryTerms,GSEaccession,GSEplatform)<br>
<br>

Terminal Capture:<br>
 "GSE23339"<br>
[1] "group A:  disease state: endometrioma"<br>
[1] "group B:  disease state: control"<br>
[1] "Number of genes > 400. PPI analysis cannot be performed. Please use analyse_ppi_network(). Running enrichment analysis instead."<br>
[1] "** BP **"<br>
[1] "** MF **"<br>
[1] "** CC **"<br>
[1] "** KEGG **"<br>
[1] "pathview"<br>
[1] "** DO **"<br>
[1] "DO - No results"<br>
There were 30 warnings (use warnings() to see them)<br>
<br>
<br>

## 3) Differential Expression Workflow<br>

> queryTerms <- c("endometriosis","endometrioma")<br>
> results <- differentialexpression_workflow(queryTerms)<br>

Terminal capture:<br>
[1] "Processing (MESH)..."<br>
[1] "Endometriosis" "Endometrioses" "Endometrioma"  "Endometriomas"<br>
[1] "Processing (GEO DataSets)..."<br>
[1] "GSE25628"<br>
[1] "group A:  donor: patient"<br>
[1] "group B:  donor: healthy donor"<br>
[1] "GSE23339"<br>
[1] "group A:  disease state: endometrioma"<br>
[1] "group B:  disease state: control"<br>
[1] "GSE7846"<br>
[1] "group A:  endothelium from a patient with endometriosis"<br>
[1] "group B:  endothelium from normal control"<br>
[1] "GSE6364"<br>
[1] "group A:  Proliferative Phase Normal | Early Secretory Phase Normal | Mid Secretory Phase Normal"<br>
[1] "group B:  Proliferative Phase Endometriosis | Early Secretory Phase Endometriosis | Mid Secretory Phase Endometriosis"<br>
[1] "GSE7305"<br>
[1] "group A:  Endometrium-Normal 1 | Endometrium-Normal 2 | Endometrium-Normal 3 | Endometrium-Normal 4 | Endometrium-Normal 5 | Endometrium-Normal 6 | Endometrium-Normal 7 | Endometrium-Normal 8 | Endometrium-Normal 9 | Endometrium-Normal 10"<br>
[1] "group B:  Endometrium/Ovary-Disease 1 | Endometrium/Ovary-Disease 2 | Endometrium/Ovary-Disease 3 | Endometrium/Ovary-Disease 4 | Endometrium/Ovary-Disease 5 | Endometrium/Ovary-Disease 6 | Endometrium/Ovary-Disease 7 | Endometrium/Ovary-Disease 8 | Endometrium/Ovary-Disease 9 | Endometrium/Ovary-Disease 10"<br>
[1] "GSE5108"<br>
[1] "group A:  Human, female, of reproductive age, severe endometriosis, endometrioma | Human, female, of reproductive age, moderate endometriosis, endometrioma | Human, female, of reproductive age, severe endometriosis | Human, female, of reproductive age, mild endometriosis | Human, female, of reproductive age, severe endometriosis, peritoneal endometriosis | Human, female, of reproductive age, minimal endometriosis, peritoneal endometriosis | Human, female, of reproductive age, mild endometriosis, peritoneal endometriosis"<br>
[1] "group B:  Human, female, of reproductive age, endometrial biopsy of eutopic endometrium, late proliferative phase | Human, female, of reproductive age, endometrial biopsy of eutopic endometrium, proliferative phase | Human, female, of reproductive age, endometrial biopsy of eutopic endometrium, early secretory phase | Human, female, of reproductive age, endometrial biopsy of eutopic endometrium,"<br>
[1] "Error: Unable to create heatmap."<br>
[1] "Number of genes > 400. PPI analysis cannot be performed. Please use analyse_ppi_network(). Running enrichment analysis instead."<br>
[1] "** BP **"<br>
[1] "** MF **"<br>
[1] "** CC **"<br>
[1] "** KEGG **"<br>
[1] "pathview"<br>
[1] "** DO **"<br>
Warning messages:<br>
1: ggrepel: 5644 unlabeled data points (too many overlaps). Consider increasing max.overlaps<br>
2: ggrepel: 4297 unlabeled data points (too many overlaps). Consider increasing max.overlaps<br>
3: ggrepel: 5822 unlabeled data points (too many overlaps). Consider increasing max.overlaps<br>
4: ggrepel: 527 unlabeled data points (too many overlaps). Consider increasing max.overlaps<br>
5: In data(bods) : data set 'bods' not found<br>
6: In data(bods) : data set 'bods' not found<br>
7: In data(bods) : data set 'bods' not found<br>
8: In data(bods) : data set 'bods' not found<br>
9: In data(bods) : data set 'bods' not found<br>
10: ggrepel: 2728 unlabeled data points (too many overlaps). Consider increasing max.overlaps<br>

Note that the sample groupings for GSE5108 are not correctly assigned. Please double check the sample groupings in the terminal output and update a new set of genes. The following command can be used to perform PPI analysis or functional enrichment.<br><br>

genefile <- "newgenes.txt"<br>
geneList <- readLines(genefile)<br>
#for PPI analysis and functional enrichment (number genes < 400 due to limitation from STRINGdb package)<br>
results <- analyse_ppi_network(geneList)<br>
#for functional enrichment<br>
ORAterm <- "KEGG" # or "BP","CC","MF","DO"<br>
results <- get_enrichment_results(geneList,ORAterm,"ORA") #ORA for over-representation analysis<br>


