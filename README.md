# HA-on-Azure
Steps to prepare HA virtual appliance running on a VM in Azure

1. Download the VHDX image from https://www.home-assistant.io/hassio/installation/
2. Use Hyper-V Manager to convert the disk
    Open Hyper-V Manager and select your local computer on the left. In the menu above the computer list, select Action > Edit Disk.
    On the Locate Virtual Hard Disk page, select your virtual disk.
    On the Choose Action page, select Convert > Next.
    To convert from VHDX, select VHD > Next.
    To convert from a dynamically expanding disk, select Fixed size > Next.
    Locate and select a path to save the new VHD file.
    Select Finish.
3. Uploading it to the Azure Blob storage
    Create a Storage account e.g. GP v.2 
    Once ready, go to Blob  services and create a container
    Upload the vhd image into the container blob page blob
4. Go to images and create an image from the uploaded vhd
5. Once the image is ready, you ca now create your VM

# Json templates for storage account, image and VM are in the Repository
    
