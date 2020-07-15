# Infrastructure check

> **Part of the Multi-team Software Delivery Assessment** ([README](README.md))
>
> Copyright © 2018-2019 [Conflux Digital Ltd](https://confluxdigital.net/)
>
> Licenced under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) ![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/3.0/88x31.png)
>
> _Permalink: [SoftwareDeliveryAssessment.com](http://SoftwareDeliveryAssessment.com/)_

Possible additions to [the Multi-team Software Delivery Assessment](https://github.com/ConfluxDigital/software-delivery-assessment)

Purpose:  *Assess the awareness and practices of the team in relation to infrastructure good practices*

Method: Use the [*Spotify Squad Health Check*](https://labs.spotify.com/2014/09/16/squad-health-check-model/) approach to assess the team's answers to the following questions:

| **Question**                                                                                                                                 | **Tired (1)**                                                        | **Inspired (5)**                                             |
| ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1\. **Infrastructure provisioning** - Do you create your **infrastructure as code** or manually?       | We provision infrastructure manually                                                  | Everything is infrastructure-as-code, and that code is treated the same as all of our code (peer reviews, automated testing, etc)      |
| 2\. **Infrastructure age** - How **long-running** is your infrastructure (either physical or virtual)? | The oldest is months / years old                                                        | It's all serverless / it's all ephemeral and the oldest is less than a day old                |
| 3\. **Infrastructure housekeeping** - Do you **purge infrastructure after use**?                       | We have fixed infrastructure which lasts forever                                        | Everything has a time-to-live and is automatically purged when that TTL is reached                                     |
| 4\. **Infrastructure utilisation** - Do you **run everything hot**?                                    | We run fixed-size infrastructure that's sized to cope with occassional peaks in demand  | We run at 80%+ utilisation, scaling up and down automatically based on load                                |
| 5\. **Infrastructure patching** - Is your infrastructure all **fully patched**?                        | It's never patched / it's patched once a quarter or less frequently                     | It's never more than a day out of date                                       |
| 6\. **Design for failure** - What happens when your **infrastructure fails**?                          | We'd have to try to recover it manually                                                 | We've built it in the certain knowledge that it will fail - recovery is fully automated and well proven    |
| 7\. **Access to production** - Who has **access to production** infrastructure?                        | We're not sure - hopefully only people who really need it                               | Nobody: our logging & monitoring is comprehensive, and our release processes are fully automated, so there's no need for access to production |
