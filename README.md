# Backup Tools
Backup Tools consists of two scripts: `dump` and `restore`.
Both are designed to handle backups of the `$HOME` directory.
`dump` will dump everything into a single tar file that can
then be stored somewhere else. `restore` takes an existing
tar file and restores everything into the `$HOME` folder if
no pattern is provided. Using a pattern it is possible to do
a partial restore.

## Usage

### Backup
To create a backup run the following command. Please note
that `dump` does not backup hidden files/folders or `$HOME/Videos`.
```sh
dump
```
This will create a file in the following format: `YYYY-MM-DD.tar`. 
It is advised to store this file at a safe location.

### Restore
To do a full `$HOME` restore run `dump` without a pattern.
```sh
restore XXXX-YY-ZZ.tar
```

To only restore the `$HOME/Downloads` folder issue the 
following command.
```sh
restore XXXX-YY-ZZ.tar ./Downloads
```
