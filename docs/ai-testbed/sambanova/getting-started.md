# Getting Started

## On-Boarding

SambaNova SN30 can be accessed using your ALCF account. See [Get Started](https://www.alcf.anl.gov/support-center/get-started)
to request an account and for additional information.

## Setup

### System View

Connection to a SambaNova node is a two-step process. The first step is to **ssh** to the **login node**.
This step requires an MFA passcode for authentication - an
eight-digit passcode generated by an app on your mobile device, e.g., **MobilePASS+**.
The second step is to log in to a SambaNova node from the **login node**.

![SambaNova System View](files/sambanova_login.jpg "SambaNova System View")

### Log in to Login Node

Log in to the SambaNova **login node** from your local machine using the below command. This uses the **MobilePASS+** token generated every time you log in to the system. This is the same passcode used to authenticate into other ALCF systems, such as **Polaris**.

*In the examples below, replace* ***ALCFUserID*** *with your ALCF user id.*

```bash
ssh ALCFUserID@sambanova.alcf.anl.gov
Password: < MobilePASS+ code >
```

> **Note**: Use the ssh "-v" option in order to debug any ssh problems.

### Log in to a SambaNova Node

Once you are on the **login node**, a SambaNova node can be accessed using an alias, **sn30-r[1-4]-h[1-2]** where 'r' stands for the rack number, and 'h' stands for host. **sn30-r1-h1** is the first host of the first rack.

The 8 nodes are aliased as : **sn30-r1-h1** , **sn30-r1-h2**, **sn30-r2-h1**, **sn30-r2-h2**, **sn30-r3-h1**, **sn30-r3-h2**, **sn30-r4-h1**, **sn30-r4-h2**.

**sn30-r1-h1** can be accessed as below.

```bash
ssh sn30-r1-h1
```

### SDK setup

The required software environment (SambaFlow software stack and the associated environmental variables) for a SN30 node is set up automatically at login. This is unlike the SN10 where the environment had to be set up by each user.
