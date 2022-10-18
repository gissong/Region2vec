# Region2vec

Region2vec: Community Detection on Spatial Networks Using Graph Embedding with Node Attributes and Spatial Interactions

![Region2vec](https://github.com/GeoDS/Region2vec/blob/master/Region2Vec_Workflow.jpg)

Abstract: 
Community Detection algorithms are used to detect densely connected components in complex networks and reveal underlying relationships among components. As a special type of networks, spatial networks are usually generated by the connections among geographic regions. Identifying the spatial network communities can help reveal the spatial interaction patterns, understand the hidden regional structures and support regional development decision-making. Given the recent development of Graph Convolutional Networks (GCN) and its powerful performance in identifying multi-scale spatial interactions, we proposed an unsupervised GCN-based community detection method "region2vec" on spatial networks. Our method first generates node embeddings for regions that share common attributes and have intense spatial interactions, and then applies clustering algorithms to detect communities based on their embedding similarity and spatial adjacency. Experimental results show that while existing methods trade off either attribute similarities or spatial interactions for one another, "region2vec" maintains a great balance between both and performs the best when one wants to maximize both attribute similarities and spatial interactions within communities.


## Paper

If you find our code useful for your research, you may cite our paper:

*Liang, Y., Zhu, J., Ye, W., and Gao, S.\. (2022). [Region2vec: Community Detection on Spatial Networks Using Graph Embedding with Node Attributes and Spatial Interactions] (https://arxiv.org/abs/2210.08041). In Proceedings of 30th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems
(ACM SIGSPATIAL 2022), November 1-4, 2022, Seattle, WA, USA. DOI: https://doi.org/10.1145/3557915.3560974* 


```
@article{rao2021privacy,
  title={A privacy-preserving framework for location recommendation using decentralized collaborative machine learning},
  author={Rao, Jinmeng and Gao, Song and Li, Mingxiao and Huang, Qunying},
  journal={Transactions in GIS},
  volume={25},
  number={3},
  pages={1153--1175},
  year={2021},
  publisher={Wiley Online Library}
}
```

## Requirements

Region2 uses the following packages with Python 3.7

numpy==1.19.5

pandas==0.24.1

scikit_learn==1.1.2

scipy==1.3.1

torch==1.4.0



## Usage

1. run train.py to generate the embeddings.
```
python train.py
```
2. run clustering.py to generate the clustering result. 

```
python clustering.py --filename your_filename
```
Here the 'your_filename' should be replaced with the generated file from step 1.

3. Alternatively, to generate the clustering for all the files, please use bash, and run bash run_clustering.py.

```
bash run_clustering.sh 
```
Notes: the final results may vary depends on different platform and package versions.
The current result is obtained using Ubuntu with all pacakge versions in requirements.txt. 
