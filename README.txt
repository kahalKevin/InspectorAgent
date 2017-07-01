This is for creating agent for reporting to Inspector

To install just do:
pip install InspectorAgent


Use in Python script:

import InspectorAgent
from InspectorAgent import agent

# Require to install request and paramiko with:
# pip install requests
# pip install paramiko

agent.startAssertion('127.0.0.1:8000')
# agent.fakeName('77b0cf94-dea6-42db-ba96-33a6362acdd7')

agent.assertMetric("check first", True, "this info is additional")
agent.assertMetric("check final", True, "this info is additional")

agent.envFreeMemory("10.20.30.44", "username1", "password1", "this info is about env")
agent.envFreeMemory("10.20.33.40", "username2", "password2", "this info is about env")

agent.finishAssertion()
