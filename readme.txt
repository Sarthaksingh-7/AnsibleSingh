this is node server 

username: Sarthakuser

private key is in the repo

here are virtual machine details that is deployed machine  

Operating system:Linux (ubuntu 20.04)

Size:Standard D2s v3 (2 vcpus, 8 GiB memory)

Public IP address:104.46.97.254

Virtual network/subnet:Ansiblelab-RG-vnet/default

JSON view
{
    "name": "Nodevmubuntu",
    "id": "/subscriptions/aa1d9d6b-9e96-41b7-91b3-012dc82be976/resourceGroups/Ansiblelab-RG/providers/Microsoft.Compute/virtualMachines/Nodevmubuntu",
    "type": "Microsoft.Compute/virtualMachines",
    "location": "eastus2",
    "properties": {
        "vmId": "a3ef1e9f-5d44-44aa-afc0-d3636a686188",
        "hardwareProfile": {
            "vmSize": "Standard_D2s_v3"
        },
        "storageProfile": {
            "imageReference": {
                "publisher": "canonical",
                "offer": "0001-com-ubuntu-server-focal",
                "sku": "20_04-lts",
                "version": "latest"
            },
            "osDisk": {
                "osType": "Linux",
                "name": "Nodevmubuntu_disk1_92bb7c43d8a840d490e9ffcd5efeaed7",
                "createOption": "FromImage",
                "caching": "ReadWrite",
                "managedDisk": {
                    "storageAccountType": "Premium_LRS",
                    "id": "/subscriptions/aa1d9d6b-9e96-41b7-91b3-012dc82be976/resourceGroups/Ansiblelab-RG/providers/Microsoft.Compute/disks/Nodevmubuntu_disk1_92bb7c43d8a840d490e9ffcd5efeaed7"
                },
                "diskSizeGB": 30
            },
            "dataDisks": []
        },
        "osProfile": {
            "computerName": "Nodevmubuntu",
            "adminUsername": "Sarthakuser",
            "linuxConfiguration": {
                "disablePasswordAuthentication": true,
                "ssh": {
                    "publicKeys": [
                        {
                            "path": "/home/Sarthakuser/.ssh/authorized_keys",
                            "keyData": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCjp7zdyoVGbRCCoLD2ptMM01ya\r\np16scF+bDdA68cBsP0lhPFefW1319gZjW7OogXtzudxx45C12Pb87U9P3Y7Crnjx\r\nt4P29UDBbGPypp3s8SlXVrZkOuIQTLqjzFp8pwgTXTM/Cp8rI6m4wrS1rywenxs/\r\n4h7FHsafCqB10BEsNRF8eAvCAb3/fUlJ7it8aZZR1wmkmY/GYOV/HD6h5la0ta82\r\npP0NDA8CLKFJIC9LHqdPRxEH3E5jB+v4J23QmkUdfAWFa1bz3XJKQHzmB91q6NZ0\r\ngXKWThGNztuLOFvT64DidTDsHV+LnHMcKNCRdBo2nHCiFKlQ+S73BsKSrna7UKxQ\r\nYUDuwPl8pXctnD8zT6XkNf0FdhU96f369TiseOsw/e1d8w1xET5yYXTk7LTHNCx5\r\nWrXuVOumuGhlnJ2dpoaRN3slayMePPIZaoXCsgyva1kHVlxtW3V+Q8G7ZAZGj7cf\r\nszPsnuHu9+MD/xiKmfiqjpAqxUSQHTIZ5M+7Y5M= generated-by-azure\r\n"
                        }
                    ]
                }
            },
            "secrets": []
        },
        "networkProfile": {
            "networkInterfaces": [
                {
                    "id": "/subscriptions/aa1d9d6b-9e96-41b7-91b3-012dc82be976/resourceGroups/Ansiblelab-RG/providers/Microsoft.Network/networkInterfaces/nodevmubuntu266"
                }
            ]
        },
        "diagnosticsProfile": {
            "bootDiagnostics": {
                "enabled": true
            }
        },
        "provisioningState": "Succeeded"
    }
}