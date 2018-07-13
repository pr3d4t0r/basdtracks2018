# Bay Area Skydiving 2018 Tracking Competition

This project contains the data files for scoring the 2018 Tracking Competition,
an annual event hosted by Bay Area Skydiving in Byron, CA.

![Open Category Winners](https://raw.githubusercontent.com/pr3d4t0r/basdtracks2018/master/images/open-winners.jpg)
![Novice Category Winners](https://raw.githubusercontent.com/pr3d4t0r/basdtracks2018/master/images/novice-winners.jpg)

The setup includes a Jupyter Lab dockerized implementation with local data
storage and single user access credentials.

The data are organized in the `scoring` directory in the layout prescribed by
the [FlySafe](https://www.facebook.com/FlySafeApp/) BASE distance analysis tool.


## Requirements

### Quick start

* [FlySightViewer.app](http://www.flysight.ca/extras.htm) for viewing the
  FlySight CSV files
* Microsoft Excel to view the scoring tables
* [FlySafe](https://www.facebook.com/FlySafeApp/) for distance analysis


### Developers

* Latest Docker for Linux, MacOS, or Windows
* Firefox, Chrome, Safari, or any modern browser
* Basic knowledge of [Jupyter Lab](https://jupyter-notebook.readthedocs.io/en/stable/index.html)
  or Jupyter Notebook


## Jupyter Lab

### First time launch

Docker will pull the latest version of Jupyter Lab and run it.  This process may
take between 30 seconds and a few minutes, depending on the speed of the user's
Internet connection.

First time run generates a token to set the notebook password.  This password is
necessary to open the run-time environment because this notebook can run in a
server open to the whole Internet, if desired.  The password set up is a
one-time event.

To generate the first time password, open a terminal shell in the
`basdtracks2018` directory, then execute:

```bash
docker-compose up --remove-orphans ; docker-compose rm
```

This is a good time for the user to get some coffee ☕️ if they have a slow
Internet connection.

Jupyter Lab starts when the download is complete, and shows the legend:

```
notebook    |     Copy/paste this URL into your browser when you connect for the first time,
notebook    |     to login with a token:
notebook    |         http://b8b27455b503:8888/?token=6c7546c58eff46029e095ea0f8e95f5006fd66dfd9fa63d6&token=6c7546c58eff46029e095ea0f8e95f5006fd66dfd9fa63d6
```

Generate a new password by:

1. Log on to `http://localhost:8888` on your web browser
1. Enter the token in the _Setup a Password_ section, and enter a password of
   choice.  The token, in our example, is the string of numbers and letters
   after `token=`, or `6c7546c58eff46029e095ea0f8e95f5006fd66dfd9fa63d6` in the
   example
1. Click on _Login and set new password_ to go to the work bench
1. Click on the _Logout_ button at the top right corner
1. Go to the terminal and stop the Jupyter container by pressing Ctrl-C
1. Respond "y" to the _Going to remove notebook_ prompt

![Password set up and token browser example](https://raw.githubusercontent.com/pr3d4t0r/basdtracks2018/master/images/token-password-setup.png)


Done!  You may validate that the first time run was successful by running, this
command:

```bash
if [[ -e "scoring/_jupyter/jupyter_notebook_config.json" ]]; then echo 'Success!'; else echo "Failed - try again"; fi
```


### Work with the data

The process is super simple now:

1. Start the Jupyter Lab container
1. Log on to Jupyter at `http://localhost:8888`
1. Play with the data to your heart's content!

To start:

```bash
docker-compose up --remove-orphans ; docker-compose rm
```

When done, kill the process with Ctrl-C or turn off the computer.  That's it!


### Working with data

**Section under construction ***


## FAQ

1. **How did you calculate the tracking distance?** - By taking the first point
   during jump run before the first constant descent, down to the 3,000 ft AGL
   point _or_ the parachute deployment point, and using the difference in the
   distance traveled that FlySight reported.

1. **How accurate were the measurements?** - The FlySightViewer zoom range
   changed between measurements when the map was on display, so two consecutive
   reads, one with and one without the map in the window, for the same
   competitor, showed a difference of 20-100 ft in either direction.  Whenever
   possible the window size remained the same and the map was hidden.

1. **How were the FlySights configured?** - They came configured from Bionic
   Avionics and we used them as-is.  While the competitors were welcome to use
   their personal FlySights along with the competition devices, the enclosed
   data set only includes the competition configurations.

1. **Do you support Windows?** - Sort of.  All the tools used for analyzing the
   competition data are supposed to work under Windows, but the developers
   don't have Windows systems to test.  Fork the project or ask to join if you'd
   like to help!


# License and copyright

The code and sample data are released under the BSD 3-clause license.  All the
code is &copy; 2018 by GitHub users pr3d4t0r and benmyles.

