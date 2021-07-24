# hideproc
hideproc is a Linux kernel module that hides other processes.

## how to use
```
$ sudo insmod hideproc.ko
$ pidof cron
$ echo "add `pidof cron`" | sudo tee /dev/hideproc
$ pidof cron # 無法見到 cron
$ echo "del `pidof cron`" | sudo tee /dev/hideproc
$ pidof cron # 再次見到 cron
$ sudo rmmod hideproc
```
