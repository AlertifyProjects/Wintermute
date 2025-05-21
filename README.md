# Wintermute

Hardware Overview (Beginning 20/05/2025...)

Oscar (172.16.23.40/24):
CPU: Intel i5-7300HQ (4 cores, 2.5GHz)
RAM: 16GB
Storage: 100GB (HDD or SSD?)
GPU: NVIDIA GTX 1050 Ti Mobile (4GB VRAM, CUDA-capable)
Role: Primary compute node, leveraging the GPU for ML tasks.
Sparkles (172.16.23.41/24):
CPU: AMD A4-6300 (2 cores, ~3.7GHz)
RAM: 4GB (very limited)
Storage: 100GB (HDD or SSD?)
GPU: Integrated Radeon HD Graphics (not CUDA-capable, limited ML utility)
Role: Secondary node, likely for data preprocessing or lightweight tasks due to low RAM.
Constraints:

Oscar is well-suited for small-scale ML tasks, especially with the GTX 1050 Ti for GPU acceleration.
Sparkles is underpowered (4GB RAM is a bottleneck for most ML tasks), so it’s best used for auxiliary tasks (e.g., data pipeline, monitoring) until you add more RAM or hardware.
Clustering: Both machines can form a basic cluster, but Sparkles’ limited RAM may restrict its role in distributed training until upgraded.
Goal for Phase 1: Set up a basic cluster with Oscar as the primary ML node and Sparkles as a support node, install ML frameworks, and run a small test model (e.g., GPT-2 small) to validate the setup.
