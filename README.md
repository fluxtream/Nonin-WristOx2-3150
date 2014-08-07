Nonin-WristOx2-3150
===================

Using an iPython notebook, configure a Nonin WristOx2 3150 to log once per second, and then pull sessions from it over USB
to graph locally and to upload to fluxtream.org for exploration.

Once you've gotten the notebook running, evaluate each section in series.  This will configure logging, and set the current
time on the device.  (Because the Nonin device does not cope with timezones or daylight savings time, this package sets
the time on the Nonin according to GMT/UDT, and assumes the same when it pulls data from the Nonin.  So you're free
to use it across timezones and DST boundaries!)

When uploading to Fluxtream, you'll want to enter your username and password for fluxtream.org.  Be sure to click the
'set' button, which reads your password into the running python kernel, and clears the password field on the page.
In particular, be sure to click set and not leave your password in the textarea field before sharing your notebook
with someone else.

After you've downloaded a batch and uploaded to fluxtream, you can optionally clear out the data on the nonin.
Simply evaluate

    nonin.clear_sessions()

(Here's an [online view of the notebook](http://nbviewer.ipython.org/github/fluxtream/Nonin-WristOx2-3150/blob/master/Nonin-WristOx2-3150.ipynb), but you'll need to be running it locally to download data from the Nonin and upload to Fluxtream)
