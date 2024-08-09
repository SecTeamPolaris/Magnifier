# Network Access Detector

The project is written in Pytorch using the following backend: Intel i7-9750 @2.6GHz, 16GB RAM, NVIDIA GeForce RTX2060; Windows 10, CUDA 10.1, and PyTorch 1.0.1.

## data

Folder data includes npy files that have been preprocessed from raw NetCess2023, only for validation.

## NetCess2023

To assess the effectiveness of Magnifier, we meticulously curated a dataset known as NetCess2023. This dataset comprises network access traffic from 26 distinct types of mobile devices representing 7 different brands. We encompass 4 real-world scenarios, encompassing three network access scenarios and one background traffic scenario.

As depicted, the traffic is captured at various network locations. In ScenarioA, we deploy a sniffer on a local router, allowing us to capture the pure traffic of network access as soon as a device joins the network. Notably, the traffic in ScenarioA exclusively involves the access behavior of the target devices. Consequently, ScenarioA serves both for Magnifier's fingerprinting and as the training set for the baseline models.

In ScenarioB, ScenarioC, and ScenarioD, we capture traffic at one of the backbone gateways within our campus network. ScenarioB encompasses the traffic associated with the initial network access, which includes the complete network access traffic. In contrast, ScenarioC captures repetitive network traffic, including only partial traffic from each network access, primarily due to the DNS cache in the local routers. It's important to note that background traffic is mixed in both ScenarioB and ScenarioC.

In ScenarioD, we capture traffic that does not contain any network access behaviors from the included mobile devices.

This dataset comprises approximately 10GB of network traffic, encompassing a broad spectrum of mainstream mobile device brands, including Apple (5 models), Huawei (5 models), Samsung (2 models), Xiaomi (5 models), Vivo (5 models), Oppo (3 models), and Coolpad (1 model).


<div align=center><img src="https://github.com/user-attachments/assets/dd92ac68-190d-41fa-b6f7-cf9c16c9561d" width="50%" height="50%"></div>

