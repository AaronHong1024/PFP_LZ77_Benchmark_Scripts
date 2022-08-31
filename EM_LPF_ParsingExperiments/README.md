# Running the analysis with Snakemake

``` bash
snakemake --cluster "sbatch -A {cluster.account} -q {cluster.qos} -c {cluster.cpus-per-task} -N {cluster.Nodes}  -t {cluster.runtime} --mem {cluster.mem} -J {cluster.jobname} --mail-type={cluster.mail_type} --mail-user={cluster.mail} --cluster-constraint {cluster.node}" --cluster-config cluster.json --jobs 1 --latency-wait 120
```
