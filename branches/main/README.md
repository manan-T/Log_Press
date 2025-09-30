# LogPress: Optimized Compression and Retrieval of Unstructured Logs.

## Dependencies

### macOS(Homebrew)
```bash
brew install go@1.22 gcc musl pkg-config sqlite curl zlib docker docker-compose
brew link go@1.22 --overwrite --force
```
### Ubuntu
```bash
sudo apt-get update
sudo apt-get install build-essential musl-tools pkg-config libsqlite3-dev zlib1g-dev libcurl4-openssl-dev docker-ce curl
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
wget https://go.dev/dl/go1.22.0.linux-amd64.tar.gz
sudo tar -C /usr/local -xvzf go1.22.0.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
```


## Dataset
For all testing all the approaches you will need datasets. We have used datasets from [Loghub](https://github.com/logpai/loghub) and [Zenodo](https://zenodo.org/). The datasets we have used in Results/Evaluation are:
| Dataset | Compressed/Download Size | Uncompressed/Original Size |
|---------|--------------------------|-------------------|
| [Mac](https://zenodo.org/records/8196385/files/Mac.tar.gz?download=1) | 1.5 MB | 16.9 MB |
| [OpenSSH](https://zenodo.org/records/8196385/files/SSH.tar.gz?download=1) | 4.6 MB | 70.02 MB |
| [Android_v1](https://zenodo.org/records/8196385/files/Android_v1.zip?download=1) | 24.9 MB | 183.37 MB |
| [HDFS_v1](https://zenodo.org/records/8196385/files/HDFS_v1.zip?download=1) | 186.6 MB | 1.47 GB |
| [Hive](https://zenodo.org/records/7094921) | 128.5 MB | 2.13 GB |
| [Spark](https://zenodo.org/records/8196385/files/Spark.tar.gz?download=1) | 183.5 MB | 2.75 GB |
