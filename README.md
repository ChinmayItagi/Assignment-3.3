Hadoop 2.x is improved version of 1.x with many aspects. Hadoop 1.x had the following drawbacks 
1) Name Node daemon can be max of 64 GB.
2) It only supports MR processing model and does not support non MR tools, this was overcome in 2.x and Hadoop 2.x supports Spark, Hama, Giraph, Message Passing Interface) MPI & HBase coprocessors.
3) Limited scaling of nodes. Limited to 4000 nodes per cluster.
4) It has a single name node to manage entire name space.
5) Also the Hadoop has single point of failure i.e. if name node fails then human intervention is needed. 
All the above points where addressed in the Hadoop 2.x with multiple name nodes each could form 4000 node cluster. It was called as the federation which scales out by many different name nodes.
Hadoop 2.x
Similar to the 1.x the HDFS of the Hadoop 2.x has Master daemon called as the name node and slave daemon as Data Node.
Also the Map reduce has master daemon as Resource Manager and slave daemon as Node Manager.
In Hadoop 2.x  YARN(Yet another Resource Manager) is the resource manager which was included to improve the functionality of the map reduce. It provides user with API’s which can used accesses the clusters but in reality the users do not directly use the YARN. They use the higher level API’s provided by higher distributing computing Frameworks e.g. SPARK.
In Hadoop 1.x the job tracker takes care of both job scheduling (matching tasks with task trackers) and task progress monitoring (keeping track of tasks, restarting failed or slow tasks, and doing task bookkeeping, such as maintaining counter totals). But in Hadoop 2.x YARN these responsibilities are handled by separate entities: the resource manager and an application master (one for each MapReduce job). The job tracker is also responsible for storing job history for completed jobs, although it is possible to run a job history server as a separate daemon to take the load off the job tracker.
