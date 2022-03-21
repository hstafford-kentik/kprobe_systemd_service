Most modern Debian based systems (e.g. Ubuntu 15.x and later) have migrated to systemd as their startup system. The following are instructions on how to create the startup script for these systems to run chfagent or kprobe as a daemon. Startup scripts are now stored in the /etc/systemd/system directory.

Create the file /etc/systemd/system/kprobe.service and include the contents of this repository.   The only edit(s) needed are for the listening interface and deviceID. The deviceID can be found in the kentik portal.  After creating the kprobe device, from the Settings->Devices page, click on the kprobe device listed.  In the right side panel that appears, the deviceID will be displayed in the upper right side of the panel.

Additional kprobe command line settings can be viewed in the kentik knowledge base article:
https://kb.kentik.com/v0/Bd03.htm

This service file will read the API email and key from the file /etc/default/kentik.env.   The email and api key can be found in the portal under your user profile.
