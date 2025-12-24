## 📑 **Gitbook** > https://sofias-notebook.gitbook.io/

## 🎧 Bluetooth connection
go to Home -> login.sh and save the following line at the bottom of the file
```bash
bluetoothctl power on && connect ${mac address}
```

## 👾 Change user picture
Choose a picture/gif and save it in the Home directory with the name `.face.jpg` (same name even if it's a gif file).
Restart session.

## 🃏 Random stuff
- check function calls : nm -u {file_name}.a

- check memory leaks : valgrind --leak-check=full
--show-leak-kinds=all make
