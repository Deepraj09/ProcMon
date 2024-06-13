# Python Automation Script
# ProcMon

This project provides a Python script to log information about running processes on a system and automatically send these logs via email. It uses various libraries and tools to achieve its objectives, such as psutil for process information, schedule for task scheduling, and smtplib for sending emails.


# Features

- Process Logging: The script collects details about currently running processes, including their PID, name, username, and memory usage.

- Directory Management: Automatically creates a specified directory for storing log files if it doesn't exist.

- Automated Email Sending: Sends the generated log file to a specified email address if an internet connection is available.

- Scheduled Execution: Uses the schedule library to run the process logging and email sending at regular intervals specified by the user.


# Usage

### Requriement

- Python 3.x
- psutil, schedule, smtplib, urllib

### Setup

- Clone this repository.
- Install the required Python packages using pip install -r requirements.txt.
- Configure the email addresses and SMTP server details in the script.
### Running the Script

Run the script from the command line with the interval (in minutes) as an argument:

```bash
  python ProcessMonitor.py <interval_in_minutes>
```

Example:

```bash
  python ProcessMonitor.py 5
```

Use -h or -H for help:

```bash
  python ProcessMonitor.py -h
```

Use -u or -U for usage information:

```bash
  python ProcessMonitor.py -u
```


# Functions

- is_connected():-
  Checks for an active internet connection by trying to reach Google's website.

- MailSender(filename, time):-
  Sends an email with the log file attached to a specified email address. It uses the SMTP protocol to connect to the email server and send the email.

- ProcessLog(log_dir='Marvellous'):-
  Generates a log file with information about running processes and sends it via email if an internet connection is available.

- main():-
  Main function to handle argument parsing, scheduling the logging tasks, and running the script.

This project aims to provide a simple yet effective way to monitor system processes and maintain logs with automated notifications, making it useful for system administrators and IT professionals.
# Reference

- Automate The Boring stuff with Python by AL SWEIGART