# OpenSelery by Example
[![Actions Status](https://github.com/protontypes/seleryexample/workflows/openselery/badge.svg)](https://github.com/protontypes/seleryexample/actions) [![Balance] (https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wiki/protontypes/seleryexample/openselery/balance_badge.json&style=flat&logo=bitcoin)]

A minimal project example showing openselery:     

* Software defined developers payout fully transparent to the bones for your Github project.
* Dependencies scanning for most languages to include all developers. 
* Only the sender needs an Coinbase account in the first instance.
* Investor creates a transparent payout with public CI logs.
  

## Github Action Integration

1. The [Gitub](https://github.com/settings/tokens) and [Libraries.io](https://libraries.io/api) tokens are easy to obtain. Simulate payouts without the [coinbase token](https://www.coinbase.com/settings/api) to find the right settings. 

2. Create a dedicated coinbase account with limited amounts. OpenSelery is based on the APIs of The Libraries.io, Github and Coinbase. To provide service you need to create tokens in the corresponding accounts. Setting simulation to false will require your coinbase tokens. Configure the [access control settings](https://github.com/protontypes/openselery/wiki/Coinbase-Settings) of the automated coinbase account.

3. Never transfer or store large values with automated cryptocurrency wallets. Use recurring automated transaction from another account to recharge you wallet on a regular base. 

4. Transfer some money to this wallet for testing. See the [price list](https://help.coinbase.com/en/coinbase/trading-and-funding/pricing-and-fees/fees.html) for transfering money to the coinbase account.
 
5. Add the token of libraries.io and coinbase to your [secrets](https://help.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets).

6. You can integrate OpenSelery in your CI by copying the `openselery.yml` file into your `.github/actions/` destination project directory. Check and modify the setting before running your CI Pipeline:

  ```
  cat .github/actions/openselery.yml 
  ```
7. Set the simulation parameter to `False` if you want pay developers or `True` to try out OpenSelery on your project.

8. Depending on the `openselery.yml` a payout will be triggered. The default setting runs OpenSelery with every new version of the destination project. 

9. Protect your master branch in the Github Setting under `Branches`. Activate the `Restrict who can push to matching branches` option. 

10. To enable runner diagnostic logging, set the following secret in the repository that contains the workflow.
This also changes the workflow behavior so that Github API calls are more stable:
```
ACTIONS_RUNNER_DEBUG to true. 
```


[![Donate with bitcoin](https://en.cryptobadges.io/badge/small/3PVdiyLPR7MgaeFRJLW9mfuESZS2aAPX9w)](https://en.cryptobadges.io/donate/3PVdiyLPR7MgaeFRJLW9mfuESZS2aAPX9w)   
