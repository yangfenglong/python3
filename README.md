
### csnet
```python
SSN.csnet(self, cells=None, alpha=0.01, boxsize=0.1, edgeW=0, to_csv=0, *args, **kwargs)
```
Construct the CSN for sepecified cells

Parameters:

    `cells`   Construct the CSNs for all cells, set cells = None (Default) otherwise input cells.list
    `alpha`   Significant level (eg. 0.001, 0.01, 0.05 ...)
              larger alpha leads to more edges, Default = 0.01
    `boxsize` Size of neighborhood, Default = 0.1
    `edgeW`   1  edge is weighted (statistic pxy(x))
              0  edge is not weighted (Default)
    `nodeW`   1  node is weighted (gene or otu abundance)
              0  node is not wieghted (Default)
    `csn`     Cell-specific network, the kth CSN is in csn{k}
              rows = genes, columns = genes

Returns:

    cells in list format

Parameters:

    `data`     Gene expression matrix (TPM/RPKM/FPKM/count), rows = genes, columns = cells. otu_even.table
    `alpha`    Significant level (eg. 0.001, 0.01, 0.05 ...), Default = 0.01
    `boxsize`  Size of neighborhood, Default = 0.1 (nx(k) = ny(k) = 0.1*n)
    `normalize`1  result is normalized (Default);
               0  result is not normalized

Note:

    If gene expression matrix is sparse, use the sparse matrix will accelerate the calculation and reduce memory footprint
