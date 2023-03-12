
# Quicklab
Quickly create/destroy (multiple) vms on vmware vcenter

## Motivation
I wanted something to quickly create and destroy vms to make labs. I tried to use tools like Terraform but those did not work due to me not having enough permissions which led me to create this tool which can work with minimal permissions.

## Features
* Define Vms in a yaml file (see lab1.yaml)
* Create and destroy multiple vms
* Autostart vms after creation if desired
* Output a json file containing the vm names and their id to use with other tooling (see lab1.json)

## Installing
Clone the repo and move quicklab to your desired script folder
```bash
git clone https://github.com/misthios/quicklab.git && cd quicklab
mv ./quicklab /usr/local/bin
chmod +x /usr/local/bin/quicklab
```
## Usage
```bash
quicklab -s https://domain.tld -f lab.<json/yaml> -m <create/destory> -u username \
    <-d> <-i>
```
