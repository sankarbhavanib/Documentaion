VIM CHCH : http://vim.rtorr.com/

Unix commands
```
to check the stage load  : $ top 
to check the users logged  in and process running : $w
to check the free space  : $ free
to check the disks available,free spaces or mounted : df
```
copy files from local mac to server 
MyMac $ >  scp someFile someUser@someServer:/somePath/someFile

to kill all services 
sudo -u qserv kill -9 14793
kill -9 $(lsof -i tcp:3000 -t)     // to kill items running on port 3000
