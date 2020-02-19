# SKO-Rollout
Simple Tech Walk-through

# SKO-Rollout
An easy technical walk-through for Rollout

![CloudBees Rollout](https://1ko9923xosh2dsbjsxpwqp45-wpengine.netdna-ssl.com/wp-content/themes/rollout/images/rollout_white_logo1.png)

`[![Integration status](https://app.rollout.io/badges/environment_key)](https://app.rollout.io/app/environment_key/settings/info)`

This repository is a YAML represnetation for Rollout configuration, it is connected (see badge for status) to Rollout service via [Rollout's github app](https://github.com/apps/rollout-io)
Configuration as code allows the entire configuration of Rollout's state to be stored as source code. It integrates Rollout's UI with engineering existing environment. This approach brings a lot of benefits.


# What is Rollout
Rollout is a multi-platform, infrastructure as code, software as a service feature management and remote configuration solution.

# What Are Feature Flags

Feature Flags is a powerfull technique based on remotetly and conditionaly opening/closing features threw the entire feature developement and delivery process.  As Martin Fowler writes on [Feature Toggles (aka Feature Flags)](https://martinfowler.com/articles/feature-toggles.html)

> Feature Toggles (often also refered to as Feature Flags) are a powerful technique, allowing teams to modify system behavior without changing code. They fall into various usage categories, and it's important to take that categorization into account when implementing and managing toggles. Toggles introduce complexity. We can keep that complexity in check by using smart toggle implementation practices and appropriate tools to manage our toggle configuration, but we should also aim to constrain the number of toggles in our system.

You can read more about the Advantages of having Rollout configuration stored and treated as code in [Rollout's support doc](https://support.rollout.io/docs/configuration-as-code)


# Repository, Directories and YAML structure
## Branches are Environments

Every environment on Rollout dashboard is mapped to a branch in git. The same name that is used for the environment will be used for the branch name. The only exception being Production environment which is mapped to `master` branch

## Directory structure

Rollout repository integration creates the following directory structure:
```
.
├── experiments             # Experiments definitions
│   └──  archived           # Archived experiments definitions
├── target_groups           # Target groups definitions
└── README.md
```

- All experiments are located under the experiment folder
- All archived experiments are located under the `experiments/archived` folder
