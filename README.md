# google-drive-lib
Simple node.js module to use Google Drive folders and files upload

Usage:

> import googleAPI from "../services/GoogleDrive.js";
> 
> // Create Google Drive folder
>
> const folderGoogleDriveName = uuidv4();
>
> const { link, id: folderId } = await googleAPI.createFolder(folderGoogleDriveName);
> 
> async _uploadFiles(folderId, files) {
>
> for (let file of Object.values(files)) {
>
>   const { link, id: fileId } = await googleAPI.uploadFile(folderId, file);
>
>}
>
>
> async _deleteFiles(deleted_files) { 
> 
> if (deleted_files) {
> 
> for (let deletedFile of JSON.parse(deleted_files)) {
>
> await googleAPI.deleteFile(deletedFile.file_google_drive_id); 
>
> }
>
> }