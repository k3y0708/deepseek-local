# DeepSeek R1 Local

Run DeepSeek R1 Locally with One Command!

![DeepSeek Logo](https://platform.theverge.com/wp-content/uploads/sites/2/chorus/uploads/chorus_asset/file/25848982/STKB320_DEEPSEEK_AI_CVIRGINIA_A.jpg?quality=90&strip=all&crop=0%2C0%2C100%2C100&w=1440)

## Getting Started

Clone the repository.

`git clone git@github.com:mischavandenburg/deepseek-local.git`

Enter the directory.

`cd deepseek-local`

Start the application (using CPU):

`docker-compose --profile cpu up`

Access the application by opening your browser and entering:

`http://localhost:8080`

## Using GPU

You will need to [upgrade your Container Runtime](https://docs.nvidia.com/dgx/nvidia-container-runtime-upgrade/) to enable CUDA.

`docker-compose --profile gpu-nvidia up`

## Cleaning up

Remove all containers & volumes (CPU)

`docker compose --profile cpu down --volumes --remove-orphans`

Remove all containers & volumes (GPU)

`docker compose --profile gpu-nvidia down --volumes --remove-orphans`
