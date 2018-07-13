# Bay Area Skydiving 2018 Tracking Competition

This project contains the data files for scoring the 2018 Tracking Competition,
an annual event hosted by Bay Area Skydiving in Byron, CA.

![Open Category Winners](https://raw.githubusercontent.com/pr3d4t0r/basdtracks2018/0000-initial-setup/images/open-winners.jpg)
![Novice Category Winners](https://raw.githubusercontent.com/pr3d4t0r/basdtracks2018/0000-initial-setup/images/novice-winners.jpg)

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


## FAQ

1. **How did you calculate the tracking distance?** - By taking the first point
   during jump run before the first constant descent, down to the 3,000 ft AGL
   point _or_ the parachute deployment point, and using the difference in the
   distance traveled that FlySight reported.

1. **How were the FlySights configured?** - They came configured from Bionic
   Avionics and we used them as-is.  While the competitors were welcome to use
   their personal FlySights along with the competition devices, the enclosed
   data set only includes the competition configurations.

1. **Do you support Windows?** - Sort of.  All the tools used for analyzing the
   competition data are supposed to work under Windows, but the develoepers
   don't have Windows systems to test.  Fork the project or ask to join if you'd
   like to help!


# License and copyright

The code and sample data are released under the BSD 3-clause license.  All the
code is &copy; 2018 by GitHub users pr3d4t0r and benmyles.

