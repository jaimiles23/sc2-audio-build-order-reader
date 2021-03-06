# StarCraft 2 Audio Build Order Reader

This project takes in a build order and reads it using text-to-speech based on the timestamps included in the build order itself. The supply markers, currently, are purely cosmetic.

This does not work without timestamps.

An example build is included in this repo. Copying and pasting a build from SpawningTool should be good enough, but make sure there aren't empty lines at the start or at the end of the file.

# Requirements and Running the Application

This project requires Python 3. Install the necessary requirements using `pip3 install -r requirements.txt`.

Place a build file into the `builds` folder with the build order. Run:

`python3 ./main.py --build=name-of-build.txt --shorthand=True --supply=False --delay=0`

The application takes the following command line arguments:

`--build`: Filename of the build order

`--shorthand`: Whether to abbreviate the names of units/buildings to common shorthand (eg. "Barracks" -> "Rax")

`--supply`: Whether to read out the supply along with the action that needs to be performed

`--delay`: How long to delay the start of the speech (negative means starts sooner)

# Tips and Tricks

1. Start the build right as the "3" in the countdown to the start of the game begins with a -2 delay. 5 seconds is a decent enough time for the lines to become reminders of what to build in the future, rather than markers of units or buildings that you should already have built.
2. Feel free to add in actions that aren't strictly build items in your build order file. Spreading creep, dropping mules, or moving out your army are great candidates for reminders.


# License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
