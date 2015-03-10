# Import Map Data for kufi.ifcontro.ch

This repository can be used to create test-users with new test data at kufi.ifcontrol.ch.

The procedure is as follows:

1. Clone this repository: `git clone git@github.com:hoodiehq/ifcontrol-map-data.git`.
2. Create new directory within the data directory, that has the **same name** as the user you want to log in as, later. e.g. `mkdir data/test22`.
3. Populate the newly created directory with `.json` files that match the specifications under `data/testuser/`. (see below for details).
4. Commit the new data:
   `git add data/test22`
   `git commit -am 'new data for test22 user'`
5. Push the new data to GitHub: `git push`
6. Wait.
7. The repo is cloned to the production server every 10 minutes on the full hour, 10 past, 20 past and so on. Wait until one of those times is passed. When in doubt, wait until the next one.
8. Go to http://admin.kufi.ifcontrol.ch and log in.
9. Click on *Users* in the sidebar.
10. Create a new user on the top of the page. Make sure the name you enter **matches** the new directory from earlier **exactly**. e.g. `test22`. Your choice of password is free.
11. Log in as the new user into http://kufi.ifcontro.ch and see all new inspection data.


## The Data Format

TBD: Expand (Espy)

(notes from Jan)
The data directory name must match an existing or future username.
The needs to be a flat list of files in the data directory.
There can’t be any sub-folders.
All files need to end in `.json`.
All files need to be of the form `PREFIX_type.json`, e.g. `GR1008_perimeter.json`.
All files must be UTF-8 encoded.
