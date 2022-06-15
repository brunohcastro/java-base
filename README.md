# java-base

## Usage

### Base commands

```bash
# Runs the command inside an ephemeral container using the app service described in the docker-compose file as a base
$ dbin/exec <command>

# Rebuild the image after any changes to the dockerfile
$ dbin/build

# Remove all containers and their volumes (WARNING any cache or files not stored in the filesystem will be deleted)
$ dbin/dispose

# Moves the target folder contents to the root folder and deletes the target folder
# it also renames this file to INSTRUCTIONS.md
$ dbin/mvroot <target>
```

### Aliases

```bash
# Creates a new file in dbin to alias that command inside the docker container
$ dbin/mkalias

# Runs mvn in the project folder
$ dbin/mvn

# Runs gradle in the project folder
$ dbin/gradle

# Runs spring cli in the project folder
$ dbin/spring
```

## Examples

### New spring boot project

```bash
$ dbin/spring init my-app
$ dbin/mvroot my-app
$ dbin/mvn spring-boot:run
```
