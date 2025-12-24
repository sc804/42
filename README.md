📑 **Gitbook** : https://sofias-notebook.gitbook.io/

## connecting bluetooth automatically
go to Home -> login.sh and save the following line at the bottom of the file
```bash
bluetoothctl power on && connect ${mac address}
```
(my headset's address : E8:EE:CC:A1:C5:BF)

- check function calls : nm -u {file_name}.a

- check memory leaks : valgrind --leak-check=full
--show-leak-kinds=all make
