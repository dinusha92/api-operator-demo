## Scenario-5 : Override default configuration values

You can override the default configuration values of relavant artifacts.

There are different set of profiles based on each patterns. Some of them are:

In pattern-1 we have,

* api-manager-1
* api-manager-2
* analytics-dashboard
* analytics-worker

For the above profiles, you can override the fields such as,

* Replicas
* MinReadySeconds
* Resources 
  * Requests 
    * Memory 
    * CPU
  * Limits 
    * Memory 
    * CPU
* LivenessProbe
  - InitialDelaySeconds
  - PeriodSeconds
  - FailureTHreshold
* ReadinessProbe
  - InitialDelaySeconds
  - PeriodSeconds
  - FailureTHreshold
* imagePullPolicy

You can specify to any or all of the profiles using the given wso2-apim.yaml file. A sample configuration values for 1 of the profile is given, you can include required profiles as an array. Then apply the command,

#### Deploy Pattern-1 by overriding configurations

Please follow the prerequisites section in scenario 2 to deploy Pattern-1 and execute the following command.

```
  kubectl apply -f wso2-apim.yaml
```
