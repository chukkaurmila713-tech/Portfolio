# Personal Portofolio website Development on AWS via Docker
A containerized static personal portofolio website deployed on an **AWS EC2(Ubuntu)** cloud instance utilizing **Docker** for seamless application delivery
## Tech Stack & Architecture
* Cloud provider: Amazon Web Services(AWS)
* Compute Instance: EC2 Virtual Server (Ubuntu 26.04 LTS)
* Containerization: Docker Engine
* Web Architecture: HTML5,CSS3,Static Assets
* Version Control: Github
## Setup
* Github Setup: Pushed index.file,style.css and Dockerfile to the rpository
* Launched EC2 and opened port 80 for web traffic.
* Cloned the repo on the server and built the Docker image:bash
  sudo docker build -t portfolio-web
sudo docker run -d -p 80:80 --name my-portfolio portfolio-web


### Task 3: CI/CD Automation Pipeline 
An automated Continuous Integratin(CI) pipeline has been implemented using **GitHub Actions**.

### How it works:
- **Trigger:** Every time code changes are committed and pushed to the 'main' branch,the workflow automatically runs.
- **Environment:** The pipeline spins up an isolated 'ubuntu-latest' virtual runner.
- **Authencation:** It securely logs into Docker Hub using a Personal Access Token stored in GitHub Secrets.'DOCKER_PASSWORD'.
- **Build & Deliver:** It builds the updated Docker container image from the project's local 'Dockerfile' and automatically pushes the tagged image 'latest' straight to my public Docker Hub repository.
