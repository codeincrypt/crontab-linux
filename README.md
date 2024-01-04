## Installing Cron
Almost every Linux distribution has some form of cron installed by default. However, if you’re using an Ubuntu machine on which cron isn’t installed, you can install it using APT.

Before installing cron on an Ubuntu machine, update the computer’s local package index:

```
sudo apt update
```

Then install cron with the following command:

```
sudo apt install cron
```
 
You’ll need to make sure it’s set to run in the background too:
```
sudo systemctl enable cron
```

You can edit your crontab with the following command:
```
crontab -e
```

If you’d like to view the contents of your crontab, but not edit it, you can use the following command:

```
crontab -l
```

You can erase your crontab with the following command:
Warning: The following command will not ask you to confirm that you want to erase your crontab. Only run it if you are certain that you want to erase it.
```
crontab -r
```

This command will delete the user’s crontab immediately. However, you can include the -i flag to have the command prompt you to confirm that you actually want to delete the user’s crontab:

```
crontab -r -i
 ```
Output
crontab: really delete sammy's crontab? (y/n)


For example
```
0 0 * * * /etc/python/project1/main.py
0 5 * * * pm2 restart 0
 ```

## Crontab guru
The quick and simple editor for cron schedule expressions by Cronitor

Click here [Crontab](https://crontab.guru/)
