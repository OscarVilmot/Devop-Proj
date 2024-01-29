# Devop-Proj

## Prerequisite

Kubernetes installed and configured on your machine(s).

## How to use

```bash
git clone https://github.com/pasarcoscar/Devop-Proj
cd Devop-Proj
bash build_image.sh
```

## Important notes

The following script is written for microk8s specifically, if you are using anything else please edit the script accordingly.

## Bash script steps

#### Installation of harbor

Harbor is a local docker reposority that allows you to build, push and retrieve your personalized images.

#### Microk8s specific steps

If microk8s is installed the script will add the harbor server in the "trusted" repositories (allows insecure/HTTP connections) and then restarts it.

#### Image building

The script will build the image and push it to the harbor repository.

#### Deployment

Finally, the script will apply the steps described in the k8s.yaml file

