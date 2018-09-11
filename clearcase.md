___________________________________________
ClearCase :
If ClearCase does not install and the machine does not restart

Find hijacked files list

    On UNIX® and Linux® you can run the following command from a snapshot view:
cleartool ls -recurse | grep "hijacked"

    On Microsoft® Windows® you can run the following command from a snapshot view:
cleartool ls -recurse | findstr "hijacked"

CMD command to find all non-read-only files
dir /S/A-R *.java

List all views created by an user
ct lsview -l | grep egenerat

List all dynamic views in local
cleartool> lsview -host HOSTNAME
rmview \\HOSTNAME\ccviews\viewdyn.vws


When adding a new file
Check out the parent folder
Add the file to source control
Check in the parent folder


Remove a folder already checked in
cleartool checkout -nc root_dir
cleartool rmname dir2
cleartool checkin root_dir


Firstly, you can cleartool umount all vobs with

cleartool unmount -all

Secondly, you can mount them without making them persistent:

cleartool mount \aVob

Through the GUI, they are generally mounted as "persistent", like if you did:

cleartool mount -persistent \aVob

cleartool update .

Remove a view
rmview



Undo checkout:
unco filename


Remove a file
co parentfolder
rmname filename
ci parentfolder





Create an activity
mkact "My_Activity"

List activities on a stream
lsactivity
2015-12-14T14:59:21Z  My_Activity  emile.generat   "My Activity: new features"



Change activity

