<h1 align=center>DHAAS - DockerHub as a Storage</h1>

<p align="center">
  <img src="https://github.com/user-attachments/assets/4aa29ca4-71b9-445b-8fa9-5ccca3c5a62a" height=250px width=444px />
</p>

<!-- 
<p align="center"> 
  <img src="https://github.com/user-attachments/assets/ebdbf725-07d2-4ac1-81e0-a9caf8f1869d" />
</p>
-->

Use DockerHub as a Storage solution to store encrypted artifacts containing personal data.

## Program Flow
- Take all files in folders store it as refs in DB.
- Fetch all refs in DB convert all the refs in DB to encrypted blobs.
- store those references in DB. and push those blobs to dockerhub and store digest.
- Check DB if new files exist do the same process.

## Abilities needed
- Should be able to list files in the folder
- Should be able to list referenced files and artifacts
- Should be able to list, search, select, and fetch uploaded artifacts.

## Ideas
- Use FUSE to manage files in linux. 
- Use GPG to encrypt and decrypt artifacts
- Use ORAS to push/pull artifacts from DockerHub.

## Data Flows
### Upload
![image](https://github.com/user-attachments/assets/3726ea71-9123-4d6f-8251-0679d88a65f1)

### Download
![image](https://github.com/user-attachments/assets/d1df6ba1-f1fd-455d-be66-bf9df1372782)

## DB Structure
![image](https://github.com/user-attachments/assets/14da8512-1535-406d-82da-ba470009be20)
