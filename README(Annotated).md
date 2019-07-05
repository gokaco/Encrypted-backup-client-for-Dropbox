This repo contains the Annotated and unannotated version of:- https://www.nayuki.io/page/encrypted-backup-client-for-dropbox
using Signedness Checker.

To compile from terminal follow the steps as given below-

```
$ cd Encrypted-backup-client-for-Dropbox/Annotated
$ javac -cp nayuki-json-lib.jar:. -processor signedness io/nayuki/dropboxbackup/Utils.java
$ javac -cp nayuki-json-lib.jar:. -processor signedness io/nayuki/dropboxbackup/DropboxBackupService.java
$ javac -cp nayuki-json-lib.jar:. -processor signedness io/nayuki/dropboxbackup/DropboxBackupDecrypter.java
```

In this case study I learnt that signedness checker is weak in some classes and needs enhancements such as:-

1.)java.io.DataInputStream

2.)java.util.Base64

3.)java.lang.String

4.)java.io.ByteArrayOutputStream

Some issues occurred again like Issue #2483, #2367.
