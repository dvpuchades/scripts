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
---
# Vault

For situations where a directory needs to be moved across multiple disks but does not have immediate access to all of them, and continues to grow between syncs.

This tool allows you to track which files have already been copied to each disk, and removes them from the source directory once they have been copied to all specified destinations.

## How to Use It

1. Mark your disk as a destination by running `vault device <new_name> <path_to_disk_root>`.
   - `vault devices` will list the marked destinations that are currently mounted.
   
2. Use `vault add <destination> <path_in_destination>` into the moving directory to add a destination.
   - Run this command for each disk you want to designate as a destination for your files.
   - `vault info` will display the added destinations.
   - To remove a disk from the list of destination disks, use `vault remove <destination>`.
   - Make sure that `<path_in_destination>` exist in the destination disk.

3. Run `vault sync` in the moving directory to sync with the connected destinations.
   - Once a file has been copied to every specified destination, it will be deleted from the moving directory.