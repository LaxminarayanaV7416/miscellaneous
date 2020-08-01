### Postgres SQL Installation in Mac

# Installing Postgres via Brew

## Pre-Reqs
[Brew Package Manager](http://brew.sh)

In your command-line run the following commands:

1. `brew doctor`
1. `brew update`

## Installing
1. In your command-line run the command: `brew install postgres`
2. Run the command: `ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents`
3. Create two new aliases to start and stop your postgres server. They could look something like this:

     ```
          alias pg_start="launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist"
          alias pg_stop="launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist"
     ```

4. Run the alias you just created: `pg_start`. Use this comment to start your database service.
     - alternatively, `pg_stop` stops your database service.
5. Run the command: ``createdb `whoami` ``
6. Connect to your postgres with the command: `psql`
7. `brew reinstall readline` - **ONLY IF NEEDED**
8. `createuser -s postgres` - fixes `role "postgres" does not exist`
9. Test with `psql` command

     ```
     $ psql
     psql (12.0)
     Type "help" for help.

     lucky=# 
     ```
10. reset th password
     ```
     psql -U postgres
     postgres=# alter user postgres with password 'NEW_PASSWORD';
     ```
