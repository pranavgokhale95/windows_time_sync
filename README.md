# Sync Windows Time
I was facing a problem with my laptop's CMOS battery. The time Windows showed after a boot was wrong. 
I had to go to "adjust time/date" and sync the time online everytime. I searched for possible commands to this on the command line and wrote this batch file.

## The Purpose
If your windows doesn't display the correct time and/or date, run this batch file, the problem should be solved in most of the cases.

## How to run the batch file?
* Clone the batch file first:
```{r, engine='bash', count_lines}
git clone https://github.com/pranavgokhale95/windows_time_sync.git
```

* **Make sure you are connected to the internet before running the batch file**

* Right-click on the time_sync.bat and click on "Run as administrator". 
* Provide the necessary administrator credentials and permissions.
* The batch file will run and the time and/or date will be synced to your time zone. 

## Automate running the batch file.
One can run the batch file everytime windows starts to sync the time at startup itself. This will automate the task, no need to manually run the file everytime. 
* Copy the downloaded batch file to:
```{r, engine='bash', count_lines}
[D|C]:\Profiles\{User}AppData\Roaming\Micrsoft\Windows\Start Menu\Programs\Startup
```
* Restart and stop the annoying "why my windows shows different time?" problem once and for all.
:simple_smile:

#### To veify whether the batch file runs at startup (for Windows8+)
* Open task manager
* Switch to startup tab
* Verify that the batch file is present in the list, and it is ENABLED under the Status column.


