# Configure Git

## Get Git version

```sh
git --version
```

## Set User Name

To configure the name that Git will associate with your work.

```sh
git config --global user.name "Your Name"
```

## Set email

To configure the email that Git will associate with your work.

```sh
git config --global user.email your-email@mail.com
```

## Folder does not record ownership

If current folder does not record ownership, add exception for the directory

```sh
git config --global --add safe.directory D:/Folder_Name
```
