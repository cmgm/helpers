

#  CGP


https://cloud.google.com/free/docs/free-cloud-features#free-tier-usage-limits

## proj 
project GMAPSAPI  gmapsapi-1488981423944

## VM 
us-central1-a \
e2-micro,  1G  \
20 G  , standard persistent disk \
API and identity management  \
    Storag - Full 

## GCS
```

sudo apt-get update

# get github keys from GCS
gsutil cp gs://gmapsapi-1488981423944/id_ed25519.pub  .
gsutil cp gs://gmapsapi-1488981423944/id_ed25519 .

cd ./ssh
chmod 600 id_ed25519.pub 
chmod 600 id_ed25519 
ll

eval "$(ssh-agent -s)" 
ssh-add ~/.ssh/id_ed25519 

# install docker 
sudo apt  install docker.io

Add user to docker group  , to  run docker whitout  sudo 
# sudo groupadd docker
sudo usermod -aG docker ${USER}
newgrp docker


mkdir apps

cd apps

git clone gi

```

## Firewall

NOS  - 194.79.86.9

80,15672,8501,8888,8889,9090,9091,9092,6603


# several 

gcloud auth list

gcloud config set account `ACCOUNT`

gcloud config list project


# TERRAFORM ------------------

terraform

touch instance.tf

cat <<EOF > instance.tf
resource "google_compute_instance" "terraform" {
  project      = "gmapsapi-1488981423944"
  name         = "vm1"
  machine_type = "e2-micro"
  zone         = "us-central1-a"
  boot_disk {
    initialize_params {
      image = "ubuntu-os-cloud/ubuntu-2024-lts"
    }
  }
  network_interface {
    network = "default"
    access_config {
    }
  }
}
EOF



terraform init
terraform plan
terraform apply



gcloud compute disks list


## from gcpinfo 
https://cloud.google.com/docs/terraform/basic-commands
git clone https://github.com/GoogleCloudPlatform/terraform-docs-samples.git


https://github.com/terraform-google-modules/terraform-docs-samples/tree/main



export GOOGLE_CLOUD_PROJECT=gmapsapi-1488981423944
mkdir terra && cd terra && touch main.tf

terraform init
terraform init -upgrade
terraform plan
terraform apply

terraform fmt
terraform validate
terraform destroy
