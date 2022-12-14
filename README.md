# PFP_LZ77_Benchamrk_Scripts
Benchmark scripts for following LZ77 computing methods: PFP_LZ77[1], KKP1[2], KKP2[2], KKP3[2], semi-external KKP (SE-KKP)[3], EM_LPF[3] and ReLZ[4]. Test data set is copies of human chromosome 19[5].

# Example
###Download

```console
git clone https://github.com/AaronHong1024/PFP_LZ77_Benchmark_Scripts.git
``` 

### Run

```console
cd PFP_LZ77_ParsingExperiments
snakemake --cluster "sbatch -A {cluster.account} -q {cluster.qos} -c {cluster.cpus-per-task} -N {cluster.Nodes}  -t {cluster.runtime} --mem {cluster.mem} -J {cluster.jobname} --mail-type={cluster.mail_type} --mail-user={cluster.mail} --cluster-constraint {cluster.node}" --cluster-config cluster.json --jobs 100 --latency-wait 120
``` 


# External resources

*[PFP_LZ77](https://github.com/AaronHong1024/PFP_LZ77.git)
*[KKP](https://www.cs.helsinki.fi/group/pads/lz77.html)
*[SE-KKP](https://www.cs.helsinki.fi/group/pads/em_lz77.html)
*[EM_LPF](https://www.cs.helsinki.fi/group/pads/em_lz77.html)
*[ReLZ](https://gitlab.com/dvalenzu/ReLZ)

# References

[1] XXX

[2] Juha Kärkkäinen, Dominik Kempa, Simon J. Puglisi. Linear Time Lempel-Ziv Factorization: Simple, Fast, Small. In Proc. 24th Symposium on Combinatorial Pattern Matching (CPM 2013), Springer, 2013, pp. 189-200.

[3] Juha Kärkkäinen, Dominik Kempa, Simon J. Puglisi. Lempel-Ziv Parsing in External Memory. In Proc. 2014 Data Compression Conference (DCC 2014), IEEE Computer Society, 2014, pp. 153-162.

[4] D. Kosolobov, D. Valenzuela, G. Navarro, and S. J. Puglisi. Lempel–Ziv-Like Parsing in Small Space. Algorithmica, 82(11):3195–3215, 2020.

[5] The 1000 Genomes Project Consortium. A global reference for human genetic variation. Nature, 526:68–74, 2015.
