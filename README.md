# Class Activation Mapping
Use this repository to train and visualize class activation maps on any [Pytorch](pytorch.org) model.

![sample car obj](https://raw.githubusercontent.com/vaibhavnayel/CAM/master/CAM.png)

## Method

We calculate the chamfer distance between 2 sampled meshes and backpropagate through it to morph a template mesh into the target. Edge length regularization is used to improve smoothness.

```python
optimizer = torch.optim.Adam([m1.vertices],lr=0.01)

for i in range(epochs):

    optimizer.zero_grad()
    loss=chamfer_distance(m1,m2) + edge_length(m1)
    loss.backward()
    optimizer.step()

```
## Usage
1. Download dependencies: `kaolin`, `pytorch`, `tqdm`, `numpy`, `plotly`
2. Open the jupyter notebook  `tutorial.ipynb` and run all cells. Change path in the `get_model` function to load your own mesh.
