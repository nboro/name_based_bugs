# Name-based bugs detection
This project was made as part of my Master thesis for the MSc program *Data Science and Entrepreneurship*.

In the folder **1_find_and_merge_repositories** I present the way I collected the data. This included Ansible repositories detection, bug-related commits extraction and repository selection based on the research criteria.

In the folder **2_find tasks** I implement a heuristic mechanism in order to identify and extract Ansible tasks from a repository. 

In the folder **3_map_tasks_to_ansible_documentation** I introduce a mechanism which identifies the used module within an Ansible task by scraping information from the Ansible documentation website. In addition, the mechanism identifies the used parameters of each module based in the same fashion.

In the folder **build_ast_tokenizen** I implement an AST generator engine in order to create a token sequence from Ansible task bodies.  

In the folder **5_rq3_identify_name_method_inconsistency** I answer the 3rd research question of my research by including information about how I perform text transformations in order to create incosistent examples of Ansible tasks. Next, I build two classifiers in order to be able to detect name-based bugs:
1. The first classifier leverages Doc2Vec for the inconsistency detection.
2. The second classifier trains a Word2Vec model and embedds the correspondind vector representations in a CNN in order to detect inconsistency between Ansible task names and task bodies

In the folder **rq1 - topic modeling task names**  I answer the 1st research question of my research by performing topic modeling on the Ansible task names in order to identify common Ansible insfrastructure usages.

In the folder **rq2 - topic modeling commit messsages**  I answer the 2nd research question of my research by performing topic modeling on the extracted bug-related commit messages in order to identify common bug issues in Ansible.

All used datasets are located within the corresponding folders. Datasets are consideredd all files with extension ***.pkl***. For rq2 the dataset is within the file ***commits_from_merged_repos.xlsx***. 

For the raw repository data contact [nborovits@gmail.com](nborovits@gmail.com).



