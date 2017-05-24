# ELDOgraph - External Least Divergent Ortholog graph


## Introduction:

	ELDOgraph is a tool for comparative genomics analysis that 
	assesses the species relationship considering the phylogenetic 
	distance provided by several gene trees. 


## Prerequisites:

	Unix Platform;
	PERL;
	Internet connection;


## For impatients:

	> tar -zxvf ELDOgraph_vXXX.tgz
	> cd eldograph
	> ./eldograph_db -treedir <tree_directory> -taxtable <table_name> 
	> ./eldograph_analayse -hashfile <hash_file> -rank <rank_code> 

For detailed description of ELDOgraph parameters:

	> ./eldograph_db -man
	> ./eldograph_analyse -man

	
## Installation:

	ELDOgraph is ready to use  in  most  of  Unix  Platform.  But  it  only 
	works if the  folders  lib/  that follow this script are  in  the  same 
	location. If you want to freely run ELDOgraph  in  other  location, add  
	the ELDOgraph folder  into  the  environment  variable  by  using,  for 
	example, the following commands:
	
	> echo "export PATH=$PATH:/path/to/program/eldograph/" >> ~/.bash_profile
	> source ~/.bash_profile

	
## Running with sample files:

	In the eldograph directory try the following commands
	> ./eldograph_db -treedir sample_trees/ -taxtable sample_tax.tab -out sample_db.hash
	> ./eldograph_analayse -hashfile sample_db.hash -rank genus -out sample_result


## Outputs:

	eldograph_db: a hash file containing the taxonomic and distance information.
	
	eldograph_analyse:
      *.html:       a web page in which the results can be visualized in a graph
                    structure.
      *.matrix.tab: a matrix containing the frequency of ELDO of a taxon with all 
                    other taxon in the analysis
      *.tab:        same data as *.matrix.tab, but in 3-column-table.
	
