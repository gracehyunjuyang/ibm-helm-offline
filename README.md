# ibm-helm-offline
Offline helm charts for IBM catalog

## Load packaged images
1. Login to Boot Node
```
sudo docker login mycluster.icp:8500
```
2. Load the archive package into the IBM Cloud Private private registry
```
tar xf ICP-CE-2.1.0.3.tar.gz -O | docker load
```
3. Execute the tagAndUpload.sh file against the DockerTags.txt
```
chmod +x tagAndUpload.sh
sudo ./tagAndUpload.sh DockerTags.txt
```


## Load Helm charts
 in ibm-helm-offline
```
chmod +x loadHelmCharts.sh
sudo ./loadHelmCharts.sh
```
