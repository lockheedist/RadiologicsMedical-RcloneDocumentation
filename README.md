
# Rclone Documentation

This instructions made for proper and basic using of Rclone.


## Installation


```bash
  sudo apt install rclone
```



  
## Configuration and bounding with G-Drive
1_ Open the config menu with command below.

```bash
  rclone config
```

2_ You will have three choices, write n for creating new remote.
```bash
  n
```

3_ After chosed new remote, it will ask you for a remotename you can choice whatever you want.

4_ Then it will ask "storage" and give you a list of options with index numbers you need to find the index of Google Drive option and write it to the shell After you choosed the Google Drive it will ask for client-id and client-secret you just need to skip by pressing enter. (We don't need client-id and secret bc. we just want to mount data to Google Drive we don't have anything to do with Google API services for now.)

5_ It will ask for "scope" you need to choose option 1 because we need full access to do Google Drive folders. After that it will ask you for "root_folder_id" and "service_account_file" you just need to skip these questions by pressing enter for default Rclone.

6_ It will ask for "Edit advanced config?" entry "n" and keep going.
```bash
  n
```

7_ It will ask for "Use auto config?" entry "y" and keep going.
```bash
  y
```

8_ After config choices.. It will direct you to a website on your default browser. you need to log in your google account that related with your g-drive.(If the system don't direct otomaticly copy the link and open in your browser.)

9_  It will ask you "Configure this as team drive?" entry "n" and proceed.
```bash
  n
```

10_ In final it will give you a information about remote that you created just entry "y" and approve the all process. Than you can quit by entry "q" we are done here.
```bash
  y
```

```bash
  q
```


## Basic Commands 


1_ List all of the remotes.

```bash
  rclone listremotes
```
  
2_ To see folders in Drive.

```bash
  rclone ls remotename
```


## Uploading Files

```bash
  rclone copy -P filename "remotename:(you can specify any folder here but not necessary.)"
```

