# autossh-proxy

Local socks proxy using an SSH connection to a remote host 

It will use your current SSH keys so make sure to have copied them to the remote host first (`ssh-copy-id ...`)

# Build

`docker-compose build`

# Run

Example docker-compose file is included. Edit the environment variables and run `docker-compose up -d`

# Configuration

Here is a list of the environment variables used to configure this docker container:

| Option   | Description         | Default
|---       |---                  |---
| SSH_USER | Remote SSH username | $USER
| SSH_HOST | Remote SSH host     | None
| SSH_PORT | Remote SSH port     | 22

Other than that [all autossh environment variables](https://linux.die.net/man/1/autossh) will also work

# Usage

After running the container with the correct configuration port 58080 will be exposed and you shoud be able to connect to that as a socks proxy 

