# JBoss ON

# About JBoss Operations Network

The primary use for JBoss ON is to give administrators a single point of access to view their systems.

JBoss ON centralizes all of its operations in an installed server. The JBoss ON server communicates with locally installed JBoss ON agents, which interact directly with the platform and services to carry out local tasks such as monitoring.

## Agents

JBoss ON agents are deployed on every machine that JBoss ON manages. The agent is an intermediary between the resource itself and the central JBoss ON server.

## JBoss ON Servers

The JBoss ON server is the central location for administrators to manage an operating environment. The server is used to set baseline configuration and provision applications, to define alerts and notifications, and to initiate operations.

# General Management

## JBoss ON Server File Locations 

                          serverRoot
                               |
                              jon
                               |
      ----------------------------------------------------------
      |          |     |      |       |        |       |       |
alert-scripts/  bin/  etc/  EULA  jbossas/  LICENSE  logs/  plugins/


## JBoss ON Agent File Locations

                   serverRoot
                       |
                  rhq-agent/
                       |
      ------------------------------------
      |      |     |      |      |       |
     bin/  conf/  data/  lib/  logs/  plugins/


# Starting the JBoss ON Server (Basic)

The JBoss ON server process is started by running a scripting in the serverRoot/bin/ directory. There is an .sh script for Linux and Unix systems and a .bat script for Windows systems.

        serverRoot/bin/rhq-server.{sh|bat} start
        Trying to start the RHQ Server...
        RHQ Server (pid 27547) is starting

Needs RHQ_SERVER_JAVA_HOME to be set.

# Starting the JBoss ON Agent

        /opt/rhq-agent/bin/rhq-agent.sh

        RHQ 3.1.2.0-SNAPSHOT [cda7569] (Tue Apr 13 13:39:16 EDT 2012)
        >

**Tip:** If there are any errors when starting the JBoss ON agent, run the agent start script with the `--cleanconfig` to wipe the previous agent configuration and start fresh.

# Creating Affinity Groups

An affinity group sets a preference for which JBoss ON servers manage which JBoss ON agents. An affinity group only sets a preference or hint for which server will manage the agent, not an absolute requirement. All agents are still managed within the JBoss ON server cloud, so any JBoss ON server can, theoretically, manage any JBoss ON agent based on the current load and performance.

# Configuring Agents

The agent can be configured and managed through the agent prompt, which is opened through the `rhq-agent.sh` script.

# Managing the Agent as a Resource

The agent can be added as a resource to the JBoss ON inventory, so its behavior and metrics can be monitored to ensure that it is working properly and it can have alerts and operations launched, as with any other resource.


