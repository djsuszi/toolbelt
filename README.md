# Set of useful scripts


## Oneliner: Ping host and save the result 

    */10 * * * * echo -n `date -R` >> /home/osmc/esp.ping; ping -c 4 192.168.0.105 > /dev/null 2>&1; echo ' ' $? >> /home/osmc/esp.ping


## Links

 * [megatools](https://megous.com/git/megatools)
 * [plowshare](https://github.com/mcrapet/plowshare)
 * [rclone](https://github.com/rclone/rclone)
