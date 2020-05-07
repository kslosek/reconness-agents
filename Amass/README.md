## Amass Command

Using {{domain}} ReconNess replace {{domain}} to the root domain, for example, yahoo.com if we define that as a root domain adding the Target.

```
/bin/amass enum --passive -d {{domain}}
```

## Amass Script

Check [Script file](https://github.com/reconness/reconness-agents/blob/master/Amass/Script)

## Amass Dockerfile Entry

```
# -------- Agents dependencies --------

# To allow run amass inside the docker
RUN apt-get update && apt-get install -y wget && apt-get install unzip -y
RUN cd /tmp/ ; wget https://github.com/OWASP/Amass/releases/download/v3.5.5/amass_v3.5.5_linux_amd64.zip ; unzip amass_v3.5.5_linux_amd64.zip
RUN mv /tmp/amass_v3.5.5_linux_amd64/amass /bin

# -------- End Agents dependencies --------
```
