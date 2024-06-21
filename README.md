### 1. Start a Service
```
systemctl start <service-name>.service

Example: systemctl start google.service


```

### Example of a service

```
[Service]
#Environment="JAVA_OPTS=-Dspring.profiles.active=production"
WorkingDirectory=/home/ubuntu
ExecStart=/opt/jdk-17.0.9/bin/java -Dsun.misc.URLClassPath.disableJarChecking=true -jar /home/ubuntu/bin/java.jar
SuccessExitStatus=143
TimeoutStopSec=10
Restart=on-failure
RestartSec=5

```
we will create a file with any editor like google.service or any service name we want and paste above content and then start the service

### 2. Check Service Status

```
systemctl status <service-name>.service

Example: systemctl status google.service

```

### 3. Stop Service

```
systemctl stop <service-name>.service

Example: systemctl stop google.service

```

### 4. Reload Daemon After Making Changes to Service

```
systemctl restart <service-name>.service

Example: systemctl restart google.service

```
