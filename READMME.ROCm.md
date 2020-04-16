# requirement
1.use the specified file in pytorch extension
https://github.com/HCYXAS/pytorch/blob/master/torch/utils/cpp_extension.py

# Install Horovod-hip-x
1. download sourcecode
git clone -b hip-x --recursive https://github.com/HCYXAS/horovod/tree/hip-x

2. install pytorch-horovod
CC=hcc HOROVOD_GPU_ALLREDUCE=NCCL HOROVOD_GPU_BROADCAST=NCCL ROCM_HOME=/opt/rocm HOROVOD_GPU=ROCM HOROVOD_WITHOUT_GLOO=1 \
HOROVOD_GPU=ROCM HOROVOD_WITHOUT_MXNET=1 HOROVOD_WITH_PYTORCH=1 HOROVOD_WITHOUT_TENSORFLOW=1 python3 setup.py install

3.install tensorflow-horovod

