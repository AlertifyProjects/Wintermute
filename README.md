# Wintermute
## ~ Clustered ML training project ~

## Hardware Overview (Beginning 20/05/2025...)

### Oscar (172.16.23.40/24):
CPU: Intel i5-7300HQ (4 cores, 2.5GHz)<br>
RAM: 16GB<br>
Storage: 100GB (HDD or SSD?)<br>
GPU: NVIDIA GTX 1050 Ti Mobile (4GB VRAM, CUDA-capable)<br>
Role: Primary compute node, leveraging the GPU for ML tasks.<br>

### Sparkles (172.16.23.41/24):
CPU: AMD A4-6300 (2 cores, ~3.7GHz)<br>
RAM: 4GB (very limited)<br>
Storage: 100GB (HDD or SSD?)<br>
GPU: Integrated Radeon HD Graphics (not CUDA-capable, limited ML utility)<br>
Role: Secondary node, likely for data preprocessing or lightweight tasks due to low RAM.<br>


#### Constraints:

Oscar is well-suited for small-scale ML tasks, especially with the GTX 1050 Ti for GPU acceleration.<br>
Sparkles is underpowered (4GB RAM is a bottleneck for most ML tasks), so it’s best used for auxiliary tasks (e.g., data pipeline, monitoring) until you add more RAM or hardware.<br>
Clustering: Both machines can form a basic cluster, but Sparkles’ limited RAM may restrict its role in distributed training until upgraded.<br>
Goal for Phase 1: Set up a basic cluster with Oscar as the primary ML node and Sparkles as a support node, install ML frameworks, and run a small test model (e.g., GPT-2 small) to validate the setup.<br>

## ...22/5/25 - Gathered additional hardware<br>

### Dixie (172.16.23.42/24):
CPU: 2x Xeon E5-2699 v3 (18 cores each, Base: 2.3 GHz, Max: 3.6 GHz)<br>
RAM: 256GB - 8x 32GB PC4-2133P<br>
Storage: 2x 900GB 10K SAS HDD<br>
GPU_1: NVIDIA Quadro P5000 (16GB VRAM, CUDA-capable)<br>
GPU_2: NVIDIA Quadro M6000 (24GB VRAM, CUDA-capable)<br>
PSU: 2x500W

