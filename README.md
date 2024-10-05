# scripts
## visit_valencia
Seeks flights from Cork to Valencia staying there for 2 weeks, from Saturday to Saturday.

## weeks_to
Returns the number of weeks or hours left to a deadline

## next_sunny_day
Returns the next good weather day in Cork City

## next_sunny_evening
Gets the next good weather evening in Cork City, understanding evening as the period from
5pm to 10pm

## will_it_rain
Advices to take an umbrella from weather forecast for 8am to 10am and 5pm to 7pm for that day,
it works only for Cork City

##
Performs a backup of the specified directory. The specified directory
must contain a .vault-config file that specifies the backup destination.

.vault-config file format:
{
  "destinations": {
    "backup_hdd" : "Vault24",
    "nas" : "<path_to_backup>"
  },
  "files": {
    "path/to/file": [<synced_destinations>]
  }
}

Every destination path must contain a .vault file that specifies its name.
.vault file format:
{
  "name": "backup_hdd"
}

Usage: vault <directory>