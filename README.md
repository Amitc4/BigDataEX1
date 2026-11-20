# BigData EX1

Name: Amit Chen.

default run - first run:

launched map tasks - 9

launched reduce tasks - 3

merged map outputs - 27


after adding -numReduceTasks 6:

launched map tasks - 16

launched reduce tasks - 6

merged map outputs - 54


Q1: there are 6 files

Q2: the number of mapper changed from 9 to 16

Q3: the number of reducer changed from 3 to 6

Q4: the number of files changed from 3 to 6. each reducer tasks writes its own seperate file, in the first run the default reducer tasks was 3 so there were 3 files in the partition and because we changed it to 6 the number of files in the partition changed to 6 as well.

Q5: Merged Map outputs represents the total number of intermediate map output segments (partitions) that were fetched by all Reducer tasks and merged (sorted together) before being passed into the reduce function.
During the Shuffle and Sort phase, every Reducer task must fetch its assigned partition from every Map task and merge those outputs into a single sorted input stream.

PART 2:
The change is in the mapper
the code is in the repository in mapper.py

PART 3:
The change is in the reducer
the code is in the repository in reducer.py

The output of the MapReduce after applying the changes to only display the top 3:

the     74369

and     42768

of      34588

<img width="1118" height="584" alt="image" src="https://github.com/user-attachments/assets/ce7f221f-35c7-430e-941e-ec489a44971c" />


