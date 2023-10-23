# Sentinel-SOAR
Orchestration, Automation and Response for Azure Sentinel


## The Orchestrator

![](https://media.tenor.com/BYEFsf3x6oAAAAAC/whiplash-fletcher.gif)

The Orchestrator is found in Sentinel's Automation rules. These rules can trigger conditionals on every alert or incident creation. If these conditionals turn out to be true, the Orchestrator can do the following:

- Call upon and run logic apps (playbooks)
- Change incident severity
- Assign an owner to the incident
- Add tags to an incident
- Add tasks to an incident

In the context of SOAR, we are mainly interested in calling upon logic apps and adding tags to an incident.

## Automation

![](https://comicvine.gamespot.com/a/uploads/original/10/104794/2242216-eve_wall_e_11444456_885_370.jpg)

Azure Logic Apps are usually used to automate workflows and business processes. In Azure Sentinel, they are given the colloquial name of "Playbooks". Traditionally, response teams followed strict playbooks when dealing with security incidents. Under the SOAR framework, we should look to replicate these practices when producing logic apps. 

## Response

![](https://media1.giphy.com/media/3ShTiUlx5IWQnQ2TKE/200w.gif?cid=6c09b952ctcynrsha7kn6eqn08fvk53k8awnbdjwe4j1358j&ep=v1_gifs_search&rid=200w.gif)

Once they reach their conclusion, Logic Apps will usually call upon an API. For instance, a logic app that triggers once a user clicks on a phishing link can call upon the password reset API function of the authentication service an organization is using, giving it the user's unique identifier as an input. With this, the authentication service can clear the user's sessions and reset their password.

### As you can see, by following the SOAR framework in Azure Sentinel, we are able to automate simple tasks, letting us focus on bigger things and avoiding waking up the poor 24/7 SOC Officer On-Duty at 3am because someone in France clicked on pesky links

### This repository will contain fully fledged automations, including rules, playbooks and responses ready to be used for your organization.
