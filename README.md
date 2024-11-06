# avctl-github-ci-example

AVCTL gives you the option to deploy your agents to the [cloud](https://agentverse.ai) with simple command line instructions. We've created this repository as a template for you to integrate AVCTL and Github Actions to have a simple workflow of development and deployment. 

This repo contains two parts, deployment scripts and the agent itself. 

### Development

It is recommended you template this repo to build from, and this page instructions assumes you have.

In our agent folder, we have a very simple Alice agent. We've initalised a poetry file too. Poetry is used to build the agent in the deployment section, we see it as beneficial tool for containing our imported library, and python versions. If you're unfamiliar with poetry and agent installation, check out the [docs](https://fetch.ai/docs/guides/agents/getting-started/installing-uagent).

For more advanced agent examples, check out the agent templates on [agentverse.ai](https://agentverse.ai)

### Deployment

You will need to go to agentverse.ai and create an API key and create this as an action secret in github.

Our action is set to run on pushes to `main`, this works for simplicity but it is recommended you update the workflow to only run on merges into a branch like `release/production`, one which has appropriate branch protection rules. 

If you make a change to your agent and push, you'll see the workflow run.


### Agent private keys & addresses

Agents are identified by addresses derived from private keys. When building and deploying agents on agentverse, agentverse will create your private key and address for you. To learn more about agent addresses and seeds, please visit the [fetch.ai/docs](https://fetch.ai/docs) 
