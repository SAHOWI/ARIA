# Software Stack for ARIA

## Operating System

Right from the beginning it ws clear to me, that the operating system should be LINUX as I wanted full controll with no extra costs.
As I wanted to use the same machine also for interactive tasks I decided for CachyOS.

CachyOS is checking in the background automatically and informs the user accordingly - but only in the Desktop.
As I quite often ust work remotely on the console of the machine, I do update all manually at least once in a week by
```bash
sudo pacman -Syu
```

To make sure all necessary drivers are installed.
CachyOS should recognize the NVIDIA card during the installation already - but in my case I added the card after the basic installation, I had to install the NVIDIA drivers manually.

In addition I made sure that the CUDA support is installed.

```bash
sudo pacman -S cuda cudnn
``` 

## OLAMA
OLAMA manages the local model and provides the necessary API to other system (e.g. OpenClaw)

## The LLM Model
Will be managed by OLAMA
Need to be capable to run on RTX3050 with 6GB of VRAM and Intel i7-7700-T/64GB RAM. (see: Hardware)

## Installation of Ollama and Gemma

```bash
# install ollama
curl -fsSL https://ollama.com/install.sh | sh

# pull gemma4:26b
ollama pull gemma4:26b


```

### Options

#### QWEN

#### GEMMA-4

Run OpenClaw in a local Container.

Run Olama/QWEN as local LLM.





## OpenClaw

To separatate OpenClaw from the rest of the machine, I decided to run it in a container.

Clone the official OpenClaw Repo:
```bash
git clone https://github.com/openclaw/openclaw.git
```
Install Dockers buildx tool, if not already available on your machine:
```bash
sudo pacman -S docker-buildx
```

Install OpenClaw into a Docker Image
```bash
sudo ./docker-setup.sh
```







