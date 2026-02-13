Versioning is the practice of replicating the code base so that several people can work on it at the same time. Versioning is especially difficult for machine learning because you are not only updating the code but also the database and model daily.

Here is a list of data versioning tools:




| Tool                        | License     | Notes                                                                                                                                                       |
| --------------------------- | ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| IBM Watson ML               | Proprietary | Focused on model versioning                                                                                                                                 |
| DVC                         | Open-source | Popular lightweight open-source tool focused on data, model and pipeline versioning. Can be easily integrated with CML.                                     |
| Pachyderm                   | Open-source | Data platform built on Docker and Kubernetes. Focused on Version Control and automating workloads with parallelization.                                     |
| MLflow                      | Open-source | Popular tool for many parts of the Machine Learning lifecycle, including versioning of processes and experiments. Can be easily integrated with other tools |
| Git LFS (Large File System) | Open-source | Git extension that permits large files on Git repositories. Can be used to share large data files and models, using Git versioning.                         |
[^1]


[^1]: https://mlops-guide.github.io/MLOps/Data/