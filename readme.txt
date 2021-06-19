this is ansible server virtual machine which will be our ansible configration manager tool server


username:sarthakuser


here are details 

Operating system:Linux (centos 7.9.2009)

Size:Standard D2s v3 (2 vcpus, 8 GiB memory)

Public IP address:20.98.222.38

Virtual network/subnet:Ansiblelab-RG-vnet/default

JSON VIEW


{
    "name": "Ansibleserver",
    "id": "/subscriptions/aa1d9d6b-9e96-41b7-91b3-012dc82be976/resourceGroups/Ansiblelab-RG/providers/Microsoft.Compute/virtualMachines/Ansibleserver",
    "type": "Microsoft.Compute/virtualMachines",
    "location": "eastus2",
    "tags": {
        "Config Manager ": "Ansibleserver"
    },
    "properties": {
        "vmId": "7f54ce0c-42cd-4342-9016-2687511eb1d9",
        "hardwareProfile": {
            "vmSize": "Standard_D2s_v3"
        },
        "storageProfile": {
            "imageReference": {
                "publisher": "OpenLogic",
                "offer": "CentOS",
                "sku": "7_9",
                "version": "latest"
            },
            "osDisk": {
                "osType": "Linux",
                "name": "Ansibleserver_OsDisk_1_f7bbd61635ce4788b3ccd3d3244aa2fd",
                "createOption": "FromImage",
                "caching": "ReadWrite",
                "managedDisk": {
                    "storageAccountType": "Premium_LRS",
                    "id": "/subscriptions/aa1d9d6b-9e96-41b7-91b3-012dc82be976/resourceGroups/Ansiblelab-RG/providers/Microsoft.Compute/disks/Ansibleserver_OsDisk_1_f7bbd61635ce4788b3ccd3d3244aa2fd"
                },
                "diskSizeGB": 30
            },
            "dataDisks": []
        },
        "osProfile": {
            "computerName": "Ansibleserver",
            "adminUsername": "sarthakuser",
            "linuxConfiguration": {
                "disablePasswordAuthentication": true,
                "ssh": {
                    "publicKeys": [
                        {
                            "path": "/home/sarthakuser/.ssh/authorized_keys",
                            "keyData": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCqpLd5KJih7/ydYyX5P/vboYnh\r\nBhpkJNZslh94spqoq+i0ShS55Qq/Dvvg28Oc6gF7hbyfm+y7HK1b2uCLkdywNW0q\r\n2kUC45HsRivKwjtGMHYhs53c1LbIGSSukigBR3pqicTHWXbr23NqCM+hJGV6MGCQ\r\n2Un7VI/2c5BkMksRQOCuZBwKm67++zJm0o4uuSrMOM84Tq0geu/B0lSJfYnWxwh7\r\nK97yi6gCJv1TegoRWs48FOTO4Rl2L8bq21q0hdDVBEOqNaH1g1447FTwcxcRmN3s\r\nrPirFTPnPmMuC/TfTy3oZqeVudO19OisgZIEnhEq5lixat1Ux8nH+tsAt6YJySfW\r\nRwVI8zgWENqQQkT/EL10AdAqWtKOdU845vd2wxckqpsI+VzdL9l5MEWvaCDjNyIE\r\nRl+y3VPxeE6oBKyGHJwpxif9wYOKOA1QORqRjfNTtfpzfIO9pkrI9FJnqyrP3Pr7\r\ngEqMlQoF5CUr/SO++yRlfXgvrx7x6TICbvc+N1M= generated-by-azure\r\n"
                        }
                    ]
                }
            },
            "secrets": []
        },
        "networkProfile": {
            "networkInterfaces": [
                {
                    "id": "/subscriptions/aa1d9d6b-9e96-41b7-91b3-012dc82be976/resourceGroups/Ansiblelab-RG/providers/Microsoft.Network/networkInterfaces/ansibleserver587"
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
