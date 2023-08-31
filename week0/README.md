# Week 0 project guidelines

## starting a roscore node

ROS 1 requires a 'core' node to operate. This is what is pointed to by the ROS_MASTER_URI environment variable:

```
export | grep ROS_MASTER_URI
```

If you haven't changed anything, it should read https://localhost:11311

That means it is looking on your computer (localhost) on port 11311. You can change both the computer it is looking for (hostname or IP) or the port number.

Start a roscore node:

```
roscore
```

(some things are easy)

Look up at Dave

## publisher and subscriber tutorial

First things first, complete the publisher and subscriber tutorial (python versions) from the ROS wiki: https://wiki.ros.org

Note: do this in your week0 package, don't create a beginners tutorials package for this.

When you've set this up correctly, you should be able to run:

```
rosrun week0 talker.py
```

From the command-line and have it output some messages. Then try running the listener node from another terminal.

```
rosrun week0 listener.py
```

### make some changes

Take some time to play with these a bit:

* What happens when you close one or the other?
* What happens when you close the core node?
* What happens when you change the rate for the talker?
  * default is 10
  * rate = 1
  * rate = 100
  * rate = 100000
  * rate = 0.1
  * rate = 0.001
* What happens when you start 2 talker nodes?
* What happens when you start 2 listener nodes?

## customize an HRI message

Look at this tutorial for creating your own message type: https://wiki.ros.org/ROS/Tutorials/CreatingMsgAndSrv

Let's create a new message type for a person that we want to keep track of:

```
float64 x
float64 y
float64 z
```

Let's modify our talker and listener scripts to use this new message. 


## commit changes back to your repository

you want to add any new files with:

```
git add <filename>
```

You can also see what has changed using the command:

```
git status
```


```
git commit -m 'INSERT MEMO HERE'
```


## push changes to github

If you go to your week0 directory on the github website for your project, you'll notice no changes, yet. That's because while you've committed those changes, you haven't pushed them to github. You can do so by typing:

```
git push
```

You might have to set some variables the first time. Refresh the github website and you should see your changes!