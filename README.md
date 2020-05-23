# Routine Commands (NERSC)

- `module load esslurm`
- `module load pytorch/v1.4.0-gpu` [[updated]](https://docs.nersc.gov/analytics/machinelearning/pytorch/)
- `salloc -C gpu -N 1 --time 60 --ntasks 1 --gpus-per-task 1 --cpus-per-task 10` [[interactive jobs]](https://docs.nersc.gov/jobs/interactive/)[[examples]](https://docs.nersc.gov/jobs/examples/)
- `pip --user install ANYTHING`
- `srun python SCRIPT` 
- OR `srun --pty bash` [[prompt]](https://slurm.schedmd.com/faq.html#prompt)
- `ssh NODE`
- `srun nvidia-smi`

### No DDP SETUP
```
def main():
  ...

def train():
  ...
```
### DDP Setup
```
def main():
  ...
  [torch.multiprocessing.spawn(*args, **kwargs)](https://pytorch.org/docs/stable/multiprocessing.html#torch.multiprocessing.spawn)
  ...
 def train():
  ...
  [torch.distributed.init_process_group(*args, **kwargs)](https://pytorch.org/docs/stable/distributed.html#torch.distributed.init_process_group)
  ...
``` 
# PyTorch (DDP) 101

- [Training a Classifier : PyTorch](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html)
- [torchvision.datasets : default datasets of PyTorch](https://pytorch.org/docs/stable/torchvision/datasets.html)
- [torchvision.models : default models](https://pytorch.org/docs/stable/torchvision/models.html) 
- [Creating dataset class](https://stanford.edu/~shervine/blog/pytorch-how-to-generate-data-parallel)
- [Dataloader : torch.utils.data](https://pytorch.org/docs/stable/data.html)
- [Writing Custom Datasets, Dataloaders and Transforms](https://pytorch.org/tutorials/beginner/data_loading_tutorial.html)

# DDP

- [DDP101](https://yangkky.github.io/2019/07/08/distributed-pytorch-tutorial.html)
- [Getting Started with DDP](https://pytorch.org/tutorials/intermediate/ddp_tutorial.html)
- [DDP application with PyTorch](https://pytorch.org/tutorials/intermediate/dist_tuto.html)
- [DDP](https://pytorch.org/docs/master/notes/ddp.html)
- [PyTorch distributed trainer for AWS](https://pytorch.org/tutorials/beginner/aws_distributed_training_tutorial.html)
- [Do Detailed](http://www.telesens.co/2019/04/04/distributed-data-parallel-training-using-pytorch-on-aws/)
- [Apex](https://nvidia.github.io/apex/index.html)
- [torch.distributed](https://pytorch.org/docs/stable/distributed.html)

# Containers

- [Docker - Singularity - Shifter](https://tin6150.github.io/psg/blogger_container_hpc.html)
- [HPC School 2019](https://ulhpc-tutorials.readthedocs.io/en/latest/containers/singularity/slides.pdf)
- [Interesting...](https://www.stackhpc.com/the-state-of-hpc-containers.html)
