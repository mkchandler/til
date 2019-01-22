Every once in a while I start getting messages when creating a Git commit that says:

> error: gpg failed to sign the data<br>
  fatal: failed to write commit object
  
Since I sign all commits and tags with a GPG key, `gpg-agent` is required to run. Follow these steps to restart the process:

Kill the process:

    killall gpg-agent

Start the process in the background:

    gpg-agent --daemon
