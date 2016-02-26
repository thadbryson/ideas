# Task Man

Manage automated tasks through GUI system. This would be a stand-alone web app. Controls cron daemon maybe?

Look at Gearman???

## Overall concept
PARV: Plan - Act - Record - Verify

## Features
1. Web interface: graphs, point-click turn on/off tasks, logs in realtime, forms for filling out task information
2. Reporting: # of failures, # of non-runs, # of successful runs, time each task took, logs
3. Fail Over: if a task didn't run or failed to run: run again or run another task
4. Task flows: Run certain tasks after other tasks have run
5. Store: system configurations and settings
6. Notification: Send Task output to people
7. Notification Groups: groups of people to send notifications to

## Tasks
Local Filesystem: use Symfony\Component\Filesystem
     - create files, directories
     - touch files, directories
     - symlinks
     - set permissions, chown, chgrp, chmod
     - delete files, directories
Remote Filesystem: use Flysystem
     - create files, directories, read, write, has, set visibility, delete
     - Dropbox, Rackspace Files, AWS, SCP
Communication: email, texting, phone calls, instant message, Twitter, Facebook
IFTTT: ifttt.com If This Then That
Process: use Symfony\Component\Process
     - services: status, start, restart, stop
     - run top, get processes running, memory consumption
     - memory consumption
Log rotating
     - remote or local filesystems
Code Versioning Systems: Git, SVN, Mercurial
     - checkout/clone
     - create branch
SQL: select, insert, update, delete
     - Run SQL statements
     - Get result
Callback Function: pass callback function into task


## Run Conditionals
1. At a certain time
2. If another task just ran successfully/failed/failed to run
3. Event fired
4. Custom ifCondition() in Task object
5. If on
6. If another task is on or off
7. If another task is running

## Tasks Properties
- config(array $conf) // configuration of Task, name and everything
- run() // run actual task
- setLog()
- getLog()
- logOnSuccess()
- logOnFailure()
- logOnError()
- logOnFailedToRun()

## Task Manager
- collection of tasks
- tells whether a task is on or off
- when to run tasks
- executes task running
- logs time of task execution
- get success/fail/didn't run/error of tasks - runStatus
- passes in Log object to ask for running

## Scheduler
- run continuously
- run repeat year/month/day/hour/minute/second - cron schedule pattern
- Skip at certain years/months/day/hour/minutes/seconds
- Run every number of years/months/days/hours/minutes/seconds

## Log
- passed into Task
- logs in realtime by Task
- or returned by Task to add to Log when complete
- logOnSuccess()
- logOnFailure()
- logOnError()

## Reporting
- Show logs
- Show run times and outcomes of Tasks
- order by task, date/time, return status,
- search: task, date/time, return status, logs, on/off,