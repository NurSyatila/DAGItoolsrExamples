# DAGItoolsrExamples

This section describes results from DAGItoolsr package.

1) GeneSearch Workflow
2) Single Differential Expression Workflow

queryTerms <- c("endometriosis","endometrioma")<br>
> GSEaccession <- "GSE23339"<br>
> GSEplatform <- "GPL6102"<br>
> results <- differentialexpression_single_workflow(queryTerms,GSEaccession,GSEplatform)<br>
<br>
Terminal Capture:
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
3) Differential Expression Workflow
