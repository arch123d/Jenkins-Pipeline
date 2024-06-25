# Step 1: Add Jenkins User to Docker Group
Add the Jenkins user to the Docker group to grant it access to the Docker daemon.


```
sudo usermod -aG docker jenkins
```
Restart Jenkins to apply the new group membership.

```
sudo systemctl restart jenkins
```
# Step 2: Verify Docker Group Membership
Check that the Jenkins user is now part of the Docker group.

```
groups jenkins
```
The output should include docker.

# Step 3: Ensure Docker Service is Running
Check if the Docker service is running.

```
sudo systemctl status docker
```
If it is not running, start it:

```
sudo systemctl start docker
```

